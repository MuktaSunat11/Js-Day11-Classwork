# Key Pressed
This is a simple HTML and JavaScript code that allows the user to enter a keyword and then displays the keyword.

# HTML File

The HTML code creates a simple container div with the class "main". This div will contain the input field and the button.
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>KeyCodes</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="main">Press Any Keyboard Key</div>
    <script src="script.js"></script>
</body>
</html>
```
# Css File
The CSS code simply styles the container div, h1 and p tags.
```
.main{
    width: 100vw;
    height: 100vh;
    display: flex;
    background-color: beige;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    font-weight: 700;
    font-size: 4rem;
}

p,h1{
    margin-top: 10px;
    font-size: 5rem;
}

p{
    color: rgb(7, 213, 96);
}
```
# JS File
The JavaScript code adds an event listener to the input field. When the user enters a keyword and presses the enter key, the keyword is displayed on the screen.
```
let container = document.querySelector(".main");

document.addEventListener("keydown", function (event) {
    container.innerText = "";
    console.log(event);
  
  	let h1 = document.createElement("h1");
    h1.innerText = ` You Pressed  ${event.key}`;
    let p = document.createElement("p");
    p.innerText = `${event.keyCode}`;
    container.appendChild(h1);
    container.appendChild(p);
});
```
