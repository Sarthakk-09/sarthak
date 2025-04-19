<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Alphabet Flashcards</title>
  <style>
    body {
      background: #f4f4f4;
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 20px;
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
    }

    .card {
      background-color: transparent;
      width: 140px;
      height: 180px;
      perspective: 1000px;
      margin: 10px;
    }

    .card-inner {
      position: relative;
      width: 100%;
      height: 100%;
      text-align: center;
      transition: transform 0.8s;
      transform-style: preserve-3d;
      cursor: pointer;
    }

    .card:hover .card-inner {
      transform: rotateY(180deg);
    }

    .card-front, .card-back {
      position: absolute;
      width: 100%;
      height: 100%;
      backface-visibility: hidden;
      border: 2px solid #333;
      border-radius: 10px;
      background: white;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      font-size: 2em;
      box-shadow: 0 4px 6px rgba(0,0,0,0.1);
    }

    .card-back {
      transform: rotateY(180deg);
      font-size: 1.2em;
    }

    .emoji {
      font-size: 2.5em;
      margin-top: 10px;
    }
  </style>
</head>
<body>

  <!-- A to Z Cards -->
  <script>
    const data = {
      A: ["Apple", "🍎"],
      B: ["Ball", "⚽"],
      C: ["Cat", "🐱"],
      D: ["Dog", "🐶"],
      E: ["Elephant", "🐘"],
      F: ["Fish", "🐟"],
      G: ["Grapes", "🍇"],
      H: ["House", "🏠"],
      I: ["Ice cream", "🍦"],
      J: ["Jug", "🫗"],
      K: ["Kite", "🪁"],
      L: ["Lion", "🦁"],
      M: ["Monkey", "🐒"],
      N: ["Nest", "🪺"],
      O: ["Owl", "🦉"],
      P: ["Parrot", "🦜"],
      Q: ["Queen", "👑"],
      R: ["Rabbit", "🐰"],
      S: ["Sun", "☀️"],
      T: ["Tiger", "🐯"],
      U: ["Umbrella", "🌂"],
      V: ["Van", "🚐"],
      W: ["Watch", "⌚"],
      X: ["Xylophone", "🎼"],
      Y: ["Yacht", "⛵"],
      Z: ["Zebra", "🦓"]
    };

    for (let letter in data) {
      document.write(`
        <div class="card">
          <div class="card-inner">
            <div class="card-front">
              ${letter}
            </div>
            <div class="card-back">
              ${letter} for ${data[letter][0]}<div class="emoji">${data[letter][1]}</div>
            </div>
          </div>
        </div>
      `);
    }
  </script>

</body>
</html>
