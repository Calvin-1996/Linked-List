# Sorted LinkedList Program

A Java console application that demonstrates efficient sorted data structure implementation using the Java Collections Framework. The program reads integer numbers from user input and maintains them in a sorted LinkedList using binary search insertion.

## Table of Contents

- [Features](#features)
- [Demo](#demo)
- [Architecture](#architecture)
- [Installation](#installation)
- [Usage](#usage)
- [Documentation](#documentation)
- [Project Structure](#project-structure)
- [Code Reuse Philosophy](#code-reuse-philosophy)
- [License](#license)
- [Author](#author)

## Features

- **Real-time Sorting**: Numbers are inserted in sorted order as they're entered
- **Efficient Performance**: O(log n) insertion using binary search algorithm
- **Input Validation**: Graceful handling of invalid input with user-friendly error messages
- **Clean Architecture**: SOLID principles implementation with interface-based design
- **Extensive Code Reuse**: Leverages Java Collections Framework and standard libraries
- **Professional Documentation**: Comprehensive Javadoc with detailed code reuse analysis

## Demo

```
=== Sorted LinkedList Program ===
Enter integer numbers (one per line).
Press Enter on an empty line to finish input.
Numbers will be automatically sorted from smallest to largest.

Enter number: 25
Added 25
Enter number (or press Enter to finish): 10
Added 10
Enter number (or press Enter to finish): 30
Added 30
Enter number (or press Enter to finish): 15
Added 15
Enter number (or press Enter to finish): 

=== Final Results ===
Final sorted list (smallest to largest): [10, 15, 25, 30]
```

## Architecture

The application follows SOLID principles with a clean separation of concerns:

- **Single Responsibility**: Each class has one clear purpose
- **Open/Closed**: Easy to extend with new input/output methods
- **Liskov Substitution**: Interface implementations are interchangeable
- **Interface Segregation**: Focused interfaces for specific needs
- **Dependency Inversion**: Depends on abstractions, not concrete implementations

## Installation

### Prerequisites

- Java Development Kit (JDK) 8 or higher
- Command line terminal
- Git (for cloning the repository)

### Quick Start

1. **Clone the repository**
   ```bash
   git clone https://github.com/Cal9233/Linked_List.git
   cd Linked_List
   ```

2. **Navigate to the program directory**
   ```bash
   cd src
   ```

3. **Compile the program**
   ```bash
   javac *.java
   ```

4. **Run the program**
   ```bash
   java SortedList
   ```

## Usage

### Basic Usage

1. Start the program using `java SortedList`
2. Enter integer numbers one per line when prompted
3. Press Enter on an empty line to finish input
4. View your numbers displayed in sorted order

### Advanced Usage

The program supports dependency injection for custom implementations:

```java
// Custom implementation example
SortedCollection customCollection = new CustomSortedCollection();
InputHandler customInput = new FileInputHandler(customCollection);
DisplayManager customDisplay = new GraphicalDisplayManager();

SortedList program = new SortedList(customCollection, customInput, customDisplay);
program.run();
```

## Documentation

### Generate Javadoc

```bash
cd SortedListProgram
javadoc -d javadoc -author -version -use -windowtitle "Sorted LinkedList Program" -doctitle "CSC6301 Module 4 - Sorted LinkedList Implementation" *.java
```

### View Documentation

Open the generated documentation:

- **macOS**: `open javadoc/index.html`
- **Windows**: `start javadoc/index.html`
- **Linux**: `xdg-open javadoc/index.html`

## Project Structure

```
Linked_List/
├── README.md
├── LICENSE
├── .gitignore
├── src/
│   ├── SortedList.java              # Main program coordinator
│   ├── SortedIntegerCollection.java  # LinkedList implementation
│   ├── ConsoleInputHandler.java      # Console input handling
│   ├── ConsoleDisplayManager.java    # Console display handling
│   ├── SortedCollection.java         # Collection interface
│   ├── InputHandler.java             # Input interface
│   ├── DisplayManager.java           # Display interface
│   └── javadoc/                     # Generated documentation
```

## Code Reuse Philosophy

This project demonstrates strategic code reuse rather than reimplementation:

### Key Reuse Examples

1. **Java Collections Framework**: Uses `LinkedList<Integer>` instead of implementing custom linked list
2. **Binary Search Algorithm**: Leverages `Collections.binarySearch()` for O(log n) performance
3. **Input Processing**: Utilizes `Scanner` and `Integer.parseInt()` for robust input handling
4. **String Operations**: Employs `StringBuilder` for efficient string concatenation

### Benefits

- **Reduced Development Time**: Focus on business logic rather than infrastructure
- **Higher Reliability**: Battle-tested implementations from Java standard library
- **Better Performance**: Optimized algorithms and data structures
- **Easier Maintenance**: Standard patterns and well-documented APIs

See the [generated Javadoc](javadoc/index.html) for detailed code reuse documentation.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Author

**Calvin Malagon**
- Course: CSC6301 - Module 4
- Email: [malagonc@merrimack.edu](mailto:malagonc@merrimack.edu)
- GitHub: [@Cal9233](https://github.com/Cal9233)

---
