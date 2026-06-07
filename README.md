<div align="center">
  ![Shaur Logo](Shaur%20.png?raw=true)
  
  # Shaur Compiler (v5.0)
  
  [![Discord](https://img.shields.io/badge/Discord-7289DA?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/DtFCDBzVT)
  
</div>

**Shaur** — экспериментальный компилятор и язык программирования, разработанный для глубокого изучения внутреннего устройства исполняемых файлов (Windows PE/EXE) и машинного кода (x86).

Проект построен как «bare-metal» транслятор: он не использует сторонние библиотеки для сборки, а вручную формирует бинарную структуру PE-файла, включая таблицу импорта (IAT) и управление регистрами процессора.

---

## 🚀 Основные возможности

- **Native EXE Generation** — прямая генерация исполняемых файлов для Windows без зависимостей
- **Two-Pass Compilation** — двухпроходный компилятор с функциями (`function`), вызовами (`call`) и метками
- **WinAPI Integration** — встроенная поддержка WinAPI для вывода через `MessageBoxA`
- **Minimalist ISA** — упрощённая система команд (регистры EAX/EBX, память)

## 🛠 Как это работает

Проект состоит из одного PowerShell-скрипта, который выполняет роль ассемблера и линкера:

1. **Сбор команд** — разбор кода и построение таблицы символов
2. **Машинный код** — трансляция команд в байты x86
3. **PE-структура** — сборка PE-заголовка, импорты, расчёт смещений

## 💡 Пример кода (Shaur)

```plaintext
function my_math
    set 10
    add 5
    print
    ret

call my_math
run
```

## ⚠️ Статус

**Educational Sandbox / Early Development.**  
Цель проекта — изучение архитектуры x86, загрузчика Windows и принципов компиляции.

---

<div align="center">
  <a href="https://discord.gg/DtFCDBzVT">
    <img src="https://img.shields.io/badge/Join_Discord-7289DA?style=for-the-badge&logo=discord&logoColor=white" alt="Discord"/>
  </a>
</div>