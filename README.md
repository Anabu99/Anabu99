<details>
<summary>Click to see a typing effect</summary>

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Typing Hello World</title>
  <style>
    .typing {
      font-family: 'Courier New', Courier, monospace;
      font-size: 2em;
      border-right: 2px solid;
      width: 15ch;
      white-space: nowrap;
      overflow: hidden;
      animation: typing 3s steps(15) 1s 1 normal both, blink 0.75s step-end infinite;
    }
    
    @keyframes typing {
      from {
        width: 0;
      }
      to {
        width: 15ch;
      }
    }
    
    @keyframes blink {
      50% {
        border-color: transparent;
      }
    }
  </style>
</head>
<body>
  <div class="typing">Hello, World!</div>

  <script>
    // This script ensures the typing effect works for GitHub markdown.
    window.addEventListener('load', function() {
      const element = document.querySelector('.typing');
      let text = element.textContent;
      element.textContent = '';
      
      let i = 0;
      let interval = setInterval(function() {
        element.textContent += text[i];
        i++;
        if (i >= text.length) {
          clearInterval(interval);
        }
      }, 200);
    });
  </script>
</body>
</html>

</details>
