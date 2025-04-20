# unite-quest-maker
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>프론티어 길드 퀘스트 생성기</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <style>
    body {
      background-image: url('https://images.unsplash.com/photo-1610312277056-21906a90e299?ixlib=rb-4.0.3&auto=format&fit=crop&w=1600&q=80');
      background-size: cover;
      background-position: center;
    }
  </style>
</head>
<body class="bg-yellow-50/90 font-serif min-h-screen flex items-center justify-center p-6">
  <div class="bg-white/90 backdrop-blur-md max-w-3xl w-full rounded-2xl shadow-2xl border border-yellow-300 p-6">
    
    <!-- 길드 제목 -->
    <div class="text-center mb-6">
      <h1 class="text-4xl font-extrabold text-yellow-900 drop-shadow-lg">🏰 프론티어 길드</h1>
      <p class="mt-2 text-gray-700 italic">신입 모험가를 위한 퀘스트 생성 시스템</p>
    </div>

    <!-- 버튼 -->
    <div class="flex justify-center mb-6">
      <button onclick="generateQuest()" class="bg-yellow-800 hover:bg-yellow-900 text-white py-2 px-6 rounded-xl text-lg transition">
        퀘스트 생성하기
      </button>
    </div>

    <!-- 결과 출력 -->
    <div id="output" class="bg-yellow-100 border border-yellow-300 p-4 rounded-lg space-y-2">
      <p class="text-gray-800"><strong>🎯 제목:</strong> <span id="title">-</span></p>
      <p class="text-gray-800"><strong>📜 내용:</strong> <span id="description">-</span></p>
      <p class="text-gray-800"><strong>💰 보상:</strong> <span id="reward">-</span></p>
      <p class="text-gray-800"><strong>🧭 유형:</strong> <span id="type">-</span></p>
    </div>

    <p class="text-center text-sm text-gray-500 mt-6">Powered by 프론티어 길드 | 디자인 참고: IceJack</p>
  </div>

  <script>
    const questTitles = ["숲의 마물 퇴치", "실종된 상인 수색", "마을 우물 정령 진정"];
    const questDescriptions = [
      "근처 숲에 마물이 출몰하여 주민들이 공포에 떨고 있습니다.",
      "마을로 향하던 상인이 실종되었습니다. 실마리를 찾아주세요.",
      "우물에서 이상한 소리가 들립니다. 정령이 분노한 것 같습니다."
    ];
    const rewards = ["500 골드 + 명성 10", "200 골드 + 아이템 보상", "1000 골드 + 희귀 아이템"];
    const types = ["퇴치", "탐색", "정령 진정", "호위", "정보 수집"];

    function generateQuest() {
      const randomIndex = () => Math.floor(Math.random() * 3);
      document.getElementById("title").innerText = questTitles[randomIndex()];
      document.getElementById("description").innerText = questDescriptions[randomIndex()];
      document.getElementById("reward").innerText = rewards[randomIndex()];
      document.getElementById("type").innerText = types[Math.floor(Math.random() * types.length)];
    }
  </script>
</body>
</html>
