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
      background-color: #f9f3e9;
      font-family: 'NanumMyeongjo', serif;
    }

    .scroll-paper {
      position: relative;
      background-image: url('/mnt/data/77e1226a-e82e-44fd-99d4-cfe133eda768.png');
      background-size: contain;
      background-repeat: no-repeat;
      width: 600px;
      height: 850px;
      margin: auto;
      padding: 60px 50px;
      box-shadow: 0 0 30px rgba(0,0,0,0.2);
    }

    .scroll-paper .field {
      position: absolute;
      color: #2c1a10;
    }

    .title { top: 130px; left: 130px; font-size: 28px; font-weight: bold; }
    .subtitle { top: 180px; left: 135px; font-size: 16px; }
    .difficulty { top: 190px; right: 100px; font-size: 16px; }
    .guild { bottom: 90px; left: 50px; font-size: 18px; }
  </style>
</head>
<body class="py-10">

  <div class="scroll-paper">
    <div class="field title" id="outTitle">temp</div>
    <div class="field subtitle" id="outSubtitle">부제목</div>
    <div class="field difficulty" id="outDifficulty">난이도</div>
    <div class="field guild">프론티어 길드</div>
  </div>

</body>
</html>
