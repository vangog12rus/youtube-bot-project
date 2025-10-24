# 🚀 YouTube Shorts Автопостер v4.7

<div align="center">

![YouTube Bot](https://img.shields.io/badge/YouTube-Bot-red?style=for-the-badge&logo=youtube)
![Python](https://img.shields.io/badge/Python-3.11+-blue?style=for-the-badge&logo=python)
![Selenium](https://img.shields.io/badge/Selenium-4.15-green?style=for-the-badge&logo=selenium)
![Status](https://img.shields.io/badge/Status-Active-success?style=for-the-badge)

**Автоматический постер коротких видео на YouTube с современным GUI**

[![GitHub](https://img.shields.io/github/license/vangog12rus/youtube-bot-logs)](https://github.com/vangog12rus/youtube-bot-logs)
[![GitHub stars](https://img.shields.io/github/stars/vangog12rus/youtube-bot-logs)](https://github.com/vangog12rus/youtube-bot-logs)
[![GitHub issues](https://img.shields.io/github/issues/vangog12rus/youtube-bot-logs)](https://github.com/vangog12rus/youtube-bot-logs)

</div>

## ✨ Особенности

### 🎯 **Основные функции**
- **Автоматический постинг** коротких видео на YouTube
- **Мульти-аккаунт режим** с индивидуальными настройками
- **OCR обнаружение блокировок** YouTube с компьютерным зрением
- **GitHub интеграция** для автоматических отчетов и бэкапов
- **Современный GUI** в стиле Cursor IDE

### 🔧 **Продвинутые возможности**
- **Захват канала** - копирование контента с определенного канала
- **Скачивание по URL** - загрузка конкретного видео
- **Массовая загрузка** из папки
- **Система повторных попыток** (3 попытки на видео)
- **Автоматическое исключение** заблокированных аккаунтов

### 🛡️ **Безопасность и надежность**
- **Приватный репозиторий** с защищенными данными
- **Автоматические бэкапы** настроек в GitHub
- **Мониторинг блокировок** с уведомлениями
- **Обработка ошибок** и восстановление

## 🚀 Быстрый старт

### 📋 Требования
- Python 3.11+
- Chrome браузер
- macOS/Linux/Windows

### ⚙️ Установка

```bash
# Клонирование репозитория
git clone https://github.com/vangog12rus/youtube-bot-logs.git
cd youtube-bot-logs

# Установка зависимостей
pip install -r requirements.txt

# Настройка переменных окружения
cp .env.example .env
# Отредактируйте .env с вашими данными
```

### 🎮 Запуск

```bash
# Запуск GUI
python3 final_gui.py

# Или автоматический режим
python3 super_autopilot_v4.7_FINAL.py --auto-start
```

## 📊 Интерфейс

### 🖥️ Главное окно
- **Левая панель**: Управление аккаунтами и настройки
- **Центральная панель**: Логи и прогресс
- **Правая панель**: Статистика в реальном времени
- **Нижняя панель**: Статус и быстрые действия

### 🎯 Быстрые действия
- **🎯 Захват канала** - копирование с определенного канала
- **📥 Скачать по URL** - загрузка конкретного видео
- **📂 Загрузить из папки** - массовая загрузка
- **📊 Статистика** - просмотр результатов работы

## 🔧 Конфигурация

### 📁 Структура файлов
```
youtube-bot-logs/
├── final_gui.py              # Основной GUI
├── super_autopilot_v4.7_FINAL.py  # Основной бот
├── final_uploader_v4.py     # Загрузчик видео
├── github_integration.py    # GitHub интеграция
├── requirements.txt         # Зависимости
├── Dockerfile              # Docker контейнер
├── docker-compose.yml      # Docker Compose
└── .github/workflows/      # GitHub Actions
```

### ⚙️ Настройки аккаунтов
```json
{
  "accounts": ["email1@gmail.com", "email2@gmail.com"],
  "current_profile": "email1@gmail.com",
  "daily_limit": 10,
  "custom_description": "Описание для видео",
  "keywords": ["trending", "viral", "shorts"],
  "channel_capture": {
    "enabled": true,
    "channel_url": "https://youtube.com/@channel"
  }
}
```

## 🐳 Docker развертывание

### 🚀 Быстрый запуск
```bash
# Создание .env файла
echo "GITHUB_TOKEN=your_token" > .env
echo "GITHUB_REPO_OWNER=vangog12rus" >> .env
echo "GITHUB_REPO_NAME=youtube-bot-logs" >> .env

# Запуск с Docker Compose
docker-compose up -d
```

### 🔧 Ручная сборка
```bash
# Сборка образа
docker build -t youtube-bot .

# Запуск контейнера
docker run -d \
  --name youtube-bot \
  -e GITHUB_TOKEN="your_token" \
  -v $(pwd)/logs:/app/logs \
  youtube-bot
```

## 📈 GitHub интеграция

### 🔗 Настройка
1. Создайте Personal Access Token на GitHub
2. Создайте приватный репозиторий
3. Настройте переменные окружения

### 📊 Возможности
- **Автоматические отчеты** о блокировках аккаунтов
- **Резервное копирование** настроек
- **Issues** для отслеживания проблем
- **Статистика работы** в реальном времени

## 🛠️ Разработка

### 🔧 Локальная разработка
```bash
# Установка зависимостей для разработки
pip install -r requirements.txt

# Запуск в режиме отладки
python3 final_gui.py --debug

# Тестирование функций
python3 test_github.py
python3 test_ocr_blocking.py
```

### 🧪 Тестирование
```bash
# Тест GitHub интеграции
python3 test_github.py

# Тест OCR обнаружения блокировок
python3 test_ocr_blocking.py

# Тест загрузки видео
python3 test_launcher.py
```

## 📊 Статистика

### 📈 Мониторинг
- **Всего загружено**: Количество успешных загрузок
- **Сегодня**: Загрузки за текущий день
- **Успешность**: Процент успешных загрузок
- **Просмотры**: Статистика просмотров видео

### 🔄 Автоматическое обновление
Статистика обновляется каждые 30 секунд автоматически.

## 🚨 Безопасность

### 🔒 Меры защиты
- **Приватный репозиторий** - доступ только для владельца
- **Исключение личных данных** из Git (.gitignore)
- **Шифрование токенов** в переменных окружения
- **Автоматическая ротация** токенов доступа

### ⚠️ Важные замечания
- Никогда не коммитьте реальные данные аккаунтов
- Используйте приватные репозитории для чувствительных данных
- Регулярно обновляйте токены доступа

## 🤝 Поддержка

### 📞 Связь
- **GitHub Issues**: [Создать issue](https://github.com/vangog12rus/youtube-bot-logs/issues)
- **Документация**: [Wiki](https://github.com/vangog12rus/youtube-bot-logs/wiki)

### 🐛 Сообщение об ошибках
1. Проверьте существующие issues
2. Создайте новый issue с подробным описанием
3. Приложите логи и скриншоты

## 📄 Лицензия

Этот проект распространяется под лицензией MIT. См. файл [LICENSE](LICENSE) для подробностей.

## 🙏 Благодарности

- **YouTube** за предоставление API
- **Selenium** за автоматизацию браузера
- **yt-dlp** за скачивание видео
- **GitHub** за хостинг и интеграцию

---

<div align="center">

**⭐ Если проект полезен, поставьте звезду! ⭐**

[![GitHub stars](https://img.shields.io/github/stars/vangog12rus/youtube-bot-logs?style=social)](https://github.com/vangog12rus/youtube-bot-logs)

</div>