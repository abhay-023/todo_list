📝 Todo App (React + Context API)
A simple and elegant Todo Management Application built using React, Context API, and localStorage.
This app allows users to add, edit, delete, and mark todos as completed, with data persisting even after page refresh.

🚀 Features
➕ Add new todos
✏️ Edit existing todos
✅ Mark todos as completed / uncompleted
❌ Delete todos
💾 Persistent storage using localStorage
🌐 Global state management using React Context API
🎨 Clean UI with Tailwind CSS


🛠️ Tech Stack
React (Hooks) – useState, useEffect, useContext
Context API – Global state management
Tailwind CSS – Styling
localStorage – Data persistence


📁 Project Structure
src/
│
├── App.jsx
├── main.jsx
│
├── components/
│   ├── TodoForm.jsx
│   ├── TodoItems.jsx
│   └── index.js
│
├── contexts/
│   ├── TodoContext.js
│   └── index.js
│
└── App.css


🧠 Context API Explanation
📌 TodoContext.js
Creates a global TodoContext
Stores:
todos array
Functions: addTodo, updateTodo, deleteTodo, toggleComplete
Exposes a custom hook: useTodo()
export const TodoContext = createContext();
export const useTodo = () => useContext(TodoContext);


🧩 Components Overview
🔹 App.jsx
Manages the main todo state
Handles:
Adding
Updating
Deleting
Toggling completion
Syncs todos with localStorage
Wraps app with TodoProvider
🔹 TodoForm.jsx
Input form for adding new todos
Uses addTodo() from context
Prevents empty submissions
🔹 TodoItems.jsx
Displays each todo item
Allows:
Edit mode
Completion toggle
Deletion
Disables editing for completed todos


💾 Local Storage Support
Todos are automatically:
Loaded from localStorage on app start
Saved to localStorage on every change
useEffect(() => {
  localStorage.setItem("todos", JSON.stringify(todos));
}, [todos]);


▶️ How to Run the Project
Clone the repository
git clone <your-repo-url>
Install dependencies
npm install
Start the development server
npm run dev


📸 UI Preview
Clean and minimal UI
Color-coded completed todos
Responsive design


🔮 Future Improvements
🔍 Search todos
🗂️ Filter (Completed / Pending)
📅 Due dates
☁️ Backend integration

👨‍💻 Author
Abhay Singh
