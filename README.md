<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TrioGames — Зомби Космос</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: #0b0e14;
            color: #e0e0e0;
            font-family: 'Segoe UI', Tahoma, sans-serif;
            line-height: 1.6;
            padding: 20px;
        }

        .container {
            max-width: 1100px;
            margin: 0 auto;
            background: #141a22;
            padding: 30px;
            border-radius: 20px;
            box-shadow: 0 0 30px rgba(0, 255, 100, 0.08);
        }

        .header {
            display: flex;
            align-items: center;
            justify-content: space-between;
            flex-wrap: wrap;
            border-bottom: 2px solid #2a3a3a;
            padding-bottom: 20px;
            margin-bottom: 30px;
        }

        .logo h1 {
            font-size: 2.8rem;
            background: linear-gradient(135deg, #b3ffb3, #00cc66);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            letter-spacing: 2px;
        }

        .logo p {
            color: #8899aa;
            font-size: 1rem;
        }

        .game-title {
            font-size: 2.5rem;
            font-weight: 700;
            color: #f0f0f0;
            margin: 10px 0;
        }

        .game-title span {
            color: #66ff99;
        }

        .section {
            margin: 40px 0;
        }

        .section h2 {
            font-size: 2rem;
            border-left: 6px solid #66ff99;
            padding-left: 20px;
            margin-bottom: 25px;
            color: #ffffff;
        }

        .buy-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 30px;
            justify-content: center;
            margin: 30px 0;
        }

        .buy-card {
            background: #1f2a33;
            padding: 25px;
            border-radius: 16px;
            flex: 1 1 220px;
            text-align: center;
            border: 1px solid #2d3d4a;
            transition: 0.25s;
        }

        .buy-card:hover {
            border-color: #66ff99;
            box-shadow: 0 0 20px rgba(102, 255, 153, 0.10);
        }

        .buy-card .price {
            font-size: 2.2rem;
            font-weight: 700;
            color: #ffffff;
            margin: 10px 0;
        }

        .buy-card .platform {
            font-size: 1rem;
            color: #aabbcc;
        }

        .btn {
            display: inline-block;
            background: #2a3f4a;
            color: #ffffff;
            padding: 14px 30px;
            border-radius: 40px;
            text-decoration: none;
            font-weight: 600;
            margin-top: 15px;
            transition: 0.25s;
            border: none;
            cursor: pointer;
            font-size: 1rem;
        }

        .btn-steam {
            background: #1b2838;
            border: 2px solid #66b3ff;
            color: #c7d5e0;
        }

        .btn-steam:hover {
            background: #2a3f5a;
            border-color: #99ccff;
        }

        .btn-itch {
            background: #2a1a1a;
            border: 2px solid #ff6666;
            color: #ffaaaa;
        }

        .btn-itch:hover {
            background: #3d2222;
            border-color: #ff8888;
        }

        .btn-site {
            background: #1a2a1a;
            border: 2px solid #66ff99;
            color: #99ffbb;
        }

        .btn-site:hover {
            background: #223d22;
            border-color: #88ffaa;
        }

        .warning-red {
            color: #ff4444;
            font-weight: 700;
            background: #1f0f0f;
            padding: 15px;
            border-radius: 12px;
            border: 1px solid #ff4444;
            margin: 20px 0;
            font-size: 1.1rem;
        }

        .warning-red strong {
            color: #ff7777;
        }

        .specs {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 30px;
            background: #0d141c;
            padding: 25px;
            border-radius: 16px;
            margin-top: 20px;
        }

        .specs h3 {
            color: #66ff99;
            margin-bottom: 12px;
        }

        .specs ul {
            list-style: none;
        }

        .specs li {
            padding: 6px 0;
            border-bottom: 1px solid #1f2a33;
        }

        .specs li strong {
            color: #dddddd;
        }

        .footer {
            margin-top: 50px;
            text-align: center;
            border-top: 1px solid #1f2a33;
            padding-top: 30px;
            color: #667788;
            font-size: 0.95rem;
        }

        .footer a {
            color: #88ccaa;
            text-decoration: none;
        }

        .badge {
            display: inline-block;
            background: #1f2a33;
            padding: 4px 14px;
            border-radius: 30px;
            font-size: 0.8rem;
            color: #99aabb;
            margin-right: 6px;
        }

        @media (max-width: 700px) {
            .specs {
                grid-template-columns: 1fr;
            }
            .header {
                flex-direction: column;
                align-items: start;
            }
        }
    </style>
</head>
<body>

<div class="container">

    <!-- ШАПКА -->
    <div class="header">
        <div class="logo">
            <h1>🎮 TrioGames</h1>
            <p>Инди-студия из трёх друзей</p>
        </div>
        <div>
            <span class="badge">🛸 В разработке</span>
            <span class="badge">⏳ 2026</span>
        </div>
    </div>

    <!-- НАЗВАНИЕ ИГРЫ -->
    <div class="game-title">
        🧟 <span>Зомби Космос</span> 🌍
    </div>
    <p style="font-size: 1.2rem; color: #aabbcc; margin-top: -5px;">
        100 точек выживания по всему миру. Боссы. Лут. Самолётик.
    </p>

    <!-- СИСТЕМНЫЕ ТРЕБОВАНИЯ -->
    <div class="section">
        <h2>⚙️ Системные требования</h2>
        <div class="specs">
            <div>
                <h3>🔻 Минимальные</h3>
                <ul>
                    <li><strong>ОС:</strong> Windows 10 (64-bit)</li>
                    <li><strong>Процессор:</strong> Intel i3-2100 / AMD FX-6300</li>
                    <li><strong>RAM:</strong> 4 ГБ</li>
                    <li><strong>Видеокарта:</strong> GTX 750 Ti / Radeon HD 7870 (2GB)</li>
                    <li><strong>Место:</strong> 8 ГБ</li>
                    <li><strong>DirectX:</strong> 11</li>
                </ul>
            </div>
            <div>
                <h3>🚀 Рекомендуемые</h3>
                <ul>
                    <li><strong>ОС:</strong> Windows 10/11 (64-bit)</li>
                    <li><strong>Процессор:</strong> Intel i5-8400 / AMD Ryzen 5 2600</li>
                    <li><strong>RAM:</strong> 8–16 ГБ</li>
                    <li><strong>Видеокарта:</strong> GTX 1060 / RX 580 (4GB+)</li>
                    <li><strong>Место:</strong> 8 ГБ (SSD)</li>
                    <li><strong>DirectX:</strong> 12</li>
                </ul>
            </div>
        </div>
    </div>

    <!-- КНОПКИ ПОКУПКИ -->
    <div class="section">
        <h2>🛒 Где купить</h2>

        <div class="buy-grid">

            <!-- Steam -->
            <div class="buy-card">
                <div class="platform">🔥 Steam</div>
                <div class="price">$2.49</div>
                <div style="color: #88aacc; font-size: 0.9rem;">Полная игра + все обновления</div>
                <a href="#" class="btn btn-steam">Купить в Steam</a>
            </div>

            <!-- Itch.io -->
            <div class="buy-card">
                <div class="platform">🎲 Itch.io</div>
                <div class="price">$0.99</div>
                <div style="color: #cc8888; font-size: 0.9rem;">Урезанная версия</div>
                <a href="#" class="btn btn-itch">Купить на Itch.io</a>
                <div class="warning-red" style="margin-top: 15px; font-size: 0.9rem;">
                    ⚠️ <strong>ВНИМАНИЕ!</strong><br>
                    Эта версия <strong>НЕ ПОЛУЧАЕТ ОБНОВЛЕНИЙ</strong>.<br>
                    В ней отсутствуют новые уровни, зомби и оружие.
                </div>
            </div>

            <!-- Собственный сайт -->
            <div class="buy-card">
                <div class="platform">🌐 Сайт TrioGames</div>
                <div class="price">$2.49</div>
                <div style="color: #88ccaa; font-size: 0.9rem;">DRM-free + все будущие патчи</div>
                <a href="#" class="btn btn-site">Купить с сайта</a>
            </div>

        </div>
    </div>

    <!-- КОРОТКОЕ ПРИМЕЧАНИЕ -->
    <div class="warning-red">
        ❗ <strong>Версия на Itch.io ($0.99) — это демо-билд.</strong> 
        Она не будет обновляться. Полный контент (Зона 51, Король Зомби, 100 точек) — только в Steam или на нашем сайте.
    </div>

    <!-- ПОДВАЛ -->
    <div class="footer">
        <p>© 2026 TrioGames — сделано с ❤️ и 🧠</p>
        <p style="margin-top: 8px;">
            <a href="#">GitHub</a> · 
            <a href="#">Telegram</a> · 
            <a href="#">YouTube</a>
        </p>
    </div>

</div>

</body>
</html>
