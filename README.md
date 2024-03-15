# To-Do-List-Web-Application-COD4374
Sure, I'll organize the provided information into the specified sections according to your instructions:

 1. Title : CODTECH IT SOLUTIONS Intern - Task Submission -To-Do List Web Application


  2. Introduction
This document serves as the documentation for the To-Do List web application developed as a part of the internship project at CODTECH IT SOLUTIONS. The application allows users to create and manage their to-do tasks efficiently.

  3. Intern Information
Name: Aafreen Shaik  
Intern ID: COD4374  
Company: CODTECH IT SOLUTIONS

  4. Task Description
As an intern at CODTECH IT SOLUTIONS, I was tasked with developing a To-Do List web application using HTML, CSS, and JavaScript technologies. The application enables users to add tasks, mark them as completed, and delete them as needed.
 
5. Implementation
The To-Do List application was implemented using HTML for structure, CSS for styling, and JavaScript for dynamic functionality. The application provides a user-friendly interface for managing tasks efficiently.

 6. Code and Code Explanation
#### HTML Code:
 <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>To-Do List App</title>
    <link rel="stylesheet" href="./styles.css">
    <link rel="icon" href="./icon1.png">
</head>
<body>
    <div class="container">
        <div class="todoapp">
            <h2>To-Do List <img src="./icon.png" alt="image"></h2>
            <div class="row">
                <input type="text" id="input-box" placeholder="Add Your Text">
                <button onclick="addTask()">Add</button>
            </div>
            <ul id="list-container">
                <!-- <li class="checked">Task 1</li>
                <li>Task 2</li>
                <li>Task 3</li> -->

            </ul>
        </div>
    </div>
    <script src="./scrip.js"></script>
</body>

</html>

-This part of the code defines the basic structure of an HTML document.
-The <head> section includes meta tags for character set and viewport settings, as well as a title for the web application.
-External stylesheets and icons are linked using the <link> tag.
-The <body> section is where the visible content of the web page resides. However, the actual content is not provided in the snippet.

 CSS Code:
 *
{
    margin: 0;
    padding: 0;
    font-family: 'Times New Roman', Times, serif;
    box-sizing: border-box;
}

.container
{
    width: 100%;
    min-height: 100vh;
    background: linear-gradient(135deg, #157717, #14b2bd);
    padding: 10px;
}


.todoapp
{
    width: 100%;
    max-width: 540px;
    background: #fff;
    margin: 100px auto 20px;
    padding: 40px 30px 70px;
    border-radius: 10px;
}

.todoapp h2
{
    color: #002765;
    display: flex;
    align-items: center;
    margin-bottom: 20px;

}

.todoapp h2 img
{
    width: 30px;
    margin-left: 10px;
}

.row
{
    display: flex;
    align-items: center;
    justify-content: space-between;
    background: #edeef0;
    border-radius: 30px;
    padding-left: 20px;
    margin-bottom: 25px;
}

input
{
    flex: 1;
    border: none;
    outline: none;
    background: transparent;
    padding: 10px;
}

button
{
    border: none;
    outline: none;
    padding: 16px 50px;
    background: #39e09a;
    color: #fff;
    font-size: 16px;
    cursor: pointer;
    border-radius: 40px;
}

ul li
{
    list-style: none;
    font-size: 17px;
    padding: 12px 8px 12px 50px;
    user-select: none;
    cursor: pointer;
    position: relative;

}

ul li::before
{
    content: '';
    position: absolute;
    height: 28px;
    width: 28px;
    border-radius: 50%;
    background-image: url(./unchecked.png);
    background-size: cover;
    background-position: center;
    top: 12px;
    left: 8px;
}
 ul li.checked
 {
    color: #555;
    text-decoration: line-through;

 }

 ul li.checked::before
 {
    background-image: url(./checked.png);
 }

 ul li span
 {
    position: absolute;
    right: 0;
    top: 5px;
    width: 40px;
    height: 40px;
    font-size: 22p;
    color: #555;
    line-height: 40px;
    text-align: center;
    border-radius: 50%;
 }

 ul li span:hover
 {
    background: #edeef0;
    
 }

-The CSS code provided styles the various elements of the To-Do List application.
-It includes styles for the container, todoapp, input fields, buttons, list items, and their respective properties like colors, margins, padding, borders, and positioning.


JavaScript Code:
 const inputBox = document.getElementById("input-box");
const listContainer = document.getElementById("list-container");

function addTask()
{
    if(inputBox.value === '')
    {
        alert("You must Write something!");
    }
    else
    {
        let li = document.createElement("li");
        li.innerHTML = inputBox.value;
        listContainer.appendChild(li);
        let span = document.createElement("span");
        span.innerHTML = "\u00d7";
        li.appendChild(span);
    }
    inputBox.value = "";
    saveData();
}


listContainer.addEventListener("click", function(e)
{
    if(e.target.tagName === "LI")
    {
        e.target.classList.toggle("checked");
        saveData();
    }
    else if(e.target.tagName === "SPAN")
    {
        e.target.parentElement.remove();
        saveData();
    }
}, false)

function saveData()
{
    localStorage.setItem("data", listContainer.innerHTML);
}

function showTask()
{
    listContainer.innerHTML = localStorage.getItem("data");
}

showTask();

-The JavaScript code provides the functionality for the To-Do List application.
-It starts by selecting the input box and list container elements from the HTML document using document.getElementById.
-The addTask() function is defined to add tasks to the list when the user clicks the "Add" button.
-It first checks if the input box is empty and alerts the user if it is.
-If not, it creates a new <li> element containing the text from the input box, appends it to the list container, and adds a delete button (<span>) to it.
-An event listener is added to the list container to handle clicks on list items and delete buttons.
-If the click occurs on a list item (<li>), it toggles the 'checked' class to mark the task as completed.
-If the click occurs on the delete button (<span>), it removes the corresponding list item from the list.
-saveData() function is defined to save the tasks to the browser's local storage whenever there is a change in the task list.
-showTask() function is called to display the tasks from local storage when the page is loaded.
-Overall, the JavaScript code adds interactivity to the To-Do List application, allowing users to add, remove, and mark tasks as completed dynamically.


 



7. Conclusion
In conclusion, the To-Do List web application developed by Aafreen Shaik successfully fulfills the requirements of the internship project. It demonstrates proficiency in HTML, CSS, and JavaScript and provides a functional tool for managing tasks efficiently.

This documentation provides an overview of the project, including its purpose, implementation details, and code structure.
