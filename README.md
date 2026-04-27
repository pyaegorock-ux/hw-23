# hw-23
<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <title>hw23 - 按鈕實作</title>
    <style>
        /* 這裡放 CSS：負責控制外觀 */
        body { 
            font-family: 'Roboto', sans-serif; 
            background-color: #f6f6f6; 
            padding: 50px;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .image-container {
            position: relative;
            background: #fff;
            padding: 10px;
            border: 1px solid #ddd;
        }

        /* 根據設計稿：高度22px, 圓角8px, 顏色#2f2f2f */
        .spec-button {
            height: 22px;
            border-radius: 8px;
            border: 1px solid #2f2f2f;
            background: #fff;
            color: #2f2f2f;
            font-size: 13px;
            cursor: pointer;
            padding: 0 10px;
        }

        .info-panel {
            margin-top: 20px;
            padding: 15px;
            background-color: #e8f3ff;
            border: 1px solid #cfddff;
            color: #707070;
            width: 450px;
        }

        .hidden {
            display: none;
        }
    </style>
</head>
<body>

    <div class="image-container">
        <img src="https://via.placeholder.com/450x240" alt="Sample View">
        <br><br>
        <button id="infoBtn" class="spec-button">查看資訊</button>
    </div>

    <div id="infoPanel" class="info-panel hidden">
        <p><strong>修改日期:</strong> 2017/10/12</p>
        <p><strong>類型:</strong> JPG</p>
        <p><strong>大小:</strong> 466.97KB</p>
        <p><strong>路徑:</strong> /vdesigncenter.qnap.com/tw/DesignCenter/...</p>
    </div>

    <script>
        /* 這裡放 JavaScript：負責控制按鈕動作 */
        const btn = document.getElementById('infoBtn');
        const panel = document.getElementById('infoPanel');

        btn.addEventListener('click', () => {
            panel.classList.toggle('hidden');
        });
    </script>

</body>
</html>
