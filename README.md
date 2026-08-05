<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Solo Rocket Games (SRG) — Pulse World, Argus Core и другие проекты</title>
    <meta name="description" content="Solo Rocket Games — независимая студия. Pulse World, Argus Core, Horror at the School и другие проекты.">
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
            padding: 20px;
        }
        .container {
            max-width: 1100px;
            margin: 0 auto;
            background: #141a22;
            padding: 30px;
            border-radius: 20px;
            box-shadow: 0 0 30px rgba(255, 80, 80, 0.06);
        }
        .disclaimer-banner {
            background: #1f0f0f;
            border: 2px solid #ff4444;
            border-radius: 14px;
            padding: 18px 25px;
            margin-bottom: 30px;
            text-align: center;
            font-weight: 700;
            font-size: 1.2rem;
            color: #ff8888;
            letter-spacing: 0.5px;
            box-shadow: 0 0 25px rgba(255, 68, 68, 0.15);
        }
        .disclaimer-banner strong { color: #ff6666; }
        .disclaimer-banner span {
            background: #2a0f0f;
            padding: 3px 12px;
            border-radius: 30px;
            border: 1px solid #ff4444;
            margin: 0 6px;
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
            background: linear-gradient(135deg, #ff8844, #ff3344);
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
            border: 1px solid #ff6644;
            padding: 8px 16px;
            border-radius: 30px;
            font-size: 0.8rem;
            color: #ff8844;
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
            border-color: #ff6644;
            background: #1a2a22;
            color: #ffffff;
        }
        .game-tab:hover {
            border-color: #ff6644;
            color: #ffffff;
        }
        .game-content { display: block; }
        .game-content.hidden { display: none; }
        .game-title {
            font-size: 2.5rem;
            font-weight: 700;
            color: #f0f0f0;
            margin: 10px 0;
        }
        .game-title span { color: #ff6644; }
        .game-description {
            background: #0d141c;
            padding: 25px;
            border-radius: 16px;
            margin: 20px 0;
            border-left: 4px solid #ff6644;
            font-size: 1.1rem;
            color: #c0d0d0;
            white-space: pre-wrap;
        }
        .game-description.argus-specs { border-left-color: #44aaff; }
        .game-description.argus-specs strong { color: #44aaff; }
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
        .game-meta-item strong { color: #ff8844; }
        .section { margin: 40px 0; }
        .section h2 {
            font-size: 2rem;
            border-left: 6px solid #ff6644;
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
        .buy-card:hover { border-color: #ff6644; }
        .buy-card .price {
            font-size: 2.2rem;
            font-weight: 700;
            color: #ffffff;
            margin: 10px 0;
        }
        .buy-card .platform { color: #aabbcc; }
        .btn {
            display: inline-block;
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
        .btn-pc {
            background: #1a2a3a;
            border: 2px solid #44aaff;
            color: #88ccff;
        }
        .btn-pc:hover { background: #1a3a4a; }
        .btn-android {
            background: #1a3a2a;
            border: 2px solid #66ff99;
            color: #88ffbb;
        }
        .btn-android:hover { background: #1a4a3a; }
        .btn-pulse {
            background: #2a2a1a;
            border: 2px solid #ffaa44;
            color: #ffcc88;
        }
        .btn-pulse:hover { background: #3a3a2a; }
        .btn-horror {
            background: #2a1a2a;
            border: 2px solid #cc66ff;
            color: #dd99ff;
        }
        .btn-horror:hover { background: #3a2a3a; }
        .btn-steam {
            background: #1b2838;
            border: 2px solid #66b3ff;
            color: #c7d5e0;
        }
        .btn-steam:hover { background: #2a3f5a; }
        .btn-itch {
            background: #2a1a1a;
            border: 2px solid #ff6666;
            color: #ffaaaa;
        }
        .btn-itch:hover { background: #3d2222; }
        .btn-site {
            background: #1a2a1a;
            border: 2px solid #ff8844;
            color: #ffcc88;
        }
        .btn-site:hover { background: #223d22; }
        .warning-yellow {
            color: #ffaa44;
            background: #1f1a0f;
            padding: 15px;
            border-radius: 12px;
            border: 1px solid #ffaa44;
            margin: 20px 0;
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
        .specs h3 { color: #ff8844; margin-bottom: 12px; }
        .specs ul { list-style: none; }
        .specs li { padding: 6px 0; border-bottom: 1px solid #1f2a33; }
        .specs li strong { color: #dddddd; }
        .footer {
            margin-top: 50px;
            text-align: center;
            border-top: 1px solid #1f2a33;
            padding-top: 30px;
            color: #667788;
            font-size: 0.95rem;
        }
        .footer a { color: #88ccaa; text-decoration: none; }
        .badge {
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
        .badge-blue {
            background: #1a1a2a;
            color: #66aaff;
            border: 1px solid #66aaff;
        }
        .badge-red {
            background: #2a1a1a;
            color: #ff6666;
            border: 1px solid #ff6666;
        }
        .secret-text {
            color: #ff44aa;
            text-shadow: 0 0 20px rgba(255, 68, 170, 0.3);
            font-style: italic;
            text-align: center;
            font-size: 1.5rem;
            padding: 40px 0;
        }
        .argus-features {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 15px;
            margin: 20px 0;
        }
        .argus-features li {
            background: #1a222a;
            padding: 12px 18px;
            border-radius: 12px;
            list-style: none;
            border-left: 3px solid #44aaff;
            font-size: 1rem;
        }
        .download-buttons {
            display: flex;
            gap: 20px;
            justify-content: center;
            flex-wrap: wrap;
            margin: 25px 0;
        }
        @media (max-width: 700px) {
            .specs { grid-template-columns: 1fr; }
            .header { flex-direction: column; align-items: start; }
            .argus-features { grid-template-columns: 1fr; }
        }
    </style>
</head>
<body>
<div class="container">

    <!-- БАННЕР-ПРЕДУПРЕЖДЕНИЕ -->
    <div class="disclaimer-banner">
        ⚡ <strong>ВАЖНО:</strong>  
        <span>Solo Rocket Games (SRG)</span>  
        — это совершенно новая студия.  
        Мы <strong>НЕ ИМЕЕМ</strong> никакого отношения к TrioGames.  
        Это наш собственный путь, наши проекты, наша ответственность.
    </div>

    <!-- ШАПКА -->
    <div class="header">
        <div class="logo">
            <h1>🚀 Solo Rocket Games</h1>
            <p>независимая студия <span class="corp-badge">⚡ SRG</span></p>
        </div>
        <div>
            <span class="badge">🛸 В разработке</span>
            <span class="badge badge-green">Pulse World: 2027</span>
        </div>
    </div>

    <!-- ВЫБОР ИГРЫ -->
    <div class="game-selector">
        <div class="game-tab active" data-game="pulse">🌍 Pulse World</div>
        <div class="game-tab" data-game="argus">🛡️ Argus Core</div>
        <div class="game-tab" data-game="horror">🏫 Horror at the School</div>
        <div class="game-tab" data-game="zombie">🧟 Зомби Космос</div>
        <div class="game-tab" data-game="secret">🔮 Секретный проект</div>
    </div>

    <!-- ============================================================ -->
    <!-- PULSE WORLD -->
    <!-- ============================================================ -->
    <div id="game-pulse" class="game-content">
        <div class="game-title">🌍 <span>Pulse World</span> 🤖</div>
        <div class="game-description">
            <strong>Приключение робота в мире, где пульс бьётся в каждой детали.</strong>
            Ты — маленький робот, который просыпается в Хабе. Чтобы спасти мир, нужно собрать 83 микро-схемы, пройти через 7 уникальных карт и победить финального босса.
            <br><br>
            🌟 Открой для себя: Деревню роботов, Зимний биом, Пустыню, Джунгли, Лавовый вулкан и Убежище.
            <br>
            🎁 Собирай монеты, открывай сундуки, меняй скины и подписывайся на PW Gold.
        </div>
        <div class="game-meta">
            <span class="game-meta-item"><strong>🎮 Жанр:</strong> 3D-приключение / Платформер</span>
            <span class="game-meta-item"><strong>👥 Игроков:</strong> 1 (мультиплеер в обновлении 2)</span>
            <span class="game-meta-item"><strong>📅 Выход:</strong> 2027</span>
            <span class="game-meta-item"><strong>🎨 Студия:</strong> Solo Rocket Games (SRG)</span>
        </div>
        <div class="download-buttons">
            <a href="#" class="btn btn-pulse">💾 Скачать Pulse World</a>
        </div>
    </div>

    <!-- ============================================================ -->
    <!-- ARGUS CORE -->
    <!-- ============================================================ -->
    <div id="game-argus" class="game-content hidden">
        <div class="game-title">🛡️ <span>Argus Core</span> 💻</div>
        <div class="game-description argus-specs">
            <strong>🛡️ Argus Core — антивирус, который я делаю сам.</strong>
            <br><br>
            <strong>Что умеет:</strong>
        </div>
        <ul class="argus-features">
            <li>⚡ Быстрое и полное сканирование ПК</li>
            <li>🔍 Следит за загрузками</li>
            <li>❓ Сам спрашивает: удалить или оставить?</li>
            <li>🌗 Тёмная / светлая тема</li>
            <li>🇷🇺🇬🇧 Русский и английский язык</li>
        </ul>
        <div class="game-description argus-specs" style="border-left-color: #44aaff;">
            <strong>💰 Бесплатно. Без рекламы. Без подписок.</strong>
            <br>
            📱 В планах — мобильная версия.
            <br><br>
            🔗 <strong>Сайт:</strong> <a href="https://maratktoa-sketch.github.io/Argus-Core/" style="color: #44aaff;" target="_blank">https://maratktoa-sketch.github.io/Argus-Core/</a>
            <br>
            📱 <strong>Telegram:</strong> <a href="https://t.me/ymarat123tube" style="color: #44aaff;" target="_blank">t.me/ymarat123tube</a>
        </div>
        <div class="game-meta">
            <span class="game-meta-item"><strong>📅 Выход:</strong> Конец 2027 – начало 2028</span>
            <span class="game-meta-item"><strong>🎨 Студия:</strong> Solo Rocket Games (SRG)</span>
        </div>
        <div class="download-buttons">
            <a href="#" class="btn btn-pc">💻 Скачать для ПК</a>
            <a href="#" class="btn btn-android">📱 Скачать для Android</a>
        </div>
    </div>

    <!-- ============================================================ -->
    <!-- HORROR AT THE SCHOOL -->
    <!-- ============================================================ -->
    <div id="game-horror" class="game-content hidden">
        <div class="game-title">🏫 <span>Horror at the School</span> 👻</div>
        <div class="game-description">
═══════════════════════════════════════
         HORROR AT THE SCHOOL
═══════════════════════════════════════
   Обычное утро. Ты собираешь рюкзак,
   выходишь из дома и садишься в автобус.
   Вокруг — ни души. Город пуст.
   Когда ты прибываешь к школе, ты понимаешь:
   обратной дороги нет.
═══════════════════════════════════════
   ИССЛЕДУЙ ШКОЛУ — 3 этажа страха
   ВСТРЕЧАЙ МОНСТРОВ — физрук, математичка, руссычка, штука в биологии и ДИРЕКТОР
   СЛЕДИ ЗА СОСТОЯНИЕМ — пульс и рассудок
   СОБИРАЙ РЕСУРСЫ — ключи, аптечки, записки, оружие
   ВЫБИРАЙСЯ ЖИВЫМ — собери 3 ключа, победи директора, открой главную дверь
═══════════════════════════════════════
        </div>
        <div class="game-meta">
            <span class="game-meta-item"><strong>🎮 Жанр:</strong> Психологический хоррор</span>
            <span class="game-meta-item"><strong>📅 Выход:</strong> 2028</span>
            <span class="game-meta-item"><strong>🎨 Студия:</strong> Solo Rocket Games (SRG)</span>
        </div>
        <div class="download-buttons">
            <a href="#" class="btn btn-horror">⬇️ Скачать Horror at the School</a>
        </div>
    </div>

    <!-- ============================================================ -->
    <!-- ЗОМБИ КОСМОС (TrioGames) -->
    <!-- ============================================================ -->
    <div id="game-zombie" class="game-content hidden">
        <div class="game-title">🧟 <span>Зомби Космос</span> 🌍</div>
        <div class="game-description" style="border-left-color: #ff4444;">
            <strong>⚠️ Этот проект создан студией TrioGames.</strong>
            <br><br>
            Solo Rocket Games (SRG) не имеет отношения к разработке этой игры. Однако мы с уважением относимся к труду разработчиков TrioGames и готовы поддержать их проект.
            <br><br>
            📌 <strong>Официальная страница игры появится позже. Следите за новостями.</strong>
        </div>
        <div class="game-meta">
            <span class="game-meta-item"><strong>🎮 Жанр:</strong> Выживание / Action</span>
            <span class="game-meta-item"><strong>🎨 Студия:</strong> TrioGames</span>
            <span class="game-meta-item"><strong>📅 Выход:</strong> Неизвестно</span>
        </div>
        <div class="warning-yellow">
            ⏳ <strong>Ссылка на игру появится позже.</strong>  
            Следите за обновлениями на этой странице или в Telegram-канале SRG.
        </div>
    </div>

    <!-- ============================================================ -->
    <!-- СЕКРЕТНЫЙ ПРОЕКТ -->
    <!-- ============================================================ -->
    <div id="game-secret" class="game-content hidden">
        <div class="game-title">🔮 <span>Секретный проект</span> 🕵️</div>
        <div class="secret-text">
            ⚡ КОДОВОЕ НАЗВАНИЕ: "NOVA" ⚡<br>
            <span style="font-size: 1rem; color: #667788;">
                Информация засекречена.<br>
                Следите за обновлениями.
            </span>
        </div>
        <div class="game-description" style="border-left-color: #ff44aa; text-align: center;">
            <strong>🚧 В РАЗРАБОТКЕ</strong><br>
            Мы не можем рассказать детали,<br>
            но это будет нечто <strong>совершенно новое</strong>.<br>
            Следите за анонсами в 2028 году.
        </div>
        <div class="game-meta">
            <span class="game-meta-item"><strong>🎮 Жанр:</strong> ???</span>
            <span class="game-meta-item"><strong>📅 Выход:</strong> ???</span>
            <span class="game-meta-item"><strong>🎨 Студия:</strong> Solo Rocket Games (SRG)</span>
        </div>
    </div>

    <!-- ПОДВАЛ -->
    <div class="footer">
        <p>© 2026 <strong>Solo Rocket Games (SRG)</strong> — все права защищены.</p>
        <p style="margin-top: 8px;">
            <a href="#">GitHub</a> · 
            <a href="#">Telegram</a> · 
            <a href="#">YouTube</a>
        </p>
    </div>
</div>

<script>
    const tabs = document.querySelectorAll('.game-tab');
    const contents = {
        pulse: document.getElementById('game-pulse'),
        argus: document.getElementById('game-argus'),
        horror: document.getElementById('game-horror'),
        zombie: document.getElementById('game-zombie'),
        secret: document.getElementById('game-secret')
    };

    tabs.forEach(tab => {
        tab.addEventListener('click', function() {
            tabs.forEach(t => t.classList.remove('active'));
            this.classList.add('active');
            Object.values(contents).forEach(c => c.classList.add('hidden'));
            const game = this.dataset.game;
            if (contents[game]) contents[game].classList.remove('hidden');
        });
    });
</script>
</body>
</html>
