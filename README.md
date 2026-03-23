# FileSystem-CLI

FileSystem-CLI is a Java-based application that simulates an in-memory file system and provides a Command Line Interface (CLI) integrated within a Graphical User Interface (GUI). 

The project is built using **Java** and **JavaFX**, and it follows a multi-module architecture separating the core business logic from the presentation layer.

## 🚀 Features

* **In-Memory File System Simulation**: Create and manage directories, files, and soft links.
* **Graphical Interface (JavaFX)**: A rich user interface that includes a command-line input area, an output console, and a visual representation of the file system.
* **Supported Commands**: Fully functional commands imitating Unix-like systems:
  * `cd` - Change directory
  * `ls` - List directory contents
  * `mkdir` - Create a new directory
  * `touch` - Create a new empty file
  * `rm` - Remove files
  * `rmdir` - Remove empty directories
  * `mv` - Move or rename files and directories
  * `ln` - Create soft links
  * `pwd` - Print working directory
  * `clear` - Clear the terminal output
  * `help` - Display command usage and information
* **Save & Load State**: Export the current state of your file system to a JSON file and load it back later.
* **User Preferences**: Save and restore user configurations.
* **Internationalization (i18n)**: Supports multiple languages, including English and Italian.

## 🏗️ Project Structure

The project is structured as a Maven multi-module application:

* **`backend`**: Contains the core business logic, command parsing and execution, file system models (`DirectoryNode`, `FileNode`, `Inode`, `SoftLink`), and data access objects (DAO) for saving/loading the state (e.g., via Jackson).
* **`frontend`**: Contains the JavaFX graphical user interface, including Views, Controllers, Event handling, and Models.

## 🛠️ Prerequisites

To build and run this project, you will need:
* **Java Development Kit (JDK)** (version 11 or higher recommended, depending on your `pom.xml` configuration)
* **Apache Maven**

## ⚙️ Build and Run

1. **Clone the repository**:
   ```bash
   git clone <your-repository-url>
   cd FileSystem-CLI
   ```

2. **Build the project using Maven**:
   ```bash
   mvn clean install
   ```

3. **Run the application**:
   Navigate to the `frontend` module and run the main JavaFX class:
   ```bash
   mvn javafx:run -pl frontend
   ```
   *(Alternatively, run the `ch.supsi.fscli.frontend.MainFx` class directly from your IDE).*

## 🧪 Testing

The project includes unit tests for both backend logic and frontend UI components. To execute the test suite, run:
```bash
mvn test
```
