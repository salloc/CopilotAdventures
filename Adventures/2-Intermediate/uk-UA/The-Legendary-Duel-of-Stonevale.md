## Легендарний поєдинок Стоунвейла

<a href="#">
    <img src="../../Images/stonevale.jpg" style="width: 830px" />
</a>

### Передісторія

У містичному царстві Стоунвейл двох воїнів, Рока та Папіру, обрано для поєдинку, який визначатиме долю їхніх племен на наступне століття. Арена, відома як Ціссорія, — місце, де кожен хід має вагу та наслідки.

### Мета

Ваше завдання — змоделювати поєдинок між Роком і Папірою. Кожен воїн виконує серію ходів, і кожен хід має певний результат. Щоб перемогти, воїн повинен набрати найбільшу кількість очок за низку раундів.

### Вимоги

1. **Ходи та бали:**
    - Кожен воїн може обрати один із трьох ходів: камінь, папір або ножиці.
        - Перемога каменя = 1 бал
        - Перемога паперу = 2 бали
        - Перемога ножиць = 3 бали

2. **Динаміка поєдинку:**
    - Якщо обидва воїни обирають однаковий хід, це нічия, і бали не нараховуються.
    - Камінь розбиває ножиці, папір накриває камінь, ножиці ріжуть папір.
    - Бали нараховуються відповідно до переможного ходу.

3. **Гра:**
    - Поєдинок складається з 5 раундів.
    - Мета — заробити найбільшу кількість очок за ці раунди.

4. **Ходи гравців:**

    **Ходи Рока (Гравець 1)**

    | Раунд 1   | Раунд 2 | Раунд 3  | Раунд 4 | Раунд 5 |
    |-----------|---------|----------|---------|---------|
    | ножиці    | папір   | ножиці   | камінь  | камінь  |

    **Ходи Папіри (Гравець 2)**

    | Раунд 1 | Раунд 2 | Раунд 3 | Раунд 4 | Раунд 5 |
    |---------|---------|---------|---------|---------|
    | камінь  | камінь  | папір   | ножиці  | папір   |

5. **Додаткові можливості (якщо є час):**
    - Реалізувати систему підказок, яка радитиме хід гравцеві.
    - Дозволити гравцям обирати ходи для кожного раунду замість автоматичного вибору.

### Обмеження

* Виконуйте симуляцію за допомогою GitHub Copilot та будь-якої мови на ваш вибір.
* Забезпечте ефективність алгоритмів для динаміки поєдинку. Запитайте GitHub Copilot/Chat: «Як зробити код більше читабельним та підтримуваним?».
* Надання графічного інтерфейсу для симуляції необов’язкове.

### Підсумок основних завдань

1. Використати консольний додаток для виведення результатів.
2. Ініціалізувати рахунки обох воїнів.
3. Кожен воїн обирає хід для кожного раунду.
4. Визначити переможця кожного раунду та нарахувати бали.
5. Підсумувати бали після 5 раундів.
6. Оголосити загального переможця поєдинку.

### Поради для початку

1. Якщо ви використовуєте GitHub Codespace, можете починати!
2. Якщо працюєте локально, переконайтеся, що у вас встановлена потрібна мова/фреймворк.
    - [Node.js](https://nodejs.org)
    - [Python](https://www.python.org/downloads/)
    - [.NET](https://dot.net)
3. Створіть папку для коду.
    - JavaScript: створіть папку `stonevale` і додайте файл `app.js`.
    - Python: створіть папку `stonevale` і додайте файл `app.py`.
    - C#: створіть папку `stonevale` і виконайте `dotnet new console`.

### Поради GitHub Copilot

<a href="#">
    <img src="../../Images/copilot-tips.jpg" style="width: 830px" />
</a>

#### Використовуйте Copilot для підвищення ефективності

Спробуйте дізнатися у Copilot складність алгоритму (нотація Big O).

1. Відкрийте [GitHub Copilot Chat](https://docs.github.com/en/copilot/github-copilot-chat/using-github-copilot-chat#asking-your-first-question) у бічній панелі.
2. Запитайте Copilot Chat про складність коду.
3. Запитайте Copilot Chat про оптимізацію коду.
4. Знову перевірте складність — чи покращилась вона?

#### Використовуйте Copilot для генерації коментарів до коду

1. Виділіть увесь код за допомогою <kbd>Ctrl</kbd>/<kbd>Cmd</kbd>+<kbd>A</kbd>.
2. Натисніть <kbd>Ctrl</kbd>/<kbd>Cmd</kbd>+<kbd>I</kbd>, щоб відкрити вбудований чат.
3. Введіть `/doc` і натисніть Enter.
4. Прийміть згенерований коментар.

#### Використовуйте Copilot, щоб спростити код

1. Відкрийте GitHub Copilot Chat у бічній панелі.
2. Введіть `/simplify` і натисніть <kbd>Enter</kbd>.
3. Перегляньте пропозиції для спрощення коду.

#### Виправлення помилок

Скопіюйте повідомлення про помилку та вставте його в чат. Copilot Chat допоможе вирішити проблему.

