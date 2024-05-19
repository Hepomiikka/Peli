<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pääseekö ahtaaja Turja Lehtosten ohi?</title>
    <style>
        canvas {
            display: block;
            margin: 0 auto;
            background-color: #87CEEB;
        }
    </style>
</head>
<body>
    <canvas id="gameCanvas" width="800" height="600"></canvas>
    <script>
        const canvas = document.getElementById('gameCanvas');
        const ctx = canvas.getContext('2d');

        const SCREEN_WIDTH = canvas.width;
        const SCREEN_HEIGHT = canvas.height;
        const PLAYER_SIZE = 50;
        const OBSTACLE_WIDTH = 50;
        const OBSTACLE_HEIGHT = 50;
        const OBSTACLE_SPEED = 5;
        const GOAL_WIDTH = 100;  // Maalin leveys
        const GOAL_HEIGHT = 100;  // Maalin korkeus
        const FONT_SIZE = 36;
        const GAME_DURATION = 60;  // Pelin kesto sekunneissa

        const playerImg = new Image();
        playerImg.src = 'player.png';
        const obstacleImg = new Image();
        obstacleImg.src = 'obstacle.png';
        const goalImg = new Image();
        goalImg.src = 'goal.png';

        class Player {
            constructor() {
                this.width = PLAYER_SIZE;
                this.height = PLAYER_SIZE;
                this.x = 50;
                this.y = SCREEN_HEIGHT / 2 - this.height / 2;
                this.dy = 5;
                this.image = playerImg;
            }

            draw() {
                ctx.drawImage(this.image, this.x, this.y, this.width, this.height);
            }

            update() {
                if (keys['ArrowUp'] && this.y > 0) {
                    this.y -= this.dy;
                }
                if (keys['ArrowDown'] && this.y < SCREEN_HEIGHT - this.height) {
                    this.y += this.dy;
                }
            }
        }

        class Obstacle {
            constructor(x, y) {
                this.width = OBSTACLE_WIDTH;
                this.height = OBSTACLE_HEIGHT;
                this.x = x;
                this.y = y;
                this.dx = OBSTACLE_SPEED;
                this.image = obstacleImg;
            }

            draw() {
                ctx.drawImage(this.image, this.x, this.y, this.width, this.height);
            }

            update() {
                this.x -= this.dx;
                if (this.x + this.width < 0) {
                    this.x = SCREEN_WIDTH;
                    this.y = Math.random() * (SCREEN_HEIGHT - this.height);
                }
            }
        }

        class Goal {
            constructor() {
                this.width = GOAL_WIDTH;
                this.height = GOAL_HEIGHT;
                this.x = SCREEN_WIDTH - this.width - 20;
                this.y = SCREEN_HEIGHT / 2 - this.height / 2;
                this.image = goalImg;
            }

            draw() {
                ctx.drawImage(this.image, this.x, this.y, this.width, this.height);
            }
        }

        let player = new Player();
        let obstacles = [];
        for (let i = 0; i < 5; i++) {
            let x = Math.random() * (SCREEN_WIDTH - OBSTACLE_WIDTH) + SCREEN_WIDTH;
            let y = Math.random() * (SCREEN_HEIGHT - OBSTACLE_HEIGHT);
            obstacles.push(new Obstacle(x, y));
        }
        let goal = new Goal();

        let keys = {};
        let startTime = Date.now();
        let gameEnded = false;

        window.addEventListener('keydown', function (e) {
            keys[e.key] = true;
        });

        window.addEventListener('keyup', function (e) {
            keys[e.key] = false;
        });

        function collisionDetection(player, obstacle) {
            return player.x < obstacle.x + obstacle.width &&
                   player.x + player.width > obstacle.x &&
                   player.y < obstacle.y + obstacle.height &&
                   player.y + player.height > obstacle.y;
        }

        function gameLoop() {
            if (gameEnded) return;

            ctx.clearRect(0, 0, SCREEN_WIDTH, SCREEN_HEIGHT);

            player.update();
            player.draw();

            obstacles.forEach(obstacle => {
                obstacle.update();
                obstacle.draw();

                if (collisionDetection(player, obstacle)) {
                    alert('Game Over');
                    gameEnded = true;
                    return;
                }
            });

            if (collisionDetection(player, goal)) {
                alert('You Win!');
                gameEnded = true;
                return;
            }

            let elapsedTime = (Date.now() - startTime) / 1000;
            if (elapsedTime >= GAME_DURATION) {
                alert('You Win!');
                gameEnded = true;
                return;
            }

            goal.draw();

            ctx.fillStyle = 'black';
            ctx.font = `${FONT_SIZE}px Arial`;
            ctx.fillText('Pääseekö ahtaaja Turja Lehtosten ohi?', 50, 50);

            requestAnimationFrame(gameLoop);
        }

        gameLoop();
    </script>
</body>
</html>
