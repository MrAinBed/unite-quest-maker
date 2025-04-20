<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>유나이트 길드 의뢰서</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <style>
    @font-face {
      font-family: 'NanumMyeongjo';
      src: url('https://cdn.jsdelivr.net/gh/projectnoonnu/noonfonts_2107@1.1/NanumMyeongjo.woff') format('woff');
      font-weight: normal;
      font-style: normal;
    }

    body {
      background-color: #fef9f0;
      font-family: 'NanumMyeongjo', serif;
    }

    .scroll-output {
      position: relative;
      width: 600px;
      height: 850px;
      margin: auto;
      background-image: url('/mnt/data/77e1226a-e82e-44fd-99d4-cfe133eda768.png');
      background-size: contain;
      background-repeat: no-repeat;
      background-position: center;
      padding: 50px;
      color: #2f1b0c;
      box-shadow: 0 0 20px rgba(0, 0, 0, 0.3);
    }

    .scroll-output .field {
      position: absolute;
    }

    .title { top: 130px; left: 130px; font-size: 28px; font-weight: bold; }
    .subtitle { top: 180px; left: 135px; font-size: 16px; }
    .difficulty { top: 190px; right: 100px; font-size: 16px; }
    .reward { top: 300px; left: 100px; font-size: 16px; }
    .type { top: 330px; left: 100px; font-size: 16px; }
    .description { top: 370px; left: 100px; width: 400px; font-size: 16px; line-height: 1.5; }
    .client { bottom: 90px; left: 50px; font-size: 18px; }
  </style>
</head>
<body class="p-6">

  <div class="max-w-2xl mx-auto bg-white rounded-xl p-6 shadow-lg space-y-4">
    <h1 class="text-3xl font-bold text-center text-yellow-900 mb-4">유나이트 길드 의뢰서</h1>

    <form class="space-y-4">
      <input type="text" id="title" class="w-full p-2 border rounded-md" placeholder="제목" />
      <input type="text" id="subtitle" class="w-full p-2 border rounded-md" placeholder="부제목" />
      <input type="text" id="difficulty" class="w-full p-2 border rounded-md" placeholder="난이도" />
      <input type="text" id="type" class="w-full p-2 border rounded-md" placeholder="의뢰 유형" />
      <input type="text" id="reward" class="w-full p-2 border rounded-md" placeholder="보상" />
      <textarea id="description" class="w-full p-2 border rounded-md" placeholder="설명"></textarea>
      <input type="text" id="client" class="w-full p-2 border rounded-md" placeholder="의뢰주" />

      <button type="button" onclick="generateScroll()" class="bg-yellow-700 hover:bg-yellow-800 text-white px-4 py-2 rounded-md">
        의뢰서 출력
      </button>
    </form>
  </div>

  <!-- 출력 영역 -->
  <div id="output" class="scroll-output hidden mt-10">
    <div class="field title" id="outTitle"></div>
    <div class="field subtitle" id="outSubtitle"></div>
    <div class="field difficulty" id="outDifficulty"></div>
    <div class="field type" id="outType"></div>
    <div class="field reward" id="outReward"></div>
    <div class="field description" id="outDescription"></div>
    <div class="field client" id="outClient"></div>
  </div>

  <script>
    function generateScroll() {
      document.getElementById("outTitle").innerText = document.getElementById("title").value;
      document.getElementById("outSubtitle").innerText = document.getElementById("subtitle").value;
      document.getElementById("outDifficulty").innerText = document.getElementById("difficulty").value;
      document.getElementById("outType").innerText = document.getElementById("type").value;
      document.getElementById("outReward").innerText = document.getElementById("reward").value;
      document.getElementById("outDescription").innerText = document.getElementById("description").value;
      document.getElementById("outClient").innerText = document.getElementById("client").value;

      document.getElementById("output").classList.remove("hidden");
    }
  </script>

</body>
</html>
