
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Welcome Site</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            background: linear-gradient(135deg, #1a1a2e, #16213e);
            font-family: 'Arial', sans-serif;
            color: #ffffff;
            overflow: hidden;
        }

        .welcome {
            font-size: 3rem;
            font-weight: bold;
            text-transform: uppercase;
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4, #45b7d1);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            animation: textGlow 2s ease-in-out infinite;
            text-shadow: 0 0 10px rgba(255, 107, 107, 0.5);
            margin-bottom: 2rem;
        }

        .link-button {
            display: flex;
            align-items: center;
            padding: 15px 30px;
            font-size: 1.2rem;
            font-weight: bold;
            text-decoration: none;
            color: #ffffff;
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4);
            border-radius: 50px;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            box-shadow: 0 5px 15px rgba(255, 107, 107, 0.4);
        }

        .link-button:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(255, 107, 107, 0.6);
        }

        .link-button img {
            width: 24px;
            height: 24px;
            margin-right: 10px;
            filter: brightness(0) invert(1);
        }

        @keyframes textGlow {
            0%, 100% {
                text-shadow: 0 0 10px rgba(255, 107, 107, 0.5), 0 0 20px rgba(78, 205, 196, 0.3);
            }
            50% {
                text-shadow: 0 0 20px rgba(255, 107, 107, 0.7), 0 0 30px rgba(78, 205, 196, 0.5);
            }
        }

        /* Animated background particles */
        .particles {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            background: transparent;
        }

        .particle {
            position: absolute;
            background: rgba(255, 107, 107, 0.3);
            border-radius: 50%;
            animation: float 15s infinite;
        }

        @keyframes float {
            0% {
                transform: translateY(0);
                opacity: 0.5;
            }
            50% {
                opacity: 0.2;
            }
            100% {
                transform: translateY(-100vh);
                opacity: 0;
            }
        }
    </style>
</head>
<body>
    <div class="particles" id="particles"></div>
    <h1 class="welcome">Welcome</h1>
    <a href="https://hindustanlaboratory.github.io/Hindustan-Laboratory-/" class="link-button">
        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRhREKEddhJEmeTdq-JU_MPIr4RkQeZnYZjRcvMAHXY1EGZzUtohR4f8Zo&s=10" alt="Link Icon">
        Visit Site
    </a>

    <script>
        // Generate random particles for background animation
        const particlesContainer = document.getElementById('particles');
        const particleCount = 50;

        for (let i = 0; i < particleCount; i++) {
            const particle = document.createElement('div');
            particle.classList.add('particle');
            particle.style.width = `${Math.random() * 10 + 5}px`;
            particle.style.height = particle.style.width;
            particle.style.left = `${Math.random() * 100}%`;
            particle.style.animationDelay = `${Math.random() * 15}s`;
            particle.style.animationDuration = `${Math.random() * 10 + 10}s`;
            particlesContainer.appendChild(particle);
        }
    </script>
</body>
</html>
