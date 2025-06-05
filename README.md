  <!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Buat Kamu yang Lagi Ngambek 💔</title>
  <style>
    body {
      font-family: 'Comic Sans MS', cursive, sans-serif;
      background-color: #ffe6e6;
      color: #333;
      text-align: center;
      padding: 30px;
    } 

    .box {
      background: #fff0f5;
      padding: 30px;
      border-radius: 20px;
      box-shadow: 0 0 20px #ffc0cb;
      max-width: 500px;
      margin: auto;
    }

    h1 {
      color: #e75480;
    }

    p {
      font-size: 18px;
    }

    button {
      background-color: #ff69b4;
      color: white;
      border: none;
      padding: 12px 20px;
      font-size: 16px;
      border-radius: 8px;
      cursor: pointer;
      margin-top: 15px;
    }

    button:hover {
      background-color: #ff1493;
    }

    .emoji {
      font-size: 2em;
      margin: 10px 0;
    }

    audio {
      display: none;
    }
  </style>
</head>
<body>

  <audio id="musik.mp3" autoplay loop>
    <source src="musik.mp3" type="audio/mpeg">
    Browser kamu tidak mendukung audio :(
  </audio>

  <div class="box">
    <h1>Hai... Pacarku Elvira Khairunnisa</h1>
    <p id="text">Buat kamu yang lagi kuliah..... Semangat ya sayangku kuliah nya
    <div class="emoji">😍</div>
    <button onclick="nextStep()">Lanjut Sayang...</button>
  </div>

  <script>
    const teksRayuan = [
      "Aku nggak suka lihat kamu sedih...",
      "Aku cuma mau bilang satu hal penting...",
      "Aku sayang banget sama kamu. ❤️",
      "Maaf ya kalau aku bikin kamu kecewa.",
      "Aku janji bakal lebih baik lagi.",
      "Boleh nggak kita baikan? 😢",
      "Aku kangen senyum kamu... 😭",
      "Ayo peluk dulu, meski cuma virtual... 🤗",
      "Makasih udah jadi orang paling sabar dan manis di dunia ini 💖"
    ];

    let index = 0;

    function nextStep() {
      if (index < teksRayuan.length) {
        document.getElementById("text").innerText = teksRayuan[index];
        index++;
      } else {
        document.querySelector("button").style.display = "none";
        document.querySelector(".emoji").innerText = "💞";
        document.getElementById("text").innerText = "Kita damai ya? Aku sayang kamu selalu. 😘";
      }
    }

    // Autoplay fix for some browsers (trigger on user interaction)
    document.addEventListener('click', function () {
      const music = document.getElementById("musik.mp3");
      if (music.paused) {
        music.play().catch(() => {});
      }
    }, { once: true });
  </script>

</body>
</html>
