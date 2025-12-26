<!DOCTYPE html>
<html lang="zh">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>心理测试</title>
</head>
<body>
    <!-- 测试容器 -->
    <div id="test-container">
        <h1>心理测试</h1>
        <p class="question">你现在开心吗？</p>
        <div class="options">
            <button onclick="showResult('A')">A. 开心</button>
            <button onclick="showResult('B')">B. 不开心</button>
        </div>
    </div>

    <!-- 结果容器，初始隐藏 -->
    <div id="result-container" style="display: none;">
        <h1>测试结果</h1>
        <p id="result-text"></p>
    </div>
</body>
</html>



<style>
    body {
        font-family: sans-serif;
        text-align: center;
        background-color: #f4f4f4;
        margin-top: 50px;
    }
    #test-container, #result-container {
        width: 90%;
        max-width: 500px;
        margin: auto;
        padding: 20px;
        background-color: #fff;
        border-radius: 8px;
        box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }
    .question {
        font-size: 1.2em;
        margin-bottom: 20px;
    }
    .options button {
        display: block;
        width: 100%;
        padding: 15px;
        margin-bottom: 10px;
        border: none;
        border-radius: 5px;
        background-color: #007BFF;
        color: white;
        font-size: 1em;
        cursor: pointer;
    }
    .options button:hover {
        background-color: #0056b3;
    }
</style>


<script>
    function showResult(choice) {
        // 获取需要操作的元素
        const testContainer = document.getElementById('test-container');
        const resultContainer = document.getElementById('result-container');
        const resultText = document.getElementById('result-text');

        // 根据选项设置不同的结果
        if (choice === 'A') {
            resultText.innerText = "太棒了！继续保持这份好心情，愿你的每一天都充满阳光。";
        } else {
            resultText.innerText = "没关系，生活总有起落。找个朋友聊聊天，或者做些自己喜欢的事，希望你能尽快开心起来。";
        }

        // 隐藏问题，显示结果
        testContainer.style.display = 'none';
        resultContainer.style.display = 'block';
    }
</script>

