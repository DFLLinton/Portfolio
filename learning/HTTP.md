# HTTP portfolio

## 1. Write code that executes asynchronously
Here I wrote a function which uses the function 'fetchinglaps' within the LapContainer function
``` js
function RenderLaps(){
  var LapContainer = document.querySelector('.lapcontainer');
     LapContainer.innerHTML = `Laps:<br>    ${fetchinglaps(1)}
${fetchinglaps(2)}
```

## 2. Use callbacks to access values that aren't available synchronously
This is from another project but here I used callbacks to access which item should be affected by the function
```js
function openDoor(x){
  if (mm >= 12 && dd >= x){
document.getElementById("item"+x).style.backgroundImage=findCorrectImage(x);  
document.getElementById("item"+x).style.color="rgba(0, 0, 0, 0.0)";
    localStorage.setItem('item'+x, 'open');
}else{};
}
```

## 3. Use promises to access values that aren’t available synchronously
I used promises in the workshop more than the project itself
``` js 
Promise.all([oliverPromise, starsuitPromise])
        .then(console.log)
        .catch(console.error);
        ```

## 4. Use the fetch method to make HTTP requests and receive responses
Here we used fetch to access a business slogan generator
``` js
function GenerateTagLine() {
  fetch('https://corporatebs-generator.sameerkumar.website/')
    .then((response) => response.json())
    .then((response) => document.getElementById("x2").innerHTML = response.phrase)
}
```

## 5. Configure the options argument of the fetch method to make GET and POST requests
I used GET and POST requests mainly in the workshops rather than the project. This is an example.
``` js
      const oliverPromise = getUser("oliverjam");
      const starsuitPromise = getUser("starsuit");

      Promise.all([oliverPromise, starsuitPromise])
        .then(console.log)
        .catch(console.error);
        ```

## 6. Use the map array method to create a new array containing new values
I didn't use this in my project but I did multiple times of the execute program course
```js
const nums = [1, 2, 3];
nums.map(num => num * 10);
```

## 7. Use the filter array method to create a new array with certain values removed
I didn't use this in my project either but I did multiple times of the execute program course
``` js 
const arrays = [
  [1, 2],
  [2, 3],
  [3, 4],
];
arrays.filter(array => array.includes(2));
```

## 8. Access DOM nodes using a variety of selectors
Here we acessed the value of an input field.
``` js
function displayName() {
  const name = document.querySelector("#name").value;
  ```

## 9. Add and remove DOM nodes to change the content on the page
Here we used information from an input to change the content on the page
``` js 
function displayEmail() {
  const email = document.querySelector("#email").value;
  console.log(email);
  document.getElementById("x3").innerHTML = email;
}
```

## 10. Toggle the classes applied to DOM nodes to change their CSS properties
Here we changed the CSS properties of a DOM node
``` js
function showImage() {
  document.getElementById('x4').style.display = "block";
}
```

## 11. Use consistent layout and spacing
I don't think I used consistent layout and spacing within this project but my work was centred.
``` css
.container {
  margin: auto;
  margin-top: 20px;
  position: relative;
  text-align: center;
  color: white;
  width: 350px;
  height: 200px;
    font-family: "Poppins";
}
```

## 12. Follow a spacing guideline to give our app a consistent feel
I didn't use it in this project but went on to use CSS grid extensively.

## 13. Debug client side JS in our web browser
Here I used catch and console.error to record errors
``` js
getUser("oliverjam")
        .then(getRepos)
        .then(console.log)
        .catch(console.error);
        ```

## 14. Use console.log() to help us debug our code
Here I used console.log extensively as it would help double check the inputted was being retrieved
``` js
function displayName() {
  const name = document.querySelector("#name").value;
  console.log(name);
  document.getElementById("x").innerHTML = name;
}
```
