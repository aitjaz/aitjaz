# Расшифровка из командной строки · Command-line transcription

[Русский](#русский) · [English](#english)

---

## Русский

С версии 0.3.12 AitJaz умеет расшифровывать аудио и видео без окна программы — одной командой. Это удобно для
скриптов, планировщика Windows и ИИ-помощников (например, Claude Code), которым нужно получить текст записи.

Работает так же, как раздел «Аудио и видео в текст» в окне: те же модели, словарь, язык и облако «свой ключ»
(если оно включено для файлов). Нужна действующая лицензия или пробный период. Программа может быть запущена
в это время — расшифровка идёт отдельным процессом.

### Где программа

- Версия с сайта (GitHub): `"%LOCALAPPDATA%\Programs\Aitjaz\Aitjaz.exe"` (если при установке не выбрали другую папку).
- Версия из Microsoft Store (с 0.3.12): просто `Aitjaz.exe` — из PowerShell, cmd и «Выполнить». Если команда не
  находится, включите AitJaz в «Параметры → Приложения → Дополнительные параметры приложений → Псевдонимы
  выполнения приложений».

### Команда

```
Aitjaz.exe --transcribe "C:\Записи\встреча.m4a" --format docx --speakers --out "C:\Расшифровки"
```

| Параметр | Что делает |
|---|---|
| `--transcribe <файл>` | Запись: mp3, m4a, wav, ogg, голосовые WhatsApp и Telegram, mp4, mov, mkv и др. |
| `--format docx\|txt\|srt` | Word, обычный текст или субтитры. По умолчанию — как в последний раз в программе (обычно Word) |
| `--out <папка>` | Куда сохранить. По умолчанию — рядом с записью |
| `--lang <код>` | Язык речи: ru, kk, uz, ky, uk, en, de, fr, es, it, pt, pl, tr, zh, ja, ko, ar, hi. По умолчанию — из настроек |
| `--speakers [N]` | Разделить по говорящим («Спикер 1», «Спикер 2»…); N — от 2 до 6, без числа — автоматически |
| `--no-timestamps` | Без отметок времени [00:12:30] |
| `--no-paragraphs` | Не делить на абзацы по паузам |
| `--local` | Только на этом компьютере, даже если включено облако |
| `--json <файл>` | Записать итог в JSON (состояние, путь к результату, длительность, код выхода) |
| `--help` | Подсказка |

Готовый файл называется как запись: `встреча.docx`; если такой уже есть — `встреча (2).docx`.

### Коды выхода

| Код | Значение |
|---|---|
| 0 | Готово |
| 1 | Ошибка распознавания или сохранения (текст ошибки — в JSON и в консоли) |
| 2 | Неверные параметры или файл не найден |
| 3 | Нужна активация (пробный период закончился) |
| 4 | В записи нет речи |
| 130 | Прервано (Ctrl+C) |

### PowerShell и cmd

`Aitjaz.exe` — оконная программа, поэтому PowerShell не ждёт её сам. Используйте `Start-Process -Wait`:

```powershell
$p = Start-Process -FilePath "$env:LOCALAPPDATA\Programs\Aitjaz\Aitjaz.exe" `
     -ArgumentList '--transcribe', '"C:\Записи\встреча.m4a"', '--format', 'txt', '--json', '"C:\Temp\итог.json"' `
     -Wait -PassThru -NoNewWindow
$p.ExitCode
Get-Content "C:\Temp\итог.json" -Encoding UTF8 | ConvertFrom-Json
```

В cmd: `start /wait "" "%LOCALAPPDATA%\Programs\Aitjaz\Aitjaz.exe" --transcribe "C:\Записи\встреча.m4a" --json "C:\Temp\итог.json"`.

Для версии из Microsoft Store в `-FilePath` пишите просто `Aitjaz.exe`.

Ход работы («Распознаю: 45 %…») печатается в консоль, из которой запустили команду. Самый надёжный способ узнать
итог — файл `--json` и код выхода. Старый файл `--json` программа удаляет в начале работы и пишет новый всегда,
даже при неверных параметрах. Файлы .txt и .srt сохраняются в UTF-8 (с BOM).

```json
{
  "file": "C:\\Записи\\встреча.m4a",
  "state": "done",
  "message": "Готово: встреча.docx…",
  "result": "C:\\Расшифровки\\встреча.docx",
  "seconds_audio": 1932.4,
  "exit_code": 0,
  "format": "docx",
  "language": "ru",
  "speakers": 3,
  "cloud": "",
  "version": "0.3.12"
}
```

### Для ИИ-помощников (Claude и др.)

Скопируйте этот блок в инструкции своего помощника (например, `CLAUDE.md`):

```
Чтобы расшифровать аудио/видео в текст на этом компьютере, используй AitJaz:
  Start-Process -FilePath "$env:LOCALAPPDATA\Programs\Aitjaz\Aitjaz.exe" -ArgumentList '--transcribe','"<файл>"',
    '--format','txt','--json','"<папка>\aitjaz.json"' -Wait -PassThru -NoNewWindow
Потом прочитай <папка>\aitjaz.json: exit_code 0 — текст в файле из поля "result" (UTF-8). 3 — нужна активация
AitJaz (скажи пользователю), 4 — в записи нет речи. Для разделения по говорящим добавь '--speakers'.
Распознавание идёт на компьютере пользователя; время зависит от ПК, языка и модели (на слабом ПК — дольше).
Для версии из Microsoft Store вместо полного пути пиши просто Aitjaz.exe.
```

### Конфиденциальность

Запись не покидает компьютер, если облако «свой ключ» выключено (или выключено для файлов) или указан `--local`. С включённым облаком звук
уходит выбранному вами сервису по вашему ключу — как и при работе из окна программы.

---

## English

Since version 0.3.12 AitJaz can transcribe audio and video files without opening its window — with a single
command. Useful for scripts, Windows Task Scheduler and AI assistants (for example Claude Code).

It works exactly like "Audio & video to text" in the app: the same models, vocabulary, language and your own
cloud key (if enabled for files). A valid license or the trial is required. The app may be running at the same time.

### Where the program is

- Website (GitHub) version: `"%LOCALAPPDATA%\Programs\Aitjaz\Aitjaz.exe"` (unless you chose another folder).
- Microsoft Store version (0.3.12+): just `Aitjaz.exe` — from PowerShell, cmd and Run. If it is not found, turn
  AitJaz on in Settings → Apps → Advanced app settings → App execution aliases.

### Command

```
Aitjaz.exe --transcribe "C:\Recordings\meeting.m4a" --format docx --speakers --out "C:\Transcripts"
```

| Option | What it does |
|---|---|
| `--transcribe <file>` | Recording: mp3, m4a, wav, ogg, WhatsApp/Telegram voice messages, mp4, mov, mkv and more |
| `--format docx\|txt\|srt` | Word, plain text or subtitles. Default: the last format used in the app (usually Word) |
| `--out <folder>` | Where to save. Default: next to the recording |
| `--lang <code>` | Speech language: ru, kk, uz, ky, uk, en, de, fr, es, it, pt, pl, tr, zh, ja, ko, ar, hi. Default: from settings |
| `--speakers [N]` | Split by speakers ("Speaker 1", "Speaker 2"…); N = 2..6, or automatic |
| `--no-timestamps` | No [00:12:30] marks |
| `--no-paragraphs` | Do not split into paragraphs by pauses |
| `--local` | This computer only, even if the cloud is enabled |
| `--json <file>` | Write the result as JSON (state, result path, duration, exit code) |
| `--help` | Help |

Exit codes: 0 done · 1 recognition/saving error · 2 bad arguments or file not found · 3 activation needed ·
4 no speech in the recording · 130 interrupted.

### PowerShell and cmd

`Aitjaz.exe` is a windowed program, so PowerShell does not wait for it by itself. Use `Start-Process -Wait`:

```powershell
$p = Start-Process -FilePath "$env:LOCALAPPDATA\Programs\Aitjaz\Aitjaz.exe" `
     -ArgumentList '--transcribe', '"C:\Recordings\meeting.m4a"', '--format', 'txt', '--json', '"C:\Temp\result.json"' `
     -Wait -PassThru -NoNewWindow
$p.ExitCode
Get-Content "C:\Temp\result.json" -Encoding UTF8 | ConvertFrom-Json
```

cmd: `start /wait "" "%LOCALAPPDATA%\Programs\Aitjaz\Aitjaz.exe" --transcribe "C:\Recordings\meeting.m4a" --json "C:\Temp\result.json"`.
For the Microsoft Store version use just `Aitjaz.exe` as `-FilePath`.

Progress ("Recognizing: 45%…") is printed to the console you started it from. The reliable way to get the result is
the `--json` file plus the exit code. The app deletes an old `--json` file at start and always writes a new one,
even for bad arguments. .txt and .srt files are saved as UTF-8 (with BOM).

```json
{
  "file": "C:\\Recordings\\meeting.m4a",
  "state": "done",
  "message": "Done: meeting.docx…",
  "result": "C:\\Transcripts\\meeting.docx",
  "seconds_audio": 1932.4,
  "exit_code": 0,
  "format": "docx",
  "language": "en",
  "speakers": 3,
  "cloud": "",
  "version": "0.3.12"
}
```

### For AI assistants (Claude and others)

Paste this into your assistant's instructions (for example `CLAUDE.md`):

```
To transcribe audio/video to text on this computer, use AitJaz:
  Start-Process -FilePath "$env:LOCALAPPDATA\Programs\Aitjaz\Aitjaz.exe" -ArgumentList '--transcribe','"<file>"',
    '--format','txt','--json','"<folder>\aitjaz.json"' -Wait -PassThru -NoNewWindow
Then read <folder>\aitjaz.json: exit_code 0 means the text is in the file from the "result" field (UTF-8);
3 means AitJaz needs activation (tell the user); 4 means there is no speech. Add '--speakers' to split by speakers.
Recognition runs on the user's computer; the time depends on the PC, language and model (longer on a slow PC).
For the Microsoft Store version use just Aitjaz.exe instead of the full path.
```

### Privacy

The recording stays on your computer unless your own cloud key is enabled for files (and `--local` is not used);
then the audio goes to the service you chose, with your key — the same as in the app window.
