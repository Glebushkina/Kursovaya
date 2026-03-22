# Conway's Game of Life

## Description
Conway's Game of Life is a cellular automaton devised by mathematician John Conway in 1970. It is a model where each cell on a two-dimensional grid can be in one of two states:  
- **"Alive"** (white)  
- **"Dead"** (black)  

The state of the cells changes according to specific rules, creating interesting dynamic patterns.

### Simulation Rules:
- **Survival**: A live cell remains alive if it has 2 or 3 live neighbors.  
- **Death**:  
  - From loneliness (fewer than 2 neighbors)  
  - From overpopulation (more than 3 neighbors)  
- **Birth**: A dead cell becomes alive if it has exactly 3 live neighbors.  

### Relevance
This software automates and accelerates the creation of simulations with various configuration data and provides a convenient way to set initial parameters.

---

## Specification

### Functional Requirements
#### 1. Functions:
- Processing two integer values (field width and length).  
- Creating a window of the corresponding size.  
- Setting the state of each cell (even-numbered click — dead, odd-numbered click — alive).  
- Determining the subsequent state of the cell.  
- Updating the field by changing cell states.  
- Pausing/resuming the simulation via keypress.  
- Exiting the program via keypress.  
- Displaying game rules via keypress.  
- Generation counter.  
- Automatic termination when all cells become extinct.  
- Interface language selection (Russian/English).  

#### 2. Input Data:
- **Field Width**: `int` (1–25).  
- **Field Length**: `int` (1–25).  
- **Cell State**: interactive editing.  
- **Simulation Control**:  
  - `Space` — pause/resume.  
  - `Esc` — exit.  
  - `Q` — show rules.  

#### 3. Output Data:  
- A dynamically changing game board.  
- "Simulation Over" message upon completion.  
- Current generation number.  

#### 4. User Interface:
- Initial window with input fields for width and length.  
- Prompts for incorrect input.  
- Game board with control instructions.  
- Simulation completion message.  

#### 5. Use Cases:
The user sets the field dimensions and starting configuration, starts the simulation, and observes the evolution.  

#### 6. Constraints:
- Input restricted to integers from 1 to 25.  

#### 7. Dependencies:
- The simulation can only be started after the field dimensions are defined.  

---

### Non-functional Requirements
1. **Performance**: Response time ≤ 2 sec.  
2. **Reliability**: Availability ≥ 99.9%.  
3. **Security**: Input data validation.  
4. **Usability**: 99.9% of users complete the task on the first attempt.  
5. **Scalability**: Support for complex configurations.  
6. **Compatibility**: Works on PCs and laptops under various Operating Systems.  
7. **Availability**: 24/7 operation.  
8. **Standards**: Compliance with ISO 9241 (interface).  

---

## Implementation Features
- Graphical interface based on **SFML**.  
- Adjustable field size (**1x1 – 25x25**).  
- **Toroidal topology** (the edges of the field are connected).  
- Controls:  
  - Start/stop simulation.  
  - Manual cell editing.  
- Current generation visualization.  
- Automatic termination upon cell extinction.  

---

## Controls
- **LMB** (Left Mouse Button) — interaction with buttons and cells.  
- **Enter** — confirm input.  
- **Space** — pause/resume.  
- **Esc** — exit.  
- **Q** — game rules.  

---

## Constraints
- Field size: **1x1 – 25x25** (integers only).  
- Cell state: "alive" or "dead".  

---

## Installation
1. Download the code from [GitHub]().  
2. Install **SFML 2.6.2**.  
3. Link the library in your project.  
4. Add the **Arial** font to the project folder.  

---

## Implemented Functions
### `GameOfLife` Class
- `toggleCell(int x, int y)` — switches cell state.  
- `countLiveCells()` — counts the number of live cells.  
- `change()` — calculates the next generation.  
- `draw()` — renders the field.  
- `toggleSimulation()` — starts/stops the simulation.  

### Main Function (`main`)
1. Font loading.  
2. Input window creation.  
3. Game field initialization.  
4. Main loop execution.  

---

## Testing Methodology
1. **Unit Testing** — verifying individual functions and classes.  
2. **Integration Testing** — checking module interactions.  
3. **System Testing** — verifying the entire system.  
4. **Acceptance Testing** — user-based testing.  
5. **Performance Testing** — response time evaluation.  
6. **Security Testing** — input validation checks.  
7. **Automated Testing** (Appium).
