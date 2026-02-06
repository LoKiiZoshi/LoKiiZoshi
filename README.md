<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Welcome - Backend Developer Portfolio</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 20px;
        }

        .container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
            max-width: 1200px;
            width: 100%;
            align-items: center;
            background: white;
            padding: 60px;
            border-radius: 20px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.1);
        }

        .content {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        h1 {
            font-size: 48px;
            color: #1a1a1a;
            font-weight: 700;
            margin-bottom: 10px;
        }

        .description {
            display: flex;
            flex-direction: column;
            gap: 12px;
        }

        .item {
            font-size: 16px;
            line-height: 1.6;
            color: #333;
            opacity: 0;
            transform: translateX(-20px);
            animation: slideInLeft 0.6s ease-out forwards;
            transition: all 0.3s ease;
        }

        .item:nth-child(1) { animation-delay: 0.1s; }
        .item:nth-child(2) { animation-delay: 0.2s; }
        .item:nth-child(3) { animation-delay: 0.3s; }
        .item:nth-child(4) { animation-delay: 0.4s; }
        .item:nth-child(5) { animation-delay: 0.5s; }
        .item:nth-child(6) { animation-delay: 0.6s; }
        .item:nth-child(7) { animation-delay: 0.7s; }

        .item:hover {
            color: #ff69b4;
            transform: translateX(10px);
        }

        strong {
            color: #1a1a1a;
            font-weight: 600;
        }

        .item:hover strong {
            color: #ff1493;
        }

        @keyframes slideInLeft {
            from {
                opacity: 0;
                transform: translateX(-20px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }

        .circle-container {
            display: flex;
            align-items: center;
            justify-content: center;
            height: 100%;
            position: relative;
            min-height: 400px;
        }

        .circle-wrapper {
            position: relative;
            width: 300px;
            height: 300px;
            cursor: none;
        }

        .circle {
            position: absolute;
            border-radius: 50%;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            transition: all 0.1s ease-out;
        }

        .circle-1 {
            width: 320px;
            height: 320px;
            border: 4px solid;
            border-image: linear-gradient(45deg, #ff1493, #ff69b4) 1;
            animation: rotate1 20s linear infinite, pulse1 2s ease-in-out infinite;
        }

        .circle-2 {
            width: 280px;
            height: 280px;
            border: 3px solid;
            border-image: linear-gradient(45deg, #9370db, #ba55d3) 1;
            animation: rotate2 25s linear infinite reverse, pulse2 2.5s ease-in-out infinite;
            opacity: 0.7;
        }

        .circle-3 {
            width: 240px;
            height: 240px;
            border: 3px solid;
            border-image: linear-gradient(45deg, #4169e1, #6495ed) 1;
            animation: rotate3 30s linear infinite, pulse3 3s ease-in-out infinite;
            opacity: 0.5;
        }

        .circle-4 {
            width: 200px;
            height: 200px;
            border: 2px solid;
            border-image: linear-gradient(45deg, #ff6347, #ff4500) 1;
            animation: rotate1 22s linear infinite reverse, pulse4 2.2s ease-in-out infinite;
            opacity: 0.6;
        }

        .center-glow {
            position: absolute;
            width: 160px;
            height: 160px;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            border-radius: 50%;
            background: radial-gradient(circle, rgba(255, 105, 180, 0.3), transparent);
            animation: glow 2s ease-in-out infinite;
            pointer-events: none;
        }

        @keyframes rotate1 {
            from { transform: translate(-50%, -50%) rotate(0deg); }
            to { transform: translate(-50%, -50%) rotate(360deg); }
        }

        @keyframes rotate2 {
            from { transform: translate(-50%, -50%) rotate(0deg); }
            to { transform: translate(-50%, -50%) rotate(-360deg); }
        }

        @keyframes rotate3 {
            from { transform: translate(-50%, -50%) rotate(0deg); }
            to { transform: translate(-50%, -50%) rotate(360deg); }
        }

        @keyframes pulse1 {
            0%, 100% {
                box-shadow: 0 0 20px rgba(255, 20, 147, 0.4), 0 0 40px rgba(255, 105, 180, 0.2);
            }
            50% {
                box-shadow: 0 0 40px rgba(255, 20, 147, 0.6), 0 0 80px rgba(255, 105, 180, 0.3);
            }
        }

        @keyframes pulse2 {
            0%, 100% {
                box-shadow: 0 0 15px rgba(147, 112, 219, 0.3), 0 0 30px rgba(186, 85, 211, 0.15);
            }
            50% {
                box-shadow: 0 0 30px rgba(147, 112, 219, 0.5), 0 0 60px rgba(186, 85, 211, 0.25);
            }
        }

        @keyframes pulse3 {
            0%, 100% {
                box-shadow: 0 0 12px rgba(65, 105, 225, 0.25), 0 0 25px rgba(100, 149, 237, 0.12);
            }
            50% {
                box-shadow: 0 0 25px rgba(65, 105, 225, 0.4), 0 0 50px rgba(100, 149, 237, 0.2);
            }
        }

        @keyframes pulse4 {
            0%, 100% {
                box-shadow: 0 0 18px rgba(255, 99, 71, 0.35), 0 0 35px rgba(255, 69, 0, 0.18);
            }
            50% {
                box-shadow: 0 0 35px rgba(255, 99, 71, 0.55), 0 0 70px rgba(255, 69, 0, 0.28);
            }
        }

        @keyframes glow {
            0%, 100% {
                box-shadow: inset 0 0 30px rgba(255, 105, 180, 0.3);
            }
            50% {
                box-shadow: inset 0 0 50px rgba(255, 105, 180, 0.5);
            }
        }

        .circle-wrapper:hover .circle {
            animation-play-state: paused;
        }

        .circle-wrapper:hover .circle-1 {
            width: 340px;
            height: 340px;
            animation: none;
            border: 4px solid;
            border-image: linear-gradient(45deg, #ff1493, #ff69b4) 1;
        }

        .circle-wrapper:hover .circle-2 {
            width: 300px;
            height: 300px;
            animation: none;
            border: 3px solid;
            border-image: linear-gradient(45deg, #9370db, #ba55d3) 1;
        }

        .circle-wrapper:hover .circle-3 {
            width: 260px;
            height: 260px;
            animation: none;
            border: 3px solid;
            border-image: linear-gradient(45deg, #4169e1, #6495ed) 1;
        }

        .circle-wrapper:hover .circle-4 {
            width: 220px;
            height: 220px;
            animation: none;
            border: 2px solid;
            border-image: linear-gradient(45deg, #ff6347, #ff4500) 1;
        }

        .circle-wrapper:hover .center-glow {
            animation: none;
            box-shadow: inset 0 0 60px rgba(255, 105, 180, 0.6), 0 0 50px rgba(255, 105, 180, 0.4);
        }

        @media (max-width: 768px) {
            .container {
                grid-template-columns: 1fr;
                gap: 40px;
                padding: 40px 20px;
            }

            h1 {
                font-size: 36px;
            }

            .item {
                font-size: 14px;
            }

            .circle-wrapper {
                width: 250px;
                height: 250px;
                min-height: 300px;
            }

            .circle-1 {
                width: 280px;
                height: 280px;
            }

            .circle-2 {
                width: 240px;
                height: 240px;
            }

            .circle-3 {
                width: 200px;
                height: 200px;
            }

            .circle-4 {
                width: 160px;
                height: 160px;
            }

            .center-glow {
                width: 130px;
                height: 130px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="content">
            <h1>Welcome</h1>
            <div class="description">
                <div class="item">👋🏻 I'm a <strong>Back End Developer</strong> with expertise in <strong>Python</strong>, <strong>Django</strong>, <strong>Java</strong>, and <strong>Spring Boot</strong>.</div>
                <div class="item">🤖 I'm an <strong>AI enthusiast</strong> passionate about building intelligent and scalable web applications.</div>
                <div class="item">🚀 I'm a <strong>tech explorer</strong> constantly learning new tools and technologies.</div>
                <div class="item">🌐 I'm an <strong>open-source contributor</strong>, collaborating with global communities.</div>
                <div class="item">⚙️ I'm an <strong>innovator</strong>, blending logic and creativity in every project.</div>
                <div class="item">🎨 I'm both a <strong>frontend artist</strong> and a <strong>backend engineer</strong>.</div>
                <div class="item">🇳🇵 I'm proudly based in <strong>Nepal</strong>.</div>
            </div>
        </div>

        <div class="circle-container">
            <div class="circle-wrapper">
                <div class="circle circle-1"></div>
                <div class="circle circle-2"></div>
                <div class="circle circle-3"></div>
                <div class="circle circle-4"></div>
                <div class="center-glow"></div>
            </div>
        </div>
    </div>
</body>
</html>
