<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>유나이트 길드 의뢰서</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <link href="https://fonts.googleapis.com/css2?family=Great+Vibes&display=swap" rel="stylesheet">
  <style>
    body {
      background-color: #fef9f0;
      font-family: 'Nanum Myeongjo', serif;
    }

    .parchment {
      background: #fdf6e3;
      border: 2px solid #d4b37f;
      box-shadow: 0 0 20px rgba(0,0,0,0.15);
      background-image: url('https://www.transparenttextures.com/patterns/aged-paper.png');
    }

    .scroll-output {
      background-image: url('https://cdn.pixabay.com/photo/2017/01/31/13/14/paper-2025378_1280.png');
      background-size: cover;
      background-repeat: no-repeat;
      background-position: center;
      background-color: #fdf6e3;
      min-height: 300px;
      color: #3b2f1c;
      font-family: 'Nanum Myeongjo', serif;
      border: 2px solid #d6b47d;
      position: relative;
    }

    .wax-seal {
      position: absolute;
      bottom: 20px;
      right: 20px;
      width: 80px;
      opacity: 0.8;
    }

    .signature {
      font-family: 'Great Vibes', cursive;
      font-size: 1.75rem;
      text-align: right;
      padding-top: 40px;
      color: #6b2e1c;
      padding-right: 20px;
    }
  </style>
</head>
<body class="min-h-screen flex items-center justify-center p-6">

  <div class="parchment max-w-2xl w-full rounded-xl p-6 relative">
    <h1 class="text-3xl font-bold text-center text-yellow-900 mb-4">유나이트 길드 의뢰서</h1>

    <form class="space-y-4">
      <div>
        <label class="block text-lg font-semibold text-gray-800">제목</label>
        <input type="text" id="title" class="w-full p-2 rounded-md border border-yellow-300 bg-yellow-50" />
      </div>

      <div>
        <label class="block text-lg font-semibold text-gray-800">난이도</label>
        <input type="text" id="difficulty" class="w-full p-2 rounded-md border border-yellow-300 bg-yellow-50" />
      </div>

      <div>
        <label class="block text-lg font-semibold text-gray-800">퀘스트 기간</label>
        <input type="text" id="duration" class="w-full p-2 rounded-md border border-yellow-300 bg-yellow-50" />
      </div>

      <div>
        <label class="block text-lg font-semibold text-gray-800">반복 가능 여부</label>
        <input type="text" id="repeatable" class="w-full p-2 rounded-md border border-yellow-300 bg-yellow-50" />
      </div>

      <div>
        <label class="block text-lg font-semibold text-gray-800">설명</label>
        <textarea id="description" class="w-full h-28 p-2 rounded-md border border-yellow-300 bg-yellow-50"></textarea>
      </div>

      <div>
        <label class="block text-lg font-semibold text-gray-800">의뢰 조건</label>
        <input type="text" id="condition" class="w-full p-2 rounded-md border border-yellow-300 bg-yellow-50" />
      </div>

      <div>
        <label class="block text-lg font-semibold text-gray-800">의뢰 유형</label>
        <input type="text" id="type" class="w-full p-2 rounded-md border border-yellow-300 bg-yellow-50" />
      </div>

      <div>
        <label class="block text-lg font-semibold text-gray-800">보상</label>
        <input type="text" id="reward" class="w-full p-2 rounded-md border border-yellow-300 bg-yellow-50" />
      </div>

      <div>
        <label class="block text-lg font-semibold text-gray-800">의뢰주</label>
        <input type="text" id="client" class="w-full p-2 rounded-md border border-yellow-300 bg-yellow-50" />
      </div>

      <div>
        <button type="button" onclick="generateScroll()" class="bg-yellow-800 hover:bg-yellow-900 text-white py-2 px-6 rounded-xl text-lg shadow-lg">
          의뢰서 출력
        </button>
      </div>
    </form>

  <!-- 출력 결과 -->
<div id="output" class="scroll-output mt-8 hidden relative rounded-xl shadow-inner text-center px-10 py-12">
  <div class="space-y-3">
    <h2 class="text-2xl font-bold"><span id="outTitle"></span></h2>
    <p><strong>난이도:</strong> <span id="outDifficulty"></span></p>
    <p><strong>퀘스트 기간:</strong> <span id="outDuration"></span></p>
    <p><strong>반복 가능 여부:</strong> <span id="outRepeatable"></span></p>
    <p><strong>설명:</strong> <span id="outDescription"></span></p>
    <p><strong>의뢰 조건:</strong> <span id="outCondition"></span></p>
    <p><strong>의뢰 유형:</strong> <span id="outType"></span></p>
    <p><strong>보상:</strong> <span id="outReward"></span></p>
    <p><strong>의뢰주:</strong> <span id="outClient"></span></p>
  </div>

  <!-- 실링 왁스 이미지 -->
  <img src="https://i.imgur.com/lxzPLbG.png" alt="실링 왁스" class="wax-seal">

  <!-- Unite 필기체 서명 -->
  <div class="signature">Unite</div>
</div>


  <script>
    function generateScroll() {
      document.getElementById("outTitle").innerText = document.getElementById("title").value;
      document.getElementById("outDifficulty").innerText = document.getElementById("difficulty").value;
      document.getElementById("outDuration").innerText = document.getElementById("duration").value;
      document.getElementById("outRepeatable").innerText = document.getElementById("repeatable").value;
      document.getElementById("outDescription").innerText = document.getElementById("description").value;
      document.getElementById("outCondition").innerText = document.getElementById("condition").value;
      document.getElementById("outType").innerText = document.getElementById("type").value;
      document.getElementById("outReward").innerText = document.getElementById("reward").value;
      document.getElementById("outClient").innerText = document.getElementById("client").value;

      document.getElementById("output").classList.remove("hidden");
    }
  </script>

</body>
</html>
