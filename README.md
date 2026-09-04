<div align="center">

# 📱 Termux API Agent Tools

### *Прямой доступ к аппаратным датчикам Android, батарее, буферу обмена и системным диалогам*

[![Termux](https://img.shields.io/badge/Termux-Android-000000?style=for-the-badge&logo=termux&logoColor=white)](https://termux.dev/)
[![Android API](https://img.shields.io/badge/Android-Termux%3AAPI-3DDC84?style=for-the-badge&logo=android&logoColor=white)](https://wiki.termux.com/wiki/Termux:API)
[![Bash](https://img.shields.io/badge/Bash-Automation-2B35AF?style=for-the-badge&logo=gnubash&logoColor=white)](https://www.gnu.org/software/bash/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](LICENSE)

<br/>

**Termux API Agent Tools** — практический инструментарий и скилл для взаимодействия автономных ИИ-агентов (Antigravity CLI, OpenCode и др.) с операционной системой Android и аппаратными сенсорами смартфона через `Termux:API`.

---

</div>

## 📋 Требования и подготовка

1. **Пакет утилит в Termux:**
   ```bash
   pkg install -y termux-api
   ```
2. **Приложение-компаньон:**
   Установите APK [Termux:API](https://github.com/termux/termux-api/releases) (с F-Droid или GitHub Releases; подпись ключа должна совпадать с установленным Termux).
3. **Разрешения Android:**
   Предоставьте Termux:API доступ к уведомлениям, геолокации/датчикам и отключите оптимизацию батареи.

---

## 🛠 Набор готовых скриптов

Все скрипты находятся в папке [`scripts/`](scripts/) и готовы к прямому вызову:

| Скрипт | Назначение | Пример использования |
| :--- | :--- | :--- |
| [`battery_check.sh`](scripts/battery_check.sh) | Мониторинг уровня заряда, температуры и статуса питания | `./scripts/battery_check.sh [--json]` |
| [`notify.sh`](scripts/notify.sh) | Отправка системного push-уведомления в шторку Android | `./scripts/notify.sh "Заголовок" "Сообщение"` |
| [`vibrate.sh`](scripts/vibrate.sh) | Тактильный виброотклик заданной длительности | `./scripts/vibrate.sh 300` |
| [`toast.sh`](scripts/toast.sh) | Всплывающее системное сообщение (Toast) на экране | `./scripts/toast.sh "Готово!"` |
| [`clipboard.sh`](scripts/clipboard.sh) | Чтение и запись в системный буфер обмена Android | `./scripts/clipboard.sh set "текст"` |
| [`dialog.sh`](scripts/dialog.sh) | Вызов нативного GUI-диалога (подтверждение или текстовый ввод) | `./scripts/dialog.sh confirm "Вопрос" "Продолжить?"` |
| [`sensor_read.sh`](scripts/sensor_read.sh) | Однократный безопасный опрос аппаратных датчиков | `./scripts/sensor_read.sh list` |
| [`tts_speak.sh`](scripts/tts_speak.sh) | Голосовое воспроизведение текста через системный движок TTS | `./scripts/tts_speak.sh "Задача завершена"` |

---

## 🔗 Сообщество и полезные ссылки

- 🔌 **[TecnicalBot/termux-mcp](https://github.com/TecnicalBot/termux-mcp)** — MCP-сервер для прямого подключения Termux:API к LLM-агентам с политикой default-deny и аудитом каждого вызова.
- 🧩 **[ZH3KA11/Termux-Assistent-](https://github.com/ZH3KA11/Termux-Assistent-)** — модульный трёхкомпонентный набор скиллов для Termux (device, comms, system).
- ⚡ **[lobehub/android-shizuku-mcp](https://github.com/lobehub/android-shizuku-mcp)** — Shizuku MCP мост для выполнения привилегированных системных операций Android без root-доступа.
- 🚀 **[wallentx/antigravity-cli-termux](https://github.com/wallentx/antigravity-cli-termux)** — официальный апстрим автономного ядра Antigravity CLI для Termux с поддержкой 39-bit VA space.
- 📖 **[Официальная документация Termux:API](https://wiki.termux.com/wiki/Termux:API)** — справочник команд и спецификации API.

---

## 🚀 Быстрый запуск

```bash
git clone https://github.com/Enigman-Termux-lab/termux-api.git ~/projects/lab-termux-api
cd ~/projects/lab-termux-api

# Проверка уровня заряда батареи
./scripts/battery_check.sh

# Отправка тестового уведомления
./scripts/notify.sh "Termux API" "Связь с Android установлена"
```

---

## 📄 Лицензия

Распространяется под лицензией [MIT](LICENSE). Разработано для открытой экосистемы **[Enigman-Termux-lab](https://github.com/Enigman-Termux-lab)**.
