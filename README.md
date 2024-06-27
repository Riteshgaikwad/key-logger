# Keypress Logger ⌨️

This simple web application keeps track of the keys you press on your keyboard! 

### Description

Start logging keypresses, and the application will display the pressed key and its state (down or up) in dedicated areas. You can stop logging at any time to clear the log and pause keypress detection.

### Features

* Logs keypresses (`keydown` and `keyup` events).
* Displays the pressed key and its state (down or up).
* Provides buttons to start and stop logging.
* Clears the log and resets the state display when stopping.

### How to Use

1. Open the `index.html` file in a web browser.
2. Click the "Start Logging Keypress" button.
3. Start typing - the application will log each keypress and its state.
4. When you're finished, click the "Stop Logging Keypress" button.
5. The application will stop logging and clear the previous entries.

### Technologies Used

* HTML: Provides the basic structure and content for the application.
* CSS: Styles the visual elements of the application for a user-friendly interface.
* JavaScript: Adds interactivity and handles keypress events.

### Installation

There's no complex installation required. Simply follow the "How to Use" instructions above.

### Contributing

We welcome contributions to this project! Feel free to fork the repository and submit pull requests with your improvements.


### Author

* [Ritesh Gaikwad] [https://github.com/Riteshgaikwad]

### Demo

[https://riteshgaikwad.github.io/key-logger/]

**Code Snippets**

Here are some relevant code snippets for reference:

***index.html***(structure sample)

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Keypress Logger</title>
  <style>
    /* Your CSS styles here */
  </style>
</head>
<body>
  <div class="container">
    <h1>KeyLogger</h1>
    <p>Don't forget to subscribe to our channel</p>
    <div class="button-container">
      <button id="start-btn">Start Logging Keypress</button>
      <button id="stop-btn">Stop Logging Keypress</button>
    </div>
    <div class="button-container">
      <div id="log"></div>
      <div id="state"></div>
    </div>
  </div>
  <script src="script.js"></script>
</body>
</html>

```

***style.css***(sample style)

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

h1 {
  border: 2px solid black;
  padding: 2px;
  border-radius: 10px;
}

.container {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 50px;
}

#log, #state {
  width: 500px;
  height: 50px;
  border: 1px solid black;
  padding: 10px;
  font-size: 20px;
  text-align: center;
  margin-top: 20px;
  background-color: #ffa500;
  border-radius: 10px;
}

.button-container {
  display: flex;
  flex-direction: row;
  gap: 10px;
}

button {
  font-size: 20px;
  padding: 10px 20px;
  margin-top: 20px;
}

```
***script.js***(stuctured logic)

```javascript
const logDiv = document.getElementById("log");
const stateDiv = document.getElementById("state");
const startBtn = document.getElementById("start-btn");
const stopBtn = document.getElementById("stop-btn");

startBtn.addEventListener("click", () => {
  document.addEventListener("keydown", handleDown);
  // ... rest of your JavaScript code
});
