# unite-quest-maker
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>프론티어 길드 퀘스트 생성기</title>
  <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-yellow-50 font-serif p-4">
  <div class="max-w-3xl mx-auto p-6 bg-white rounded-2xl shadow-xl border border-yellow-200">
    
    <!-- 길드 제목 영역 -->
    <div class="text-center mb-6">
      <h1 class="text-4xl font-bold text-yellow-900 drop-shadow-lg">🏰 프론티어 길드</h1>
      <p class="mt-2 text-gray-700 italic">신입 모험가를 위한 퀘스트 발급 시스템</p>
    </div>
    
    <!-- 사용자 입력 영역 -->
    <div class="space-y-4">
      <div>
        <label class="block text-lg font-semibold text-gray-800">퀘스트 제목</label>
        <input type="text" class="w-full border rounded-lg p-2" placeholder="예: 숲의 마물 퇴치" />
      </div>

      <div>
        <label class="block text-lg font-semibold text-gray-800">의뢰 내용</label>
        <textarea class="w-full border rounded-lg p-2 h-32" placeholder="의뢰 내용을 작성해주세요."></textarea>
      </div>

      <div>
        <label class="block text-lg font-semibold text-gray-800">보상</label>
        <input type="text" class="w-full border rounded-lg p-2" placeholder="예: 500 골드 + 명성 10" />
      </div>

      <button class="w-full mt-4 bg-yellow-700 hover:bg-yellow-800 text-white py-2 px-4 rounded-xl transition">
        퀘스트 생성하기
      </button>
    </div>

    <!-- 결과 영역 -->
    <div class="mt-8 bg-yellow-100 border border-yellow-300 p-4 rounded-lg">
      <h2 class="text-xl font-bold text-yellow-900">📜 생성된 퀘스트</h2>
      <p class="text-gray-800 mt-2 italic">입력 내용을 기반으로 퀘스트가 여기 표시됩니다.</p>
    </div>

  </div>
</body>
</html>
