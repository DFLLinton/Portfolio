# Testing portfolio

## 1. Check that passing a given input into our tests returns the expected output
Here we inputted 'drink water' into the input box and pressed the submit button. We then checked that the output was indentical.
``` js
test("Should add taskinput to list", () => { //works
  const taskInput = document.getElementById("mytask");
  taskInput.value = "drink water";
  const submitButton = document.querySelector("button[id='push']");
  submitButton.click();
  let result = document.querySelector("#tasks");
  equal(result.textContent.slice(73, 78), taskInput.value);
  taskInput.value = "drink water";
```
## 2. Write tests to mimic the behaviour of a user performing different actions
Here we stimulated the pressing of certain buttons and inputs to check that the delete function worked.
``` js
test("Clicking delete will remove a task from the list", () => {
  const trashBtns = document.querySelectorAll(".delete");
  trashBtns[0].click();
  equal(trashBtns[0].offsetParent, null, "Task deleted from the list");
});
```

## 3. Write testable, modular functions
The function that deleted items from the to do list was easily testable
``` js
var current_tasks = document.querySelectorAll(".delete");
        for(var i=0; i<current_tasks.length; i++){
            current_tasks[i].onclick = function(){
                this.parentNode.remove();
                ```
## 4. Write functions that add, remove or modify DOM nodes
This function add a strike-through to completed tasks using Javascript to affect the CSS
``` js
      var current_tasks = document.querySelectorAll(".done");
        for(var i=0; i<current_tasks.length; i++){
            current_tasks[i].onclick = function(){
                this.parentNode.style.textDecoration ="line-through";
                ```
## 5. Apply event listeners to HTML form elements
We used an event listener to make sure that non-existent tasks weren't added to the to do list
``` js
const addBtn = document.getElementById("push");
addBtn.addEventListener("click", raiseError);

function raiseError() {
    if(document.querySelector('#newtask input').value.length == 0){
        window.alert("Please Enter a Task");
    }
// Extracting the input value and addisng buttons
    else{
        entertask();
    }
    ```
## 6. Use scope to control what variables are accessible inside functions and blocks
Within my take-home challenge I used both 'var' and 'let' to define different variables as demonstrated below.
`` js
var dd = String(today.getDate()).padStart(2, '0');

for (let i = 1; i < 25; i++) {
loadProgress(i);
}
```
## 7. Use CSS grid to create complex layouts
I used css grid more in the take-home challenges but I have included it below.
``` css
.grid-container {
  margin-left:auto;
  margin-right:auto;
  display: grid;
  grid-template: 150px 150px 150px 150px 150px 150px 150px 150px / 150px 150px 150px;
  grid-gap: 10px;
  padding: 10px;
  padding-top: 20px;
    padding-bottom: 20px;
  justify-content: center;
  min-width: 500px;
  max-width: 600px;
}
```
## 8. Use CSS grid to make layouts that adapt to the viewport size
I tested the same CSS using percentages instead and it adapted to viewport size well. It is included below
``` css
.grid-container {
  margin-left:auto;
  margin-right:auto;
  display: grid;
  grid-template: 20% 20% 20% 20% 20% 20% 20% 20%/ 20% 20% 20%;
  grid-gap: 10px;
  padding: 10px;
  padding-top: 20px;
    padding-bottom: 20px;
  justify-content: center;
  width: 80%;
}
```
