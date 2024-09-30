
# To-Do List Application

A simple and interactive to-do list application that allows users to add, mark, and delete tasks. This project is built using HTML, CSS, and JavaScript, and it uses `localStorage` to persist data across browser sessions.


## Features

- **Add Tasks**: Users can add new tasks by entering text in the input box and clicking the "Add" button.
- **Mark Tasks as Completed**: Users can click on a task to mark it as completed or uncompleted.
- **Delete Tasks**: Each task has a delete button to remove it from the list.
- **Persistent Data**: All tasks are saved in the browser's `localStorage`, so they remain even if the page is refreshed.

## Installation

To run the to-do list application on your local machine, follow these steps:

1. **Clone the repository:**

   ```sh
   git https://github.com/akremsoussi/To-Do.git
   ```

2. **Navigate to the project directory:**

   ```sh
   cd todo-list-app
   ```

3. **Open `index.html` in your preferred browser:**

   ```sh
   open index.html
   ```

   Or simply double-click the `index.html` file.

## Usage

1. **Add a Task**: Type your task into the input field and click the "Add" button to add it to the list.
2. **Mark as Completed**: Click on the task text to mark it as completed or uncompleted.
3. **Delete a Task**: Click the "✖" button to delete a task.

## Code Overview

### HTML (`index.html`)

- The structure of the to-do list application, including the input box and list container.

### CSS (`style.css`)

- Styling for the application, including a gradient background, rounded buttons, and styling for list items.

### JavaScript (`script.js`)

- Functions for adding tasks, marking tasks as complete, deleting tasks, and saving the list to `localStorage`.

### Key JavaScript Functions:

- **`Add()`**: Adds a new task to the list.
- **`save()`**: Saves the current list to `localStorage`.
- **`showData()`**: Loads the saved list from `localStorage` when the page is loaded.

## Example Code

```javascript
function Add() {
    const inputBox = document.getElementById("input-box");
    const task = inputBox.value.trim();

    if (task === "") {
        alert("You must write something!");
    } else {
        let li = document.createElement("li");
        li.innerHTML = task;
        listContainer.appendChild(li);
        let span = document.createElement("span");
        span.innerHTML = "×";
        li.appendChild(span);
    }
    inputBox.value = "";
    save();
}
```

## Technologies Used

- **HTML**: Structure of the app.
- **CSS**: Styling for the app.
- **JavaScript**: Interactivity, adding/removing tasks, saving to `localStorage`.

## Contributing

Contributions are welcome! If you'd like to make improvements or add new features:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/new-feature`).
3. Make your changes.
4. Commit your changes (`git commit -m 'Add some feature'`).
5. Push to the branch (`git push origin feature/new-feature`).
6. Open a pull request.


## Contact

If you have any questions or feedback, feel free to contact me:

- GitHub: [akremsoussi](https://github.com/akremsoussi)
- Email: soussiakrem@gmail.com

## Acknowledgments

- Icons used in the application were taken from 
[unchecked Icon Source](https://www.flaticon.com/free-icons/unchecked)
[checked Icon Source](https://www.flaticon.com/free-icons/unchecked)
[Todo list Icon Source](https://www.flaticon.com/free-icons/list).

- This project was inspired by a simple to-do list tutorial.
