<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>常用链接</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f9f5e3;
            margin: 0;
            padding: 0;
        }
        header, footer {
            background-color: #333;
            color: #fff;
            text-align: center;
            padding: 1rem;
        }
        main {
            max-width: 800px;
            margin: 0 auto;
            padding: 2rem;
            background-color: #fff;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
            min-height: calc(100vh - 70px);
        }
        button {
            background-color: #ffcc00;
            color: #333;
            border: none;
            padding: 0.5rem 1rem;
            font-size: 1rem;
            cursor: pointer;
            margin-right: 1rem;
        }
        button:hover {
            background-color: #ffdd66;
        }
        input[type="text"] {
            padding: 0.5rem 1rem;
            font-size: 1rem;
            border: 1px solid #ccc;
            border-radius: 4px;
            margin-right: 1rem;
        }
        .error {
            color: red;
        }
        .success {
            color: green;
        }
        .blue-window {
            background-color: #0074D9;
            color: #fff;
            padding: 1rem;
            border-radius: 4px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
            display: none;
        }
    </style>
</head>
<body>
    <header><h1>欢迎来到我的网页</h1></header>
    <main>
        <p>QQ：3542395682</p>
        <p>这里有一些常用链接跳转：</p>
        <button onclick="window.location.href='https://www.dh-studios.cn'">DHCraft官网</button>
        <button onclick="window.location.href='https://bbs.dh-studios.cn'">DHCraft论坛</button>
        <button onclick="window.location.href='https://cloud.yghpy.com'">融珂之悦云
        </button><br><br>
        <input id="passwordInput" type="password" placeholder="请输入密码">
        <button onclick="checkPassword()">确认</button>
        <p id="message" class="success"></p>
        <div class="blue-window" id="blueWindow">222.187.239.32:40251  administrator</div>
    </main>
    <footer>&copy; heyuxuan</footer>
    <script>
        let attempts = 0;
        function checkPassword() {
            const password = document.getElementById("passwordInput").value;
            const message = document.getElementById("message");
            const blueWindow = document.getElementById("blueWindow");
            if (password === "") {
                message.textContent = "请填写密码";
                message.className = "success";
            } else if (password === "823894") {
                message.textContent = "密码正确！欢迎访问下方的文本。";
                message.className = "success";
                blueWindow.style.display = "block";
            } else {
                attempts++;
                if (attempts >= 3) {
                    message.textContent = "密码错误次数过多";
                    message.className = "error";
                } else {
                    message.textContent = "密码错误，请重新输入。";
                    message.className = "error";
                }
            }
        }
    </script>
</body>
</html>
