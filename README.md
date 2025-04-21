<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8" />
  <title>유나이트 길드 의뢰서</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <style>
    @font-face {
      font-family: 'NanumMyeongjo';
      src: url('https://cdn.jsdelivr.net/gh/projectnoonnu/noonfonts_2107@1.1/NanumMyeongjo.woff') format('woff');
      font-weight: normal;
      font-style: normal;
    }
    @import url('https://fonts.googleapis.com/css2?family=Great+Vibes&display=swap');

    body {
      background-color: #fef9f0;
      font-family: 'NanumMyeongjo', serif;
    }

    .scroll-output {
      position: relative;
      width: 600px;
      height: 850px;
      margin: auto;
      background-image: url('https://imgur.com/a/JjijrTq.jpeg'); /* 새 배경 이미지 적용 */
      background-size: cover;
      background-repeat: no-repeat;
      background-position: center;
      padding: 50px;
      color: #2f1b0c;
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
    .client-box {
      bottom: 90px; left: 50px;
      font-size: 18px;
      display: flex;
      align-items: center;
      gap: 15px;
    }

    .signature {
      font-family: 'Great Vibes', cursive;
      font-size: 24px;
      color: #5e1d10;
    }

    .seal {
      width: 60px;
      height: auto;
    }
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

      <button type="button" onclick="generateScroll()" class="w-full bg-yellow-800 hover:bg-yellow-900 text-white font-semibold py-2 rounded-md">
        의뢰서 출력
      </button>
    </form>
  </div>

  <script>
    function generateScroll() {
      const title = document.getElementById('title').value;
      const subtitle = document.getElementById('subtitle').value;
      const difficulty = document.getElementById('difficulty').value;
      const reward = document.getElementById('reward').value;
      const type = document.getElementById('type').value;
      const description = document.getElementById('description').value;
      const client = document.getElementById('client').value;

      const scroll = document.createElement('div');
      scroll.className = 'scroll-output';

      scroll.innerHTML = `
        <div class="field title">${title}</div>
        <div class="field subtitle">${subtitle}</div>
        <div class="field difficulty">${difficulty}</div>
        <div class="field reward">${reward}</div>
        <div class="field type">${type}</div>
        <div class="field description">${description}</div>
        <div class="field client-box">
          <span class="signature">${client}</span>
          <span class="signature">Unite</span>
          <img src="https://upload.wikimedia.org/wikipedia/commons/9/94/Wax_Seal_Red.png" class="seal" />
        </div>
      `;

      const existing = document.getElementById('scroll-container');
      if (existing) existing.remove();

      const container = document.createElement('div');
      container.id = 'scroll-container';
      container.className = 'mt-10 flex justify-center';
      container.appendChild(scroll);
      document.body.appendChild(container);
    }
  </script>
</body>
</html>
