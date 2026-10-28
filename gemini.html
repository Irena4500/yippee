<!DOCTYPE html>
<html lang="ms">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Permainan Pac-Man Arcade Classic</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Font Awesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Retro Pixel Google Font -->
    <link href="https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap" rel="stylesheet">

    <style>
        * {
            user-select: none;
            -webkit-user-select: none;
            touch-action: manipulation;
        }

        body {
            font-family: 'Press Start 2P', cursive;
            background: linear-gradient(135deg, #030712, #0f172a);
            margin: 0;
            padding: 0;
            overflow: hidden;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        #game-container {
            position: relative;
            box-shadow: 0 0 35px rgba(234, 179, 8, 0.2);
            border-radius: 16px;
            overflow: hidden;
            border: 4px solid #2563eb;
            background-color: #000000;
        }

        canvas {
            display: block;
            background-color: #000000;
        }

        .btn-retro {
            transition: all 0.15s ease;
            box-shadow: 0 5px 0 #ca8a04;
        }

        .btn-retro:active {
            transform: translateY(3px);
            box-shadow: 0 2px 0 #ca8a04;
        }

        .dpad-btn {
            background: rgba(255, 255, 255, 0.08);
            border: 2px solid rgba(234, 179, 8, 0.4);
            backdrop-filter: blur(4px);
            transition: background 0.1s;
        }

        .dpad-btn:active {
            background: rgba(234, 179, 8, 0.4);
        }

        .neon-yellow {
            text-shadow: 0 0 8px rgba(234, 179, 8, 0.8);
        }
        
        .neon-blue {
            text-shadow: 0 0 8px rgba(37, 99, 235, 0.8);
        }
    </style>
</head>
<body class="flex flex-col items-center justify-center min-h-screen p-2 text-white">

    <!-- MAIN GAME CONTAINER -->
    <div id="game-container" class="relative max-w-full">
        
        <!-- CANVAS ELEMENT -->
        <canvas id="pacmanCanvas" width="448" height="496"></canvas>

        <!-- TOP HUD DISPLAY OVERLAY -->
        <div id="hud-bar" class="absolute top-0 left-0 w-full p-3 flex justify-between items-center text-[10px] md:text-xs text-white pointer-events-none z-10 bg-black/60 backdrop-blur-xs border-b border-blue-900/50">
            <div>
                <span class="text-yellow-400">SKOR</span><br>
                <span id="score-display" class="neon-yellow text-sm">0000</span>
            </div>
            <div class="text-center">
                <span class="text-amber-400"><i class="fa-solid fa-trophy"></i> TERTINGGI</span><br>
                <span id="high-score-display" class="neon-yellow text-sm">0000</span>
            </div>
            <div class="text-right">
                <span class="text-red-400">NYAWA</span><br>
                <span id="lives-display" class="text-yellow-300 text-sm">💛💛💛</span>
            </div>
        </div>

        <!-- START SCREEN OVERLAY -->
        <div id="start-screen" class="absolute inset-0 bg-black/90 flex flex-col items-center justify-between p-6 text-center z-20">
            <div class="mt-6">
                <div class="inline-block p-3 bg-yellow-950/50 rounded-full mb-3 border border-yellow-500/30">
                    <i class="fa-solid fa-ghost text-4xl text-yellow-400 animate-bounce"></i>
                </div>
                <h1 class="text-2xl md:text-4xl font-extrabold text-yellow-400 drop-shadow-[0_3px_0_#000] tracking-wider">
                    PAC-<span class="text-blue-500">MAN</span>
                </h1>
                <p class="text-[9px] md:text-[10px] text-yellow-200/70 mt-2">EDISI ARCADE RETRO</p>
            </div>

            <!-- GHOST INTRO DISPLAY -->
            <div class="my-auto w-full max-w-xs space-y-2 text-[10px]">
                <p class="text-amber-300 mb-2">MUSUH HANTU:</p>
                <div class="flex justify-around items-center bg-slate-900/80 p-3 rounded-xl border border-blue-900">
                    <span class="text-red-500 font-bold"><i class="fa-solid fa-ghost"></i> BLINKY</span>
                    <span class="text-pink-400 font-bold"><i class="fa-solid fa-ghost"></i> PINKY</span>
                    <span class="text-cyan-400 font-bold"><i class="fa-solid fa-ghost"></i> INKY</span>
                    <span class="text-orange-400 font-bold"><i class="fa-solid fa-ghost"></i> CLYDE</span>
                </div>
            </div>

            <div class="space-y-3 mb-4 w-full max-w-xs">
                <button onclick="startGame()" class="btn-retro bg-yellow-400 hover:bg-yellow-500 text-black font-extrabold py-3.5 px-6 rounded-xl border-2 border-black text-xs tracking-wide cursor-pointer w-full">
                    MULA MAIN
                </button>
                <p class="text-[8px] text-gray-400 leading-relaxed">
                    Kawalan: W A S D / Panah Kekunci / Sentuh D-Pad
                </p>
            </div>
        </div>

        <!-- GAME OVER / WIN OVERLAY -->
        <div id="game-over-screen" class="hidden absolute inset-0 bg-black/85 flex flex-col items-center justify-center p-6 text-center z-30">
            <h2 id="game-over-title" class="text-2xl md:text-3xl font-black text-red-500 drop-shadow-[0_3px_0_#000] mb-2">TAMAT PERMAINAN!</h2>
            <p id="game-over-reason" class="text-[10px] text-gray-300 mb-5">Hantu telah menangkap Pac-Man.</p>
            
            <div class="bg-slate-900/90 p-4 rounded-xl border border-yellow-500/40 mb-5 w-full max-w-xs text-left space-y-2 text-[10px]">
                <div class="flex justify-between items-center">
                    <span class="text-gray-400">JUMLAH SKOR:</span>
                    <span id="final-score" class="text-yellow-400 font-bold text-sm">0</span>
                </div>
                <hr class="border-slate-800">
                <div class="flex justify-between items-center">
                    <span class="text-gray-400">REKOD TERTINGGI:</span>
                    <span id="final-high-score" class="text-amber-400 font-bold text-sm">0</span>
                </div>
            </div>

            <button onclick="restartGame()" class="btn-retro bg-yellow-400 hover:bg-yellow-500 text-black font-bold py-3 px-6 rounded-xl border-2 border-black text-xs cursor-pointer">
                MAIN SEMULA
            </button>
        </div>

    </div>

    <!-- MOBILE ON-SCREEN D-PAD CONTROLS -->
    <div id="touch-dpad" class="mt-4 flex flex-col items-center gap-1.5 md:hidden z-10">
        <button id="btn-dpad-up" class="dpad-btn w-12 h-12 rounded-xl text-yellow-400 text-lg flex items-center justify-center">
            <i class="fa-solid fa-arrow-up"></i>
        </button>
        <div class="flex gap-4">
            <button id="btn-dpad-left" class="dpad-btn w-12 h-12 rounded-xl text-yellow-400 text-lg flex items-center justify-center">
                <i class="fa-solid fa-arrow-left"></i>
            </button>
            <button id="btn-dpad-down" class="dpad-btn w-12 h-12 rounded-xl text-yellow-400 text-lg flex items-center justify-center">
                <i class="fa-solid fa-arrow-down"></i>
            </button>
            <button id="btn-dpad-right" class="dpad-btn w-12 h-12 rounded-xl text-yellow-400 text-lg flex items-center justify-center">
                <i class="fa-solid fa-arrow-right"></i>
            </button>
        </div>
    </div>

    <!-- FOOTER TIPS -->
    <p class="text-gray-500 text-[9px] mt-3 text-center">Gunakan Papan Kekunci, Sentuhan D-Pad atau Leret Skrin untuk Mengawal Pac-Man</p>

    <!-- GAME ENGINE SCRIPT -->
    <script>
        // Web Audio API Synthetic Sound Generator
        const AudioContext = window.AudioContext || window.webkitAudioContext;
        let audioCtx = null;

        function initAudio() {
            if (!audioCtx) {
                audioCtx = new AudioContext();
            }
        }

        function playWakaSound() {
            if (!audioCtx) return;
            const osc = audioCtx.createOscillator();
            const gain = audioCtx.createGain();
            osc.type = 'triangle';
            osc.frequency.setValueAtTime(280, audioCtx.currentTime);
            osc.frequency.exponentialRampToValueAtTime(480, audioCtx.currentTime + 0.08);
            gain.gain.setValueAtTime(0.12, audioCtx.currentTime);
            gain.gain.exponentialRampToValueAtTime(0.01, audioCtx.currentTime + 0.08);
            osc.connect(gain);
            gain.connect(audioCtx.destination);
            osc.start();
            osc.stop(audioCtx.currentTime + 0.08);
        }

        function playEatGhostSound() {
            if (!audioCtx) return;
            const osc = audioCtx.createOscillator();
            const gain = audioCtx.createGain();
            osc.type = 'sawtooth';
            osc.frequency.setValueAtTime(400, audioCtx.currentTime);
            osc.frequency.exponentialRampToValueAtTime(800, audioCtx.currentTime + 0.2);
            gain.gain.setValueAtTime(0.2, audioCtx.currentTime);
            gain.gain.exponentialRampToValueAtTime(0.01, audioCtx.currentTime + 0.2);
            osc.connect(gain);
            gain.connect(audioCtx.destination);
            osc.start();
            osc.stop(audioCtx.currentTime + 0.2);
        }

        function playPowerPelletSound() {
            if (!audioCtx) return;
            const osc = audioCtx.createOscillator();
            const gain = audioCtx.createGain();
            osc.type = 'sine';
            osc.frequency.setValueAtTime(600, audioCtx.currentTime);
            osc.frequency.exponentialRampToValueAtTime(1200, audioCtx.currentTime + 0.15);
            gain.gain.setValueAtTime(0.15, audioCtx.currentTime);
            gain.gain.exponentialRampToValueAtTime(0.01, audioCtx.currentTime + 0.15);
            osc.connect(gain);
            gain.connect(audioCtx.destination);
            osc.start();
            osc.stop(audioCtx.currentTime + 0.15);
        }

        function playGameOverSound() {
            if (!audioCtx) return;
            const osc = audioCtx.createOscillator();
            const gain = audioCtx.createGain();
            osc.type = 'sawtooth';
            osc.frequency.setValueAtTime(300, audioCtx.currentTime);
            osc.frequency.exponentialRampToValueAtTime(60, audioCtx.currentTime + 0.5);
            gain.gain.setValueAtTime(0.3, audioCtx.currentTime);
            gain.gain.exponentialRampToValueAtTime(0.01, audioCtx.currentTime + 0.5);
            osc.connect(gain);
            gain.connect(audioCtx.destination);
            osc.start();
            osc.stop(audioCtx.currentTime + 0.5);
        }

        // Canvas Setup
        const canvas = document.getElementById('pacmanCanvas');
        const ctx = canvas.getContext('2d');

        const TILE_SIZE = 16;
        const GRID_WIDTH = 28;
        const GRID_HEIGHT = 31;

        // UI References
        const startScreen = document.getElementById('start-screen');
        const gameOverScreen = document.getElementById('game-over-screen');
        const scoreDisplay = document.getElementById('score-display');
        const highScoreDisplay = document.getElementById('high-score-display');
        const livesDisplay = document.getElementById('lives-display');
        const finalScoreEl = document.getElementById('final-score');
        const finalHighScoreEl = document.getElementById('final-high-score');
        const gameOverTitle = document.getElementById('game-over-title');
        const gameOverReason = document.getElementById('game-over-reason');

        // Game State Variables
        let score = 0;
        let highScore = parseInt(localStorage.getItem('pacman_high_score') || '0');
        let lives = 3;
        let gameRunning = false;
        let frightenedTimer = 0;
        let frameCount = 0;
        let pelletsLeft = 0;

        highScoreDisplay.innerText = String(highScore).padStart(4, '0');

        // Map Legend: 1 = Wall, 2 = Pellet, 3 = Power Pellet, 0 = Empty, 4 = Ghost House
        const MAP_TEMPLATE = [
            [1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1],
            [1,2,2,2,2,2,2,2,2,2,2,2,2,1,1,2,2,2,2,2,2,2,2,2,2,2,2,1],
            [1,2,1,1,1,1,2,1,1,1,1,1,2,1,1,2,1,1,1,1,1,2,1,1,1,1,2,1],
            [1,3,1,1,1,1,2,1,1,1,1,1,2,1,1,2,1,1,1,1,1,2,1,1,1,1,3,1],
            [1,2,1,1,1,1,2,1,1,1,1,1,2,1,1,2,1,1,1,1,1,2,1,1,1,1,2,1],
            [1,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,1],
            [1,2,1,1,1,1,2,1,1,2,1,1,1,1,1,1,1,1,2,1,1,2,1,1,1,1,2,1],
            [1,2,1,1,1,1,2,1,1,2,1,1,1,1,1,1,1,1,2,1,1,2,1,1,1,1,2,1],
            [1,2,2,2,2,2,2,1,1,2,2,2,2,1,1,2,2,2,2,1,1,2,2,2,2,2,2,1],
            [1,1,1,1,1,1,2,1,1,1,1,1,0,1,1,0,1,1,1,1,1,2,1,1,1,1,1,1],
            [0,0,0,0,0,1,2,1,1,1,1,1,0,1,1,0,1,1,1,1,1,2,1,0,0,0,0,0],
            [0,0,0,0,0,1,2,1,1,0,0,0,0,0,0,0,0,0,0,1,1,2,1,0,0,0,0,0],
            [0,0,0,0,0,1,2,1,1,0,1,1,1,4,4,1,1,1,0,1,1,2,1,0,0,0,0,0],
            [1,1,1,1,1,1,2,1,1,0,1,4,4,4,4,4,4,1,0,1,1,2,1,1,1,1,1,1],
            [0,0,0,0,0,0,2,0,0,0,1,4,4,4,4,4,4,1,0,0,0,2,0,0,0,0,0,0],
            [1,1,1,1,1,1,2,1,1,0,1,4,4,4,4,4,4,1,0,1,1,2,1,1,1,1,1,1],
            [0,0,0,0,0,1,2,1,1,0,1,1,1,1,1,1,1,1,0,1,1,2,1,0,0,0,0,0],
            [0,0,0,0,0,1,2,1,1,0,0,0,0,0,0,0,0,0,0,1,1,2,1,0,0,0,0,0],
            [0,0,0,0,0,1,2,1,1,0,1,1,1,1,1,1,1,1,0,1,1,2,1,0,0,0,0,0],
            [1,1,1,1,1,1,2,1,1,0,1,1,1,1,1,1,1,1,0,1,1,2,1,1,1,1,1,1],
            [1,2,2,2,2,2,2,2,2,2,2,2,2,1,1,2,2,2,2,2,2,2,2,2,2,2,2,1],
            [1,2,1,1,1,1,2,1,1,1,1,1,2,1,1,2,1,1,1,1,1,2,1,1,1,1,2,1],
            [1,2,1,1,1,1,2,1,1,1,1,1,2,1,1,2,1,1,1,1,1,2,1,1,1,1,2,1],
            [1,3,2,2,1,1,2,2,2,2,2,2,2,0,0,2,2,2,2,2,2,2,1,1,2,2,3,1],
            [1,1,1,2,1,1,2,1,1,2,1,1,1,1,1,1,1,1,2,1,1,2,1,1,2,1,1,1],
            [1,1,1,2,1,1,2,1,1,2,1,1,1,1,1,1,1,1,2,1,1,2,1,1,2,1,1,1],
            [1,2,2,2,2,2,2,1,1,2,2,2,2,1,1,2,2,2,2,1,1,2,2,2,2,2,2,1],
            [1,2,1,1,1,1,1,1,1,1,1,1,2,1,1,2,1,1,1,1,1,1,1,1,1,1,2,1],
            [1,2,1,1,1,1,1,1,1,1,1,1,2,1,1,2,1,1,1,1,1,1,1,1,1,1,2,1],
            [1,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,2,1],
            [1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1]
        ];

        let map = [];

        // Pac-Man Entity
        const pacman = {
            x: 13.5 * TILE_SIZE,
            y: 23 * TILE_SIZE,
            speed: 2,
            dirX: 0,
            dirY: 0,
            nextDirX: 0,
            nextDirY: 0,
            mouthAngle: 0.2,
            mouthSpeed: 0.02,

            reset() {
                this.x = 13.5 * TILE_SIZE;
                this.y = 23 * TILE_SIZE;
                this.dirX = 0;
                this.dirY = 0;
                this.nextDirX = 0;
                this.nextDirY = 0;
            },

            draw() {
                ctx.fillStyle = '#facc15'; // Yellow
                ctx.beginPath();

                let angle = 0;
                if (this.dirX === 1) angle = 0;
                else if (this.dirX === -1) angle = Math.PI;
                else if (this.dirY === 1) angle = Math.PI / 2;
                else if (this.dirY === -1) angle = (Math.PI * 3) / 2;

                const openMouth = Math.abs(Math.sin(frameCount * 0.2)) * 0.25;

                ctx.arc(
                    this.x + TILE_SIZE / 2,
                    this.y + TILE_SIZE / 2,
                    TILE_SIZE / 2 - 1,
                    angle + openMouth,
                    angle + Math.PI * 2 - openMouth
                );
                ctx.lineTo(this.x + TILE_SIZE / 2, this.y + TILE_SIZE / 2);
                ctx.fill();
            },

            update() {
                // Check if can apply next direction at intersection
                if (canMove(this.x + this.nextDirX * this.speed, this.y + this.nextDirY * this.speed)) {
                    this.dirX = this.nextDirX;
                    this.dirY = this.nextDirY;
                }

                if (canMove(this.x + this.dirX * this.speed, this.y + this.dirY * this.speed)) {
                    this.x += this.dirX * this.speed;
                    this.y += this.dirY * this.speed;
                }

                // Screen Wrap (Tunnel)
                if (this.x < -TILE_SIZE / 2) this.x = (GRID_WIDTH - 1) * TILE_SIZE;
                if (this.x > (GRID_WIDTH - 0.5) * TILE_SIZE) this.x = 0;

                // Collect Pellets
                const gridX = Math.floor((this.x + TILE_SIZE / 2) / TILE_SIZE);
                const gridY = Math.floor((this.y + TILE_SIZE / 2) / TILE_SIZE);

                if (gridX >= 0 && gridX < GRID_WIDTH && gridY >= 0 && gridY < GRID_HEIGHT) {
                    if (map[gridY][gridX] === 2) {
                        map[gridY][gridX] = 0;
                        addScore(10);
                        pelletsLeft--;
                        playWakaSound();
                    } else if (map[gridY][gridX] === 3) {
                        map[gridY][gridX] = 0;
                        addScore(50);
                        pelletsLeft--;
                        frightenedTimer = 350; // Enable frightened ghosts mode
                        playPowerPelletSound();
                    }

                    if (pelletsLeft === 0) {
                        gameWin();
                    }
                }
            }
        };

        // Ghost Constructor
        class Ghost {
            constructor(color, startTileX, startTileY) {
                this.color = color;
                this.startTileX = startTileX;
                this.startTileY = startTileY;
                this.x = startTileX * TILE_SIZE;
                this.y = startTileY * TILE_SIZE;
                this.speed = 1.6;
                this.dirX = 0;
                this.dirY = -1;
                this.eaten = false;
            }

            reset() {
                this.x = this.startTileX * TILE_SIZE;
                this.y = this.startTileY * TILE_SIZE;
                this.dirX = 0;
                this.dirY = -1;
                this.eaten = false;
            }

            draw() {
                const cx = this.x + TILE_SIZE / 2;
                const cy = this.y + TILE_SIZE / 2;
                const radius = TILE_SIZE / 2 - 1;

                ctx.save();
                ctx.translate(this.x, this.y);

                if (frightenedTimer > 0 && !this.eaten) {
                    // Frightened Blue Ghost Effect
                    ctx.fillStyle = frightenedTimer < 100 && Math.floor(frameCount / 10) % 2 === 0 ? '#ffffff' : '#2563eb';
                } else {
                    ctx.fillStyle = this.color;
                }

                // Head
                ctx.beginPath();
                ctx.arc(TILE_SIZE / 2, TILE_SIZE / 2, radius, Math.PI, 0, false);
                ctx.lineTo(TILE_SIZE, TILE_SIZE);
                
                // Wavy Skirt
                ctx.lineTo((TILE_SIZE * 3) / 4, TILE_SIZE - 3);
                ctx.lineTo(TILE_SIZE / 2, TILE_SIZE);
                ctx.lineTo(TILE_SIZE / 4, TILE_SIZE - 3);
                ctx.lineTo(0, TILE_SIZE);
                ctx.closePath();
                ctx.fill();

                // Eyes
                ctx.fillStyle = '#ffffff';
                ctx.beginPath();
                ctx.arc(5, 6, 3, 0, Math.PI * 2);
                ctx.arc(11, 6, 3, 0, Math.PI * 2);
                ctx.fill();

                // Pupils
                ctx.fillStyle = '#000000';
                ctx.beginPath();
                ctx.arc(5 + this.dirX, 6 + this.dirY, 1.5, 0, Math.PI * 2);
                ctx.arc(11 + this.dirX, 6 + this.dirY, 1.5, 0, Math.PI * 2);
                ctx.fill();

                ctx.restore();
            }

            update() {
                // Move Ghost
                const currentSpeed = frightenedTimer > 0 ? this.speed * 0.7 : this.speed;

                if (canMoveGhost(this.x + this.dirX * currentSpeed, this.y + this.dirY * currentSpeed)) {
                    this.x += this.dirX * currentSpeed;
                    this.y += this.dirY * currentSpeed;
                } else {
                    // Choose new random valid direction at wall/intersection
                    const possibleDirs = [
                        { x: 1, y: 0 },
                        { x: -1, y: 0 },
                        { x: 0, y: 1 },
                        { x: 0, y: -1 }
                    ].filter(d => (d.x !== -this.dirX || d.y !== -this.dirY) && canMoveGhost(this.x + d.x * currentSpeed, this.y + d.y * currentSpeed));

                    if (possibleDirs.length > 0) {
                        const chosen = possibleDirs[Math.floor(Math.random() * possibleDirs.length)];
                        this.dirX = chosen.x;
                        this.dirY = chosen.y;
                    } else {
                        this.dirX = -this.dirX;
                        this.dirY = -this.dirY;
                    }
                }

                // Screen Wrap
                if (this.x < -TILE_SIZE / 2) this.x = (GRID_WIDTH - 1) * TILE_SIZE;
                if (this.x > (GRID_WIDTH - 0.5) * TILE_SIZE) this.x = 0;
            }
        }

        const ghosts = [
            new Ghost('#ef4444', 13, 11), // Blinky (Red)
            new Ghost('#f472b6', 14, 11), // Pinky (Pink)
            new Ghost('#22d3ee', 12, 14), // Inky (Cyan)
            new Ghost('#fb923c', 15, 14)  // Clyde (Orange)
        ];

        function canMove(nextX, nextY) {
            const margin = 2;
            const corners = [
                { x: nextX + margin, y: nextY + margin },
                { x: nextX + TILE_SIZE - margin, y: nextY + margin },
                { x: nextX + margin, y: nextY + TILE_SIZE - margin },
                { x: nextX + TILE_SIZE - margin, y: nextY + TILE_SIZE - margin }
            ];

            return corners.every(c => {
                const gx = Math.floor(c.x / TILE_SIZE);
                const gy = Math.floor(c.y / TILE_SIZE);
                if (gx < 0 || gx >= GRID_WIDTH || gy < 0 || gy >= GRID_HEIGHT) return true; // Allows Tunneling
                return map[gy][gx] !== 1 && map[gy][gx] !== 4; // Wall or Ghost House Door
            });
        }

        function canMoveGhost(nextX, nextY) {
            const margin = 1;
            const corners = [
                { x: nextX + margin, y: nextY + margin },
                { x: nextX + TILE_SIZE - margin, y: nextY + margin },
                { x: nextX + margin, y: nextY + TILE_SIZE - margin },
                { x: nextX + TILE_SIZE - margin, y: nextY + TILE_SIZE - margin }
            ];

            return corners.every(c => {
                const gx = Math.floor(c.x / TILE_SIZE);
                const gy = Math.floor(c.y / TILE_SIZE);
                if (gx < 0 || gx >= GRID_WIDTH || gy < 0 || gy >= GRID_HEIGHT) return true;
                return map[gy][gx] !== 1; // Ghosts can traverse Ghost House (4)
            });
        }

        function drawMap() {
            for (let y = 0; y < GRID_HEIGHT; y++) {
                for (let x = 0; x < GRID_WIDTH; x++) {
                    const tile = map[y][x];
                    const px = x * TILE_SIZE;
                    const py = y * TILE_SIZE;

                    if (tile === 1) {
                        // Blue Arcade Walls
                        ctx.fillStyle = '#1d4ed8';
                        ctx.fillRect(px, py, TILE_SIZE, TILE_SIZE);
                        ctx.strokeStyle = '#3b82f6';
                        ctx.lineWidth = 1;
                        ctx.strokeRect(px + 2, py + 2, TILE_SIZE - 4, TILE_SIZE - 4);
                    } else if (tile === 2) {
                        // Yellow Food Pellet
                        ctx.fillStyle = '#fef08a';
                        ctx.beginPath();
                        ctx.arc(px + TILE_SIZE / 2, py + TILE_SIZE / 2, 2.5, 0, Math.PI * 2);
                        ctx.fill();
                    } else if (tile === 3) {
                        // Flashing Power Pellet
                        if (Math.floor(frameCount / 15) % 2 === 0) {
                            ctx.fillStyle = '#facc15';
                            ctx.beginPath();
                            ctx.arc(px + TILE_SIZE / 2, py + TILE_SIZE / 2, 6, 0, Math.PI * 2);
                            ctx.fill();
                        }
                    } else if (tile === 4) {
                        // Ghost House Hatch Line
                        ctx.fillStyle = '#f472b6';
                        ctx.fillRect(px, py + TILE_SIZE / 2 - 1, TILE_SIZE, 2);
                    }
                }
            }
        }

        function checkGhostCollisions() {
            ghosts.forEach(ghost => {
                const dist = Math.hypot(pacman.x - ghost.x, pacman.y - ghost.y);

                if (dist < TILE_SIZE - 2) {
                    if (frightenedTimer > 0) {
                        // Pac-Man eats Ghost
                        playEatGhostSound();
                        addScore(200);
                        ghost.reset();
                    } else {
                        // Ghost catches Pac-Man
                        handlePacmanDeath();
                    }
                }
            });
        }

        function handlePacmanDeath() {
            lives--;
            updateLivesDisplay();
            playGameOverSound();

            if (lives <= 0) {
                gameOver(false, 'Hantu telah menangkap Pac-Man.');
            } else {
                pacman.reset();
                ghosts.forEach(g => g.reset());
            }
        }

        function addScore(pts) {
            score += pts;
            scoreDisplay.innerText = String(score).padStart(4, '0');

            if (score > highScore) {
                highScore = score;
                highScoreDisplay.innerText = String(highScore).padStart(4, '0');
                localStorage.setItem('pacman_high_score', highScore);
            }
        }

        function updateLivesDisplay() {
            livesDisplay.innerText = '💛'.repeat(Math.max(0, lives));
        }

        function resetLevel() {
            map = MAP_TEMPLATE.map(row => [...row]);
            pelletsLeft = 0;

            for (let y = 0; y < GRID_HEIGHT; y++) {
                for (let x = 0; x < GRID_WIDTH; x++) {
                    if (map[y][x] === 2 || map[y][x] === 3) {
                        pelletsLeft++;
                    }
                }
            }

            pacman.reset();
            ghosts.forEach(g => g.reset());
        }

        function gameLoop() {
            if (!gameRunning) return;

            frameCount++;
            if (frightenedTimer > 0) frightenedTimer--;

            // Update Logic
            pacman.update();
            ghosts.forEach(g => g.update());
            checkGhostCollisions();

            // Render Logic
            ctx.fillStyle = '#000000';
            ctx.fillRect(0, 0, canvas.width, canvas.height);

            drawMap();
            pacman.draw();
            ghosts.forEach(g => g.draw());

            requestAnimationFrame(gameLoop);
        }

        function changeDirection(dx, dy) {
            pacman.nextDirX = dx;
            pacman.nextDirY = dy;
        }

        // Keyboard Event Handlers
        window.addEventListener('keydown', e => {
            if (['ArrowUp', 'KeyW'].includes(e.code)) {
                e.preventDefault(); changeDirection(0, -1);
            } else if (['ArrowDown', 'KeyS'].includes(e.code)) {
                e.preventDefault(); changeDirection(0, 1);
            } else if (['ArrowLeft', 'KeyA'].includes(e.code)) {
                e.preventDefault(); changeDirection(-1, 0);
            } else if (['ArrowRight', 'KeyD'].includes(e.code)) {
                e.preventDefault(); changeDirection(1, 0);
            }
        });

        // Mobile D-Pad Touch Handlers
        const setupDPad = (id, dx, dy) => {
            const btn = document.getElementById(id);
            btn.addEventListener('touchstart', (e) => {
                e.preventDefault();
                initAudio();
                changeDirection(dx, dy);
            });
            btn.addEventListener('mousedown', (e) => {
                e.preventDefault();
                initAudio();
                changeDirection(dx, dy);
            });
        };

        setupDPad('btn-dpad-up', 0, -1);
        setupDPad('btn-dpad-down', 0, 1);
        setupDPad('btn-dpad-left', -1, 0);
        setupDPad('btn-dpad-right', 1, 0);

        // Touch Swipe Gesture Handlers
        let touchStartX = 0;
        let touchStartY = 0;

        canvas.addEventListener('touchstart', e => {
            touchStartX = e.touches[0].clientX;
            touchStartY = e.touches[0].clientY;
            initAudio();
        }, { passive: true });

        canvas.addEventListener('touchend', e => {
            if (!touchStartX || !touchStartY) return;

            let diffX = e.changedTouches[0].clientX - touchStartX;
            let diffY = e.changedTouches[0].clientY - touchStartY;

            if (Math.abs(diffX) > Math.abs(diffY)) {
                if (Math.abs(diffX) > 20) changeDirection(diffX > 0 ? 1 : -1, 0);
            } else {
                if (Math.abs(diffY) > 20) changeDirection(0, diffY > 0 ? 1 : -1);
            }

            touchStartX = 0;
            touchStartY = 0;
        }, { passive: true });

        function startGame() {
            initAudio();
            startScreen.classList.add('hidden');
            gameOverScreen.classList.add('hidden');

            score = 0;
            lives = 3;
            frightenedTimer = 0;
            scoreDisplay.innerText = '0000';
            updateLivesDisplay();

            resetLevel();
            gameRunning = true;
            gameLoop();
        }

        function gameOver(win = false, reason = '') {
            gameRunning = false;

            gameOverTitle.innerText = win ? 'TAHNIAH! MENANG!' : 'TAMAT PERMAINAN!';
            gameOverTitle.className = win ? 'text-2xl md:text-3xl font-black text-yellow-400 drop-shadow-[0_3px_0_#000] mb-2' : 'text-2xl md:text-3xl font-black text-red-500 drop-shadow-[0_3px_0_#000] mb-2';
            gameOverReason.innerText = reason;

            finalScoreEl.innerText = score;
            finalHighScoreEl.innerText = highScore;

            setTimeout(() => {
                gameOverScreen.classList.remove('hidden');
            }, 400);
        }

        function gameWin() {
            gameOver(true, 'Anda berjaya membersihkan semua pelet makanan!');
        }

        function restartGame() {
            startGame();
        }

        window.onload = () => {
            map = MAP_TEMPLATE.map(row => [...row]);
            drawMap();
        };
    </script>
</body>
</html>
