---
Title: VSO - Manpage - Frost OS
Description: Керування для утиліти vso.
PublicationDate: 2023-06-10
Listed: true
Authors: 
  - Frost-OS
---

## Найменування

```md
VSO - утиліта, за допомогою якої ви можете виконувати завдання з обслуговування вашої системи Frost OS.
```

## Короткий опис

```md
vso [параметри] [команда] [аргументи]
```

## Опис

```md
Використання:


Параметри:
    -h, --help              Показати це повідомлення і вийти

Команди:
    config                  Налаштувати VSO
    create-task             Створити нове завдання
    delete-task             Видалити завдання
    developer-program       Приєднатися до програми розробників
    help                    Показати це повідомлення і вийти
    list-tasks              Перерахувати всі завдання
    rotate-tasks            Чергувати завдання
    trigger-update          Запустити оновлення системи
    version                 Показати версію і вийти
```

## Конфігурація

```md
Опис:
    Налаштування VSO

Використання:
    vso config [options] [command] [command] (vso config [options])

Параметри:
    --help/-h               Показати це повідомлення
    --assume-yes/-y         Вважати, що ви відповіли "так" на всі питання

Команди:
    show                    Показати поточну конфігурацію
    get <key>               Отримати значення конфігурації
    set <key> <value>       Встановити значення конфігурації

Приклади:
    vso config get updates::schedule
    vso config set updates::schedule weekly
```

## Створення нових завдань

```md
Опис:
    Створити нове завдання

Використання:
    vso create-task [options] [arguments] [options] [arguments] [options].

Параметри:
    --help/-h                   Показати це повідомлення

Аргументи:
    --name/-n                   Назва завдання
    --description/-d            Опис завдання
    --need-confirm              Запитати підтвердження перед виконанням завдання
    --command/-c                Команда для виконання
    --after-task                Виконати завдання після іншого завдання
    --after-task-success        Виконати завдання після іншого завдання, якщо воно було успішним
    --after-task-failure        Виконати завдання після іншого завдання, якщо воно завершилося невдало
    --every/-e виконувати       Завдання кожні X (хвилин, годин, днів)
    --at/-a                     Виконати завдання у визначений час (hh:mm)
    --on-boot                   Виконувати завдання під час завантаження
    --on-shutdown               Виконувати завдання при завершенні роботи
    --on-login                  Виконувати завдання при вході в систему
    --on-network                Виконувати завдання при підключенні до мережі
    --on-disconnect             Виконати завдання при відключенні від мережі
    --on-battery                Виконати завдання заряду батареї
    --on-low-battery            Виконати завдання при низькому заряді батареї (20%)
    --on-charge                 Виконати завдання під час заряджання акумулятора
    --on-full-battery           Виконувати завдання при повному заряді акумулятора
    --on-condition-command      Виконати завдання за командою умови
    --on-process                Виконати завдання при запуску процесу

Приклади:
    vso create-task -n "Батарея повністю заряджена" -d "Повідомляти про повний заряд" -c "notify-send 'Батарея повністю заряджена'" --on-full-battery
    vso create-task -n "Запустити термінал" -d "Запускати термінал, коли відкриваєш Налаштування." -c "kgx" --on-process gnome-control-center
```

## Видалення завдань

```md
Опис:
Видалення завдання

Використання:
vso delete-task [task] [options] [options] [task] [options].

Параметри:
    --help/-h показати це повідомлення

Приклади:
    vso delete-task my-task
    vso delete-task "Моє завдання"
```

## Програма для розробників

```md
Опис:
    Приєднатися до програми для розробників

Використання:
    vso developer-program [options] [options] [options].

Параметри:
    --help/-h               Показати це повідомлення

Приклади:
    vso developer-program
```

## Перелік завдань

```md
Опис:
    Перерахувати всі завдання

Використання:
    vso list-tasks [опції].

Параметри:
    --help/-h               Показати це повідомлення

Приклади:
    vso list-tasks
```

## Ротація завдань

```md
Опис:
    Ротація завдань

Використання:
    vso rotate-tasks [options] [параметри].

Параметри:
    --help/-h               Показати це повідомлення

Приклади:
    vso rotate-tasks
```

## Запуск оновлення системи

```md
Опис:
    Запустити оновлення системи

Використання:
    vso trigger-update [options] [опції].

Параметри:
    --help/-h               Показати це повідомлення
    --now                   Негайно запустити оновлення системи

Приклади:
    vso trigger-update --now
```

## Дивіться також

- [`apx`](apx)
- [`abroot`](abroot)

## Автори

```md
Спільнота Frost OS
Переклад: Сапуцький Петро (@voxelin)
```

## Повідомлення про помилки

Повідомляйте про баги на [трекері помилок](https://github.com/Frost-OS/vanilla-system-operator/issues).