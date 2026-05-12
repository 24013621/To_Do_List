# Ex03 To-Do List using JavaScript
## Date: 12-05-2026

## AIM
To create a To-do Application with all features using JavaScript.

## ALGORITHM
### STEP 1
Build the HTML structure (index.html).

### STEP 2
Style the App (style.css).

### STEP 3
Plan the features the To-Do App should have.

### STEP 4
Create a To-do application using Javascript.

### STEP 5
Add functionalities.

### STEP 6
Test the App.

### STEP 7
Open the HTML file in a browser to check layout and functionality.

### STEP 8
Fix styling issues and refine content placement.

### STEP 9
Deploy the website.

### STEP 10
Upload to GitHub Pages for free hosting.

## PROGRAM
```
index.html
```
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>To-Do List</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

<div class="container">
    <h1>To-Do List</h1>
    
    <div class="input-section">
        <input type="text" id="taskInput" placeholder="Enter a task">
        <button onclick="addTask()">Add</button>
    </div>

    <ul id="taskList"></ul>
</div>

<script src="script.js"></script>
</body>
</html>
```
```
style.css
```
```
body {
    font-family: Arial, sans-serif;
    background: linear-gradient(to right, #74ebd5, #ACB6E5);
    text-align: center;
}

.container {
    width: 320px;
    margin: 60px auto;
    background: white;
    padding: 20px;
    border-radius: 12px;
    box-shadow: 0 4px 10px rgba(0,0,0,0.2);
}

h1 {
    color: #ff4b5c;
}

input {
    padding: 10px;
    width: 70%;
    border: 2px solid #74ebd5;
    border-radius: 6px;
}

button {
    padding: 10px;
    background: #ff4b5c;
    color: white;
    border: none;
    border-radius: 6px;
    cursor: pointer;
    transition: 0.3s;
}

button:hover {
    background: #e63946;
}

li {
    list-style: none;
    margin: 10px 0;
    padding: 10px;
    background: #f1f1f1;
    border-left: 5px solid #74ebd5;
    border-radius: 6px;
    display: flex;
    justify-content: space-between;
}

li:hover {
    background: #dff6ff;
}

.completed {
    text-decoration: line-through;
    color: gray;
}
```
```
script.js
```
```
function addTask() {
    let input = document.getElementById("taskInput");
    let task = input.value;

    if (task === "") {
        alert("Please enter a task");
        return;
    }

    let li = document.createElement("li");
    li.textContent = task;

    li.onclick = function () {
        li.classList.toggle("completed");
    };

    let delBtn = document.createElement("button");
    delBtn.textContent = "X";
    delBtn.onclick = function () {
        li.remove();
    };

    li.appendChild(delBtn);

    document.getElementById("taskList").appendChild(li);

    input.value = "";
}
```

## OUTPUT
<img width="1907" height="1185" alt="image" src="https://github.com/user-attachments/assets/eb058b9f-c6db-4fab-b63d-c25ee0885f8c" />



## RESULT
The program for creating To-do list using JavaScript is executed successfully.
