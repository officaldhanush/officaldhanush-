## 🌐 Socials:
[![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?logo=linkedin&logoColor=white)](https://linkedin.com/in/Gummala Naga Dhanush ) [![email](https://img.shields.io/badge/Email-D14836?logo=gmail&logoColor=white)](mailto:officaldhanush90@gmail.com)
<!-- Snake Game Repo View -->

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Retro Snake Game</title>
    <style>
        body {
            background-color: #1a1a1a;
            color: #ffffff;
            font-family: 'Courier New', Courier, monospace;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            margin: 0;
        }
        canvas {
            border: 4px solid #ffffff;
            background-color: #000000;
            box-shadow: 0 0 20px rgba(255, 255, 255, 0.2);
        }
        #score {
            font-size: 24px;
            margin-bottom: 10px;
        }
    </style>
</head>
<body>
    <div id="score">Score: 0</div>
    <canvas id="gameCanvas" width="400" height="400"></canvas>

    <script>
        const canvas = document.getElementById("gameCanvas");
        const ctx = canvas.getContext("2d");

        const gridSize = 20;
        const tileCount = canvas.width / gridSize;

        let snake = [{ x: 10, y: 10 }];
        let food = { x: 5, y: 5 };
        let dx = 0;
        let dy = 0;
        let score = 0;
        let gameInterval;

        function gameLoop() {
            moveSnake();
            if (isGameOver()) {
                alert("Game Over! Final Score: " + score);
                resetGame();
                return;
            }
            clearCanvas();
            drawFood();
            drawSnake();
        }

        function clearCanvas() {
            ctx.fillStyle = "#000000";
            ctx.fillRect(0, 0, canvas.width, canvas.height);
        }

        function drawSnake() {
            ctx.fillStyle = "#00FF00";
            snake.forEach(part => {
                ctx.fillRect(part.x * gridSize, part.y * gridSize, gridSize - 2, gridSize - 2);
            });
        }

        function moveSnake() {
            const head = { x: snake[0].x + dx, y: snake[0].y + dy };
            snake.unshift(head);

            if (head.x === food.x && head.y === food.y) {
                score += 10;
                document.getElementById("score").innerText = "Score: " + score;
                generateFood();
            } else {
                snake.pop();
            }
        }

        function generateFood() {
            food.x = Math.floor(Math.random() * tileCount);
            food.y = Math.floor(Math.random() * tileCount);
            snake.forEach(part => {
                if (part.x === food.x && part.y === food.y) generateFood();
            });
        }

        function drawFood() {
            ctx.fillStyle = "#FF0000";
            ctx.fillRect(food.x * gridSize, food.y * gridSize, gridSize - 2, gridSize - 2);
        }

        function isGameOver() {
            const head = snake[0];
            if (head.x < 0 || head.x >= tileCount || head.y < 0 || head.y >= tileCount) return true;
            for (let i = 1; i < snake.length; i++) {
                if (head.x === snake[i].x && head.y === snake[i].y) return true;
            }
            return false;
        }

        function resetGame() {
            snake = [{ x: 10, y: 10 }];
            dx = 0;
            dy = 0;
            score = 0;
            document.getElementById("score").innerText = "Score: " + score;
            generateFood();
        }

        window.addEventListener("keydown", e => {
            switch (e.key) {
                case "ArrowLeft": if (dx === 0) { dx = -1; dy = 0; } break;
                case "ArrowUp": if (dy === 0) { dx = 0; dy = -1; } break;
                case "ArrowRight": if (dx === 0) { dx = 1; dy = 0; } break;
                case "ArrowDown": if (dy === 0) { dx = 0; dy = 1; } break;
            }
        });

        generateFood();
        gameInterval = setInterval(gameLoop, 100);
    </script>
</body>
</html>

## 🏆 GitHub Trophies
![](https://github-profile-trophy.vercel.app/?username=officaldhanush&theme=radical&no-frame=false&no-bg=true&margin-w=4)

# 💻 Tech Stack:
![C](https://img.shields.io/badge/c-%2300599C.svg?style=for-the-badge&logo=c&logoColor=white) ![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
# 📊 GitHub Stats:
![](https://github-readme-stats.shion.dev/api?username=officaldhanush&theme=dark&hide_border=false&include_all_commits=true&count_private=false)<br/>
![](https://streak-stats.demolab.com/?user=officaldhanush&theme=dark&hide_border=false)<br/>
![](https://github-readme-stats.shion.dev/api/top-langs/?username=officaldhanush&theme=dark&hide_border=false&include_all_commits=true&count_private=false&layout=compact)



### ✍️ Random Dev Quote
![](https://quotes-github-readme.vercel.app/api?type=horizontal&theme=radical)

### 🔝 Top Contributed Repo
![](https://github-contributor-stats.vercel.app/api?username=officaldhanush&limit=5&theme=dark&combine_all_yearly_contributions=true)

---
[![](https://komarev.com/ghpvc/?username=officaldhanush&icon=0&color=0)](https://visitcount.itsvg.in)

<!-- Proudly created with GPRM ( https://gprm.itsvg.in ) -->