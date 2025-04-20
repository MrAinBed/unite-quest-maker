<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>유나이트 길드 의뢰서</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <style>
    body {
      background-color: #fef9f0;
      background-image: url('https://via.placeholder.com/600x400?text=양피지');
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
}
  </style>
</head>
<body class="min-h-screen flex items-center justify-center p-6">

  <div class="parchment max-w-2xl w-full rounded-xl p-6 relative">
    <!-- 인장 -->
    <div class="absolute top-4 right-4">
      <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/90/Seal_red.svg/200px-Seal_red.svg.png" alt="유나이트 인장" class="w-16 opacity-80">
    </div>

    <h1 class="text-3xl font-bold text-center text-yellow-900 mb-4">유나이트 길드 의뢰서</h1>

    <form class="space-y-4">
      <div>
        <label class="block text-lg font-semibold text-gray-800">제목</label>
        <input type="text" id="title" class="w-full p-2 rounded-md border border-yellow-300 bg-yellow-50" placeholder="예: 고블린 소굴 소탕" />
      </div>

      <div>
        <label class="block text-lg font-semibold text-gray-800">내용</label>
        <textarea id="description" class="w-full h-28 p-2 rounded-md border border-yellow-300 bg-yellow-50" placeholder="의뢰 내용을 상세히 작성해주세요."></textarea>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
        <div>
          <label class="block text-lg font-semibold text-gray-800">보상</label>
          <input type="text" id="reward" class="w-full p-2 rounded-md border border-yellow-300 bg-yellow-50" placeholder="예: 300골드 + 명성 5" />
        </div>
        <div>
          <label class="block text-lg font-semibold text-gray-800">유형</label>
          <input type="text" id="type" class="w-full p-2 rounded-md border border-yellow-300 bg-yellow-50" placeholder="예: 퇴치 / 호위 / 정찰" />
        </div>
      </div>

      <div>
        <label class="block text-lg font-semibold text-gray-800">의뢰주</label>
        <input type="text" id="client" class="w-full p-2 rounded-md border border-yellow-300 bg-yellow-50" placeholder="예: 농장주 브렌" />
      </div>

      <div class="text-center mt-6">
        <button type="button" onclick="generateScroll()" class="bg-yellow-800 hover:bg-yellow-900 text-white py-2 px-6 rounded-xl text-lg shadow-lg">
          의뢰서 출력
        </button>
      </div>
    </form>

    <!-- 결과 출력: 양피지 느낌 박스 -->
    <div id="output" class="scroll-output mt-8 hidden border border-yellow-700 rounded-xl p-6 space-y-4 shadow-inner">
      <h2 class="text-2xl font-bold text-center"><span id="outTitle"></span></h2>
      <p><strong>내용:</strong> <span id="outDesc"></span></p>
      <p><strong>보상:</strong> <span id="outReward"></span></p>
      <p><strong>유형:</strong> <span id="outType"></span></p>
      <p><strong>의뢰주:</strong> <span id="outClient"></span></p>
    </div>
  </div>

  <script>
    function generateScroll() {
      document.getElementById("outTitle").innerText = document.getElementById("title").value;
      document.getElementById("outDesc").innerText = document.getElementById("description").value;
      document.getElementById("outReward").innerText = document.getElementById("reward").value;
      document.getElementById("outType").innerText = document.getElementById("type").value;
      document.getElementById("outClient").innerText = document.getElementById("client").value;

      document.getElementById("output").classList.remove("hidden");
    }
  </script>

</body>
</html>
