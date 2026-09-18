<img src="https://capsule-render.vercel.app/api?type=waving&height=220&color=0:0f2027,50:203a43,100:2c5364&text=Aldiyar%20Beisenbek&fontColor=ffffff&fontSize=52&fontAlignY=38&desc=AI%20%2F%20Full-stack%20Developer%20%C2%B7%20MedTech&descAlignY=58&descSize=18&animation=fadeIn" width="100%"/>

<p align="center">
  <a href="https://git.io/typing-svg">
    <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=22&duration=3000&pause=800&color=38BDF8&center=true&vCenter=true&width=640&lines=%D0%93%D0%BE%D0%BB%D0%BE%D1%81%D0%BE%D0%B2%D1%8B%D0%B5+%D0%98%D0%98-%D0%B0%D1%81%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BD%D1%82%D1%8B+%D0%B4%D0%BB%D1%8F+%D0%BF%D0%BE%D0%BB%D0%B8%D0%BA%D0%BB%D0%B8%D0%BD%D0%B8%D0%BA+%F0%9F%8F%A5;STT+%E2%86%92+LLM+%E2%86%92+TTS+%D0%B2+%D1%80%D0%B5%D0%B0%D0%BB%D1%8C%D0%BD%D0%BE%D0%BC+%D0%B2%D1%80%D0%B5%D0%BC%D0%B5+%E2%9A%A1;%D0%98%D0%BD%D1%82%D0%B5%D0%B3%D1%80%D0%B0%D1%86%D0%B8%D0%B8+%D1%81+%D0%9C%D0%98%D0%A1+%D0%B1%D0%B5%D0%B7+API+%F0%9F%94%8C;%D0%9E%D1%82+MVP+%D0%B4%D0%BE+%D0%BF%D1%80%D0%BE%D0%B4%D0%B0%D0%BA%D1%88%D0%B5%D0%BD%D0%B0+%F0%9F%9A%80" alt="Typing SVG"/>
  </a>
</p>

<p align="center">
  <a href="https://t.me/belyix"><img src="https://img.shields.io/badge/Telegram-@belyix-26A5E4?style=for-the-badge&logo=telegram&logoColor=white"/></a>
  <a href="mailto:aldiyarbeysenbek@gmail.com"><img src="https://img.shields.io/badge/Email-Написать-EA4335?style=for-the-badge&logo=gmail&logoColor=white"/></a>
  <img src="https://img.shields.io/badge/📍-Kazakhstan-0f766e?style=for-the-badge"/>
  <img src="https://komarev.com/ghpvc/?username=alherc&style=for-the-badge&color=2c5364&label=Profile+views"/>
</p>

---

## 🏥 Айжан — ИИ-регистратор для поликлиник РК

Голосовой ассистент на киоске в холле поликлиники. Пациент говорит на **казахском или русском**, Айжан понимает запрос
и **сама записывает его к врачу в медицинскую информационную систему**.

> 🟢 **В продакшене** в государственных поликлиниках: Карасайская ЦРБ, Баканас

```mermaid
flowchart LR
    P([🎙️ Пациент]) -- PCM · WebSocket --> B[BFF · Node.js]
    B --> S[STT]
    S --> L{{LLM}}
    L --> T[TTS · Python<br/>Piper / Sherpa-ONNX]
    T -- аудио ~250 мс --> P
    L -- запись к врачу --> M[(МИС<br/>1С / e-MIS)]
    B <--> D[(PostgreSQL)]
```

| | |
|---|---|
| ⚡ **Real-time голос** | STT → LLM → TTS по WebSocket, KZ / RU |
| 🔊 **Self-hosted TTS** | FastAPI + Piper / Sherpa-ONNX, задержка ~200–300 мс |
| 🔌 **Интеграция с МИС** | Playwright-RPA → реверс HTTP-протокола 1С: логин, слоты и бронь без браузера |
| 🏢 **Мультиорганизационность** | несколько больниц, роли, синхронизация расписаний врачей |
| 📹 **Телемедицина** | видеоконсультации с дежурным врачом, SOS-вызов, Telegram |
| 🔐 **Безопасность** | RLS, закрытие IDOR, аудиты, данные хранятся в Казахстане |
| 🖥️ **Киоски** | Electron-приложение, деплой в Docker / Coolify |

<sub>🔒 Код проекта коммерческий и закрыт. Демо и архитектуру покажу на созвоне.</sub>

---

## 🛠️ Стек

<p align="center">
  <img src="https://skillicons.dev/icons?i=python,fastapi,ts,nodejs,express,react,tailwind,vite&perline=8" /><br/><br/>
  <img src="https://skillicons.dev/icons?i=postgres,supabase,docker,linux,electron,git,github&perline=8" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Gemini_API-8E75B2?style=flat-square&logo=googlegemini&logoColor=white"/>
  <img src="https://img.shields.io/badge/ONNX_Runtime-005CED?style=flat-square&logo=onnx&logoColor=white"/>
  <img src="https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white"/>
  <img src="https://img.shields.io/badge/WebSocket-010101?style=flat-square&logo=socketdotio&logoColor=white"/>
  <img src="https://img.shields.io/badge/Coolify-6B16ED?style=flat-square&logo=coolify&logoColor=white"/>
</p>

---

## 💡 Чем могу быть полезен

```yaml
- Довести MVP от идеи до продакшена в реальной клинике, а не только до демо
- Разобраться в МИС и процессах регистратуры и сделать интеграцию там, где нет API
- Собрать голосового или чат-ассистента на LLM под казахский и русский
- Закрыть безопасность и требования к медданным до того, как о них спросят
```

---

## 📈 Активность

<p align="center">
  <img src="https://streak-stats.demolab.com?user=alherc&theme=tokyonight&hide_border=true&background=0D1117&ring=38BDF8&fire=38BDF8&currStreakLabel=38BDF8" width="70%"/><br/>
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=alherc&theme=tokyo-night&hide_border=true&bg_color=0D1117&color=38BDF8&line=2c5364&point=ffffff&area=true" width="100%"/>
</p>

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/alherc/alherc/output/github-snake-dark.svg" />
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/alherc/alherc/output/github-snake.svg" />
    <img alt="snake" src="https://raw.githubusercontent.com/alherc/alherc/output/github-snake.svg" />
  </picture>
</p>

<img src="https://capsule-render.vercel.app/api?type=waving&height=120&color=0:2c5364,50:203a43,100:0f2027&section=footer" width="100%"/>
