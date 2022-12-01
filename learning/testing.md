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
## 7. Use CSS grid to create complex layouts
## 8. Use CSS grid to make layouts that adapt to the viewport size
