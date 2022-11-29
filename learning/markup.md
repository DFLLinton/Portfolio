# Markup portfolio

## 1. Structure a site using semantic HTML to aid accessibility
We used 'alt' tags to aid accessibility
``` html
<img src="img/Nerdwhale2-01.png" alt="company image" class="company-pic" />
```

## 2. Make a web page more readable for screen readers
We used h1, h2 and h3 tags to distinguish content for screen readers
`<h1>We create<span class="color"> Websites, Apps</span><h2>Dominic Linton</h2><h3>Streets of Rage Tribute Page</h3>`

## 3. Design a UI without relying solely on colour, so that we don’t exclude colour-blind users
We used multiple font sizes to differentiate sections
`.home-text h1 {
  font-size: 3.5rem;
}
.home-text p {
  font-size: 1.2rem;
  margin-bottom: 1.5rem;
}`

## 4. Ensure our UI has sufficient colour contrast so that everyone can perceive it comfortably
We used high contrast colours throughout the website 
`:root {
  --main-color: #647bff;
  --body-color: #090a1a;
  --container-color: #171b3c;
  --heading-color: #222231;
  --box-color: #0d0f26;
  --bg-color: #fff;
}`

## 5. Use various tools to check that a website meets accessibility criteria
We used Google Chrome's lighthouse to check it met criteria

## 6. Ensure a website displays well on screens of different sizes
We used media queries to check that it displayed well on screens of different sizes
`@media (max-width: 800px) {
  header {
    position: fixed;
    top: 0;
    left: 0;
    width: 50%;
    background: var(--bg-color);
    z-index: 100;
    padding: 1rem;
  }`

## 7. Use CSS media queries to ensure content is always presented effectively
This is another example of using media queries to ensure the description of projects section was always presented well
`  .description {
    max-width: 400px;
    width: 400px;
    font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
    position: absolute;
    margin: auto;
    margin-top: -225px;
    margin-left: 10%;
    background-color: hsl(47, 100%, 69%);
    border-radius: 10px;
    padding: 50px;
    text-align: center;
    opacity: 0;
    transition: 0.5s ease;
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
  }`

## 8. Demonstrate a mobile-first approach to designing a website with a great user experience
We designed the website for desktop first and later adapted it to mobile

## 9. Create an attractive and accessible colour palette for a project
We defined a distinct and simple palette which can be found below
`:root {
  --main-color: #647bff;
  --body-color: #090a1a;
  --container-color: #171b3c;
  --heading-color: #222231;
  --box-color: #0d0f26;
  --bg-color: #fff;
}`

## 10. Use CSS variables to apply repeated colours to HTML elements
We used CSS variables as shown above. It's application is demonstrated below with the navbar
`.navbar {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  background: var(--bg-color);
  z-index: 100;
  display: flex;
  align-items: center;
  justify-content: space-between;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
  padding: 1rem;
}`
