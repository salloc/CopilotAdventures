## The Gridlock Arena of Mythos

<a href="#">
   <img src="../../Images/mythos-arena-full.jpg" style="width: 830px" />
</a>

### Background

In the mystical land of Mythos, creatures from various realms come together to battle in the Gridlock Arena, a chess-like grid where strategy, power, and cunning are tested. Each creature has its unique move, power, and strategy.

### Objective

Your task is to simulate a battle in the Gridlock Arena. Each creature will make a series of moves, and after each move, the creature might inflict damage on its opponent if they land on the same square. The goal is to accumulate the highest score by the end of the battle. A round is completed when all creatures have taken one move this round. To track the progress of the battle, visualize the grid after each round and display the current scores right below the grid.

### Specifications

1. **Grid Dynamics:**
    - The Gridlock Arena is a 5x5 grid.
    - Each cell in the grid can be empty or occupied by a creature.
    - Creatures can move up, down, left, or right by one cell.

2. **Creature Data:**

    | Name   | Start | Moves                | Power | Icon |
    |--------|-------|----------------------|-------|------|
    | Dragon | 2,2   | RIGHT, LEFT, DOWN    | 7     | 🐉   |
    | Goblin | 2,3   | LEFT, RIGHT, UP      | 3     | 👺   |
    | Ogre   | 0,0   | RIGHT, DOWN, DOWN    | 5     | 👹   |

3. **Turn Order**
    - Creatures take turns making moves.
    - Each creature is evaluated in a sequential order, starting with topmost, then the next.
    - The creature always takes the move that is the leftmost not yet executed move in its move specification.
    - If a creature were to land on a cell occupied by another creature, the creature does not move, insteady a battle occurrs (see Battle Dynamics below).
    - A round is completed when all creatures have made exactly one move this round.
    - After that, the next round starts with the topmost creature.
    - If a creature has no more moves left in its specification, the game ends.

4. **Battle Dynamics:**

    - If the creature would land on a cell already occupied by another creature, they both inflict damage on each other.
    - Each creature gets points equal to the amount of damage it inflicted on the other creature.
    - Each creature loses points equal to the amount of damage it received.
    - Each pair of creatures may only battle once per round

5. **Output:**
    - After each round, visualize the grid by printing it to the console using ⬜️ to represent a cell. 
    - Above the grid add a title that either says "Initial Board" (to show the initial state of the board) or "Round X" where X is the current round number.
    - Use each creature's icon to represent it on the grid. 
    - Empty cells can be represented by a ⬜️.
    - Battle cells can be represented by a 🤺.
    - Display the current scores for each creature right below the grid after each round.
    - At the end of the game, return the total points each creature accumulated.

      
      <a href="#">
         <img src="../../Images/mythos-board-example.png">
      </a>

### Constraints

- Use GitHub Copilot and write the simulation in any language you'd like.
- Ensure efficient algorithms to handle the battle dynamics. Ask GitHub Copilot/Chat, "How can I make this code more readable and maintainable?".
- The program should have 100% test coverge. Use the /tests command in GitHub Copilot Chat.

### Summary of High-Level Tasks to Perform

1. Use a console application to render the output.

1. **Define Constants and Data Structures**:
   - Define the `creatures` array containing the creature details.
   - Define a `directions` object to map the movement directions to their respective changes in coordinates.

1. **Initialize the Battle Grid**:
   - Set the grid size and create a 2D array (`grid`) with all cells initialized to `null`.

1. **Initialize Scores and Grid**:
   - Loop through each creature in the `creatures` array.
   - For each creature, initialize its score to 0 in the `scores` object.
   - Place each creature on the grid using its starting position and icon.

1. **Simulate Battle Moves**:
   - Loop through the number of moves, starting from -1 (to represent the initial state).
   - If it's the initial state (`move` is -1), render the grid.
   - If it's the last move, exit the loop after rendering.
   - For each move:
     - Determine the new position of the creature based on its move direction.
     - Check if the new position overlaps with another creature.
     - Update scores and grid state based on overlaps or successful moves.

1. **Render the Grid**:
   - For each state of the grid (initial and after each round):
     - Display the round number or "Initial Board" for the initial state.
     - Print the grid state with creatures or an empty cell representation.
     - Display the current scores for all creatures.

1. **Return Final Scores**:
   - After all moves have been simulated, return the final scores for each creature. 

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
