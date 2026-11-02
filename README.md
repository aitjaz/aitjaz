# AitJaz: голосовой ввод для Windows

Зажмите правый Ctrl, скажите фразу и отпустите клавишу. Текст с запятыми, точками и заглавными буквами появится там, где стоит курсор: в Word, почте, браузере, 1С, мессенджере, в любой программе Windows 10 и 11. Речь распознаётся на вашем компьютере, без интернета.

Название по-казахски значит «скажи, напиши» («Айт, жаз»).

**Лучше скачивать с сайта [aitjaz.com](https://aitjaz.com)**: оттуда AitJaz ставится через Microsoft Store: без окна «Windows защитила ваш компьютер», и антивирусы реже принимают программу за угрозу ([почему так лучше](#почему-лучше-скачивать-с-сайта)).

Прямая ссылка: [AitJaz-Setup.exe](https://github.com/aitjaz/aitjaz/releases/latest/download/AitJaz-Setup.exe) (последняя версия, около 223 МБ) · [Microsoft Store](https://apps.microsoft.com/detail/9NB5F8LH5PJZ)

В этом репозитории только выпуски программы (установщики), исходного кода здесь нет. [English version below](#english).

## Что умеет программа

- Печатает голосом в любую программу. Клавишу диктовки можно сменить в настройках.
- Распознаёт речь на компьютере. Модель для русского языка уже есть в установщике. Для других языков модель скачивается один раз, при первом выборе языка, и дальше интернет для диктовки не нужен.
- Понимает 18 языков: русский, казахский, английский, украинский, узбекский, кыргызский, немецкий, французский, испанский, итальянский, португальский, польский, турецкий, китайский, японский, корейский, арабский, хинди. Для казахского, узбекского и кыргызского у программы отдельная модель.
- Переводит в текст аудио и видео. Подойдут mp3, m4a, wav, голосовые из WhatsApp и Telegram, mp4, mov и другие записи. Результат сохраняется в Word, .txt или субтитры .srt; можно добавить отметки времени, разбить текст на абзацы по паузам и подписать, кто говорит. Ограничения по длине записи нет.
- Расшифровывает ролики с YouTube, вебинары и любой звук компьютера: включаете ролик, нажимаете «Начать запись», после «Стоп» получаете Word, .txt или субтитры. Сам ролик не скачивается. [Как это сделать](docs/computer-sound.md)
- Быстрые команды: подпись, реквизиты, шаблон ответа вставляются по названию: дважды быстро нажмите клавишу диктовки — у курсора откроется список; назовите команду голосом или пролистайте список. [Подробнее](docs/quick-commands.md)
- Расшифровка из командной строки для скриптов и ИИ-помощников: `Aitjaz.exe --transcribe "файл"`. [Инструкция](docs/command-line.md)
- По желанию распознаёт через облачный сервис по вашему собственному ключу API. По умолчанию это выключено.
- Окна и меню программы — на 15 языках: русский, английский, немецкий, испанский, французский, итальянский, португальский, польский, турецкий, украинский, китайский, японский, корейский, арабский, хинди. Язык выбирается по языку Windows, сменить его можно в окне настроек.

![Окно AitJaz, раздел «Аудио и видео в текст»](https://aitjaz.com/img/app/audio-v-tekst.png)

![Пример расшифровки в Word: реплики двух говорящих с отметками времени](https://aitjaz.com/img/app/word-govoryashchie.png)

## Цена и пробный период

- Первые 7 дней бесплатно, со всеми функциями, без регистрации и карты.
- Потом один платёж. Лицензия бессрочная, на 2 компьютера, обновления бесплатные, подписки нет.
- Если программа не подошла, деньги можно вернуть в течение 14 дней без объяснения причин ([условия возврата](https://aitjaz.com/refund.html)).
- Цены: [для Казахстана](https://aitjaz.com/#price) · [для других стран](https://aitjaz.com/en/#pricing).

## Как установить

Нужны Windows 10 или 11 (64-бит) и микрофон.

**Без предупреждений Windows — через сайт.** Откройте [aitjaz.com](https://aitjaz.com) и нажмите «Скачать бесплатно»: откроется страница AitJaz в Microsoft Store, установите программу оттуда.

**Установщик с этой страницы** (права администратора не нужны, программа ставится в папку пользователя):

1. Скачайте [AitJaz-Setup.exe](https://github.com/aitjaz/aitjaz/releases/latest/download/AitJaz-Setup.exe) и запустите его.
2. Если Windows покажет синее окно «Windows защитила ваш компьютер», нажмите «Подробнее», затем «Выполнить в любом случае».
3. Когда значок AitJaz появится возле часов, зажмите правый Ctrl и говорите.

### Почему лучше скачивать с сайта

- **Нет предупреждений.** Главная кнопка на сайте ставит AitJaz из Microsoft Store. Это та же программа, но её проверил Microsoft и подписал пакет. Поэтому нет окна «Windows защитила ваш компьютер» и надписи «Неизвестный издатель», а ложные тревоги антивирусов бывают реже.
- **Обновления — через Microsoft Store**, как у других программ из Store.
- **Всё на одной странице.** На сайте пошаговая инструкция на вашем языке, ответы на частые вопросы, цена и покупка ключа.
- **Пробный период и ключ те же.** 7 дней бесплатно, купленный ключ подходит к версии из Store и к установщику.

Если Microsoft Store у вас не открывается или недоступен (например, в России), скачайте установщик: на сайте ссылка ведёт на этот же файл последней версии. Из России откройте [aitjaz.com/ru/](https://aitjaz.com/ru/).

### Если браузер или антивирус блокирует установщик

У установщика пока нет цифровой подписи издателя (платного сертификата разработчика), а программа новая. Поэтому Windows, браузеры и антивирусы проверяют его строже обычного. Что может случиться и что делать:

- **Браузер пишет, что файл скачивают редко или он может быть опасен.** В Edge: в списке загрузок нажмите «…» рядом с AitJaz-Setup.exe → «Сохранить» → «Показать больше» → «Всё равно сохранить». В Chrome: откройте загрузки (Ctrl+J) и у AitJaz-Setup.exe выберите скачать файл, несмотря на предупреждение.
- **Синее окно «Windows защитила ваш компьютер», издатель «неизвестен».** Нажмите «Подробнее», затем «Выполнить в любом случае».
- **Защитник Windows или другой антивирус удалил файл или назвал его угрозой.** Если файл скачан с этой страницы или с aitjaz.com, скорее всего, это ложная тревога. Каждый выпуск перед публикацией мы проверяем Защитником Windows. Когда однажды, в версии 0.3.5, Защитник ошибся, Microsoft по нашей заявке проверил файл и ответил: угроз нет. Антивирус не отключайте. Установите AitJaz из [Microsoft Store](https://apps.microsoft.com/detail/9NB5F8LH5PJZ) и напишите нам на info@aitjaz.com, какой антивирус сработал и какое название угрозы он показал, чтобы мы сообщили о ложном срабатывании.

### Зачем файл AitJaz-Setup.exe.sig

В каждом выпуске два файла: установщик и `AitJaz-Setup.exe.sig`. Второй файл нужен программе, чтобы обновление ставилось безопасно: перед установкой она проверяет, что обновление настоящее. Скачивать его вручную не нужно.

## Куда уходит голос

Пока вы не включили облачное распознавание, голос и распознанный текст остаются на вашем компьютере. Программа не собирает статистику, журнал работы пишется без текстов. В интернет программа выходит, чтобы:

- скачать модель распознавания для выбранного языка (с Hugging Face) и, при первом включении «Разделить по говорящим», модель голосов (с GitHub);
- раз в сутки проверить, вышла ли новая версия (на GitHub; у версии из Microsoft Store это делает сам Store);
- раз в 7 дней проверить ключ, если лицензия куплена картой;
- отправить сообщение о проблеме, когда вы сами нажали «Сообщить о проблеме» и «Отправить»: текст обращения, e-mail (если указали), версии программы и Windows, языки, случайный номер установки и, если не снимете галочку (она стоит сразу), голос и текст последних фраз за 30 минут, не больше 10;
- узнать, есть ли ответ на ваше обращение, и спросить сайт, идёт ли «Тест распознавания» для вашего языка (уходят номер обращения, язык и версия программы, без голоса и текста);
- распознать речь в облаке, если вы включили его со своим ключом: тогда звук уходит выбранному вами сервису.

Подробно: [политика конфиденциальности](https://aitjaz.com/privacy.html).

## Кто делает AitJaz

AitJaz делает Нурбек Рахметов в Атырау, Казахстан. Продавец: ИП «Lotus Group».

- Почта: info@aitjaz.com
- WhatsApp: [+7 705 791 0303](https://wa.me/77057910303)
- YouTube: [@aitjaz_app](https://www.youtube.com/@aitjaz_app)

С вопросами и ошибками пишите на почту или в WhatsApp, либо нажмите «Сообщить о проблеме» в программе.

Документы: [публичная оферта](https://aitjaz.com/terms.html) · [возврат](https://aitjaz.com/refund.html) · [конфиденциальность](https://aitjaz.com/privacy.html). Лицензионное соглашение показывается при установке.

## English

AitJaz is voice typing for Windows 10 and 11. Hold the right Ctrl key, speak, and release it: your words appear as text with punctuation and capital letters wherever the cursor is, in any program. Speech is recognized on your computer, without internet. The name is Kazakh for "say, write".

**Best way to get it: [aitjaz.com/en](https://aitjaz.com/en/)**. The website installs AitJaz from Microsoft Store: without the "Windows protected your PC" screen, and with fewer antivirus false alarms ([why](#why-download-from-the-website)).

Direct link: [AitJaz-Setup.exe](https://github.com/aitjaz/aitjaz/releases/latest/download/AitJaz-Setup.exe) (latest version, about 223 MB) · [Microsoft Store](https://apps.microsoft.com/detail/9NB5F8LH5PJZ)

This repository holds only the program's releases (installers). There is no source code here.

### What it does

- Types what you say into any program. The dictation key can be changed in settings.
- Works offline. The Russian model ships with the installer; for other languages the model downloads once.
- Recognizes 18 languages: English, Russian, Kazakh, Ukrainian, Uzbek, Kyrgyz, German, French, Spanish, Italian, Portuguese, Polish, Turkish, Chinese, Japanese, Korean, Arabic and Hindi.
- Turns audio and video files into Word, .txt or .srt subtitles, with optional timestamps and speaker labels. There is no length limit.
- Transcribes YouTube videos, webinars and any computer sound: start the video, click "Start recording", and after "Stop" you get Word, .txt or subtitles. The video itself is not downloaded. [How to](docs/computer-sound.md)
- Quick commands insert a signature, bank details or a reply template by name: press the dictation key twice quickly, and a list opens next to the cursor; say the name or step through the list. [Details](docs/quick-commands.md)
- Command-line transcription for scripts and AI assistants: `Aitjaz.exe --transcribe "file"`. [Guide](docs/command-line.md)
- Can use a cloud service with your own API key if you turn it on. It is off by default.
- The program's windows and menus come in 15 languages (English, Russian, German, Spanish, French, Italian, Portuguese, Polish, Turkish, Ukrainian, Chinese, Japanese, Korean, Arabic, Hindi). The language follows Windows and can be changed in Settings.

### Price

The first 7 days are free, with all features, no sign-up and no card. After that, a one-time payment buys a lifetime license for 2 computers with free updates and no subscription. Refunds are available within 14 days. [Prices](https://aitjaz.com/en/#pricing) · [refund policy](https://aitjaz.com/en/refund.html).

### Installing

You need Windows 10 or 11 (64-bit) and a microphone. The easiest way: open [aitjaz.com/en](https://aitjaz.com/en/), click the download button, and install AitJaz from Microsoft Store.

With the installer from this page (admin rights are not required): run AitJaz-Setup.exe. If Windows shows a "Windows protected your PC" screen, click "More info", then "Run anyway".

### Why download from the website

- **No warnings.** The main button on the website installs AitJaz from Microsoft Store. It is the same app, checked by Microsoft and with a package signed by Microsoft, so there is no "Windows protected your PC" screen or "Unknown publisher", and antivirus false alarms are less likely.
- **Updates come through Microsoft Store**, like any other Store app.
- **Everything in one place.** Step-by-step instructions in your language, answers to common questions, prices and the license purchase.
- **Same trial, same key.** 7 days free; a purchased key works in both the Store version and the installer.

If Microsoft Store is missing or blocked on your PC, use the installer: the website links to this same file, always the latest version.

### If your browser or antivirus blocks the installer

The installer does not have a code signing certificate yet, and the app is new, so Windows, browsers and antivirus programs check it more strictly.

- **The browser says the file is not commonly downloaded or may be dangerous.** In Edge: in the downloads list, click "…" next to AitJaz-Setup.exe → "Keep" → "Show more" → "Keep anyway". In Chrome: open Downloads (Ctrl+J) and choose to download the file despite the warning.
- **A "Windows protected your PC" screen with an unknown publisher.** Click "More info", then "Run anyway".
- **Windows Defender or another antivirus deleted the file or called it a threat.** If you downloaded it from this page or from aitjaz.com, it is most likely a false alarm. We scan every release with Windows Defender before publishing; when Defender once flagged version 0.3.5, Microsoft reviewed the file at our request and found no threat. Do not turn your antivirus off. Install AitJaz from [Microsoft Store](https://apps.microsoft.com/detail/9NB5F8LH5PJZ) and email info@aitjaz.com with the antivirus name and the threat name it showed, so we can report the false alarm.

### The .sig file

Each release has two files: `AitJaz-Setup.exe` and `AitJaz-Setup.exe.sig`. The second file lets the program install updates safely: before installing, it checks that the update is genuine. You do not need to download it yourself.

### Privacy

Unless you turn on cloud recognition, your voice and text stay on your computer, and the program collects no usage statistics. It goes online to download language models (from Hugging Face) and the speaker model (from GitHub), to check for updates once a day, to check a license key bought by card once every 7 days, and to send a problem report only when you click "Report a problem" and "Send" (your text, e-mail if given, app and Windows versions, a random install ID and, unless you untick the box, which is ticked by default, the audio and text of up to 10 recent phrases). It also checks the status of your problem reports and asks the website whether a voice test is open for your language (report number, language and app version only, no voice or text). Details: [privacy policy](https://aitjaz.com/en/privacy.html).

### Who makes it

AitJaz is made by Nurbek Rakhmetov in Atyrau, Kazakhstan (sole proprietor "Lotus Group"). Email: info@aitjaz.com · WhatsApp: [+7 705 791 0303](https://wa.me/77057910303) · [YouTube](https://www.youtube.com/@aitjaz_app)

Documents: [terms](https://aitjaz.com/en/terms.html) · [refund](https://aitjaz.com/en/refund.html) · [privacy](https://aitjaz.com/en/privacy.html).

## Guides / Инструкции

**In this repo / В репозитории:** [Command line](docs/command-line.md) · [Computer sound](docs/computer-sound.md) · [Quick commands](docs/quick-commands.md)

**English**
- [Transcribe audio from the command line on Windows](https://aitjaz.com/en/blog/transcribe-audio-from-command-line/)
- [How to type with your voice on a Windows PC](https://aitjaz.com/en/blog/how-to-type-with-your-voice-on-windows/)
- [Offline dictation software for Windows](https://aitjaz.com/en/blog/offline-dictation-software-windows/)
- [All articles](https://aitjaz.com/en/blog/)

**Deutsch**
- [Diktiersoftware für Windows: offline und privat](https://aitjaz.com/de/blog/diktiersoftware-windows-offline/)
- [Mit der Stimme tippen am Windows-PC](https://aitjaz.com/de/blog/mit-der-stimme-tippen-windows/)
- [Alle Artikel](https://aitjaz.com/de/blog/)

**Español**
- [Programa para dictar en Windows sin internet](https://aitjaz.com/es/blog/programa-para-dictar-windows-sin-internet/)
- [Cómo escribir con la voz en el PC con Windows](https://aitjaz.com/es/blog/escribir-con-la-voz-en-pc/)
- [Todos los artículos](https://aitjaz.com/es/blog/)

**Русский**
- [Как перевести видео с YouTube в текст на компьютере](https://aitjaz.com/blog/video-youtube-v-tekst/)
- [Как печатать голосом в Telegram и WhatsApp на компьютере](https://aitjaz.com/blog/kak-pechatat-golosom-v-telegram-i-whatsapp/)
- [Голосовой ввод для ChatGPT, Claude и DeepSeek](https://aitjaz.com/blog/golosovoj-vvod-dlya-chatgpt-claude/)
- [Аудио в текст по говорящим: как расшифровать совещание](https://aitjaz.com/blog/audio-v-tekst-po-govoryashchim/)
- [Все статьи](https://aitjaz.com/blog/)

**Қазақша**
- [Компьютерде қазақша дауыспен жазу](https://aitjaz.com/kz/blog/kompyuterde-dauyspen-zhazu/)
- [Барлық мақалалар](https://aitjaz.com/kz/blog/)

**Скачать / Download: [aitjaz.com](https://aitjaz.com) · [aitjaz.com/en](https://aitjaz.com/en/)** (Microsoft Store) · [AitJaz-Setup.exe](https://github.com/aitjaz/aitjaz/releases/latest/download/AitJaz-Setup.exe) · 7 дней бесплатно / 7-day free trial
