<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sentagon Corporation — TrioGames</title>
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

        .corp-badge {
            background: #1a2a2a;
            border: 1px solid #2a4a3a;
            padding: 8px 16px;
            border-radius: 30px;
            font-size: 0.8rem;
            color: #66cc99;
            letter-spacing: 1px;
        }

        .game-selector {
            display: flex;
            gap: 15px;
            margin: 30px 0 20px 0;
            flex-wrap: wrap;
        }

        .game-tab {
            background: #1f2a33;
            padding: 12px 25px;
            border-radius: 40px;
            cursor: pointer;
            border: 2px solid transparent;
            transition: 0.3s;
            color: #8899aa;
            font-weight: 600;
        }

        .game-tab.active {
            border-color: #66ff99;
            background: #1a2a22;
            color: #ffffff;
        }

        .game-tab:hover {
            border-color: #66ff99;
            color: #ffffff;
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

        .game-description {
            background: #0d141c;
            padding: 25px;
            border-radius: 16px;
            margin: 20px 0;
            border-left: 4px solid #66ff99;
            font-size: 1.1rem;
            color: #c0d0d0;
        }

        .game-meta {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            margin: 20px 0;
        }

        .game-meta-item {
            background: #1a222a;
            padding: 8px 20px;
            border-radius: 30px;
            font-size: 0.9rem;
            color: #88aabb;
        }

        .game-meta-item strong {
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

        .btn-demo {
            background: #1a222a;
            border: 2px solid #ffaa33;
            color: #ffcc88;
        }

        .btn-demo:hover {
            background: #2a2a1a;
            border-color: #ffbb44;
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

        .warning-yellow {
            color: #ffaa44;
            background: #1f1a0f;
            padding: 15px;
            border-radius: 12px;
            border: 1px solid #ffaa44;
            margin: 20px 0;
            font-size: 1.1rem;
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

        .badge-green {
            background: #1a2a1a;
            color: #66ff99;
            border: 1px solid #66ff99;
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

    <!-- ШАПКА С КОРПОРАЦИЕЙ -->
    <div class="header">
        <div class="logo">
            <h1>🎮 TrioGames</h1>
            <p>под управлением <strong>Sentagon Corporation</strong> <span class="corp-badge">🏛️ EST. 2026</span></p>
        </div>
        <div>
            <span class="badge">🛸 В разработке</span>
            <span class="badge badge-green">Демо: 2027</span>
        </div>
    </div>

    <!-- ВЫБОР ИГРЫ -->
    <div class="game-selector">
        <div class="game-tab active">🧟 Зомби Космос</div>
        <div class="game-tab">🏫 Horror at the School</div>
        <div class="game-tab">🔮 Секретный проект</div>
    </div>

    <!-- НАЗВАНИЕ ИГРЫ -->
    <div class="game-title">
        🧟 <span>Зомби Космос</span> 🌍
    </div>

    <!-- ОПИСАНИЕ ИГРЫ -->
    <div class="game-description">
        <strong>🌍 Путешествие по миру в поисках выживания.</strong><br>
        100 точек, 10 стран, 10 уникальных боссов. Ты — выживший, который должен пройти через Казахстан, Францию, Италию, Тунис, ЮАР, Индонезию, Вьетнам, Индию, Бразилию и Зону 51, чтобы найти способ остановить зомби-апокалипсис. Собирай ресурсы, строй базу, сражайся с ордами зомби и становись сильнее с каждым боем.
    </div>

    <!-- МЕТАДАННЫЕ -->
    <div class="game-meta">
        <span class="game-meta-item"><strong>🎮 Жанр:</strong> Выживание / Action / Roguelike</span>
        <span class="game-meta-item"><strong>👥 Игроков:</strong> 1</span>
        <span class="game-meta-item"><strong>📅 Выход:</strong> Демо в 2027, полная версия 2028</span>
        <span class="game-meta-item"><strong>🎨 Студия:</strong> TrioGames (Sentagon Corp)</span>
    </div>

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

            <!-- DEMO -->
            <div class="buy-card">
                <div class="platform">🎮 Демо (2027)</div>
                <div class="price">Бесплатно</div>
                <div style="color: #88aacc; font-size: 0.9rem;">Первые 30 точек, 3 босса</div>
                <a href="#" class="btn btn-demo">Скачать демо</a>
                <div class="warning-yellow" style="margin-top: 15px; font-size: 0.9rem;">
                    ⏳ <strong>Доступно в 2027 году</strong><br>
                    Следите за новостями!
                </div>
            </div>

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
                    Только Steam версия получает все патчи и новый контент.
                </div>
            </div>

            <!-- Собственный сайт -->
            <div class="buy-card">
                <div class="platform">🌐 Sentagon Store</div>
                <div class="price">$2.49</div>
                <div style="color: #88ccaa; font-size: 0.9rem;">DRM-free + все будущие патчи</div>
                <a href="#" class="btn btn-site">Купить с сайта</a>
            </div>

        </div>
    </div>

    <!-- ПРЕДУПРЕЖДЕНИЕ -->
    <div class="warning-yellow">
        ⏳ <strong>Игра доступна в демо-версии с 2027 года.</strong><br>
        Полная версия приблизительно выйдет в половине 2027 года. Следите за новостями TrioGames и Sentagon Corporation!
    </div>

    <!-- ПОДВАЛ -->
    <div class="footer">
        <p>© 2026 <strong>Sentagon Corporation</strong> — все права защищены.</p>
        <p style="margin-top: 8px;">
            TrioGames — игровое подразделение Sentagon Corp.
        </p>
        <p style="margin-top: 8px;">
            <a href="#">GitHub</a> · 
            <a href="#">Telegram</a> · 
            <a href="#">YouTube</a>
        </p>
    </div>

</div>

</body>
</html>
