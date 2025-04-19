## Арена заторів Міфосу

<a href="#">
   <img src="../../Images/mythos-arena-full.jpg" style="width: 830px" />
</a>

### Передісторія

У містичній землі Міфосу створіння з різних світів збираються для бою в Арені заторів — шахоподібній сітці, де випробовуються стратегія, міць та хитрість. Кожна істота має свій унікальний хід, силу та стратегію.

### Мета

Ваше завдання — змоделювати битву в Арені заторів. Кожна істота виконує серію ходів, і після кожного ходу може завдати шкоди супернику, якщо потрапить на ту ж саму клітинку. Мета — набрати найбільшу кількість очок до кінця битви. Раунд завершується, коли всі істоти виконали по одному ходу. Щоб відстежувати хід битви, після кожного раунду візуалізуйте сітку та виводьте поточні бали під нею.

### Вимоги

1. **Динаміка сітки:**
    - Арена заторів — це сітка розміром 5×5.
    - Кожна клітинка може бути порожньою або зайнятою істотою.
    - Істоти можуть рухатися вгору, вниз, вліво або вправо на одну клітинку.

2. **Дані істот:**

    | Ім’я    | Стартова позиція | Ходи                 | Міць | Іконка |
    |---------|------------------|----------------------|------|--------|
    | Dragon  | 2,2              | RIGHT, LEFT, DOWN    | 7    | 🐉     |
    | Goblin  | 2,3              | LEFT, RIGHT, UP      | 3    | 👺     |
    | Ogre    | 0,0              | RIGHT, DOWN, DOWN    | 5    | 👹     |

3. **Послідовність ходів:**
    - Істоти ходять по черзі.
    - Оцінка ходів відбувається у порядку зверху вниз.
    - Кожна істота виконує перший невиконаний хід зі свого списку.
    - Якщо істота мала б зайти в клітинку, зайняту іншою істотою, вона не рухається, натомість відбувається бій (див. «Динаміка бою»).
    - Раунд завершується, коли всі істоти виконали по одному ходу.
    - Потім починається наступний раунд у тому самому порядку.
    - Якщо в істоти закінчуються ходи, гра завершується.

4. **Динаміка бою:**

    - Якщо істота потрапляє в клітинку, зайняту іншою, вони обидва завдають шкоди один одному.
    - Кожна істота отримує бали, рівні кількості шкоди, завданій іншій.
    - Кожна істота втрачає бали, рівні кількості шкоди, яку вона отримала.
    - Кожна пара істот може битись не частіше одного разу за раунд.

5. **Вихідні дані:**
    - Після кожного раунду візуалізуйте сітку, друкуючи її в консоль. Порожні клітинки позначайте ⬜️.
    - Над сіткою виводьте заголовок «Початкова дошка» (для початкового стану) або «Раунд X», де X — номер раунду.
    - Використовуйте іконки істот для позначення їх на сітці.
    - Порожні клітинки — ⬜️, місця боїв — 🤺.
    - Під сіткою виводьте поточні бали кожної істоти після кожного раунду.
    - Після завершення гри поверніть загальні бали кожної істоти.

      
      <a href="#">
         <img src="../../Images/mythos-board-example.png">
      </a>

### Обмеження

* Використовуйте GitHub Copilot і напишіть симуляцію будь-якою мовою.
* Забезпечте ефективні алгоритми для обробки динаміки бою. Запитайте GitHub Copilot/Chat: «Як зробити код більш читабельним і підтримуваним?».
* Програма має мати 100% покриття тестами. Використовуйте команду `/tests` у GitHub Copilot Chat.

### Підсумок основних завдань

1. Використати консольний додаток для виведення результатів.
2. **Визначити константи та структури даних**:
   - Створити масив `creatures` з деталями істот.
   - Визначити об’єкт `directions` для відповідності напрямків руху змінам координат.
3. **Ініціалізувати сітку бою**:
   - Встановити розмір сітки та створити 2D-масив `grid`, заповнений `null`.
4. **Ініціалізувати бали та розмістити істот**:
   - Ініціалізувати бали кожної істоти у об’єкті `scores`.
   - Розмістити істот на сітці за стартовими координатами та іконками.
5. **Симулювати ходи**:
   - Перебрати всі ходи, починаючи з -1 (для початкового стану).
   - Якщо `move` == -1, вивести початкову сітку.
   - Після останнього ходу завершити цикл.
   - Для кожного ходу:
     - Обчислити нову позицію істоти.
     - Перевірити, чи потрапила вона в клітинку іншої істоти.
     - Оновити бали та стан сітки відповідно.
6. **Візуалізувати сітку**:
   - Для кожного стану (початковий і після кожного раунду):
     - Вивести заголовок «Початкова дошка» або «Раунд X».
     - Надрукувати стан сітки з іконками істот і порожніми клітинками.
     - Вивести поточні бали всіх істот.
7. **Повернути остаточні бали**:
   - Після симуляції всіх ходів повернути фінальні бали кожної істоти.

### Tips to Get Started

1. If you're using a GitHub Codespace, you're ready to go!
1. If running locally, ensure that you have your target language/framework installed. 
    - [Node.js](https://nodejs.org)
    - [Python](https://www.python.org/downloads/)
    - [.NET](https://dot.net)
1. Create a folder for your code. 
    - JavaScript: Create a folder called `mythos` and add a file named `app.js`.
    - Python: Create a folder called `mythos` and add a file named `app.py`.
    - C#: Create a folder called `mythos` and run `dotnet new console`.

### GitHub Copilot Tips

<a href="#">
    <img src="../../Images/copilot-tips.jpg"  style="width: 830px" />
</a>

#### Use Copilot to improve efficiency

See if you can use Copilot to find out the complexity (BigO notation) of the code.

1. Open the [GitHub Copilot Chat view](https://docs.github.com/en/copilot/github-copilot-chat/using-github-copilot-chat#asking-your-first-question) in the sidebar if it's not already open. Make sure your solution file is still open as well.

1. Ask Copilot Chat what the complexity of the code is.

1. Ask Copilot Chat to make the code more efficient.

1. Ask for the complexity again - is it better?

#### Use Copilot to generate code comments

1. Highlight all of the code with <kbd>Ctrl</kbd>/<kbd>Cmd</kbd>+<kbd>A</kbd>.

1. Press <kbd>Ctrl</kbd>/<kbd>Cmd</kbd>+<kbd>I</kbd> to open the inline chat. 

1. Type "/doc"

1. Ask Copilot Chat to document the function.

#### Use Copilot to simplify your code

1. Open GitHub Copilot Chat in the sidebar.

1. Type "/simplify" and press <kbd>Enter</kbd>. You can also add any text you want after the "/simplify" to give Copilot more instructions.

1. What did Copilot Chat suggest you do to make it simpler?

#### Got Errors?

Copilot Chat can help with that too! Just copy the error message and paste it into Chat. Often that's all Copilot needs to resolve your issue.
