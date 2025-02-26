# Go Todo CLI

This is a simple command-line todo list application written in Go. It leverages JSON file storage to persist todo items between sessions.

## Features

- Add a new todo
- Edit an existing todo
- Delete a todo
- Toggle completion status
- List all todos in a table format (using [`github.com/aquasecurity/table`](https://pkg.go.dev/github.com/aquasecurity/table))

## Files

- [main.go](main.go): The entry point of the application.
- [command.go](command.go): Parses command-line flags and executes commands.
- [todo.go](todo.go): Implements todo operations and table rendering.
- [storage.go](storage.go): Provides storage functionality using JSON files.
- [go.mod](go.mod) & [go.sum](go.sum): Dependency management.

## Requirements

- Go 1.24.0 or later

## Installation

1. **Clone the repository:**

   ```sh
   git clone <repository-url>
   cd <repository-directory>

2. **Build the application:**

    ```sh
    go build -o todo

## Usage

Run the built executable with the following command-linge flags:

1. **Add a todo:**

    ```sh
    ./todo -add "Title of the Todo"

2. **Edit a todo:**

    ```sh
    ./todo -edit "index:new title"

3. **Delete a todo:**

    ```sh
    ./todo -del index

4. **Toggle a todo:**

    ```sh
    ./todo -toggle index

5. **List a todo:**

    ```sh
    ./todo -list

All changes are saved automatically to todos.json in the project directory.