<div align="center">

<a href="https://postimg.cc/WFHXjvJD">
  <img src="https://i.postimg.cc/4yJM64f1/s.jpg" alt="Shaur Logo" width="120"/>
</a>
# Shaur Compiler · v0.5

*Experimental bare-metal compiler for Windows PE/EXE*
*Экспериментальный bare-metal компилятор для Windows PE/EXE*

[![Discord](https://img.shields.io/badge/Discord-Join%20Server-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/DtFCDBzVT)
![Platform](https://img.shields.io/badge/Platform-Windows-0078D4?style=for-the-badge&logo=windows&logoColor=white)
![Language](https://img.shields.io/badge/Lang-x86%20%7C%20PowerShell-CC342D?style=for-the-badge&logo=powershell&logoColor=white)
![Status](https://img.shields.io/badge/Status-Early%20Dev-FFB347?style=for-the-badge)

</div>

---

**Shaur** is an experimental compiler and programming language for deep exploration of Windows executables (PE/EXE) and x86 machine code.
Built as a **bare-metal** translator — no third-party libraries, no shortcuts. Every byte of the PE file is crafted by hand, including the Import Address Table (IAT) and CPU register management.

**Shaur** — экспериментальный компилятор и язык программирования для глубокого изучения Windows-исполняемых файлов (PE/EXE) и машинного кода x86.
Построен как **bare-metal** транслятор — никаких сторонних библиотек, каждый байт PE-файла формируется вручную, включая таблицу импорта (IAT) и управление регистрами.

---

## 🚀 Features · Возможности

| Feature | EN | RU |
|---|---|---|
| ⚙️ **Native EXE** | Direct `.exe` generation, zero dependencies | Прямая генерация `.exe`, без зависимостей |
| 🔄 **Two-Pass Compiler** | Functions, calls, labels resolved in 2 passes | Функции, вызовы и метки — двухпроходный анализ |
| 🪟 **WinAPI Integration** | Built-in `MessageBoxA` + IAT support | Встроенная поддержка `MessageBoxA` + IAT |
| 🧩 **Minimalist ISA** | EAX / EBX registers, memory operations | Регистры EAX/EBX, операции с памятью |

---

## 🛠 How It Works · Как это работает
---

## 💡 Code Example · Пример кода

```shaur
function my_math
    set 10      ; load value · загрузить значение
    add 5       ; add        · прибавить
    print       ; output     · вывод
    ret         ; return     · возврат

call my_math
run
```

---

## ⚠️ Status · Статус

> 🟡 **Educational Sandbox / Early Development**
>
> **EN:** The goal is to study x86 architecture, the Windows loader, and compilation internals from scratch.
>
> **RU:** Цель проекта — изучить архитектуру x86, загрузчик Windows и принципы компиляции с нуля.

---

<div align="center">

*Made with curiosity · Сделано с любопытством*

[![Discord](https://img.shields.io/badge/Join_Discord-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/DtFCDBzVT)

</div>