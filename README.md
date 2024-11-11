<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple Todo App</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #f5f5f5;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }
        .container {
            background-color: white;
            padding: 2rem;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            width: 100%;
            max-width: 400px;
        }
        h1 {
            color: #333;
            text-align: center;
            margin-bottom: 1.5rem;
        }
        input, button {
            width: 100%;
            padding: 0.5rem;
            margin-bottom: 1rem;
            border: 1px solid #ddd;
            border-radius: 4px;
            box-sizing: border-box;
        }
        button {
            background-color: #4CAF50;
            color: white;
            border: none;
            cursor: pointer;
            transition: background-color 0.3s;
        }
        button:hover {
            background-color: #45a049;
        }
        u1{
          list-style: none;
          padding: 0;
          margin-top:20px;
          text-align: left;
          }
        li{
          margin-bottom: 10px;
          }
        #todo_display {
            margin-top: 1.5rem;
        }
        .todo-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0.5rem;
            border-bottom: 1px solid #eee;
        }
        .todo-item:last-child {
            border-bottom: none;
        }
        .todo-item button {
            width: auto;
            padding: 0.25rem 0.5rem;
            margin: 0;
        }
        .completed {
            text-decoration: line-through;
            color: #888;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Simple Todo App</h1>
        <input type="text" id="todo_title" placeholder="Enter todo title">
        <input type="text" id="todo_desc" placeholder="Enter todo description">
        <button onclick="performOperation()">Add Todo</button>
        <u1 id="todo_display"></div>
    </div>
    <script src="script.js>
      const todo_title= document.getElementById('todo_title')
      const todo_display= document.getElementById('ttodo_display')
      function performOperation() {
      const taskText = todo_title.value.trim();
         if (taskText !== '') {
         const li document.createElement('li');
         li.textContent = taskText;
         li.addEventListener('click',completeTask);
         todo_display.appendChild(li);
         todo_title.value = '';}
       }
      function completeTask(event){
      const task=event.target;
      task.classList.toggle('completed');}
      
    </script>
</body>
</html>
