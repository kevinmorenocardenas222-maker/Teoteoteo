<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Para ti...</title>
    <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@600&family=Lora:ital,wght@0,400;0,500;1,400&display=swap" rel="stylesheet">
    <style>
        * { box-sizing: border-box; margin: 0; padding: 0; }

        body {
            background: linear-gradient(135deg, #fbc2eb 0%, #a6c1ee 100%);
            font-family: 'Lora', Georgia, serif;
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 20px;
            overflow-x: hidden;
        }

        .glass-card {
            background: rgba(255, 255, 255, 0.45);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border: 1px solid rgba(255, 255, 255, 0.6);
            box-shadow: 0 8px 32px 0 rgba(31, 38, 135, 0.15);
            border-radius: 24px;
            padding: 30px 20px;
            text-align: center;
            color: #333;
            max-width: 600px;
            width: 100%;
            position: relative;
            z-index: 10;
            overflow: hidden;
        }

        .title {
            font-family: 'Dancing Script', cursive;
            font-size: 2.5rem;
            color: #d53f8c;
            margin-bottom: 20px;
            font-weight: 600;
        }

        .divider {
            width: 80px;
            height: 4px;
            background-color: #f687b3;
            margin: 0 auto 25px auto;
            border-radius: 10px;
        }

        .message-text {
            font-size: 1.1rem;
            line-height: 1.6;
            text-align: justify;
            color: #4a5568;
            font-weight: 500;
            letter-spacing: 0.5px;
            word-wrap: break-word;
            user-select: all;
            -webkit-user-select: all;
        }

        .morse-section {
            margin-top: 35px;
            padding-top: 25px;
            border-top: 1px solid #fed7e2;
        }

        .morse-title {
            font-size: 0.85rem;
            color: #d53f8c;
            font-weight: bold;
            margin-bottom: 15px;
            font-family: sans-serif;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        .morse-box {
            background-color: rgba(255, 255, 255, 0.65);
            padding: 20px;
            border-radius: 16px;
            font-family: monospace;
            font-size: 0.95rem;
            color: #2d3748;
            word-wrap: break-word;
            letter-spacing: 4px;
            font-weight: bold;
            user-select: all;
            -webkit-user-select: all;
        }

        .hint {
            font-size: 0.8rem;
            color: #718096;
            margin-top: 15px;
            font-style: italic;
            font-family: sans-serif;
        }

        .corner-flower {
            position: absolute;
            width: 90px;
            opacity: 0.7;
            pointer-events: none;
            color: #f687b3;
        }

        .top-left { top: -15px; left: -15px; transform: rotate(-45deg); }
        .bottom-right { bottom: -15px; right: -15px; transform: rotate(135deg); }

        .petal {
            position: fixed;
            background: radial-gradient(circle, #ffdde1 0%, #ff9a9e 100%);
            border-radius: 150% 0 150% 0;
            opacity: 0.6;
            animation: fall linear infinite;
            z-index: 1;
            pointer-events: none;
        }

        @keyframes fall {
            0% { transform: translateY(-10vh) rotate(0deg) scale(0.5); opacity: 0; }
            10% { opacity: 0.8; }
            100% { transform: translateY(110vh) rotate(360deg) scale(1); opacity: 0; }
        }

        ::selection { background: #fbc2eb; color: #2d3748; }
    </style>
</head>
<body>
    <script>
        function createPetals() {
            for (let i = 0; i < 20; i++) {
                let petal = document.createElement('div');
                petal.className = 'petal';
                let size = Math.random() * 12 + 8; 
                let left = Math.random() * 100; 
                let duration = Math.random() * 8 + 6; 
                let delay = Math.random() * 8; 
                petal.style.width = `${size}px`;
                petal.style.height = `${size}px`;
                petal.style.left = `${left}vw`;
                petal.style.animationDuration = `${duration}s`;
                petal.style.animationDelay = `${delay}s`;
                document.body.appendChild(petal);
            }
        }
        window.onload = createPetals;
    </script>

    <div class="glass-card">
        <svg class="corner-flower top-left" viewBox="0 0 100 100" fill="currentColor">
            <path d="M50 0 C60 30, 80 40, 100 50 C80 60, 60 70, 50 100 C40 70, 20 60, 0 50 C20 40, 40 30, 50 0 Z"/>
            <circle cx="50" cy="50" r="15" fill="#fbc2eb"/>
        </svg>
        <svg class="corner-flower bottom-right" viewBox="0 0 100 100" fill="currentColor">
            <path d="M50 0 C60 30, 80 40, 100 50 C80 60, 60 70, 50 100 C40 70, 20 60, 0 50 C20 40, 40 30, 50 0 Z"/>
            <circle cx="50" cy="50" r="15" fill="#fbc2eb"/>
        </svg>

        <h1 class="title">Un mensaje para ti...</h1>
        <div class="divider"></div>

        <p class="message-text">
            Uryyb, lbh cebonoyl jbaqre jung fgenatr guvatf V'z tvivat lbh, naq jryy, qrfcvgr zl qnevat vqrn, vg pnzr gb zr onfrq ba gur srryvat bs jnagvat gb rkcerff fbzrguvat ornhgvshy gb lbh, znlor lbh jrer rkcrpgvat vg, znlor abg, ohg ertneqyrff, V jnag lbh gb xabj gung hagvy abj, lbh ner bar bs gur orfg crbcyr V'ir zrg, V'q fnl V terj nggnpurq dhvpxyl, ohg ab, V'ir orra jnagvat lbh naq jnagvat gur bguref jvgubhg gurz xabjvat, vg jnf fnq gb xabj V jrag fb haabgvprq nf gb or pbzcyrgryl sbetbggra, ohg V qba'g whqtr lbh, V jnf arire gurer naq gung jbhyq or nfxvat sbe n cynpr V arire unq, V jba'g tb shegure, gur guvat vf, gbqnl vf n fcrpvny qnl. . . V ubcr, V'z abg fher vs lbh'yy ernq guvf gur fnzr qnl lbh sbhaq gur zrffntr be vs lbh gbbx n juvyr be qvqa'g fbyir vg, gur guvat vf, guvf vf gur svany fgrc, V'z jevgvat guvf ba Znepu 16gu, va pynffebbz 19, naq lbh unir ab vqrn jung V'z qbvat Unun, guvf zrffntr vf zrnag gb or qrpvcurerq orgjrra Znepu 27-28, orpnhfr vg'f lbhe oveguqnl, V qvqa'g xabj jung gb trg lbh naq pbhyqa'g tvir lbh nf zhpu nf lbhe zbgure qvq, vg'f abg zhpu ohg vg'f fbzrguvat, vg'f n frg bs gjb oenpryrgf gb funer jvgu fbzrbar, V tvir lbh obgu naq abg bar sbe zr naq bar sbe lbh orpnhfr vg'f zrnag sbe lbh gb qrpvqr jub lbh jnag gb funer guvf qrgnvy jvgu, naq nyfb zber guna boyvtvat lbh gb unir vg jvgu zr, V'q yvxr gb tvir lbh fbzrguvat fb lbh pna funer vg jvgu fbzrbar lbh nccerpvngr, qba'g funer vg jvgu whfg nalbar, gur inyhr bs gur nccerpvngvba V jnag lbh gb tvir vg jbhyq o ybfg. . . Nyfb, V jvfu lbh gur orfg bs oyrffvatf ba gur qnl lbh qrpelcg gur zrffntr, jvgu ybir naq fvapreryl, Xriva.
        </p>

        <div class="morse-section">
            <p class="morse-title">— Una pista para ti —</p>
            <div class="morse-box">
                .... - - .--. ... ---... -..-. -..-. .-. .- .-- .-.-.- --- .-. --. -..-. - --- --- .-.. -..-. -.-. .- . ... .- .-. -....- -.-. .. .--. .... . .-. -..-.
            </div>
            <p class="hint">(Mantén presionado para copiar los textos)</p>
        </div>
    </div>
</body>
</html>


