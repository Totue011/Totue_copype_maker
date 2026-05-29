<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<title>카피페 대화 생성기 (배포용)</title>
<script src="https://cdnjs.cloudflare.com/ajax/libs/html2canvas/1.4.1/html2canvas.min.js"></script>
<style>
  /* 전체 레이아웃 설정 */
  body {
    font-family: 'Apple SD Gothic Neo', 'Malgun Gothic', sans-serif;
    background-color: #f0f2f5;
    padding: 20px;
    display: flex;
    gap: 30px;
    flex-wrap: wrap;
    margin: 0;
  }
  .panel {
    background: #ffffff;
    padding: 20px 25px;
    border-radius: 12px;
    box-shadow: 0 4px 12px rgba(0,0,0,0.05);
  }
  .editor-panel {
    flex: 1;
    min-width: 300px;
    max-width: 350px;
    height: fit-content;
  }
  .preview-panel {
    flex: 2;
    min-width: 400px;
  }
  h3 {
    margin-top: 0;
    color: #1a1a1a;
    border-bottom: 2px solid #f0f2f5;
    padding-bottom: 10px;
    font-size: 18px;
    margin-bottom: 15px;
  }
  .section-divider {
    height: 1px;
    background-color: #e5e7eb;
    margin: 20px 0;
  }

  /* 입력 폼 스타일 */
  .form-group {
    margin-bottom: 16px;
  }
  .form-group label {
    display: block;
    font-weight: 800;
    margin-bottom: 6px;
    font-size: 14px;
    color: #333;
  }
  .form-control {
    width: 100%;
    padding: 10px;
    border: 1px solid #d1d5db;
    border-radius: 6px;
    box-sizing: border-box;
    font-size: 15px;
    font-family: inherit;
  }
  input[type="color"].form-control {
    height: 44px;
    padding: 2px 4px;
    cursor: pointer;
  }
  input[type="file"].form-control {
    padding: 8px;
    font-size: 13px;
    background-color: #f8f9fa;
  }
  textarea.form-control {
    height: 90px;
    resize: vertical;
  }

  /* 버튼 그룹 스타일 */
  .button-group {
    display: flex;
    gap: 10px;
    margin-top: 10px;
  }
  button.action-btn {
    flex: 1;
    padding: 12px;
    border: none;
    border-radius: 6px;
    font-weight: 800;
    cursor: pointer;
    font-size: 16px;
    transition: background-color 0.2s;
  }
  .add-btn {
    background-color: #1a1a1a;
    color: #ffffff;
  }
  .add-btn:hover {
    background-color: #333333;
  }
  .capture-btn {
    background-color: #339af0;
    color: #ffffff;
  }
  .capture-btn:hover {
    background-color: #228be6;
  }

  /* 팝 코믹스 디자인 스타일 */
  .pop-comic-container {
    background-color: #ffffff;
    background-image: url("data:image/svg+xml,%3Csvg width='12' height='12' viewBox='0 0 12 12' xmlns='http://www.w3.org/2000/svg'%3E%3Ccircle cx='3' cy='3' r='1.5' fill='%23cccccc'/%3E%3C/svg%3E");
    background-repeat: repeat;
    width: 100%;
    max-width: 480px;
    padding: 35px 25px;
    border: 4px solid #1a1a1a;
    border-radius: 10px;
    position: relative;
    overflow: hidden;
    display: flex;
    flex-direction: column;
    gap: 25px;
    box-shadow: 10px 10px 0px #1a1a1a;
    box-sizing: border-box;
    transition: background-color 0.3s ease;
  }
  
  /* 카피페 제목 표시 스타일 */
  .comic-title-display {
    align-self: center;
    background-color: #FFE066; 
    color: #1a1a1a;
    padding: 10px 24px;
    border-radius: 20px;
    font-size: 18px;
    font-weight: 900;
    margin-bottom: 10px;
    position: relative;
    z-index: 1;
    border: 3px solid #1a1a1a;
    box-shadow: 5px 5px 0px #1a1a1a;
    text-align: center;
    width: fit-content;
    word-break: keep-all;
    transform: rotate(-1deg);
  }

  .pop-comic-row {
    display: flex;
    flex-direction: column;
    position: relative;
    z-index: 1; 
  }
  .pop-comic-row.left { align-self: flex-start; }
  .pop-comic-row.right { align-self: flex-end; align-items: flex-end; }

  .pop-comic-bubble {
    position: relative;
    padding: 16px 22px;
    background-color: #ffffff;
    border: 3px solid #1a1a1a;
    border-radius: 20px;
    font-size: 16px;
    font-weight: 800; 
    color: #1a1a1a;
    max-width: 85%;
    word-break: keep-all;
    line-height: 1.5;
  }

  /* 말풍선 내부 첨부 이미지 스타일 */
  .bubble-image {
    max-width: 100%;
    height: auto;
    border: 2px solid #1a1a1a;
    border-radius: 8px;
    margin-top: 10px;
    display: block;
    box-sizing: border-box;
  }

  .pop-comic-name {
    display: inline-block;
    color: #ffffff;
    font-size: 13px;
    font-weight: 800;
    padding: 3px 10px;
    border-radius: 5px;
    border: 2px solid #1a1a1a;
    margin-bottom: 8px;
  }

  /* 삭제 버튼 스타일 */
  .delete-btn {
    position: absolute;
    top: -12px;
    right: -12px;
    background: #ff4757;
    color: white;
    border: 2px solid #1a1a1a;
    border-radius: 50%;
    width: 26px;
    height: 26px;
    font-size: 13px;
    font-weight: bold;
    cursor: pointer;
    display: none;
    align-items: center;
    justify-content: center;
    padding: 0;
    z-index: 10;
  }
  
  .pop-comic-container:not([data-capturing="true"]) .pop-comic-row:hover .delete-btn {
    display: flex;
  }
  .pop-comic-row.right .delete-btn {
    left: -12px;
    right: auto;
  }

</style>
</head>
<body>

<div class="panel editor-panel">
  <h3>전체 설정</h3>
  <div class="form-group">
    <label for="inputTitle">카피페 제목</label>
    <input type="text" id="inputTitle" class="form-control" placeholder="제목을 입력하세요" value="오늘의 카피페" oninput="updateTitle()">
  </div>
  <div class="form-group">
    <label for="inputBgColor">바탕 색상 (배경)</label>
    <input type="color" id="inputBgColor" class="form-control" value="#ffffff" oninput="updateBgColor()">
  </div>
  
  <div class="section-divider"></div>

  <h3>대화 추가 설정</h3>
  <div class="form-group">
    <label for="inputName">이름</label>
    <input type="text" id="inputName" class="form-control" placeholder="예: A" value="A">
  </div>
  <div class="form-group">
    <label for="inputColor">테마 색상</label>
    <input type="color" id="inputColor" class="form-control" value="#E53935">
  </div>
  <div class="form-group">
    <label for="inputAlign">위치 (화자)</label>
    <select id="inputAlign" class="form-control">
      <option value="left">왼쪽 (상대방)</option>
      <option value="right">오른쪽 (나)</option>
    </select>
  </div>
  <div class="form-group">
    <label for="inputText">대화 내용</label>
    <textarea id="inputText" class="form-control" placeholder="대화 내용을 입력하세요"></textarea>
  </div>
  <div class="form-group">
    <label for="inputFile">이미지 첨부 (선택)</label>
    <input type="file" id="inputFile" class="form-control" accept="image/*">
  </div>
  
  <div class="button-group">
    <button class="action-btn add-btn" onclick="processDialogue()">추가하기</button>
    <button class="action-btn capture-btn" onclick="captureImage()">이미지 저장</button>
  </div>
</div>

<div class="panel preview-panel">
  <h3>미리보기 (생성된 대화에 마우스를 올리면 삭제 버튼이 나타납니다)</h3>
  <div class="pop-comic-container" id="comicContainer">
    <div id="displayTitle" class="comic-title-display">오늘의 카피페</div>
  </div>
</div>

<script>
  // 제목 실시간 업데이트
  function updateTitle() {
    const titleText = document.getElementById('inputTitle').value;
    const titleElement = document.getElementById('displayTitle');
    
    if (titleText.trim() === '') {
      titleElement.style.display = 'none'; 
    } else {
      titleElement.style.display = 'block';
      titleElement.innerText = titleText;
    }
  }

  // 바탕색 실시간 업데이트
  function updateBgColor() {
    const bgColor = document.getElementById('inputBgColor').value;
    document.getElementById('comicContainer').style.backgroundColor = bgColor;
  }

  // 대화 및 이미지 처리 함수
  function processDialogue() {
    const dName = document.getElementById('inputName').value || '이름 없음';
    const dColor = document.getElementById('inputColor').value;
    const dAlign = document.getElementById('inputAlign').value;
    const rawText = document.getElementById('inputText').value;
    const fileInput = document.getElementById('inputFile');
    const file = fileInput.files[0];
    
    if (!rawText.trim() && !file) {
      alert("대화 내용이나 이미지를 입력/첨부해 주십시오.");
      return;
    }

    const dText = rawText.replace(/\n/g, '<br>');

    // 파일이 첨부된 경우 FileReader를 통해 렌더링
    if (file) {
      const reader = new FileReader();
      reader.onload = function(e) {
        const imgHtml = `<img src="${e.target.result}" class="bubble-image" alt="첨부 이미지">`;
        appendBubble(dName, dColor, dAlign, dText, imgHtml);
        fileInput.value = ''; // 파일 입력 필드 초기화
      };
      reader.readAsDataURL(file);
    } else {
      // 파일이 없는 경우 텍스트만 렌더링
      appendBubble(dName, dColor, dAlign, dText, '');
    }
  }

  // DOM에 말풍선을 추가하는 내부 함수
  function appendBubble(name, color, align, text, imgHtml) {
    const container = document.getElementById('comicContainer');
    const row = document.createElement('div');
    row.className = `pop-comic-row ${align}`;

    const shadowX = align === 'left' ? '6px' : '-6px';
    const radiusStyle = align === 'left' ? 'border-bottom-left-radius: 4px;' : 'border-bottom-right-radius: 4px; text-align: right;';
    const rotate = align === 'left' ? '-2deg' : '2deg';
    const margin = align === 'left' ? '' : 'margin-right: 5px;';

    // 텍스트와 이미지를 말풍선 안에 삽입
    row.innerHTML = `
      <button class="delete-btn" onclick="this.parentElement.remove()" title="삭제">X</button>
      <div class="pop-comic-name" style="background-color: ${color}; transform: rotate(${rotate}); ${margin}">${name}</div>
      <div class="pop-comic-bubble" style="${radiusStyle} box-shadow: ${shadowX} 6px 0px ${color};">
        ${text}
        ${imgHtml}
      </div>
    `;
    
    container.appendChild(row);
    
    // 입력창 텍스트 비우기
    document.getElementById('inputText').value = '';
    document.getElementById('inputText').focus();
  }

  // 이미지 캡처 함수
  function captureImage() {
    const container = document.getElementById('comicContainer');
    const currentBgColor = document.getElementById('inputBgColor').value;
    
    container.setAttribute('data-capturing', 'true');

    html2canvas(container, {
      scale: 2, 
      backgroundColor: currentBgColor,
      useCORS: true
    }).then(canvas => {
      container.removeAttribute('data-capturing');

      const link = document.createElement('a');
      link.download = 'copype_capture.png';
      link.href = canvas.toDataURL('image/png');
      link.click();
    }).catch(err => {
      console.error('이미지 저장 중 오류가 발생했습니다:', err);
      container.removeAttribute('data-capturing');
      alert("이미지 캡처에 실패하였습니다.");
    });
  }

  // 페이지 로드 시 초기 예시 데이터 출력 (초기화 함수 분리)
  window.onload = function() {
    appendBubble('A', '#E53935', 'left', 'B, 화내지 말고 잘 들어봐.', '');
    appendBubble('B', '#1E88E5', 'right', '그래, 들어나보자.', '');
  };
</script>
</body>
</html>
