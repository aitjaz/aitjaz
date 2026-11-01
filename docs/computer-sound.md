# Расшифровка YouTube, любого ролика и совещаний · Transcribe YouTube, any video and meetings

[Русский](#русский) · [English](#english)

---

## Русский

С версии 0.3.12 AitJaz умеет записывать **звук компьютера** — то, что звучит из динамиков или наушников, — и сразу
превращать его в текст: Word, .txt или субтитры .srt. Так можно расшифровать ролик на YouTube, вебинар,
онлайн-лекцию, запись эфира — что угодно, что играет на компьютере. Сам ролик не скачивается: программа слышит
только звук, как и вы.

### Как расшифровать ролик

1. Откройте настройки AitJaz (значок у часов → «Настройки») и выберите слева **«Аудио и видео в текст»**.
2. Вверху, в «Откуда взять звук», выберите **«Звук компьютера (YouTube, вебинар, лекция)»**.
3. Выберите язык речи, формат (Word, .txt или .srt), нужны ли отметки времени и разделение по говорящим, и папку.
   Если папку не указать — файлы попадут в «Загрузки». Язык речи сам ставится как у диктовки; для ролика на
   другом языке выберите его здесь.
4. Откройте ролик и поставьте его на начало. Нажмите **«● Начать запись»**, затем запустите ролик.
   Быстрее: значок у часов → **«Записать звук компьютера…»** — запись начнётся сразу.
5. Пока идёт запись, внизу справа видна небольшая панель: «Запись звука компьютера», время записи, полоска громкости
   и кнопки **«Пауза»** и **«■ Стоп»**. На паузе звук не записывается и время стоит — удобно пропустить рекламу или
   перерыв; **«Дальше»** продолжает запись в тот же файл. Панель можно **перетащить мышью** в любое место, чтобы не
   мешала смотреть, — программа запомнит, где её оставили. Внизу панели написан язык речи; если он неверный,
   нажмите «Исправить в настройках» — расшифровка пойдёт на новом языке.
6. Когда ролик закончится, нажмите **«Стоп»** на панели (или «■ Остановить и расшифровать» в окне, или пункт
   «Остановить запись звука компьютера» у часов). «Отмена» в окне выбрасывает запись без расшифровки.
7. Запись сразу расшифровывается. Готовый файл называется «Запись 26.10.2026 14-05.docx» (дата и время записи);
   кнопки **«Открыть»** и **«Показать в папке»** — в том же разделе.

Галочка **«Сохранить и сам звук (.m4a) рядом с текстом»** оставит рядом и звуковой файл. Без неё звук удаляется
после расшифровки. Если расшифровать не удалось, звук сохраняется в любом случае.

### Запись совещания в Zoom, Teams, Google Meet (с 0.3.13)

В «Откуда взять звук» выберите **«Совещание (Zoom, Teams, Google Meet)»**. Тогда AitJaz запишет и собеседников
(их голоса звучат из динамиков), и вас (через микрофон, тот же, что выбран для диктовки) — в одну запись. При выборе
язык речи становится как у диктовки и сами включаются галочки **«Записывать и мой микрофон»** и **«Разделить по говорящим»** (реплики будут подписаны:
«Спикер 1», «Спикер 2»…; после расшифровки кнопка «Имена говорящих…» заменит их на имена). Любую галочку можно
снять. Начните звонок и нажмите **«● Начать запись»** или **Ctrl+Shift+X** прямо в окне звонка.

**Ctrl+Shift+X** работает в любой программе и всегда записывает совещание — ваш микрофон и звук компьютера, даже
если в «Откуда взять звук» выбран другой вариант. Ещё одно нажатие — стоп и расшифровка. Сочетание можно поменять
на Ctrl+Shift+U, D, G или H или выключить: выберите «Совещание», строка **«Горячая клавиша записи»**.

- **Звук совещания всегда сохраняется рядом с текстом** (файл .m4a с тем же именем): если место в тексте непонятно,
  его можно переслушать.
- **Предупредите участников, что идёт запись.** В начале записи программа напомнит об этом.
- **В наушниках запись чище:** без них микрофон слышит ещё и динамики, и голоса собеседников попадают в запись
  дважды.
- Если микрофон не включился (занят другой программой или отключён), запись пойдёт без него — программа скажет об
  этом сразу.
- Панель записи с микрофоном называется «Запись совещания».

### Советы

- **Скорость ролика — обычная (1x).** Чем быстрее ролик, тем больше ошибок; выше 1,25x лучше не ставить.
  Запись идёт столько же, сколько играет ролик.
- **Не выключайте звук в самом ролике или плеере** — иначе записывать нечего.
- Уведомления, музыка из другой вкладки и системные звуки тоже попадут в запись — закройте лишнее.
- Наушники можно. **Не переключайте наушники и колонки во время записи** — запись остановится, и расшифруется то,
  что успело записаться.
- Запись ограничена 4 часами: дальше она остановится сама и расшифруется.
- Если закрыть AitJaz во время записи, звук не пропадёт — он сохранится в папку для расшифровок.
- **Чужие ролики записывайте только для себя.** Публиковать расшифровку чужого видео можно только с разрешения
  автора. Соблюдайте правила сайта, где смотрите ролик: онлайн-курсы часто запрещают запись.

### Работает ли без интернета

Да, если нужные модели уже скачаны: распознавание идёт на вашем компьютере (если облако «свой ключ» не включено для
файлов). Для языков, кроме русского, модель скачивается один раз при первом использовании; для разделения по
говорящим — небольшая модель (27 МБ) при первом включении. Интернет нужен самому ролику.

---

## English

Since version 0.3.12 AitJaz can record **computer sound** — whatever plays through your speakers or headphones —
and turn it into text right away: Word, .txt or .srt subtitles. Transcribe a YouTube video, a webinar, an online
lecture or a stream — anything that plays on the computer. The video itself is not downloaded: the app only hears
the sound, just like you.

### How to transcribe a video

1. Open AitJaz settings (tray icon → Settings) and choose **Audio & video to text** on the left.
2. At the top, in "Sound source", choose **Computer sound (YouTube, webinar, lecture)**.
3. Pick the speech language, format (Word, .txt or .srt), timestamps, speaker separation and the folder.
   If the folder is empty, files go to "Downloads". The speech language follows your dictation language; for a
   video in another language, choose it here.
4. Open the video and move it to the beginning. Click **● Start recording**, then play the video.
   Faster: tray icon → **Record computer sound…** — recording starts at once.
5. While recording, a small panel sits at the bottom right: "Recording computer sound", the recording time, a level
   meter and the **Pause** and **■ Stop** buttons. While paused nothing is recorded and the timer stops — handy to
   skip an ad or a break; **Resume** continues into the same file. **Drag the panel** anywhere so it does not cover
   the video — the app remembers the place. The bottom of the panel shows the speech language; if it is wrong, click
   "Change it in Settings" and the transcript will use the new language.
6. When the video ends, click **Stop** on the panel (or "■ Stop and transcribe" in the window, or
   "Stop recording computer sound" in the tray menu). "Cancel" in the window discards the recording.
7. The recording is transcribed right away. The file is named like "Recording 26.10.2026 14-05.docx" (date and time
   of the recording); **Open** and **Show in folder** are in the same section.

Tick **"Also save the sound (.m4a) next to the text"** to keep the audio as well. Otherwise the sound is deleted
after transcription. If transcription fails, the sound is kept anyway.

### Recording a Zoom, Teams or Google Meet meeting (0.3.13+)

In "Sound source", choose **Meeting (Zoom, Teams, Google Meet)**. AitJaz then records both the other participants
(their voices come from the speakers) and you (through the microphone chosen for dictation) into one recording.
Choosing it sets the speech language to your dictation language and turns on **"Also record my microphone"** and **"Separate speakers"** (lines are labeled "Speaker 1",
"Speaker 2"…; after transcription "Speaker names…" replaces them with names). You can untick either one. Start the
call and click **● Start recording** or press **Ctrl+Shift+X** right in the call window.

**Ctrl+Shift+X** works in any app and always records a meeting — your microphone and computer sound, even if a
different option is selected in "Sound source". Press it again to stop and transcribe. You can change the shortcut to
Ctrl+Shift+U, D, G or H or turn it off: choose "Meeting", then the **"Recording hotkey"** row.

- **The meeting sound is always saved next to the text** (an .m4a file with the same name), so you can listen
  again to any unclear part.
- **Tell the participants you are recording.** The app reminds you when recording starts.
- **Headphones give a cleaner recording:** without them the microphone also hears the speakers, so the other
  participants end up in the recording twice.
- If the microphone does not start (busy in another app or disconnected), recording goes on without it — the app
  tells you right away.
- With the microphone on, the recording panel says "Recording a meeting".

### Tips

- **Play at normal speed (1x).** The faster the video, the more errors; better not to go above 1.25x.
  Recording takes as long as the video plays.
- **Do not mute the video or the player** — otherwise there is nothing to record.
- Notifications, music from other tabs and system sounds are recorded too — close them.
- Headphones are fine. **Do not switch headphones/speakers while recording** — recording stops and whatever was
  recorded is transcribed.
- Recording is limited to 4 hours; then it stops and is transcribed automatically.
- If you close AitJaz while recording, the sound is not lost — it is saved to the transcripts folder.
- **Record other people's videos for your own use only.** Publish a transcript of someone else's video only with
  the author's permission. Follow the rules of the site you watch on: online courses often forbid recording.

### Does it work offline

Yes, once the needed models are downloaded: recognition runs on your computer (unless your own cloud key is enabled
for files). For languages other than Russian the model downloads once on first use; speaker separation downloads a
small model (27 MB) the first time. Only the video itself needs the internet.
