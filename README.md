# Minesweeper AI

An intelligent agent designed to play the classic **Minesweeper** game by leveraging logical reasoning and knowledge-based inference. This project uses Python to simulate the game environment and apply AI techniques to identify mines and safe cells effectively.

## Features

- **Game Simulation**: Implements a Minesweeper board with randomly placed mines.
- **AI Agent**: Uses logical inference to deduce:
  - Which cells are safe to click.
  - Which cells contain mines.
- **Knowledge Base**: Maintains and updates a dynamic knowledge base of sentences about the board's state.
- **Smart Decisions**: Combines multiple sentences to infer additional safe cells or mines when new information is added.

## How It Works

1. **Knowledge Representation**:
   - Each `Sentence` consists of a set of cells and a count of the number of mines among them.
   - Example: `{(1, 2), (1, 3), (0, 3)} = 1` means one of these cells contains a mine.

2. **Inference Rules**:
   - Safe cells and mines are inferred when sufficient information is available.
   - Sentences are combined or simplified to deduce additional knowledge.

3. **Game Logic**:
   - The AI avoids cells identified as mines.
   - It clicks safe cells based on the knowledge base.

## Code Highlights

- **Efficient Knowledge Management**: Sentences with no cells are removed for optimization:
  ```python
  self.knowledge = [sentence for sentence in self.knowledge if len(sentence.cells) > 0]



