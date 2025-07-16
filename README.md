<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>🔥 일잘러 일못러 테스트: 나의 업무 잠재력 찾기! 🔥</title>
    <!-- Google Fonts - Noto Sans KR for better Korean typography -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@300;400;500;700;800&display=swap" rel="stylesheet">
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* Custom styles */
        body {
            font-family: 'Noto Sans KR', sans-serif; /* 친근한 한글 폰트 적용 */
            background-color: #f8faff; /* 더 밝고 부드러운 배경색 */
            display: flex;
            justify-content: center;
            align-items: flex-start; /* 상단에서 시작하도록 변경 */
            min-height: 100vh;
            padding: 30px 20px; /* 상하좌우 여백 추가 */
            box-sizing: border-box;
        }
        .container {
            background-color: #ffffff;
            padding: 40px; /* 여유로운 패딩 */
            border-radius: 20px; /* 더 부드러운 모서리 */
            box-shadow: 0 12px 30px rgba(0, 0, 0, 0.08); /* 은은한 그림자 */
            max-width: 900px;
            width: 100%;
            margin-top: 20px;
            box-sizing: border-box; /* 패딩이 너비에 포함되도록 */
        }
        h1, h2 {
            color: #2c3e50;
            font-weight: 700;
            margin-bottom: 25px; /* 제목 아래 여백 증가 */
        }
        .section-title {
            font-size: 2.5rem; /* 제목 크기 키움 */
            font-weight: 800; /* 더 두껍게 */
            color: #2b6cb0; /* 메인 컬러와 어울리는 청록색 계열 */
            text-align: center;
            padding-bottom: 15px; /* 아래쪽 패딩 증가 */
            border-bottom: 4px solid #4CAF50; /* 강조 라인 */
            line-height: 1.3;
        }
        .intro-text {
            text-align: center;
            margin-bottom: 35px; /* 오프닝 텍스트 아래 여백 증가 */
            font-size: 1.15rem; /* 텍스트 크기 키움 */
            color: #4a5568;
            line-height: 1.7; /* 줄 간격 조절 */
        }
        .answer-guide {
            background-color: #e6f7ff; /* 더 부드러운 파란 계열 배경 */
            padding: 20px 25px; /* 패딩 증가 */
            border-radius: 12px;
            border: 1px solid #90cdf4; /* 테두리 색상 조정 */
            margin-bottom: 40px; /* 가이드 아래 여백 증가 */
            font-size: 1rem;
            line-height: 1.8; /* 줄 간격 조절 */
            color: #2b6cb0; /* 텍스트 색상 조정 */
            text-align: left;
        }
        .answer-guide strong {
            color: #007bb5;
            font-weight: 700; /* 더 굵게 */
        }
        .answer-guide ul {
            margin-top: 10px; /* 목록 위 여백 */
            list-style: none; /* 기본 리스트 스타일 제거 */
            padding-left: 0;
        }
        .answer-guide ul li {
            margin-bottom: 8px; /* 리스트 항목 간 여백 */
            position: relative;
            padding-left: 28px; /* 이모지 공간 */
        }
        .answer-guide ul li::before {
            content: '👉'; /* 이모지 변경 */
            position: absolute;
            left: 0;
            font-size: 1.1em;
            top: 1px; /* 위치 조정 */
        }
        .question-item {
            margin-bottom: 25px; /* 질문 항목 간 여백 증가 */
            padding: 20px; /* 패딩 증가 */
            background-color: #ffffff;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.06); /* 은은한 그림자 */
            display: flex;
            flex-direction: column;
        }
        .question-item label {
            font-weight: 600; /* 더 굵게 */
            color: #2d3748;
            margin-bottom: 18px; /* 질문과 옵션 사이 여백 증가 */
            line-height: 1.7;
            font-size: 1.1rem; /* 텍스트 크기 키움 */
        }
        .question-item .options {
            display: flex;
            flex-wrap: wrap;
            gap: 15px; /* 옵션 간 여백 증가 */
            justify-content: center; /* 중앙 정렬 유지 */
        }
        .question-item input[type="radio"] {
            display: none;
        }
        .question-item .option-label {
            display: flex;
            align-items: center;
            justify-content: center;
            background-color: #f0f4f8; /* 더 부드러운 옵션 배경색 */
            padding: 12px 22px; /* 패딩 증가 */
            border-radius: 30px; /* 더 둥글게 */
            cursor: pointer;
            transition: all 0.3s ease-in-out;
            border: 2px solid #dbe2ea; /* 테두리 색상 조정 */
            color: #4a5568;
            font-weight: 500;
            width: 150px; /* 고정 너비 */
            height: 50px; /* 고정 높이 */
            flex-shrink: 0; /* 축소 방지 */
            flex-grow: 0; /* 확장 방지 */
            text-align: center;
            white-space: nowrap; /* 텍스트 줄바꿈 방지 */
        }
        .question-item .option-label:hover {
            background-color: #e2eaf0;
            border-color: #a0b0c0;
        }
        .question-item input[type="radio"]:checked + .option-label {
            background-color: #4CAF50;
            color: white;
            font-weight: 700; /* 선택 시 더 굵게 */
            border-color: #4CAF50;
            box-shadow: 0 6px 15px rgba(76, 175, 80, 0.3); /* 그림자 강도 조정 */
            transform: translateY(-3px); /* 선택 시 살짝 위로 이동 */
        }
        .submit-button {
            background-color: #4CAF50;
            color: white;
            padding: 18px 35px; /* 패딩 증가 */
            border: none;
            border-radius: 15px; /* 더 부드러운 모서리 */
            cursor: pointer;
            font-size: 1.3rem; /* 폰트 크기 키움 */
            font-weight: 700;
            transition: background-color 0.3s ease, transform 0.2s ease, box-shadow 0.3s ease;
            width: 100%;
            margin-top: 40px; /* 위 여백 증가 */
            box-shadow: 0 10px 25px rgba(76, 175, 80, 0.35); /* 그림자 강도 조정 */
        }
        .submit-button:hover {
            background-color: #45a049;
            transform: translateY(-4px); /* 호버 시 더 많이 이동 */
            box-shadow: 0 15px 30px rgba(76, 175, 80, 0.45);
        }
        .result-section {
            margin-top: 50px; /* 결과 섹션 위 여백 증가 */
            padding: 35px; /* 패딩 증가 */
            background-color: #f0fff4; /* 더 밝고 부드러운 초록 계열 배경 */
            border-radius: 25px; /* 더 둥근 모서리 */
            border: 3px solid #66bb6a; /* 테두리 색상 조정 */
            display: none;
            text-align: center;
            animation: fadeIn 0.8s ease-out; /* 부드러운 등장 애니메이션 */
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        .result-section h2 {
            color: #28a745;
            font-size: 2.5rem; /* 결과 제목 크기 키움 */
            margin-bottom: 30px; /* 아래 여백 증가 */
            position: relative;
        }
        .result-section h2::after {
            content: '✨'; /* 이모지 추가 */
            display: inline-block;
            margin-left: 10px;
            font-size: 0.8em;
            vertical-align: middle;
        }
        .result-section h2::before { /* 아래 라인을 이모지 대신 사용 */
            content: '';
            display: block;
            width: 80px; /* 라인 길이 증가 */
            height: 5px; /* 라인 두께 증가 */
            background-color: #28a745;
            margin: 20px auto 0; /* 여백 조정 */
            border-radius: 3px;
        }
        .score-display {
            font-size: 3rem; /* 점수 표시 크기 키움 */
            font-weight: 800;
            color: #28a745;
            margin-bottom: 30px;
            animation: pulse 2s infinite ease-in-out; /* 애니메이션 속도 조정 */
        }
        @keyframes pulse {
            0% { transform: scale(1); opacity: 1; }
            50% { transform: scale(1.03); opacity: 0.95; } /* 효과를 더 부드럽게 */
            100% { transform: scale(1); opacity: 1; }
        }
        .diagnosis-summary {
            font-size: 1.3rem; /* 요약 텍스트 크기 키움 */
            line-height: 2; /* 줄 간격 넓힘 */
            color: #333;
            margin-bottom: 35px; /* 아래 여백 증가 */
            background-color: #f8fffb; /* 더 밝은 배경 */
            padding: 25px; /* 패딩 증가 */
            border-radius: 15px;
            border: 1px solid #c8e6c9; /* 테두리 색상 조정 */
            font-weight: 500;
        }
        .diagnosis-summary strong {
            color: #28a745;
        }
        .diagnosis-detail {
            text-align: left;
            margin-top: 30px; /* 위 여백 증가 */
        }
        .diagnosis-detail h3 {
            font-size: 1.8rem; /* 세부 진단 제목 크기 */
            color: #3f51b5; /* 파란 계열 색상 */
            margin-bottom: 20px; /* 아래 여백 증가 */
            border-bottom: 2px solid #a7d9ed; /* 테두리 색상 조정 */
            padding-bottom: 10px;
            font-weight: 700;
        }
        .diagnosis-detail p {
            font-size: 1.15rem; /* 텍스트 크기 */
            line-height: 1.8;
            color: #555;
            margin-bottom: 15px; /* 아래 여백 증가 */
        }
        .diagnosis-detail ul {
            list-style-type: none;
            padding-left: 0;
            margin-top: 15px; /* 목록 위 여백 */
        }
        .diagnosis-detail ul li {
            position: relative;
            padding-left: 30px; /* 이모지 공간 */
            margin-bottom: 12px; /* 리스트 항목 간 여백 */
            color: #555;
            font-size: 1.05rem;
        }
        .diagnosis-detail ul li::before {
            content: '✅';
            position: absolute;
            left: 0;
            color: #4CAF50;
            font-size: 1.3em; /* 이모지 크기 키움 */
            top: 2px; /* 위치 조정 */
        }
        .domain-score-section {
            margin-top: 40px; /* 위 여백 증가 */
            padding: 25px; /* 패딩 증가 */
            background-color: #e3f2fd; /* 더 밝고 부드러운 하늘색 배경 */
            border-radius: 20px; /* 둥근 모서리 */
            border: 2px solid #90caf9; /* 테두리 색상 조정 */
        }
        .domain-score-section h3 {
            font-size: 2rem; /* 영역별 점수 제목 크기 키움 */
            color: #1976d2; /* 파란색 계열 */
            margin-bottom: 25px; /* 아래 여백 증가 */
            text-align: center;
            font-weight: 700;
        }
        .domain-score-item {
            display: flex;
            flex-direction: column; /* 항목을 세로로 정렬 */
            align-items: flex-start; /* 왼쪽 정렬 */
            padding: 12px 0; /* 패딩 증가 */
            border-bottom: 1px dashed #bbdefb; /* 테두리 색상 조정 */
            margin-bottom: 15px; /* 항목 간 여백 */
        }
        .domain-score-item:last-child {
            border-bottom: none;
            margin-bottom: 0;
        }
        .domain-score-item .domain-name {
            font-size: 1.15rem; /* 폰트 크기 키움 */
            font-weight: 600;
            color: #263238;
            margin-bottom: 8px; /* 이름 아래 여백 */
        }
        .progress-bar-container {
            width: 100%;
            background-color: #e0e0e0;
            border-radius: 10px;
            height: 20px; /* 바 높이 */
            overflow: hidden; /* 내부 바가 튀어나오지 않도록 */
            margin-bottom: 8px; /* 바 아래 여백 */
        }
        .progress-bar {
            height: 100%;
            background-color: #66bb6a; /* 진행 바 색상 */
            border-radius: 10px;
            transition: width 0.8s ease-out; /* 부드러운 애니메이션 */
            display: flex;
            align-items: center;
            justify-content: flex-end; /* 점수를 오른쪽에 표시 */
            padding-right: 8px;
            box-sizing: border-box;
        }
        .progress-bar .score-text {
            color: white;
            font-weight: 700;
            font-size: 0.9rem;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.3);
        }
        /* Responsive adjustments */
        @media (max-width: 768px) {
            body {
                padding: 20px 15px; /* 모바일 패딩 조정 */
            }
            .container {
                padding: 25px;
                margin-top: 15px;
            }
            .section-title {
                font-size: 2rem;
            }
            .intro-text {
                font-size: 1rem;
                margin-bottom: 25px;
            }
            .answer-guide {
                padding: 15px 20px;
                font-size: 0.9rem;
                margin-bottom: 30px;
            }
            .answer-guide ul li::before {
                font-size: 1em;
                top: 0;
            }
            .question-item {
                padding: 15px;
                margin-bottom: 20px;
            }
            .question-item label {
                font-size: 1rem;
                margin-bottom: 15px;
            }
            .question-item .options {
                flex-direction: column; /* 모바일에서 옵션 세로 정렬 */
                align-items: stretch; /* 전체 너비로 확장 */
                gap: 10px; /* 옵션 간 간격 조정 */
            }
            .question-item .option-label {
                padding: 12px 15px;
                font-size: 0.95rem;
                min-width: unset; /* 최소 너비 해제 */
                width: auto; /* 모바일에서 auto로 변경 */
                height: auto; /* 모바일에서 auto로 변경 */
            }
            .submit-button {
                font-size: 1.15rem;
                padding: 15px 25px;
                margin-top: 30px;
            }
            .result-section {
                padding: 25px;
                margin-top: 40px;
            }
            .result-section h2 {
                font-size: 2rem;
                margin-bottom: 20px;
            }
            .result-section h2::before {
                width: 60px;
                margin: 15px auto 0;
            }
            .score-display {
                font-size: 2.5rem;
                margin-bottom: 20px;
            }
            .diagnosis-summary {
                font-size: 1.05rem;
                padding: 20px;
                margin-bottom: 25px;
            }
            .diagnosis-detail h3 {
                font-size: 1.5rem;
                margin-bottom: 15px;
            }
            .diagnosis-detail p, .diagnosis-detail ul li {
                font-size: 0.95rem;
                line-height: 1.6;
            }
            .diagnosis-detail ul li {
                padding-left: 25px;
                margin-bottom: 8px;
            }
            .diagnosis-detail ul li::before {
                font-size: 1.1em;
                top: 1px;
            }
            .domain-score-section {
                padding: 20px;
                margin-top: 30px;
            }
            .domain-score-section h3 {
                font-size: 1.6rem;
                margin-bottom: 20px;
            }
            .domain-score-item {
                align-items: center; /* 모바일에서 다시 중앙 정렬 */
            }
            .domain-score-item .domain-name {
                width: 100%; /* 이름도 전체 너비 */
                text-align: center; /* 이름 중앙 정렬 */
            }
            .progress-bar-container {
                width: calc(100% - 20px); /* 좌우 여백 고려 */
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1 class="section-title">🔥 일잘러 일못러 테스트: 나의 업무 잠재력 찾기! 🔥</h1>
        <p class="intro-text">
            안녕하세요! 🎉 당신의 숨겨진 **업무 잠재력**을 쉽고 재미있게 탐험해 볼 시간이에요! ✨ 지금부터 솔직한 마음으로 질문에 답하며, 당신의 진짜 업무 스타일이 '일잘러'에 가까운지, 아니면 '일못러'에서 '일잘러'로 변신 중인지 함께 알아봐요! 😉
        </p>

        <div class="answer-guide">
            <p><strong>답변 선택 가이드:</strong> 신중하게 가장 가까운 보기를 선택해 주세요.</p>
            <ul>
                <li>**거의 항상 그래요!:** 10번 중 9번 이상 해당될 때 선택해 주세요. 👍</li>
                <li>**자주 그런 편이에요:** 10번 중 7~8번 정도 해당될 때요. 😊</li>
                <li>**반반인 것 같아요:** 10번 중 5~6번 정도 해당된다면요. 🤔</li>
                <li>**가끔 그런 편이에요:** 10번 중 3~4번 정도 해당될 때요. 😅</li>
                <li>**거의 그렇지 않아요:** 10번 중 1~2번 이하로 해당된다면요. 😥</li>
            </ul>
        </div>

        <form id="selfDiagnosisForm">
            <!-- Questions will be dynamically shuffled and appended here by JavaScript -->
            <!-- Question 1-1 (업무의 양) -->
            <div class="question-item" id="q_item_1_1">
                <label for="q1_1">1. 주어진 시간 안에 가치 있는 결과물을 얼마나 많이 생산해냅니까?</label>
                <div class="options">
                    <input type="radio" id="q1_1_5" name="q1_1" value="5" required>
                    <label for="q1_1_5" class="option-label">매우 그렇다</label>
                    <input type="radio" id="q1_1_4" name="q1_1" value="4">
                    <label for="q1_1_4" class="option-label">그렇다</label>
                    <input type="radio" id="q1_1_3" name="q1_1" value="3">
                    <label for="q1_1_3" class="option-label">보통이다</label>
                    <input type="radio" id="q1_1_2" name="q1_1" value="2">
                    <label for="q1_1_2" class="option-label">거의 그렇지 않다</label>
                    <input type="radio" id="q1_1_1" name="q1_1" value="1">
                    <label for="q1_1_1" class="option-label">전혀 그렇지 않다</label>
                </div>
            </div>

            <!-- Question 1-2 (업무의 양) -->
            <div class="question-item" id="q_item_1_2">
                <label for="q1_2">2. 업무량이 많아질 때도, 효율성을 유지하며 목표를 달성할 수 있습니까?</label>
                <div class="options">
                    <input type="radio" id="q1_2_5" name="q1_2" value="5" required>
                    <label for="q1_2_5" class="option-label">매우 그렇다</label>
                    <input type="radio" id="q1_2_4" name="q1_2" value="4">
                    <label for="q1_2_4" class="option-label">그렇다</label>
                    <input type="radio" id="q1_2_3" name="q1_2" value="3">
                    <label for="q1_2_3" class="option-label">보통이다</label>
                    <input type="radio" id="q1_2_2" name="q1_2" value="2">
                    <label for="q1_2_2" class="option-label">거의 그렇지 않다</label>
                    <input type="radio" id="q1_2_1" name="q1_2" value="1">
                    <label for="q1_2_1" class="option-label">전혀 그렇지 않다</label>
                </div>
            </div>

            <!-- Question 1-3 (업무의 양) -->
            <div class="question-item" id="q_item_1_3">
                <label for="q1_3">3. 동시에 여러 업무를 처리할 때, 각 업무의 진행 상황을 효과적으로 관리할 수 있습니까?</label>
                <div class="options">
                    <input type="radio" id="q1_3_5" name="q1_3" value="5" required>
                    <label for="q1_3_5" class="option-label">매우 그렇다</label>
                    <input type="radio" id="q1_3_4" name="q1_3" value="4">
                    <label for="q1_3_4" class="option-label">그렇다</label>
                    <input type="radio" id="q1_3_3" name="q1_3" value="3">
                    <label for="q1_3_3" class="option-label">보통이다</label>
                    <input type="radio" id="q1_3_2" name="q1_3" value="2">
                    <label for="q1_3_2" class="option-label">거의 그렇지 않다</label>
                    <input type="radio" id="q1_3_1" name="q1_3" value="1">
                    <label for="q1_3_1" class="option-label">전혀 그렇지 않다</label>
                </div>
            </div>

            <!-- Question 2-1 (완성도) -->
            <div class="question-item" id="q_item_2_1">
                <label for="q2_1">4. 업무 결과물에 실수가 거의 없고, 높은 완성도를 보여줍니까?</label>
                <div class="options">
                    <input type="radio" id="q2_1_5" name="q2_1" value="5" required>
                    <label for="q2_1_5" class="option-label">매우 그렇다</label>
                    <input type="radio" id="q2_1_4" name="q2_1" value="4">
                    <label for="q2_1_4" class="option-label">그렇다</label>
                    <input type="radio" id="q2_1_3" name="q2_1" value="3">
                    <label for="q2_1_3" class="option-label">보통이다</label>
                    <input type="radio" id="q2_1_2" name="q2_1" value="2">
                    <label for="q2_1_2" class="option-label">거의 그렇지 않다</label>
                    <input type="radio" id="q2_1_1" name="q2_1" value="1">
                    <label for="q2_1_1" class="option-label">전혀 그렇지 않다</label>
                </div>
            </div>

            <!-- Question 2-2 (완성도) -->
            <div class="question-item" id="q_item_2_2">
                <label for="q2_2">5. 결과물이 고객이나 동료의 기대치를 충족시키고 만족을 주는 수준입니까?</label>
                <div class="options">
                    <input type="radio" id="q2_2_5" name="q2_2" value="5" required>
                    <label for="q2_2_5" class="option-label">매우 그렇다</label>
                    <input type="radio" id="q2_2_4" name="q2_2" value="4">
                    <label for="q2_2_4" class="option-label">그렇다</label>
                    <input type="radio" id="q2_2_3" name="q2_2" value="3">
                    <label for="q2_2_3" class="option-label">보통이다</label>
                    <input type="radio" id="q2_2_2" name="q2_2" value="2">
                    <label for="q2_2_2" class="option-label">거의 그렇지 않다</label>
                    <input type="radio" id="q2_2_1" name="q2_2" value="1">
                    <label for="q2_2_1" class="option-label">전혀 그렇지 않다</label>
                </div>
            </div>

            <!-- Question 2-3 (완성도) -->
            <div class="question-item" id="q_item_2_3">
                <label for="q2_3">6. 스스로 업무 결과물의 품질을 높이기 위해 지속적으로 노력하고 개선합니까?</label>
                <div class="options">
                    <input type="radio" id="q2_3_5" name="q2_3" value="5" required>
                    <label for="q2_3_5" class="option-label">매우 그렇다</label>
                    <input type="radio" id="q2_3_4" name="q2_3" value="4">
                    <label for="q2_3_4" class="option-label">그렇다</label>
                    <input type="radio" id="q2_3_3" name="q2_3" value="3">
                    <label for="q2_3_3" class="option-label">보통이다</label>
                    <input type="radio" id="q2_3_2" name="q2_3" value="2">
                    <label for="q2_3_2" class="option-label">거의 그렇지 않다</label>
                    <input type="radio" id="q2_3_1" name="q2_3" value="1">
                    <label for="q2_3_1" class="option-label">전혀 그렇지 않다</label>
                </div>
            </div>

            <!-- Question 3-1 (난이도) -->
            <div class="question-item" id="q_item_3_1">
                <label for="q3_1">7. 복잡하거나 어려운 "일"에 주저앉지 않고 스스로 해결하려 노력합니까?</label>
                <div class="options">
                    <input type="radio" id="q3_1_5" name="q3_1" value="5" required>
                    <label for="q3_1_5" class="option-label">매우 그렇다</label>
                    <input type="radio" id="q3_1_4" name="q3_1" value="4">
                    <label for="q3_1_4" class="option-label">그렇다</label>
                    <input type="radio" id="q3_1_3" name="q3_1" value="3">
                    <label for="q3_1_3" class="option-label">보통이다</label>
                    <input type="radio" id="q3_1_2" name="q3_1" value="2">
                    <label for="q3_1_2" class="option-label">거의 그렇지 않다</label>
                    <input type="radio" id="q3_1_1" name="q3_1" value="1">
                    <label for="q3_1_1" class="option-label">전혀 그렇지 않다</label>
                </div>
            </div>

            <!-- Question 3-2 (난이도) -->
            <div class="question-item" id="q_item_3_2">
                <label for="q3_2">8. 어려운 문제를 성공적으로 해결하기 위해 새로운 방법이나 접근 방식을 적극적으로 찾아 적용합니까?</label>
                <div class="options">
                    <input type="radio" id="q3_2_5" name="q3_2" value="5" required>
                    <label for="q3_2_5" class="option-label">매우 그렇다</label>
                    <input type="radio" id="q3_2_4" name="q3_2" value="4">
                    <label for="q3_2_4" class="option-label">그렇다</label>
                    <input type="radio" id="q3_2_3" name="q3_2" value="3">
                    <label for="q3_2_3" class="option-label">보통이다</label>
                    <input type="radio" id="q3_2_2" name="q3_2" value="2">
                    <label for="q3_2_2" class="option-label">거의 그렇지 않다</label>
                    <input type="radio" id="q3_2_1" name="q3_2" value="1">
                    <label for="q3_2_1" class="option-label">전혀 그렇지 않다</label>
                </div>
            </div>

            <!-- Question 3-3 (난이도) -->
            <div class="question-item" id="q_item_3_3">
                <label for="q3_3">9. 자신의 역량을 넘어서는 난이도의 업무를 통해 성장하는 것을 긍정적으로 받아들입니까?</label>
                <div class="options">
                    <input type="radio" id="q3_3_5" name="q3_3" value="5" required>
                    <label for="q3_3_5" class="option-label">매우 그렇다</label>
                    <input type="radio" id="q3_3_4" name="q3_3" value="4">
                    <label for="q3_3_4" class="option-label">그렇다</label>
                    <input type="radio" id="q3_3_3" name="q3_3" value="3">
                    <label for="q3_3_3" class="option-label">보통이다</label>
                    <input type="radio" id="q3_3_2" name="q3_3" value="2">
                    <label for="q3_3_2" class="option-label">거의 그렇지 않다</label>
                    <input type="radio" id="q3_3_1" name="q3_3" value="1">
                    <label for="q3_3_1" class="option-label">전혀 그렇지 않다</label>
                </div>
            </div>

            <!-- Question 4-1 (시간) -->
            <div class="question-item" id="q_item_4_1">
                <label for="q4_1">10. 주어진 기한보다 빠르고 정확히 "일"을 완료할 수 있습니까?</label>
                <div class="options">
                    <input type="radio" id="q4_1_5" name="q4_1" value="5" required>
                    <label for="q4_1_5" class="option-label">매우 그렇다</label>
                    <input type="radio" id="q4_1_4" name="q4_1" value="4">
                    <label for="q4_1_4" class="option-label">그렇다</label>
                    <input type="radio" id="q4_1_3" name="q4_1" value="3">
                    <label for="q4_1_3" class="option-label">보통이다</label>
                    <input type="radio" id="q4_1_2" name="q4_1" value="2">
                    <label for="q4_1_2" class="option-label">거의 그렇지 않다</label>
                    <input type="radio" id="q4_1_1" name="q4_1" value="1">
                    <label for="q4_1_1" class="option-label">전혀 그렇지 않다</label>
                </div>
            </div>

            <!-- Question 4-2 (시간) -->
            <div class="question-item" id="q_item_4_2">
                <label for="q4_2">11. 효율적인 시간 관리를 통해 업무 생산성을 극대화합니까?</label>
                <div class="options">
                    <input type="radio" id="q4_2_5" name="q4_2" value="5" required>
                    <label for="q4_2_5" class="option-label">매우 그렇다</label>
                    <input type="radio" id="q4_2_4" name="q4_2" value="4">
                    <label for="q4_2_4" class="option-label">그렇다</label>
                    <input type="radio" id="q4_2_3" name="q4_2" value="3">
                    <label for="q4_2_3" class="option-label">보통이다</label>
                    <input type="radio" id="q4_2_2" name="q4_2" value="2">
                    <label for="q4_2_2" class="option-label">거의 그렇지 않다</label>
                    <input type="radio" id="q4_2_1" name="q4_2" value="1">
                    <label for="q4_2_1" class="option-label">전혀 그렇지 않다</label>
                </div>
            </div>

            <!-- Question 4-3 (시간) -->
            <div class="question-item" id="q_item_4_3">
                <label for="q4_3">12. 업무 방해 요소나 예상치 못한 상황에도 시간 계획을 유연하게 조정하여 목표를 달성합니까?</label>
                <div class="options">
                    <input type="radio" id="q4_3_5" name="q4_3" value="5" required>
                    <label for="q4_3_5" class="option-label">매우 그렇다</label>
                    <input type="radio" id="q4_3_4" name="q4_3" value="4">
                    <label for="q4_3_4" class="option-label">그렇다</label>
                    <input type="radio" id="q4_3_3" name="q4_3" value="3">
                    <label for="q4_3_3" class="option-label">보통이다</label>
                    <input type="radio" id="q4_3_2" name="q4_3" value="2">
                    <label for="q4_3_2" class="option-label">거의 그렇지 않다</label>
                    <input type="radio" id="q4_3_1" name="q4_3" value="1">
                    <label for="q4_3_1" class="option-label">전혀 그렇지 않다</label>
                </div>
            </div>

            <!-- Submit button moved to the end of the form -->
            <button type="submit" class="submit-button">나의 일잘러 레벨 확인하기! 🚀</button>
        </form>

        <div id="resultSection" class="result-section">
            <h2>진단 결과 분석!</h2>
            <p class="score-display">총점: <span id="totalScore">0</span>점</p>

            <div class="domain-score-section">
                <h3>영역별 점수 살펴보기 🔍</h3>
                <div class="domain-score-item">
                    <span class="domain-name">업무의 양</span>
                    <div class="progress-bar-container">
                        <div class="progress-bar" id="domain1ProgressBar">
                            <span class="score-text" id="domain1Score">0점</span>
                        </div>
                    </div>
                </div>
                <div class="domain-score-item">
                    <span class="domain-name">완성도</span>
                    <div class="progress-bar-container">
                        <div class="progress-bar" id="domain2ProgressBar">
                            <span class="score-text" id="domain2Score">0점</span>
                        </div>
                    </div>
                </div>
                <div class="domain-score-item">
                    <span class="domain-name">난이도</span>
                    <div class="progress-bar-container">
                        <div class="progress-bar" id="domain3ProgressBar">
                            <span class="score-text" id="domain3Score">0점</span>
                        </div>
                    </div>
                </div>
                <div class="domain-score-item">
                    <span class="domain-name">시간</span>
                    <div class="progress-bar-container">
                        <div class="progress-bar" id="domain4ProgressBar">
                            <span class="score-text" id="domain4Score">0점</span>
                        </div>
                    </div>
                </div>
            </div>

            <p class="diagnosis-summary" id="diagnosisSummary"></p>
            <div id="diagnosisDetail" class="diagnosis-detail"></div>
        </div>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const form = document.getElementById('selfDiagnosisForm');
            const questionsContainer = form;
            const questionItems = Array.from(questionsContainer.getElementsByClassName('question-item'));
            const submitButton = document.querySelector('.submit-button'); // Get reference to the submit button

            // Fisher-Yates (Knuth) Shuffle algorithm
            function shuffleArray(array) {
                for (let i = array.length - 1; i > 0; i--) {
                    const j = Math.floor(Math.random() * (i + 1));
                    [array[i], array[j]] = [array[j], array[i]]; // Swap elements
                }
            }

            // Shuffle and re-append questions
            shuffleArray(questionItems);
            questionItems.forEach(item => {
                questionsContainer.appendChild(item);
            });

            // Append the submit button AFTER all shuffled questions
            // This ensures it's always at the very end of the form content.
            questionsContainer.appendChild(submitButton);


            // Update question numbers after shuffling
            questionItems.forEach((item, index) => {
                const label = item.querySelector('label');
                if (label) {
                    const originalText = label.textContent.replace(/^\d+\.\s*/, '');
                    label.textContent = `${index + 1}. ${originalText}`;
                }
            });
        });

        document.getElementById('selfDiagnosisForm').addEventListener('submit', function(event) {
            event.preventDefault(); // Prevent default form submission

            let totalScore = 0;
            let domainScores = {
                domain1: 0, // 업무의 양
                domain2: 0, // 완성도
                domain3: 0, // 난이도
                domain4: 0  // 시간
            };

            const form = event.target;
            const domainQuestions = {
                domain1: ['q1_1', 'q1_2', 'q1_3'],
                domain2: ['q2_1', 'q2_2', 'q2_3'],
                domain3: ['q3_1', 'q3_2', 'q3_3'],
                domain4: ['q4_1', 'q4_2', 'q4_3']
            };

            // 필수 응답 확인 (모든 질문에 답했는지)
            let allAnswered = true;
            for (const domain in domainQuestions) {
                for (const questionName of domainQuestions[domain]) {
                    const selectedOption = form.elements[questionName];
                    let isChecked = false;
                    if (selectedOption && selectedOption.length > 0) { // RadioNodeList
                        for (let i = 0; i < selectedOption.length; i++) {
                            if (selectedOption[i].checked) {
                                isChecked = true;
                                break;
                            }
                        }
                    } else if (selectedOption && selectedOption.checked) { // Single radio
                        isChecked = true;
                    }

                    if (!isChecked) {
                        allAnswered = false;
                        break;
                    }
                }
                if (!allAnswered) {
                    // console.warn(`Question ${questionName} not answered.`); // Debugging
                    break;
                }
            }

            if (!allAnswered) {
                // alert() 대신 커스텀 메시지 박스 또는 UI 피드백 사용 권장
                // 여기서는 간단히 alert()를 사용했지만, 실제 서비스에서는 사용자 친화적인 모달 등을 구현하는 것이 좋습니다.
                alert('앗! 모든 질문에 답변해주셔야 정확한 진단이 가능해요! 😊');
                return; // 제출 중단
            }

            // 점수 계산
            for (const domain in domainQuestions) {
                domainQuestions[domain].forEach(questionName => {
                    const selectedValue = form.elements[questionName].value;
                    const score = parseInt(selectedValue);
                    if (!isNaN(score)) {
                        domainScores[domain] += score;
                        totalScore += score;
                    }
                });
            }

            // 결과 표시
            document.getElementById('totalScore').textContent = totalScore;

            // 영역별 점수 및 프로그레스 바 업데이트
            const maxScorePerDomain = 15; // 각 영역당 최대 점수 (5점 * 3문제)
            document.getElementById('domain1Score').textContent = domainScores.domain1 + '점';
            document.getElementById('domain1ProgressBar').style.width = `${(domainScores.domain1 / maxScorePerDomain) * 100}%`;
            document.getElementById('domain2Score').textContent = domainScores.domain2 + '점';
            document.getElementById('domain2ProgressBar').style.width = `${(domainScores.domain2 / maxScorePerDomain) * 100}%`;
            document.getElementById('domain3Score').textContent = domainScores.domain3 + '점';
            document.getElementById('domain3ProgressBar').style.width = `${(domainScores.domain3 / maxScorePerDomain) * 100}%`;
            document.getElementById('domain4Score').textContent = domainScores.domain4 + '점';
            document.getElementById('domain4ProgressBar').style.width = `${(domainScores.domain4 / maxScorePerDomain) * 100}%`;


            const diagnosisSummaryDiv = document.getElementById('diagnosisSummary');
            const diagnosisDetailDiv = document.getElementById('diagnosisDetail');
            let summaryText = '';
            let detailHtml = '';

            // 총점 기준 진단 (최대 60점)
            if (totalScore >= 45) { // 45점 이상 (최고점 60점)
                summaryText = `
                    와우! 🎉 당신은 그냥 '일잘러'가 아니었어요! 타고난 **업무 마스터**였군요! ✨ 모든 영역에서 빛나는 역량을 보여주며, 주변 사람들을 깜짝 놀라게 하고 있답니다!
                `;
                detailHtml = `
                    <h3>🌟 세부 진단: 빛나는 업무 마스터! 🌟</h3>
                    <p>당신은 마치 슈퍼히어로 같아요! 💪 다음과 같은 놀라운 강점들을 가지고 있어요:</p>
                    <ul>
                        <li><strong>업무의 양 & 완성도:</strong> 주어진 시간 안에 정말 많은 가치 있는 결과물을 척척 만들어내고, 아무리 업무가 많아도 끄떡없이 효율성을 유지해요. 당신의 결과물은 거의 완벽에 가까워요! 실수가 거의 없고, 높은 품질로 고객과 동료 모두에게 깊은 만족을 선사하죠. **양과 질 모두 잡은 진정한 일잘러예요!** 특히, 업무량이 많아질수록 빛을 발하는 스타일이네요.</li>
                        <li><strong>난이도:</strong> 복잡하고 어려운 문제 앞에서도 전혀 주저하지 않아요! 새로운 해결책을 적극적으로 찾아내고, 지식 습득에도 열정적이죠. **당신에게 어려운 일이란 없어요!** 오히려 난이도 높은 업무를 통해 더욱 성장하는 것을 즐기는군요.</li>
                        <li><strong>시간:</strong> 마감 기한은 항상 당신의 친구! 주어진 시간보다 빠르고 정확하게 업무를 완료하며, 효율적인 시간 관리로 생산성을 최고치로 끌어올려요. **시간까지 완벽하게 지배하는 능력자!** 예상치 못한 상황에서도 유연하게 대처하는 능력이 탁월합니다.</li>
                    </ul>
                    <p><strong>💡 전문가의 조언:</strong> 이제 당신의 재능을 세상에 널리 알릴 시간! 🚀 지금의 뛰어난 역량을 바탕으로 팀이나 조직의 **리더**가 되어 다른 사람들에게 영감을 주고, 멘토로서 빛나는 역할을 해보시는 건 어떨까요? 끊임없는 자기 계발과 새로운 도전을 통해 최고의 전문가로서 입지를 더욱 굳건히 다지세요! 당신의 미래가 더욱 기대됩니다! 💖</p>
                `;
            } else if (totalScore >= 30 && totalScore < 45) { // 30점 이상 44점 이하
                summaryText = `
                    멋져요! 👍 당신은 이미 꽤 괜찮은 '일잘러'의 길을 걷고 있어요! ✨ 조금만 더 다듬으면, 업무의 신이 될 잠재력이 충분하답니다!
                `;
                detailHtml = `
                    <h3>✨ 세부 진단: 성장하는 업무 전문가! ✨</h3>
                    <p>당신은 이미 훌륭한 업무 습관을 가지고 있어요! 다음과 같은 특징들이 당신의 강점입니다:</p>
                    <ul>
                        <li><strong>업무의 양 & 완성도:</strong> 대부분의 업무는 무리 없이 잘 처리하지만, 가끔 엄청난 양의 업무가 주어질 때는 효율성을 유지하기 위한 노력이 조금 더 필요할 수 있어요. 결과물도 만족스럽지만, 때때로 세부적인 검토나 품질 향상에 더 신경 쓸 필요가 있답니다. **양과 질의 균형을 조금 더 맞춰봐요!** 특히, 고객이나 동료의 기대치를 충족시키는 데는 능숙하지만, 스스로 완벽을 추구하는 노력이 더해지면 더욱 빛날 거예요.</li>
                        <li><strong>난이도:</strong> 일반적인 업무는 능숙하게 처리하지만, 아주 복잡하거나 새로운 문제에 부딪혔을 때는 추가적인 학습이나 동료의 도움이 필요할 수 있어요. **새로운 도전을 두려워 말고 한 걸음 더 나아가 보세요!** 복잡한 문제 해결을 위한 다양한 접근 방식을 탐색하는 것이 도움이 될 거예요.</li>
                        <li><strong>시간:</strong> 마감 기한을 잘 지키는 편이지만, 예상치 못한 상황이 발생했을 때 시간을 유연하게 조절하는 능력을 조금 더 키워나가면 좋아요. **시간 관리 꿀팁을 찾아보는 것도 도움이 될 거예요!** 주어진 시간을 100% 활용하는 것보다, 10~20% 정도는 예상치 못한 상황에 대비하는 여유를 두는 것도 좋은 전략이랍니다.</li>
                    </ul>
                    <p><strong>💡 전문가의 조언:</strong> 지금도 잘하고 있지만, 조금 더 엣지를 더해볼까요? 💡 영역별 점수를 확인해서 상대적으로 아쉬웠던 부분을 **집중적으로 보완**해보는 건 어떨까요? 예를 들어, 특정 분야의 전문성을 더 키우거나, 스마트한 시간 관리 기술을 배워보는 거죠. 꾸준히 노력한다면 분명 놀라운 성장을 이룰 수 있을 거예요! 당신의 잠재력을 믿어요! 🌱</p>
                `;
            } else if (totalScore >= 15 && totalScore < 30) { // 15점 이상 29점 이하
                summaryText = `
                    괜찮아요! 😊 당신은 지금 '일잘러'로 변신 중인 귀여운 새싹이에요! 🌱 아직은 성장통을 겪고 있지만, 포텐셜이 가득하답니다!
                `;
                detailHtml = `
                    <h3>🚀 세부 진단: 잠재력 충전 중! 🚀</h3>
                    <p>지금은 잠시 숨을 고르며 재정비할 시간이에요! 다음과 같은 부분들을 함께 개선해나가요:</p>
                    <ul>
                        <li><strong>업무의 양 & 완성도:</strong> 업무량이 많아지면 효율성이 급격히 떨어지거나, 주어진 기한 내에 업무를 마치기 어려울 수 있어요. 결과물의 품질이 들쭉날쭉하거나, 스스로 오류를 찾아 고치는 데 어려움을 느낄 때가 있을 거예요. **작은 업무부터 꼼꼼하게 시작해봐요!** 업무의 양을 늘리기 전에, 하나의 업무를 끝까지 책임지고 완성도를 높이는 연습이 중요합니다.</li>
                        <li><strong>난이도:</strong> 새로운 업무나 복잡한 문제에 도전하는 것이 부담스럽고, 때로는 쉽게 포기하고 싶을 수도 있어요. 하지만 모든 일은 처음이 어렵답니다! **작은 성공 경험을 쌓아봐요!** 복잡한 문제는 작은 단위로 쪼개어 해결하는 연습을 해보세요.</li>
                        <li><strong>시간:</strong> 마감 기한을 자주 놓치거나, 체계적인 계획 없이 일을 진행해서 비효율적인 상황이 생길 수 있답니다. **업무 일지나 스케줄러를 활용해보는 건 어떨까요?** 시간을 효율적으로 관리하는 것은 업무 생산성 극대화에 필수적입니다. 예상치 못한 상황에 유연하게 대처하는 연습도 필요해요.</li>
                    </ul>
                    <p><strong>💡 전문가의 조언:</strong> 아직은 서툴러도 괜찮아요! 한 걸음씩 나아가면 분명 멋진 '일잘러'가 될 거예요! 💖 **아주 작은 목표**부터 시작해서 하나씩 달성하는 경험을 해보세요! 예를 들어, '오늘 할 일 목록 3가지 작성 후 완료하기'처럼요. 스스로 해냈다는 성취감을 느끼면 자신감이 쑥쑥 자랄 거예요. 필요한 경우 전문가의 멘토링이나 유용한 교육 프로그램을 찾아보는 것도 큰 도움이 될 거예요. 꾸준함이 가장 중요합니다! 당신의 도전을 응원합니다! 🌈</p>
                `;
            } else { // 14점 이하 (최저점 12점)
                summaryText = `
                    힘내세요! 🙏 지금은 잠시 '일못러' 모드일지 몰라도, 괜찮아요! 당신 안에는 무한한 성장 가능성이 숨어있으니까요! 🐛 (나비가 될 준비 중!)
                `;
                detailHtml = `
                    <h3>🌱 세부 진단: 새싹이 자라나는 중! 🌱</h3>
                    <p>지금은 업무에 조금 어려움을 느끼고 계신 것 같아요. 하지만 괜찮아요! 누구에게나 처음은 있는 법이니까요. 다음과 같은 부분부터 함께 시작해볼까요?</p>
                    <ul>
                        <li><strong>업무의 양 & 완성도:</strong> 적은 업무량도 버겁게 느껴지거나, 업무에 쉽게 압도당하는 경향이 있을 수 있어요. 결과물의 품질이 낮거나, 중요한 부분을 놓치는 경우가 잦을 수 있습니다. **기본부터 차근차근 다져나가요!** 업무 처리의 양보다는 하나의 업무라도 정확하고 만족스럽게 마무리하는 데 집중하는 것이 중요합니다.</li>
                        <li><strong>난이도:</strong> 간단한 업무도 복잡하게 느껴지거나, 새로운 도전에 대한 두려움이 클 수 있어요. 하지만 모든 일은 배우면서 성장하는 거랍니다! **작은 성공을 목표로 해봐요!** 자신의 역량을 넘어서는 난이도의 업무에 대한 부담감을 줄이고, 긍정적으로 받아들이는 연습이 필요합니다.</li>
                        <li><strong>시간:</strong> 시간 관리가 잘 안 되거나, 마감 기한을 지키기 어려워 업무에 차질이 생길 수 있어요. **시간을 친구처럼 관리하는 연습이 필요해요!** 주어진 기한을 준수하고, 효율적인 시간 관리를 통해 업무 생산성을 높이는 것이 급선무입니다.</li>
                    </ul>
                    <p><strong>💡 전문가의 조언:</strong> 지금부터가 진짜 시작이에요! 작은 변화가 큰 기적을 만들 수 있답니다. 함께 '일잘러'로 거듭나 볼까요? 🌈 가장 **기본적인 업무 원칙**부터 차근차근 다시 정립하는 것이 필요합니다. 마치 건물을 지을 때 튼튼한 기초를 다지는 것처럼요! 업무 일지를 작성하거나, 작은 성공 경험을 계속해서 만들어나가는 것이 중요해요. 주저하지 말고 멘토나 교육 프로그램을 통해 적극적으로 도움을 요청하세요. 당신은 충분히 성장할 수 있는 잠재력을 가지고 있습니다! 포기하지 마세요! 💖</p>
                `;
            }
            diagnosisSummaryDiv.innerHTML = summaryText;
            diagnosisDetailDiv.innerHTML = detailHtml;

            // 결과 섹션 보이기
            document.getElementById('resultSection').style.display = 'block';

            // 결과 섹션으로 스크롤 이동
            document.getElementById('resultSection').scrollIntoView({ behavior: 'smooth' });
        });
    </script>
</body>
</html>
