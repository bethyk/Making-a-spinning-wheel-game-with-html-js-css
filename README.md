# Spinning Wheel Game

A spinning wheel game developed with **HTML, CSS, and JavaScript** and packaged as a desktop application with **Electron**.

The project includes a login screen, a limited-attempt authentication flow, an animated prize wheel, sound effects, and a balance system that is updated according to the result of each spin.

This application was created as part of a second-year final project.

## Features

- Login screen with username and password validation
- Maximum of three login attempts
- Animated spinning wheel with eight reward and penalty segments
- Randomized wheel rotation
- Balance increases or decreases based on the selected segment
- Persistent balance storage with browser `localStorage`
- Temporary result message after each spin
- Wheel sound effect during rotation
- Responsive visual layout
- Electron-based desktop application support

## Technologies

- HTML5
- CSS3
- JavaScript
- Electron
- Node.js
- Browser Local Storage

## How the Game Works

The player starts with a balance of `100 SC`.

When the **Spin** button is clicked:

1. A random rotation value is generated.
2. The wheel rotates to a new position.
3. The final angle determines the selected segment.
4. The corresponding reward or penalty is applied to the balance.
5. The updated balance is saved in `localStorage`.

The wheel contains the following values:

```text
+100
-500
+50
-100
+2000
+10
+5
-1
```

## Login

The application starts with a login screen. The user has three attempts to enter the correct credentials. After three unsuccessful attempts, the login fields and button are disabled.

The credentials currently used in the educational version of the project are defined directly in `form.html`.

> This login mechanism is intended only for demonstration purposes. Client-side credentials should not be used for real authentication systems.

## Original Artwork

The money symbol used in this project was originally drawn by **Betül Kızılkaya**.

The same original drawing is used in two ways:

- As the repeated money-symbol pattern in the background
- As the money symbol displayed next to the account balance

The background version is a duplicated arrangement of the same original illustration. The artwork was created and integrated into the interface by the project developer.

## Project Structure

```text
Making-a-spinning-wheel-game-with-html-js-css/
└── Spin Wheel/
    ├── form.html           # Login screen and validation logic
    ├── index.html          # Spinning wheel interface and game logic
    ├── style.css           # Wheel, layout, animation, and interface styles
    ├── main.js             # Electron main process
    ├── preload.js          # Electron preload script
    ├── package.json        # Electron project configuration
    ├── sound-step.mp3      # Wheel rotation sound
    └── image assets        # Background and interface graphics
```

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/betulkizilkaya/Making-a-spinning-wheel-game-with-html-js-css.git
cd Making-a-spinning-wheel-game-with-html-js-css/Spin\ Wheel
```

### 2. Install Node.js

Install a current version of Node.js and npm.

### 3. Install Electron

```bash
npm install --save-dev electron
```

### 4. Run the application

```bash
npm start
```

Electron opens `form.html` first. After a successful login, the application redirects to the spinning wheel page.

## Browser Usage

The HTML version can also be tested directly in a browser by opening `form.html`. Some Electron-specific behavior may not apply when the project is opened this way.

## Data Storage

The balance is stored locally in the browser or Electron session with:

```javascript
localStorage.setItem("money", JSON.stringify(balance));
```

No external database or server is required for the current version.

To reset the saved balance, clear the application's local storage data.

## Project Context

This project was developed as a second-year university final assignment. It is preserved as an academic project and is not currently under active development.

The repository reflects the scope and requirements of the original coursework.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

© 2024 [Betül Kızılkaya](https://github.com/betulkizilkaya)
