# React TDD To-Do App

This project is a simple To-Do list application built with React. The primary focus of this project is on practicing and demonstrating **Test-Driven Development (TDD)**. The application was created using Create React App.

The core idea is to write tests for a feature *before* writing the implementation code. This ensures that the application's components and user interactions are well-tested and behave as expected. This repository corresponds to the work done for a "React Week 7, Day 4" module.

## Features

*   Add new tasks to a list.
*   View all the tasks.
*   Mark tasks as complete.
*   Delete tasks from the list.
*   Comprehensive test suite ensuring all functionalities work correctly.

## Project Focus: Test-Driven Development (TDD)

This project heavily utilizes the **React Testing Library** to write user-centric tests. The philosophy is to test the application in the same way a user would interact with it, focusing on component behavior rather than implementation details.

Key libraries used for testing:
*   **@testing-library/react**: Provides core utilities for testing React components.
*   **@testing-library/jest-dom**: Adds custom Jest matchers for asserting on DOM nodes.
*   **@testing-library/user-event**: Simulates real user interactions like typing, clicking, etc.

## Technologies Used

*   **React (v19)**
*   **Create React App**
*   **Jest** for test running
*   **React Testing Library** for component testing

## Getting Started

To get a local copy up and running, follow these simple steps.

### Prerequisites

Make sure you have Node.js and npm installed on your machine.
*   **npm**
    ```
    npm install npm@latest -g
    ```

### Installation

1.  **Clone the repository**
    ```
    git clone https://github.com/Kumarswamy-palakuri/react-week-7-day-4.git
    ```
2.  **Navigate to the project directory**
    ```
    cd react-week-7-day-4
    ```
3.  **Install NPM packages**
    ```
    npm install
    ```

## Available Scripts

In the project directory, you can run the following commands:

### `npm start`

Runs the app in development mode.
Open [http://localhost:3000](http://localhost:3000) to view it in your browser. The page will reload when you make changes.

### `npm test`

Launches the test runner in interactive watch mode.
This is the primary command to use while practicing TDD. It will automatically re-run tests as you save changes to your files.

### `npm run build`

Builds the app for production to the `build` folder.
It correctly bundles React in production mode and optimizes the build for the best performance.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren't satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

---





Run Locally
To run this project on your local system:

# Clone the repository
git clone 
# Install dependencies
npm install

# Start the development server
npm start

# Run test cases (Jest + React Testing Library)
npm test

# Build for production
npm run build


Application Architecture

This project is built with React, using Hooks, Context API, and Test-Driven Development (TDD) with Jest + React Testing Library.

src/
 ├─ components/
 │   ├─ TaskInput.jsx       # Input field + button for adding tasks
 │   ├─ TaskItem.jsx        # Represents a single task with toggle/remove
 │   ├─ TaskList.jsx        # Displays all tasks or "No tasks" message
 │   └─ *.test.jsx          # Unit tests for each component
 │
 ├─ hooks/
 │   ├─ useTodos.js         # Custom hook for todos (add/toggle/remove)
 │   └─ useTodos.test.js    # Tests for the custom hook
 │
 ├─ context/
 │   └─ TodosContext.js     # Context + Provider for global state (scalable)
 │
 ├─ App.js                  # Main component (uses TaskInput + TaskList)
 ├─ App.test.js             # App-level tests
 ├─ index.js                # Application entry point
 ├─ setupTests.js           # Jest + React Testing Library setup


Flow:

App uses useTodos (custom hook) for managing todos.

TaskInput allows adding tasks.

TaskList renders tasks using TaskItem.

TodosContext can provide todos globally if scaling is needed.


React Hooks & Context API:

🔹 Hooks

useState → stores todos array

useCallback → memoizes add/toggle/remove functions

useTodos (custom hook) → encapsulates todos logic

🔹 Context API

TodosContext created with React.createContext()

TodosProvider wraps the app and shares todos + actions

Components consume context with useContext(TodosContext)

Removes the need for prop drilling and makes the app scalable

Features

 Add tasks with a button or Enter key

 Toggle completion (strike-through completed tasks)

 Remove tasks from the list

 Show “No tasks” when the list is empty

 Tested with Jest + React Testing Library (components + hook)

 Reusable and modular components


 Ready for deployment (Netlify/Vercel)

