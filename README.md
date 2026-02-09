<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Message by your loki</title>
    <style>
        * { box-sizing: border-box; }

        body {
            margin: 0;
            display: flex;
            min-height: 100dvh;
            perspective: 1000px;
            font: 1em/1.4 "Poppins", sans-serif;
            overflow: hidden;
            background: linear-gradient(to right, #ff7eb9, #ff65a3, #ff165d);
            background-size: 400% 400%;
            animation: gradientAnimation 10s ease infinite;
        }

        @keyframes gradientAnimation {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        .book {
            position: relative;
            display: flex;
            margin: auto;
            width: 42cqmin;
            pointer-events: none;
            transform-style: preserve-3d;
            transition: translate 1s;
            translate: calc(min(var(--c), 1) * 50%) 0%;
            rotate: 1 0 0 30deg;
            counter-reset: page -1;
        }

        .page {
            --thickness: 4;
            flex: none;
            display: flex;
            width: 100%;
            font-size: 2cqmin;
            pointer-events: all;
            user-select: none;
            transform-style: preserve-3d;
            transform-origin: left center;
            transition: transform 1s, rotate 1s ease-in calc((min(var(--i), var(--c)) - max(var(--i), var(--c))) * 50ms);
            translate: calc(var(--i) * -100%) 0px 0px;
            transform: translateZ(calc((var(--c) - var(--i) - 0.5) * calc(var(--thickness) * 0.23cqmin)));
            rotate: 0 1 0 calc(clamp(0, var(--c) - var(--i), 1) * -180deg);
            box-shadow: 0em 0.5em 1em -0.2em #00000020;
        }

        .front, .back {
            position: relative;
            flex: none;
            width: 100%;
            backface-visibility: hidden;
            overflow: hidden;
            background-color: #fff;
            display: flex;
            flex-direction: column;
            padding: 1.5em;
            border: 1px solid #0002;
            color: hsl(0, 100%, 30%);
        }

        .back { translate: -100% 0; rotate: 0 1 0 180deg; background: linear-gradient(to right, #f7f7f7 80%, #eee 100%); }
        .front { background: linear-gradient(to left, #f7f7f7 80%, #eee 100%); }

        .cover { background: hsl(231, 32%, 29%) url("./cover.jpg") 50% / cover; color: white; }
        
        img { width: 100%; height: 100%; object-fit: cover; }

        h1, h2, h3 { margin-bottom: 5px; color: hsl(0, 100%, 30%); }
        p { margin-top: 5px; line-height: 1.4; color: hsl(0, 100%, 30%); }

        /* Final Valentine Page Styles */
        .final-valentine {
            background: linear-gradient(rgba(0,0,0,0.3), rgba(0,0,0,0.3)), radial-gradient(circle at top, #ff758c, #ff165d) !important;
            color: #fff !important;
            text-align: center;
        }
        .final-valentine h1, .final-valentine p, .final-valentine .signature { color: white !important; }
        
        .sparkle-text { animation: sparkle 2s infinite alternate; }
        @keyframes sparkle {
            from { text-shadow: 0 0 10px #fff, 0 0 20px #ff4d6d; }
            to { text-shadow: 0 0 20px #fff, 0 0 40px #ff165d; }
        }

        /* Emoji Animation */
        .emoji {
            position: absolute;
            font-size: 2.5rem;
            opacity: 0;
            animation: floatEmojis 6s ease-in-out infinite;
            bottom: -50px;
        }

        @keyframes floatEmojis {
            0% { transform: translateY(0); opacity: 1; }
            100% { transform: translateY(-100vh) rotate(20deg); opacity: 0; }
        }

        .emoji:nth-child(1) { left: 10%; animation-delay: 0s; }
        .emoji:nth-child(2) { left: 30%; animation-delay: 1.5s; }
        .emoji:nth-child(3) { left: 50%; animation-delay: 3s; }
        .emoji:nth-child(4) { left: 70%; animation-delay: 4.5s; }
        .emoji:nth-child(5) { left: 90%; animation-delay: 2s; }
    </style>
</head>
<body>

    <div class="emoji">❤️</div>
    <div class="emoji">💖</div>
    <div class="emoji">🌸</div>
    <div class="emoji">🥰</div>
    <div class="emoji">✨</div>

    <div class="book">
        <div class="page">
            <div class="front cover">
                <h1 style="color:white; text-shadow: 2px 2px 5px black;">A Message for You🤍</h1>
                <p style="color:white; text-shadow: 2px 2px 5px black;">2025.<br />SHOBHIT Special Edition</p>
            </div>
            <div class="back">
                <h2>A Special Beginning ❤️</h2>
                <p>Some people come into our lives unexpectedly, yet leave a lasting impact. You are one of those rare souls who make every moment brighter.</p>
                <p>Since we connected on Instagram on Jan 8th, 2021... it's been a journey.</p>
            </div>
        </div>

        <div class="page">
            <div class="front">
                <h2>The Magic of You ✨</h2>
                <p>There’s a charm about you, a beauty that words can hardly capture. It’s in the sparkle of your eyes and the warmth of your smile.</p>
            </div>
            <div class="back">
                <img src="./1.jpg" alt="Img 1" />
            </div>
        </div>

        <div class="page">
            <div class="front">
                <h2>The Strength Within 💫</h2>
                <p>Beyond your beauty, what stands out is your dedication and heart. Watching you grow makes me proud to know you.</p>
            </div>
            <div class="back">
                <img src="./2.jpg" alt="Img 2" />
            </div>
        </div>

        <div class="page">
            <div class="front">
                <h2>Will You Be Mine? ❤️</h2>
                <p>You make my world brighter and my heart fuller. I’d love to have you by my side forever.</p>
            </div>
            <div class="back">
                <img src="./4.png" alt="Img 4" />
            </div>
        </div>

        <div class="page">
            <div class="front final-valentine">
                <h1 class="sparkle-text">Happy Valentine's Day, Nanna 💖</h1>
                <p>From the deepest corner of my heart, this day is for you. Not just today, but every smile and heartbeat is special because of you.</p>
                <p class="signature">Forever yours,<br />❤️ Loki</p>
            </div>
            <div class="back final-valentine">
                <h2>🌹 Always & Forever 🌹</h2>
                <p>No matter where life takes us,<br />my heart will always choose you.</p>
                <p style="font-size: 0.8em; margin-top: 20px;">Made with love by Shobhit Dev</p>
            </div>
        </div>
    </div>

    <script>
        const flipBook = (elBook) => {
            elBook.style.setProperty("--c", 0);
            elBook.querySelectorAll(".page").forEach((page, idx) => {
                page.style.setProperty("--i", idx);
                page.addEventListener("click", (evt) => {
                    const curr = evt.target.closest(".back") ? idx : idx + 1;
                    elBook.style.setProperty("--c", curr);
                });
            });
        };
        document.querySelectorAll(".book").forEach(flipBook);
    </script>
</body>
</html>

