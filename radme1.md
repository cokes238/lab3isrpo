# Лабораторная работа по C# в Visual Studio Code

Краткое описание лабораторной работы. Данная лабораторная предназначена для изучения основ программирования на C# в среде Visual Studio Code. Цель работы - освоить создание консольных приложений, работу с базовыми конструкциями языка и отладку кода. В ходе выполнения будут рассмотрены основные принципы объектно-ориентированного программирования.

## Содержание (Table of Contents)

- [Структура проекта](#структура-проекта)
- [Примеры Markdown элементов](#примеры-markdown-элементов)
- [Код программы](#код-программы)
- [Результаты работы](#результаты-работы)

## Структура проекта

### Основные файлы
- `Program.cs` - главный файл программы
- `README.md` - документация проекта
- `.gitignore` - файл исключений Git

### Папки проекта
- `src/` - исходный код
  - `Models/` - классы моделей
  - `Services/` - сервисные классы
- `bin/` - скомпилированные файлы
- `obj/` - объектные файлы компиляции
- `img/` - изображения для документации

### Конфигурационные файлы
- `.vscode/` - настройки VS Code
  - `launch.json`
  - `tasks.json`
- `Lab3.csproj` - файл проекта

---

## Примеры Markdown элементов

### Заголовки различных уровней
# Заголовок H1
## Заголовок H2
### Заголовок H3

### Форматирование текста
- **Полужирный текст** - для важных моментов
- *Курсивный текст* - для терминов и определений
- ~~Зачёркнутый текст~~ - для устаревшей информации
- `Моноширинный текст` - для команд и кода

### Списки разных типов

#### Маркированный список
- Первый элемент
- Второй элемент
- Третий элемент

#### Нумерованный список
1. Первый пункт
2. Второй пункт
3. Третий пункт

#### Вложенный список
- Основной элемент 1
  - Вложенный элемент A
  - Вложенный элемент B
- Основной элемент 2
  1. Нумерованный вложенный
  2. Ещё один вложенный

### Цитата
> "Программирование - это не только написание кода, но и искусство решения проблем." - Анонимный разработчик

### Таблица

| Имя переменной | Тип данных | Описание |
|----------------|------------|----------|
| `name`         | `string`   | Имя пользователя |
| `age`          | `int`      | Возраст пользователя |
| `isActive`     | `bool`     | Флаг активности |
| `salary`       | `decimal`  | Заработная плата |

### Изображение
Пример выполнения программы:

![Пример выполнения](/img/codeCommitLab3_FIO.png)

### Ссылки
- [Внешняя ссылка на документацию C#](https://docs.microsoft.com/dotnet/csharp/)
- [Внутренняя ссылка на структуру проекта](#структура-проекта)

### Чекбоксы
- [x] Task 1 - Изучить основы C#
- [ ] Task 2 - Реализовать все методы
- [x] Task 3 - Написать тесты
- [x] Task 4 - Создать документацию

### Сноска
Для успешной компиляции проекта необходимо установить .NET SDK[^1].

[^1]: Рекомендуется использовать последнюю стабильную версию.

### Alert-блоки GitHub

> [!NOTE]
> Для работы с C# в VS Code необходимо установить расширение "C# for Visual Studio Code".

> [!TIP]
> Используйте Ctrl+Shift+P для быстрого доступа к командам VS Code.

> [!WARNING]
> Не забывайте сохранять файлы перед компиляцией проекта!

### Математические формулы

#### Inline LaTeX
Площадь круга: $S = \pi r^2$

#### Block LaTeX
Формула суммы арифметической прогрессии:

$$
\sum_{i=1}^n i = \frac{n(n+1)}{2}
$$

## Код программы

### Основная программа на C#

```csharp
using System;

namespace Lab3
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Лабораторная работа по C#");
            Console.WriteLine("==========================");
            
            // Пример использования переменных
            string studentName = "Горишний Д.О.";
            int labNumber = 3;
            DateTime submissionDate = DateTime.Now;
            
            Console.WriteLine($"Студент: {studentName}");
            Console.WriteLine($"Лабораторная №{labNumber}");
            Console.WriteLine($"Дата сдачи: {submissionDate:dd.MM.yyyy}");
            
            // Вызов методов
            DemonstrateVariables();
            DemonstrateCalculations();
            DemonstrateArrays();
        }
        
        static void DemonstrateVariables()
        {
            Console.WriteLine("\n=== Демонстрация переменных ===");
            
            int integerVar = 42;
            double doubleVar = 3.14159;
            bool boolVar = true;
            char charVar = 'A';
            
            Console.WriteLine($"Целое число: {integerVar}");
            Console.WriteLine($"Дробное число: {doubleVar}");
            Console.WriteLine($"Логическое значение: {boolVar}");
            Console.WriteLine($"Символ: {charVar}");
        }
        
        static void DemonstrateCalculations()
        {
            Console.WriteLine("\n=== Демонстрация вычислений ===");
            
            int a = 10;
            int b = 5;
            
            Console.WriteLine($"a = {a}, b = {b}");
            Console.WriteLine($"Сумма: {a + b}");
            Console.WriteLine($"Разность: {a - b}");
            Console.WriteLine($"Произведение: {a * b}");
            Console.WriteLine($"Частное: {a / b}");
            Console.WriteLine($"Остаток: {a % b}");
        }
        
        static void DemonstrateArrays()
        {
            Console.WriteLine("\n=== Демонстрация массивов ===");
            
            int[] numbers = { 1, 2, 3, 4, 5 };
            
            Console.Write("Массив чисел: ");
            foreach (int num in numbers)
            {
                Console.Write($"{num} ");
            }
            Console.WriteLine();
            
            Console.WriteLine($"Длинамассива: {numbers.Length}");
            Console.WriteLine($"Первый элемент: {numbers[0]}");
            Console.WriteLine($"Последний элемент: {numbers[numbers.Length - 1]}");
        }
    }
}
