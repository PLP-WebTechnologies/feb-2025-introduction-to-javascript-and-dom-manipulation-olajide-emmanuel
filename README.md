# Introduction to JavaScript and DOM Manipulation

## Objectives

Write basic JavaScript functions.
Manipulate the DOM dynamically.
Respond to user interactions.

## Instructions

- Create a script.js file and link it to a HTML.
- Structure the document using DOCTYPE, html, head, and body.

>[!NOTE]
>  - Write JavaScript that:
>  - Changes text content dynamically.
>  - Modifies CSS styles via JavaScript.
>  - Adds or removes an element when a button is clicked.


# Tasks
- Create a well-structured HTML5 document.
- Use at least 5 different HTML elements.
- Ensure semantic correctness.

Happy Coding! 💻✨
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>PLP JavaScript Assignment</title>

  <!-- ====== CSS Styles ====== -->
  <style>
    body {
      font-family: sans-serif;
      padding: 20px;
    }

    button {
      margin-top: 10px;
      padding: 10px;
    }

    nav ul {
      list-style-type: none;
      padding: 0;
    }

    nav li {
      display: inline;
      margin-right: 10px;
    }

    nav a {
      text-decoration: none;
      color: #333;
    }
  </style>
</head>
<body>

  <!-- ====== HTML Content ====== -->
  <header>
    <h1 id="main-title">Welcome to My Page</h1>
  </header>

  <nav>
    <ul>
      <li><a href="#">Home</a></li>
      <li><a href="#">About</a></li>
    </ul>
  </nav>

  <main>
    <section>
      <p id="dynamic-text">This text will change when the button is clicked.</p>
      <button onclick="changeText()">Change Text</button>
    </section>

    <section>
      <button onclick="changeStyle()">Change Style</button>
    </section>

    <section>
      <button onclick="toggleElement()">Add/Remove Element</button>
      <div id="toggle-container"></div>
    </section>
  </main>

  <footer>
    <p>© 2025 PLP Assignment</p>
  </footer>

  <!-- ====== JavaScript ====== -->
  <script>
    function changeText() {
      const textElement = document.getElementById('dynamic-text');
      textElement.textContent = 'Text has been changed via JavaScript!';
    }

    function changeStyle() {
      const title = document.getElementById('main-title');
      title.style.color = 'blue';
      title.style.fontSize = '2.5rem';
      title.style.fontFamily = 'Arial, sans-serif';
    }

    function toggleElement() {
      const container = document.getElementById('toggle-container');
      const existing = document.getElementById('new-paragraph');

      if (existing) {
        container.removeChild(existing);
      } else {
        const newPara = document.createElement('p');
        newPara.id = 'new-paragraph';
        newPara.textContent = 'This paragraph was added dynamically!';
        container.appendChild(newPara);
      }
    }
  </script>

</body>
</html>
