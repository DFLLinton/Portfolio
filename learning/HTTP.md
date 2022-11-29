# HTTP portfolio

## 1. Write code that executes asynchronously


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


## 7. Use the filter array method to create a new array with certain values removed

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

## 12. Follow a spacing guideline to give our app a consistent feel

## 13. Debug client side JS in our web browser

## 14. Use console.log() to help us debug our code
Here I used console.log extensively as it would help double check the inputted was being retrieved
``` js
function displayName() {
  const name = document.querySelector("#name").value;
  console.log(name);
  document.getElementById("x").innerHTML = name;
}
```
