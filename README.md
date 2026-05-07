# Pomodoro Timer (single HTML file)

One self-contained page: inline CSS and JavaScript, no build step.

## Privacy & security

- No external scripts, fonts, or analytics.
- No network requests from this page (`fetch`, XHR, WebSocket).
- Productivity stats live only in the visitor’s browser **`localStorage`** — nothing is uploaded by this code.

## Use

Open `index.html` in a browser (double-click or “Open with…”), or host as static files (GitHub Pages, any static host).

## Deploy on Vercel (GitHub → auto deploy on push)

Репозиторий на GitHub: `AvetyStrongeStaNdPowerFulwh1teMan/pomodoro-web`, ветка **`main`** (это и есть «production»; не `master`).

### Вариант A — через Vercel CLI (связывает Git и включает автодеплой)

Выполни **в своём терминале на Mac** из корня репозитория (после `git pull`):

```bash
cd /path/to/pomodoro-web
source ~/.zshrc
vercel login
```

Дальше один раз привяжи каталог к проекту и подключи Git (CLI подхватит `origin` из `.git`):

```bash
vercel link --yes
vercel git connect --yes
```

После этого каждый **`git push` в `main`** будет собирать **production** на Vercel (как настроено в проекте по умолчанию).

### Вариант B — через сайт Vercel

1. [Import Git Repository](https://vercel.com/new) → выбери **`AvetyStrongeStaNdPowerFulwh1teMan/pomodoro-web`**, framework **Other**, root **.**  
2. При запросе — установи интеграцию **Vercel ↔ GitHub** для этого репо (если ещё не стоит).  
3. В проекте: **Settings → Git → Production Branch** = **`main`**.

### Файл `vercel.json`

Минимальная статическая конфигурация (`cleanUrls`). Билд не нужен: один `index.html` в корне.

Commit/push этих файлов в `main` — и следующий деплой подхватит конфиг автоматически.
