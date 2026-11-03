<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Patiska — Бутик женской одежды</title>
    <style>
        /* ============ БАЗА ============ */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            -webkit-tap-highlight-color: transparent;
        }

        body {
            font-family: 'Segoe UI', 'Arial', sans-serif;
            background: repeating-linear-gradient(
                90deg,
                #ff6a88 0%,
                #ff9a9e 10%,
                #fbc687 20%,
                #ffd166 30%,
                #a8e063 40%,
                #56c596 50%,
                #4facfe 60%,
                #7b6cf6 70%,
                #c86dd7 80%,
                #ff6a88 90%,
                #ff6a88 100%
            );
            background-size: 200% 100%;
            animation: rainbowFlow 8s linear infinite;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            padding: 20px;
            -webkit-font-smoothing: antialiased;
            overflow-x: hidden;
            position: relative;
            user-select: none;
            -webkit-user-select: none;
            -webkit-touch-callout: none;
        }

        @keyframes rainbowFlow {
            0%   { background-position: 0% 50%; }
            100% { background-position: -200% 50%; }
        }

        /* ============ ЛЕТАЮЩИЕ РЕТРО-ЧАСТИЦЫ ============ */
        .particles {
            position: fixed;
            inset: 0;
            pointer-events: none;
            z-index: 0;
            overflow: hidden;
        }

        .particle {
            position: absolute;
            bottom: -50px;
            border-radius: 50%;
            opacity: 0;
            animation: flyUp linear infinite;
            will-change: transform, opacity;
        }

        .particle.star {
            clip-path: polygon(50% 0%, 61% 35%, 98% 35%, 68% 57%, 79% 91%, 50% 70%, 21% 91%, 32% 57%, 2% 35%, 39% 35%);
            border-radius: 0;
        }

        .particle.diamond {
            clip-path: polygon(50% 0%, 100% 50%, 50% 100%, 0% 50%);
            border-radius: 0;
        }

        @keyframes flyUp {
            0%   { transform: translateY(0) rotate(0deg) scale(0.6); opacity: 0; }
            10%  { opacity: 0.7; }
            90%  { opacity: 0.7; }
            100% { transform: translateY(-110vh) rotate(360deg) scale(1.1); opacity: 0; }
        }

        /* ============ КАРТОЧКА ============ */
        .app {
            max-width: 420px;
            width: 100%;
            background: rgba(255, 255, 255, 0.78);
            backdrop-filter: blur(18px);
            -webkit-backdrop-filter: blur(18px);
            border-radius: 28px;
            padding: 34px 24px 28px;
            box-shadow: 0 24px 48px rgba(0, 0, 0, 0.12), 0 0 0 1px rgba(255,255,255,0.5) inset;
            animation: cardAppear 1s cubic-bezier(0.22, 1, 0.36, 1) both;
            border: 1px solid rgba(255,255,255,0.6);
            position: relative;
            z-index: 1;
        }

        @keyframes cardAppear {
            from { opacity: 0; transform: translateY(40px) scale(0.97); }
            to   { opacity: 1; transform: translateY(0) scale(1); }
        }

        /* ============ ЗАГОЛОВОК ============ */
        header {
            text-align: center;
            margin-bottom: 30px;
            position: relative;
            z-index: 1;
        }

        h1 {
            font-size: 2.6rem;
            font-weight: 900;
            letter-spacing: 3px;
            background: repeating-linear-gradient(
                90deg,
                #ff6a88 0%,
                #ff9a9e 10%,
                #fbc687 20%,
                #ffd166 30%,
                #a8e063 40%,
                #56c596 50%,
                #4facfe 60%,
                #7b6cf6 70%,
                #c86dd7 80%,
                #ff6a88 90%,
                #ff6a88 100%
            );
            background-size: 200% 100%;
            -webkit-background-clip: text;
            background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 6px;
            animation: titleIn 0.9s 0.2s cubic-bezier(0.34, 1.56, 0.64, 1) both,
                       rainbowFlow 8s linear infinite;
            filter: drop-shadow(0 2px 6px rgba(255, 106, 136, 0.25));
        }

        @keyframes titleIn {
            from { opacity: 0; transform: scale(0.85) translateY(-8px); }
            to   { opacity: 1; transform: scale(1) translateY(0); }
        }

        .subtitle {
            font-size: 0.95rem;
            color: #7a7a8e;
            font-weight: 400;
            letter-spacing: 1px;
        }

        /* ============ СЕТКА ИКОНОК ============ */
        .grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 22px 14px;
            margin-bottom: 28px;
            position: relative;
            z-index: 1;
        }

        /* 🔥 ВАЖНО: базовая opacity = 1, fill-mode = backwards */
        .grid-item {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 8px;
            text-decoration: none;
            color: #2d2d3a;
            cursor: pointer;
            opacity: 1;
            background: none;
            border: none;
            padding: 0;
            font-family: inherit;
            font-size: inherit;
            animation: itemUp 0.55s cubic-bezier(0.22, 1, 0.36, 1) backwards;
            -webkit-user-select: none;
            user-select: none;
        }

        .grid-item:nth-child(1) { animation-delay: 0.3s; }
        .grid-item:nth-child(2) { animation-delay: 0.4s; }
        .grid-item:nth-child(3) { animation-delay: 0.5s; }
        .grid-item:nth-child(4) { animation-delay: 0.6s; }
        .grid-item:nth-child(5) { animation-delay: 0.7s; }
        .grid-item:nth-child(6) { animation-delay: 0.8s; }

        @keyframes itemUp {
            from { opacity: 0; transform: translateY(18px) scale(0.9); }
            to   { opacity: 1; transform: translateY(0) scale(1); }
        }

        .icon-circle {
            width: 64px;
            height: 64px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            background: #fff;
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.06);
            transition: transform 0.35s cubic-bezier(0.34, 1.56, 0.64, 1),
                        box-shadow 0.35s ease;
            position: relative;
            overflow: hidden;
            pointer-events: none; /* клики идут на родителя */
        }

        .instagram .icon-circle { background: linear-gradient(135deg, #fce4ec, #f8bbd0); }
        .whatsapp  .icon-circle { background: linear-gradient(135deg, #e8f5e9, #c8e6c9); }
        .telegram  .icon-circle { background: linear-gradient(135deg, #e3f2fd, #bbdefb); }
        .phone     .icon-circle { background: linear-gradient(135deg, #f1f8e9, #dcedc8); }
        .map       .icon-circle { background: linear-gradient(135deg, #e0f7fa, #b2ebf2); }
        .contacts  .icon-circle { background: linear-gradient(135deg, #ffebee, #ffcdd2); }

        .grid-item:hover .icon-circle {
            transform: translateY(-4px) scale(1.08);
            box-shadow: 0 16px 32px rgba(0, 0, 0, 0.1);
        }

        .grid-item:active .icon-circle {
            transform: scale(0.95);
        }

        .icon-circle svg {
            width: 28px;
            height: 28px;
            display: block;
            pointer-events: none;
        }

        .instagram .icon-circle svg { color: #E1306C; }
        .whatsapp  .icon-circle svg { color: #25D366; }
        .telegram  .icon-circle svg { color: #26A5E4; }
        .phone     .icon-circle svg { color: #7cb342; }
        .map       .icon-circle svg { color: #26c6da; }
        .contacts  .icon-circle svg { color: #e53935; }

        .grid-label {
            font-size: 0.72rem;
            font-weight: 500;
            color: #7a7a8e;
            text-align: center;
            line-height: 1.2;
            transition: color 0.3s ease;
        }

        .grid-item:hover .grid-label { color: #2d2d3a; }

        /* ============ КАРТОЧКА С ТЕЛЕФОНОМ ============ */
        .phone-card {
            background: linear-gradient(135deg, rgba(255,255,255,0.85), rgba(240,242,248,0.9));
            border-radius: 22px;
            padding: 20px 20px 20px 22px;
            position: relative;
            z-index: 1;
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.06);
            border: 1px solid rgba(255,255,255,0.8);
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 14px;
            animation: fadeUp 0.7s 0.95s ease backwards;
        }

        .phone-info {
            flex: 1;
            text-align: left;
        }

        .phone-label {
            font-size: 0.7rem;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 1.5px;
            color: #7a7a8e;
            margin-bottom: 2px;
        }

        .phone-number {
            font-size: 1.35rem;
            font-weight: 800;
            color: #2d2d3a;
            letter-spacing: 0.5px;
            white-space: nowrap;
        }

        .copy-btn {
            flex-shrink: 0;
            width: 52px;
            height: 52px;
            border-radius: 16px;
            border: none;
            background: linear-gradient(135deg, #f3e5f5, #e1bee7);
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            box-shadow: 0 6px 14px rgba(171, 71, 188, 0.15);
            transition: transform 0.3s cubic-bezier(0.34, 1.56, 0.64, 1),
                        box-shadow 0.3s ease,
                        background 0.3s ease;
        }

        .copy-btn svg {
            width: 22px;
            height: 22px;
            color: #ab47bc;
            transition: transform 0.3s ease;
            pointer-events: none;
        }

        .copy-btn:hover {
            background: linear-gradient(135deg, #e1bee7, #ce93d8);
            transform: translateY(-2px) scale(1.06);
        }

        .copy-btn:active { transform: scale(0.94); }

        .copy-btn.copied {
            background: linear-gradient(135deg, #c8e6c9, #a5d6a7);
        }

        .copy-btn.copied svg { color: #2e7d32; }

        /* ============ ФУТЕР ============ */
        footer {
            margin-top: 26px;
            font-size: 0.75rem;
            color: #fff;
            text-align: center;
            position: relative;
            z-index: 1;
            font-weight: 600;
            text-shadow: 0 2px 8px rgba(0,0,0,0.25);
            letter-spacing: 0.5px;
            animation: fadeUp 0.6s 1.15s ease backwards;
        }

        @keyframes fadeUp {
            from { opacity: 0; transform: translateY(12px); }
            to   { opacity: 1; transform: translateY(0); }
        }

        /* ============ УВЕДОМЛЕНИЕ — ЧЁТКО ПО ЦЕНТРУ ============ */
        .toast {
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%) scale(0.6);
            opacity: 0;
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: #fff;
            padding: 20px 32px;
            border-radius: 20px;
            font-weight: 700;
            font-size: 1.1rem;
            text-align: center;
            box-shadow: 0 20px 50px rgba(102, 126, 234, 0.5);
            transition: all 0.35s cubic-bezier(0.22, 1, 0.36, 1);
            z-index: 9999;
            pointer-events: none;
            max-width: 90vw;
            white-space: pre-line;
            line-height: 1.4;
        }

        .toast.show {
            opacity: 1;
            transform: translate(-50%, -50%) scale(1);
        }

        /* ============ МОБИЛЬНАЯ АДАПТАЦИЯ ============ */
        @media (max-width: 440px) {
            .app { padding: 28px 16px 22px; border-radius: 24px; }
            h1 { font-size: 2.2rem; letter-spacing: 2px; }
            .grid { gap: 18px 10px; }
            .icon-circle { width: 56px; height: 56px; }
            .icon-circle svg { width: 24px; height: 24px; }
            .grid-label { font-size: 0.68rem; }
            .phone-number { font-size: 1.15rem; }
            .copy-btn { width: 46px; height: 46px; }
        }

        /* ============ ДОСТУПНОСТЬ ============ */
        @media (prefers-reduced-motion: reduce) {
            *, *::before, *::after {
                animation-duration: 0.01ms !important;
                animation-iteration-count: 1 !important;
                transition-duration: 0.01ms !important;
            }
        }
    </style>
</head>
<body>
    <div class="particles" id="particles"></div>

    <div class="app">
        <header>
            <h1>Patiska</h1>
            <p class="subtitle">Бутик женской одежды</p>
        </header>

        <div class="grid">
            <a href="https://www.instagram.com/butik_patiska" target="_blank" rel="noopener" class="grid-item instagram">
                <div class="icon-circle">
                    <svg viewBox="0 0 24 24" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
                        <path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838a6.162 6.162 0 100 12.324 6.162 6.162 0 000-12.324zm0 10.162a4 4 0 110-8 4 4 0 010 8zm6.406-11.845a1.44 1.44 0 100 2.881 1.44 1.44 0 000-2.881z"/>
                    </svg>
                </div>
                <span class="grid-label">Instagram</span>
            </a>

            <a href="https://wa.me/79894977059" target="_blank" rel="noopener" class="grid-item whatsapp">
                <div class="icon-circle">
                    <svg viewBox="0 0 24 24" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
                        <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413Z"/>
                    </svg>
                </div>
                <span class="grid-label">WhatsApp</span>
            </a>

            <a href="https://t.me/Butik_Patiska" target="_blank" rel="noopener" class="grid-item telegram">
                <div class="icon-circle">
                    <svg viewBox="0 0 24 24" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
                        <path d="M12 0C5.373 0 0 5.373 0 12s5.373 12 12 12 12-5.373 12-12S18.627 0 12 0zm5.894 8.221-1.97 9.28c-.145.658-.537.818-1.084.508l-3-2.21-1.446 1.394a.759.759 0 01-.6.295h-.005l.213-3.054 5.56-5.022c.24-.213-.054-.334-.373-.121L8.32 13.617l-2.96-.924c-.64-.203-.658-.64.135-.954l11.566-4.458c.538-.196 1.006.128.832.941z"/>
                    </svg>
                </div>
                <span class="grid-label">Telegram</span>
            </a>

            <a href="tel:+79894977059" class="grid-item phone" onclick="handlePhoneClick(event)">
                <div class="icon-circle">
                    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" xmlns="http://www.w3.org/2000/svg">
                        <path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07 19.5 19.5 0 0 1-6-6 19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 4.11 2h3a2 2 0 0 1 2 1.72 12.84 12.84 0 0 0 .7 2.81 2 2 0 0 1-.45 2.11L8.09 9.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45 12.84 12.84 0 0 0 2.81.7A2 2 0 0 1 22 16.92z"/>
                    </svg>
                </div>
                <span class="grid-label">Позвонить</span>
            </a>

            <a href="https://yandex.ru/maps/?text=Махачкала, ул. Батырая, 99" target="_blank" rel="noopener" class="grid-item map">
                <div class="icon-circle">
                    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" xmlns="http://www.w3.org/2000/svg">
                        <path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0 1 18 0z"/>
                        <circle cx="12" cy="10" r="3"/>
                    </svg>
                </div>
                <span class="grid-label">Карты</span>
            </a>

            <button class="grid-item contacts" id="contactsBtn" type="button" onclick="addContact()">
                <div class="icon-circle">
                    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" xmlns="http://www.w3.org/2000/svg">
                        <path d="M4 19.5A2.5 2.5 0 0 1 6.5 17H20"/>
                        <path d="M6.5 2H20v20H6.5A2.5 2.5 0 0 1 4 19.5v-15A2.5 2.5 0 0 1 6.5 2z"/>
                    </svg>
                </div>
                <span class="grid-label">Контакты</span>
            </button>
        </div>

        <div class="phone-card">
            <div class="phone-info">
                <div class="phone-label">Телефон</div>
                <div class="phone-number">+7 (989) 497-70-59</div>
            </div>
            <button class="copy-btn" id="copyBtn" type="button" aria-label="Копировать номер" onclick="copyPhone()">
                <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round" xmlns="http://www.w3.org/2000/svg">
                    <rect x="9" y="9" width="13" height="13" rx="2" ry="2"/>
                    <path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"/>
                </svg>
            </button>
        </div>
    </div>

    <div class="toast" id="toast"></div>

    <footer>© Patiska — Бутик женской одежды</footer>

    <script>
        'use strict';

        // ============ ЛЕТАЮЩИЕ ЧАСТИЦЫ ============
        (function () {
            try {
                var container = document.getElementById('particles');
                if (!container) return;
                var colors = ['#ffffff', '#ffd166', '#4facfe', '#c86dd7', '#56c596', '#ff9a9e'];
                var shapes = ['', 'star', 'diamond'];
                var count = window.innerWidth < 500 ? 18 : 26;
                for (var i = 0; i < count; i++) {
                    var p = document.createElement('span');
                    p.className = 'particle ' + shapes[Math.floor(Math.random() * shapes.length)];
                    var size = 6 + Math.random() * 10;
                    var color = colors[Math.floor(Math.random() * colors.length)];
                    var duration = 12 + Math.random() * 14;
                    var delay = -Math.random() * duration;
                    p.style.width = size + 'px';
                    p.style.height = size + 'px';
                    p.style.background = color;
                    p.style.left = (Math.random() * 100) + '%';
                    p.style.animationDuration = duration + 's';
                    p.style.animationDelay = delay + 's';
                    p.style.boxShadow = '0 0 ' + (size / 2) + 'px ' + color;
                    container.appendChild(p);
                }
            } catch (e) {}
        })();

        // ============ УВЕДОМЛЕНИЕ ============
        var toastEl = document.getElementById('toast');
        var toastTimer = null;

        function showToast(text) {
            if (!toastEl) return;
            toastEl.textContent = text;
            toastEl.classList.add('show');
            if (toastTimer) clearTimeout(toastTimer);
            toastTimer = setTimeout(function () {
                toastEl.classList.remove('show');
            }, 2400);
        }

        // ============ КОПИРОВАНИЕ НОМЕРА ============
        var PHONE = '+79894977059';
        var PHONE_PRETTY = '+7 (989) 497-70-59';

        function copyPhone() {
            var btn = document.getElementById('copyBtn');

            function success() {
                if (btn) {
                    btn.classList.add('copied');
                    setTimeout(function () { btn.classList.remove('copied'); }, 1500);
                }
                showToast('✅ Номер скопирован:\n' + PHONE_PRETTY);
            }

            function manual() {
                showToast('📋 Номер:\n' + PHONE_PRETTY + '\n\nСкопируйте вручную');
            }

            // Метод 1: Clipboard API
            try {
                if (navigator.clipboard && navigator.clipboard.writeText) {
                    navigator.clipboard.writeText(PHONE).then(success).catch(function () {
                        fallbackCopy();
                    });
                    return;
                }
            } catch (e) {}

            fallbackCopy();

            // Метод 2: execCommand (работает везде, включая file:// и HTTP)
            function fallbackCopy() {
                try {
                    var ta = document.createElement('textarea');
                    ta.value = PHONE;
                    ta.setAttribute('readonly', '');
                    ta.style.position = 'fixed';
                    ta.style.top = '0';
                    ta.style.left = '0';
                    ta.style.opacity = '0.01';
                    ta.style.fontSize = '16px';
                    document.body.appendChild(ta);
                    ta.focus();
                    ta.select();
                    try { ta.setSelectionRange(0, PHONE.length); } catch (e) {}
                    var ok = false;
                    try { ok = document.execCommand('copy'); } catch (e) {}
                    document.body.removeChild(ta);
                    if (ok) { success(); } else { manual(); }
                } catch (e) {
                    manual();
                }
            }
        }

        // ============ КОНТАКТ ============
        function addContact() {
            try {
                var vcard = [
                    'BEGIN:VCARD',
                    'VERSION:3.0',
                    'FN:Patiska Бутик женской одежды',
                    'TEL;TYPE=CELL:+79894977059',
                    'ADR;TYPE=WORK:;;ул. Батырая, 99;Махачкала;;;',
                    'URL:https://t.me/Butik_Patiska',
                    'URL:https://instagram.com/butik_patiska',
                    'END:VCARD'
                ].join('\r\n');

                var blob = new Blob([vcard], { type: 'text/vcard;charset=utf-8' });

                // Метод 1: Web Share API (мобильные — сразу в контакты)
                if (navigator.share && navigator.canShare) {
                    try {
                        var file = new File([blob], 'patiska.vcf', { type: 'text/vcard' });
                        if (navigator.canShare({ files: [file] })) {
                            navigator.share({
                                files: [file],
                                title: 'Patiska — контакт'
                            }).then(function () {
                                showToast('✅ Контакт отправлен');
                            }).catch(function () {
                                downloadVcf(blob);
                            });
                            return;
                        }
                    } catch (e) {}
                }

                downloadVcf(blob);
            } catch (e) {
                showToast('⚠ Ошибка: ' + e.message);
            }

            function downloadVcf(blob) {
                try {
                    var url = URL.createObjectURL(blob);
                    var a = document.createElement('a');
                    a.href = url;
                    a.download = 'patiska_contact.vcf';
                    a.style.display = 'none';
                    document.body.appendChild(a);
                    a.click();
                    document.body.removeChild(a);
                    setTimeout(function () { URL.revokeObjectURL(url); }, 300);
                    showToast('✅ Контакт скачан\nОткройте файл .vcf');
                } catch (e) {
                    showToast('⚠ Не удалось создать контакт');
                }
            }
        }

        // ============ ТЕЛЕФОН НА ПК ============
        function handlePhoneClick(e) {
            var ua = navigator.userAgent || '';
            var isMobile = /iPhone|iPad|iPod|Android|Mobi|Windows Phone/i.test(ua);
            if (!isMobile) {
                e.preventDefault();
                showToast('📞 ' + PHONE_PRETTY);
            }
        }

        // ============ ЗАЩИТА ОТ КОПИРОВАНИЯ ТЕКСТА (только вне интерактива) ============
        document.addEventListener('copy', function (e) {
            var t = e.target;
            if (t && (t.tagName === 'INPUT' || t.tagName === 'TEXTAREA')) return;
            e.preventDefault();
        });
        document.addEventListener('cut', function (e) {
            var t = e.target;
            if (t && (t.tagName === 'INPUT' || t.tagName === 'TEXTAREA')) return;
            e.preventDefault();
        });
        document.addEventListener('contextmenu', function (e) {
            var t = e.target;
            if (t && t.closest && t.closest('a')) return;
            e.preventDefault();
        });
    </script>
</body>
</html>
