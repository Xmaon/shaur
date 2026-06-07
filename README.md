# Shaur Compiler (v5.0)

**Shaur** is an experimental compiler and programming language designed for deep study of the internal structure of executable files (Windows PE/EXE) and machine code (x86).

The project is built as a "bare-metal" translator: it does not use third-party libraries for assembly, but manually forms the binary structure of the PE file, including the Import Address Table (IAT) and CPU register management.

---

### 🚀 Key Features

*   **Native EXE Generation:** Direct generation of executable files that run on Windows without dependencies.
*   **Two-Pass Compilation:** A two-pass compiler with support for functions, calls, and labels.
*   **WinAPI Integration:** Built-in support for calling Windows API for real-time data output (`print` via `MessageBoxA`).
*   **Minimalist ISA:** A simplified instruction set for managing the state of the EAX register and memory (EBX).

### 🛠 How it Works

The project consists of a single PowerShell script that acts as both an assembler and a linker:
1.  **Command Collection:** Analyzing code and building a symbol table.
2.  **Machine Code:** Translating commands into x86 bytes.
3.  **PE Structure:** Dynamic assembly of the PE header, adding imports, and calculating memory offsets.

### 💡 Code Example

```shaur
function my_math
    set 10
    add 5
    print
    ret

call my_math
run
```

---

### 🇷🇺 Описание проекта (RU)

**Shaur** — это экспериментальный компилятор и язык программирования, разработанный для глубокого изучения внутреннего устройства исполняемых файлов (Windows PE/EXE) и машинного кода (x86).

Проект построен как «bare-metal» транслятор: он не использует сторонние библиотеки для сборки, а вручную формирует бинарную структуру PE-файла, включая таблицу импорта (IAT) и управление регистрами процессора.

#### 🚀 Основные возможности
*   **Native EXE Generation:** Прямая генерация исполняемых файлов, которые запускаются в Windows без зависимостей.
*   **Two-Pass Compilation:** Двухпроходный компилятор с поддержкой функций (function), переходов (call) и меток.
*   **WinAPI Integration:** Встроенная поддержка вызова Windows API для вывода данных в реальном времени (`print` через `MessageBoxA`).
*   **Minimalist ISA:** Упрощенная система команд для управления состоянием регистра EAX и памятью (EBX).

#### 🛠 Как это работает
Проект состоит из одного скрипта на PowerShell, который выполняет роль ассемблера и линкера одновременно:
1.  **Сбор команд:** Анализ кода и построение таблицы символов.
2.  **Машинный код:** Трансляция команд в байты x86.
3.  **PE-структура:** Динамическая сборка PE-заголовка, добавление импортов и расчет смещений в памяти.

---

### ⚠️ Project Status
**Status:** Educational Sandbox / Early Development.
**Goal:** Studying x86 architecture, Windows loader principles, and compilation techniques.
