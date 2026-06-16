<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=yes">
    <title>Bypass City Pro – Link & Executor Bypass</title>
    <style>
        * { margin:0; padding:0; box-sizing:border-box; font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif; }
        body {
            background: #0b0e14;
            color: #eef2f8;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 1.5rem 1rem 3rem;
        }
        .container { max-width: 1000px; width: 100%; }
        .header {
            display: flex;
            align-items: center;
            gap: 12px;
            margin-bottom: 2rem;
            flex-wrap: wrap;
            justify-content: center;
        }
        .logo {
            font-size: 2.4rem;
            font-weight: 800;
            background: linear-gradient(135deg, #f7971e, #ffd200);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            letter-spacing: -0.5px;
            text-shadow: 0 0 40px rgba(255, 210, 0, 0.15);
        }
        .badge {
            background: rgba(255,255,255,0.06);
            backdrop-filter: blur(8px);
            border: 1px solid rgba(255,255,255,0.08);
            padding: 0.25rem 1rem;
            border-radius: 100px;
            font-size: 0.7rem;
            font-weight: 600;
            color: #ffd200;
            letter-spacing: 0.5px;
            text-transform: uppercase;
        }
        .stats {
            font-size: 0.8rem;
            color: #8896b0;
            background: rgba(255,255,255,0.02);
            padding: 0.3rem 1rem;
            border-radius: 100px;
            border: 1px solid #1f2a3e;
        }
        .card {
            background: rgba(18, 24, 34, 0.7);
            backdrop-filter: blur(12px);
            border-radius: 2.5rem;
            border: 1px solid rgba(255,255,255,0.06);
            padding: 2rem 1.8rem;
            box-shadow: 0 30px 50px -20px rgba(0,0,0,0.6);
            margin-bottom: 2rem;
        }
        .card h2 {
            font-size: 1.2rem;
            font-weight: 600;
            margin-bottom: 0.3rem;
            color: #d0d9e8;
        }
        .card p.sub {
            color: #8896b0;
            font-size: 0.9rem;
            margin-bottom: 1.5rem;
            border-left: 3px solid #ffd200;
            padding-left: 1rem;
        }
        .input-group {
            display: flex;
            flex-wrap: wrap;
            gap: 0.8rem;
            align-items: center;
        }
        .input-group input {
            flex: 1;
            min-width: 200px;
            padding: 0.9rem 1.2rem;
            border-radius: 2rem;
            border: 1px solid #2a3348;
            background: #0b101a;
            color: #eef2f8;
            font-size: 1rem;
            outline: none;
            transition: 0.2s;
        }
        .input-group input:focus {
            border-color: #ffd200;
            box-shadow: 0 0 0 3px rgba(255, 210, 0, 0.15);
        }
        .input-group button {
            padding: 0.9rem 2rem;
            border-radius: 2rem;
            border: none;
            background: linear-gradient(135deg, #f7971e, #ffd200);
            color: #0b0e14;
            font-weight: 700;
            font-size: 1rem;
            cursor: pointer;
            transition: transform 0.1s, box-shadow 0.2s;
            white-space: nowrap;
        }
        .input-group button:active { transform: scale(0.97); }
        .input-group button:disabled { opacity: 0.4; pointer-events: none; }

        .presets {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin: 1.2rem 0 0.5rem;
        }
        .preset-btn {
            background: rgba(255,255,255,0.04);
            border: 1px solid #2a3348;
            padding: 0.4rem 1rem;
            border-radius: 2rem;
            font-size: 0.75rem;
            color: #b0c0dd;
            cursor: pointer;
            transition: 0.15s;
        }
        .preset-btn:hover {
            background: rgba(255,210,0,0.08);
            border-color: #ffd200;
            color: #fff;
        }

        .loader { display: none; text-align: center; padding: 2rem 0; }
        .loader .spinner {
            display: inline-block;
            width: 40px;
            height: 40px;
            border: 4px solid rgba(255,210,0,0.1);
            border-top-color: #ffd200;
            border-radius: 50%;
            animation: spin 0.7s linear infinite;
        }
        @keyframes spin { to { transform: rotate(360deg); } }
        .loader p { margin-top: 0.5rem; color: #8896b0; }

        #result { margin-top: 1.8rem; border-top: 1px solid #1f2a3e; padding-top: 1.5rem; display: none; }
        #result .final-url {
            background: #0b101a;
            padding: 1rem 1.2rem;
            border-radius: 1.5rem;
            word-break: break-all;
            border: 1px solid #2a3348;
            font-family: monospace;
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            gap: 0.8rem;
        }
        #result .final-url a {
            color: #ffd200;
            text-decoration: none;
            flex: 1;
        }
        #result .final-url a:hover { text-decoration: underline; }
        #result .copy-btn {
            background: #2a3348;
            border: none;
            color: #eef2f8;
            padding: 0.4rem 1rem;
            border-radius: 2rem;
            font-size: 0.8rem;
            cursor: pointer;
            transition: 0.15s;
        }
        #result .copy-btn:hover { background: #3a4a5a; }

        .supported-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(140px, 1fr));
            gap: 0.7rem;
            margin-top: 0.5rem;
        }
        .site-item {
            background: rgba(255,255,255,0.02);
            border: 1px solid #1f2a3e;
            border-radius: 1.2rem;
            padding: 0.6rem 0.8rem;
            text-align: center;
            font-size: 0.8rem;
            color: #b0c0dd;
            transition: 0.15s;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 6px;
        }
        .site-item .icon { font-size: 1.1rem; }
        .site-item:hover {
            background: rgba(255,210,0,0.04);
            border-color: #ffd200;
            color: #fff;
        }

        .executor-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(180px, 1fr));
            gap: 0.8rem;
            margin-top: 0.5rem;
        }
        .executor-item {
            background: rgba(255,255,255,0.02);
            border: 1px solid #1f2a3e;
            border-radius: 1.2rem;
            padding: 0.8rem;
            text-align: center;
            color: #b0c0dd;
        }
        .executor-item .name {
            font-weight: 600;
            color: #eef2f8;
        }
        .executor-item .key-status {
            font-size: 0.7rem;
            padding: 0.2rem 0.6rem;
            border-radius: 100px;
            background: rgba(0,200,0,0.15);
            color: #8f8;
            display: inline-block;
            margin-top: 0.3rem;
        }
        .executor-item .key-status.keyed {
            background: rgba(255,100,0,0.15);
            color: #fa0;
        }

        .tabs {
            display: flex;
            gap: 0.5rem;
            margin-bottom: 1.5rem;
            flex-wrap: wrap;
        }
        .tab-btn {
            background: rgba(255,255,255,0.04);
            border: 1px solid #2a3348;
            padding: 0.6rem 1.5rem;
            border-radius: 2rem;
            color: #b0c0dd;
            cursor: pointer;
            font-weight: 500;
            transition: 0.15s;
        }
        .tab-btn.active {
            background: rgba(255,210,0,0.1);
            border-color: #ffd200;
            color: #fff;
        }
        .tab-btn:hover { background: rgba(255,210,0,0.05); }
        .tab-content { display: none; }
        .tab-content.active { display: block; }

        .footer {
            margin-top: 2rem;
            font-size: 0.75rem;
            color: #4a5a78;
            text-align: center;
            border-top: 1px solid #1a2332;
            padding-top: 1.5rem;
        }
        .footer a { color: #ffd200; text-decoration: none; }
        @media (max-width: 600px) {
            .card { padding: 1.2rem; }
            .input-group button { width: 100%; }
            .supported-grid { grid-template-columns: repeat(auto-fill, minmax(110px, 1fr)); }
            .executor-grid { grid-template-columns: repeat(auto-fill, minmax(150px, 1fr)); }
        }
        .toast {
            position: fixed;
            bottom: 2rem;
            left: 50%;
            transform: translateX(-50%);
            background: #1f2a3e;
            padding: 0.8rem 1.5rem;
            border-radius: 2rem;
            border-left: 4px solid #ffd200;
            font-size: 0.85rem;
            color: #eef2f8;
            box-shadow: 0 10px 30px rgba(0,0,0,0.5);
            display: none;
            z-index: 999;
        }
    </style>
</head>
<body>

<div class="toast" id="toast"></div>

<div class="container">
    <div class="header">
        <span class="logo">⛓️ Bypass City Pro</span>
        <span class="badge">⚡ v4.1 – Working Bypass API</span>
        <span class="stats" id="siteCount">Loading sites…</span>
    </div>

    <!-- Tabs -->
    <div class="tabs">
        <button class="tab-btn active" data-tab="bypass">🔗 Link Bypass</button>
        <button class="tab-btn" data-tab="executor">⚡ Executor Bypass</button>
    </div>

    <!-- Tab 1: Link Bypass -->
    <div id="tab-bypass" class="tab-content active">
        <div class="card">
            <h2>🌐 Unlock any short link – using Bypass.city API</h2>
            <p class="sub">Paste a Linkvertise, LootLabs, adf.ly, or any link shortener URL.</p>

            <div class="input-group">
                <input type="text" id="urlInput" placeholder="https://linkvertise.com/..." value="https://linkvertise.com/12345">
                <button id="bypassBtn">⚡ Bypass & Get Link</button>
            </div>

            <div class="presets">
                <span class="preset-btn" data-url="https://linkvertise.com/">Linkvertise</span>
                <span class="preset-btn" data-url="https://lootlabs.com/">LootLabs</span>
                <span class="preset-btn" data-url="https://adf.ly/">adf.ly</span>
                <span class="preset-btn" data-url="https://link-to.net/">Link-to</span>
                <span class="preset-btn" data-url="https://destyy.com/">Destyy</span>
                <span class="preset-btn" data-url="https://shrinke.me/">Shrinke</span>
                <span class="preset-btn" data-url="https://cutt.ly/">Cutt.ly</span>
                <span class="preset-btn" data-url="https://bit.ly/">Bitly</span>
            </div>

            <div class="loader" id="loader">
                <div class="spinner"></div>
                <p>Resolving final URL via Bypass.city API…</p>
            </div>

            <div id="result">
                <div class="final-url">
                    <a href="#" target="_blank" id="finalLink">Click to open</a>
                    <button class="copy-btn" id="copyBtn">📋 Copy</button>
                </div>
            </div>
        </div>

        <div class="card">
            <h2>📰 Supported Shorteners & Services</h2>
            <p class="sub" style="margin-bottom: 0.8rem;">We support over 70 link shorteners and ad‑walls.</p>
            <div class="supported-grid" id="siteGrid"></div>
            <p style="margin-top: 1rem; font-size: 0.8rem; color: #4a5a78;">➕ More added weekly – request a service in the feedback.</p>
        </div>
    </div>

    <!-- Tab 2: Executor Bypass -->
    <div id="tab-executor" class="tab-content">
        <div class="card">
            <h2>⚡ Roblox Executor Bypass & Keyless Versions</h2>
            <p class="sub">Find the best Roblox executors that are keyless or have easy key bypass methods.</p>
            <div class="executor-grid" id="executorGrid"></div>
            <p style="margin-top: 1rem; font-size: 0.8rem; color: #4a5a78;">⚠️ Always use caution when downloading executors – only use trusted sources.</p>
        </div>
    </div>

    <div class="footer">
        Bypass City Pro • Made by Damon • For educational and research purposes only.<br>
        Respect the terms of service of each service.
    </div>
</div>

<script>
    (function() {
        // ---------- DATA ----------
        const sites = [
            { name: 'Linkvertise', icon: '🔗' },
            { name: 'LootLabs', icon: '💎' },
            { name: 'Loot-Link', icon: '🎁' },
            { name: 'adf.ly', icon: '📢' },
            { name: 'shorte.st', icon: '✂️' },
            { name: 'link-to.net', icon: '🔗' },
            { name: 'destyy.com', icon: '🔀' },
            { name: 'shrinke.me', icon: '📏' },
            { name: 'cutt.ly', icon: '✂️' },
            { name: 'bit.ly', icon: '🔗' },
            { name: 'tinyurl.com', icon: '🔗' },
            { name: 'ow.ly', icon: '🦉' },
            { name: 'buff.ly', icon: '📤' },
            { name: 'goo.gl', icon: '🔗' },
            { name: 'is.gd', icon: '🔗' },
            { name: 'v.gd', icon: '🔗' },
            { name: 'mcaf.ee', icon: '🛡️' },
            { name: 's.id', icon: '📲' },
            { name: 'shorturl.at', icon: '🔗' },
            { name: 'rb.gy', icon: '🔗' },
            { name: 't.co', icon: '🐦' },
            { name: 'lnkd.in', icon: '💼' },
            { name: 'g.co', icon: '🔍' },
            { name: 'maps.app.goo.gl', icon: '🗺️' },
            { name: 'youtu.be', icon: '▶️' },
            { name: 'amzn.to', icon: '🛒' },
            { name: 'spoti.fi', icon: '🎵' },
            { name: 'bitly.com', icon: '🔗' },
            { name: 'rebrandly.com', icon: '🔄' },
            { name: 'short.io', icon: '🔗' },
            { name: 'bl.ink', icon: '🔗' },
            { name: 'mylink.xyz', icon: '🔗' },
            { name: 'linktr.ee', icon: '🌿' },
            { name: 'l.instagram.com', icon: '📷' },
            { name: 'fb.watch', icon: '📘' },
            { name: 'whatsapp.com/channel', icon: '💬' },
            { name: 'discord.com/invite', icon: '💬' },
            { name: 'reddit.com/r', icon: '🤖' },
            { name: 'sub2unlock.com', icon: '🔓' },
            { name: 'work.ink', icon: '💼' },
            { name: 'exe.io', icon: '📂' },
            { name: 'cutt.us', icon: '✂️' },
            { name: 'gg.gg', icon: '🔗' },
            { name: 'ez.lv', icon: '🔗' },
            { name: 'scrnch.me', icon: '🔗' },
            { name: 'clk.ink', icon: '🔗' },
            { name: 'cutt.ly', icon: '✂️' },
            { name: 'tiny.cc', icon: '🔗' },
            { name: 'short.link', icon: '🔗' },
            { name: 'bit.do', icon: '🔗' },
            { name: 'b.link', icon: '🔗' },
            { name: 'p.tl', icon: '🔗' },
            { name: 'r.ag', icon: '🔗' },
            { name: 'tny.im', icon: '🔗' },
            { name: 'x.co', icon: '🔗' },
            { name: 'u.to', icon: '🔗' },
            { name: '1url.com', icon: '🔗' },
            { name: 'lnk.bio', icon: '🔗' },
            { name: 'taplink.cc', icon: '🔗' },
            { name: 'l.ink', icon: '🔗' },
            { name: 'link.mi', icon: '🔗' },
            { name: 'qr.ae', icon: '🔗' },
            { name: 's.c', icon: '🔗' },
            { name: 'zz.ee', icon: '🔗' },
            { name: 'gg.gg', icon: '🔗' },
            { name: 'clk.sh', icon: '🔗' },
            { name: 'shrink.one', icon: '🔗' },
            { name: 'urls.xyz', icon: '🔗' },
            { name: 'reurl.cc', icon: '🔗' },
            { name: 'kurzlinks.de', icon: '🔗' },
            { name: 'href.li', icon: '🔗' },
            { name: 'surl.li', icon: '🔗' },
            { name: 'kutt.it', icon: '🔗' },
        ];

        const executors = [
            { name: 'Krnl (Keyless)', status: 'Keyless (via beta) by default' },
            { name: 'Synapse X', status: 'Paid – key required' },
            { name: 'Script-Ware', status: 'Paid – key required' },
            { name: 'Oxygen U', status: 'Keyless (unofficial)' },
            { name: 'Comet', status: 'Keyless' },
            { name: 'Electron', status: 'Keyless' },
            { name: 'Valyse', status: 'Keyless' },
            { name: 'Nova', status: 'Keyless' },
            { name: 'Elysian', status: 'Keyless (beta)' },
            { name: 'Fluxus', status: 'Keyed (bypass available via auto-updater)' },
            { name: 'Hydrogen', status: 'Keyless' },
            { name: 'Aurora', status: 'Keyless' },
            { name: 'Calamari', status: 'Keyed (bypass via key system)' },
            { name: 'Skid', status: 'Keyless' },
            { name: 'Vega X', status: 'Keyed (bypass with Bypass.city style tools)' },
            { name: 'Delta', status: 'Keyed (some versions keyless)' },
        ];

        // ---------- UI SETUP ----------
        const grid = document.getElementById('siteGrid');
        grid.innerHTML = '';
        sites.forEach(s => {
            const div = document.createElement('div');
            div.className = 'site-item';
            div.innerHTML = `<span class="icon">${s.icon}</span> ${s.name}`;
            grid.appendChild(div);
        });
        document.getElementById('siteCount').textContent = `${sites.length} services`;

        const execGrid = document.getElementById('executorGrid');
        execGrid.innerHTML = '';
        executors.forEach(e => {
            const div = document.createElement('div');
            div.className = 'executor-item';
            const isKeyless = e.status.toLowerCase().includes('keyless');
            div.innerHTML = `
                <div class="name">${e.name}</div>
                <div class="key-status ${isKeyless ? '' : 'keyed'}">${e.status}</div>
            `;
            execGrid.appendChild(div);
        });

        // ---------- TAB SWITCHING ----------
        const tabs = document.querySelectorAll('.tab-btn');
        tabs.forEach(btn => {
            btn.addEventListener('click', function() {
                tabs.forEach(b => b.classList.remove('active'));
                this.classList.add('active');
                const tabId = this.getAttribute('data-tab');
                document.querySelectorAll('.tab-content').forEach(t => t.classList.remove('active'));
                document.getElementById('tab-' + tabId).classList.add('active');
            });
        });

        // ---------- BYPASS LOGIC (USING BYPASS.CITY API) ----------
        const urlInput = document.getElementById('urlInput');
        const bypassBtn = document.getElementById('bypassBtn');
        const loader = document.getElementById('loader');
        const resultDiv = document.getElementById('result');
        const finalLink = document.getElementById('finalLink');
        const copyBtn = document.getElementById('copyBtn');
        const toast = document.getElementById('toast');

        function showToast(msg, duration = 2500) {
            toast.textContent = msg;
            toast.style.display = 'block';
            clearTimeout(toast._timer);
            toast._timer = setTimeout(() => { toast.style.display = 'none'; }, duration);
        }

        function bypass(url) {
            let target = url.trim();
            if (!target) { showToast('Please enter a URL.', 2000); return; }
            if (!target.match(/^https?:\/\//)) target = 'https://' + target;

            loader.style.display = 'block';
            resultDiv.style.display = 'none';
            bypassBtn.disabled = true;

            // Use the official Bypass.city API (free, no key)
            const apiUrl = 'https://api.bypass.city/v1/bypass?url=' + encodeURIComponent(target);

            fetch(apiUrl, {
                method: 'GET',
                headers: { 'Accept': 'application/json' }
            })
            .then(response => {
                if (!response.ok) throw new Error('API returned ' + response.status);
                return response.json();
            })
            .then(data => {
                loader.style.display = 'none';
                resultDiv.style.display = 'block';
                if (data && data.success && data.destination) {
                    const finalUrl = data.destination;
                    finalLink.href = finalUrl;
                    finalLink.textContent = finalUrl;
                    showToast('✅ Bypassed successfully!', 1500);
                } else {
                    // Fallback: if API fails, try to use the URL directly (might not work)
                    finalLink.href = target;
                    finalLink.textContent = target + ' (API returned no destination)';
                    showToast('⚠️ Could not resolve via API – try again.', 3000);
                }
                bypassBtn.disabled = false;
            })
            .catch(err => {
                loader.style.display = 'none';
                resultDiv.style.display = 'block';
                finalLink.href = target;
                finalLink.textContent = target + ' (API error – try again later)';
                showToast('⚠️ API error: ' + err.message, 3000);
                bypassBtn.disabled = false;
            });
        }

        // ---------- EVENTS ----------
        bypassBtn.addEventListener('click', () => bypass(urlInput.value));

        document.querySelectorAll('.preset-btn').forEach(btn => {
            btn.addEventListener('click', function() {
                const base = this.getAttribute('data-url');
                // Use a random demo path to simulate a real shortened link
                const demo = base + 'example';
                urlInput.value = demo;
                bypass(demo);
            });
        });

        urlInput.addEventListener('keypress', e => {
            if (e.key === 'Enter') bypassBtn.click();
        });

        // Copy button
        copyBtn.addEventListener('click', function() {
            const link = finalLink.href;
            if (link && link !== '#') {
                navigator.clipboard.writeText(link).then(() => {
                    showToast('📋 Copied to clipboard!', 1500);
                }).catch(() => {
                    // Fallback
                    const range = document.createRange();
                    range.selectNode(finalLink);
                    window.getSelection().removeAllRanges();
                    window.getSelection().addRange(range);
                    document.execCommand('copy');
                    showToast('📋 Copied!', 1500);
                });
            }
        });

        // Pre-fill demo URL
        urlInput.value = 'https://linkvertise.com/12345';
    })();
</script>
</body>
</html>
