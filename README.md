<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bionic Reader – compact start, powerful reading</title>
    <style>
        /* === COMPACT CARD STYLES (like deepseek first page) === */
        .intro-card {
            max-width: 680px;
            width: 100%;
            background: #ffffff;
            border-radius: 42px;
            box-shadow: 0 30px 50px -20px rgba(18, 30, 55, 0.25), 0 8px 18px rgba(0,0,0,0.03);
            padding: 1.8rem 3rem 2rem 3rem;
            border: 1px solid rgba(255,255,255,0.5);
            margin: 0 auto;
            background-image: radial-gradient(circle at 20% 30%, rgba(49, 151, 149, 0.1) 2px, transparent 2px),
                              radial-gradient(circle at 80% 70%, rgba(49, 151, 149, 0.05) 1px, transparent 2px);
            background-size: 40px 40px, 30px 30px;
            transition: all 0.2s;
        }

        .tool-row {
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            justify-content: space-between;
            margin: 0.6rem 0;
        }

        .tool-info {
            flex: 2 1 280px;
        }

        .tool-name {
            font-size: 2rem;
            font-weight: 620;
            color: #1a365d;
            letter-spacing: -0.3px;
            line-height: 1.1;
        }

        .tool-desc {
            font-size: 1.1rem;
            color: #2d3748;
            margin-top: 0.1rem;
            font-weight: 400;
            border-left: 2px solid #319795;
            padding-left: 0.9rem;
        }

        .try-now-btn {
            background: transparent;
            border: 2px solid #1a365d;
            color: #1a365d;
            padding: 0.6rem 2.2rem;
            border-radius: 60px;
            font-size: 1.2rem;
            font-weight: 600;
            letter-spacing: 0.5px;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            transition: 0.2s;
            white-space: nowrap;
            background-color: #ffffff;
            box-shadow: 0 5px 12px -5px rgba(20, 30, 60, 0.2);
            line-height: 1.3;
            cursor: pointer;
        }

        .try-now-btn:hover {
            background: #1a365d;
            color: white;
            border-color: #1a365d;
            box-shadow: 0 12px 18px -8px #1a365d90;
        }

        .try-now-btn:active {
            transform: scale(0.96);
        }

        .attribution {
            font-size: 0.75rem;
            color: #718096;
            text-align: right;
            margin-top: 1rem;
            opacity: 0.45;
            border-top: 1px dashed #cbd5e0;
            padding-top: 0.6rem;
        }

        /* === BIONIC READER FULL STYLES (from original bionik.html, slightly adapted) === */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
            background: linear-gradient(135deg, #f7fafc 0%, #edf2f7 100%);
            min-height: 100vh;
            color: #1a202c;
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* two‑state body */
        body.show-editor .intro-card-wrapper {
            display: none;
        }
        body.show-editor .bionic-editor-full {
            display: block;
        }

        .intro-card-wrapper {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 1.5rem;
        }

        .bionic-editor-full {
            display: none;
        }

        /* all original styles (excerpt from bionik.html, reused with minimal tweaks) */
        :root {
            --primary-dark: #1a365d;
            --primary-main: #2d3748;
            --primary-light: #4a5568;
            --primary-gradient: linear-gradient(135deg, #2d3748 0%, #1a365d 100%);
            --accent-teal: #319795;
            --accent-teal-light: #4FD1C5;
            --accent-gradient: linear-gradient(135deg, #319795 0%, #4FD1C5 100%);
            --reading-bg: #FAFAF9;
            --reading-paper: #FFFFFF;
            --reading-border: #E2E8F0;
            --text-dark: #1a202c;
            --text-medium: #4a5568;
            --text-light: #718096;
            --focus-color: #3182ce;
            --focus-bold: #2b6cb0;
            --shadow-soft: 0 4px 20px rgba(0, 0, 0, 0.06);
            --shadow-medium: 0 8px 30px rgba(0, 0, 0, 0.08);
            --shadow-strong: 0 15px 50px rgba(0, 0, 0, 0.10);
            --border-radius-sm: 12px;
            --border-radius-md: 20px;
            --border-radius-lg: 30px;
            --transition-smooth: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .main-nav {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            background: rgba(255, 255, 255, 0.97);
            backdrop-filter: blur(10px);
            padding: 20px 40px;
            z-index: 1000;
            border-bottom: 1px solid rgba(0, 0, 0, 0.05);
            box-shadow: var(--shadow-soft);
        }

        .nav-content {
            max-width: 1400px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 15px;
            text-decoration: none;
            transition: var(--transition-smooth);
            cursor: pointer;
        }

        .logo:hover {
            transform: translateY(-2px);
        }

        .logo-icon {
            font-size: 2em;
            color: var(--accent-teal);
            filter: drop-shadow(0 2px 4px rgba(49, 151, 149, 0.3));
        }

        .logo-text {
            font-size: 1.8em;
            font-weight: 700;
            letter-spacing: -0.5px;
            color: var(--primary-dark);
        }

        .logo-subtitle {
            font-size: 0.7em;
            color: var(--accent-teal);
            font-weight: 600;
            letter-spacing: 1px;
        }

        .nav-links {
            display: flex;
            gap: 30px;
            align-items: center;
        }

        .nav-link {
            text-decoration: none;
            color: var(--text-medium);
            font-weight: 500;
            padding: 10px 20px;
            border-radius: 50px;
            transition: var(--transition-smooth);
            cursor: pointer;
        }

        .nav-link:hover {
            color: var(--accent-teal);
            background: rgba(49, 151, 149, 0.05);
        }

        .nav-link.active {
            background: var(--accent-gradient);
            color: white;
        }

        .cta-button {
            background: var(--accent-gradient);
            color: white;
            padding: 12px 30px;
            border-radius: 50px;
            font-weight: 600;
            border: none;
            cursor: pointer;
            display: inline-flex;
            align-items: center;
            gap: 10px;
            box-shadow: 0 4px 15px rgba(49, 151, 149, 0.2);
            transition: var(--transition-smooth);
        }

        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(49, 151, 149, 0.3);
        }

        .page-container {
            max-width: 1400px;
            margin: 100px auto 50px;
            padding: 0 20px;
        }

        .page { display: none; }
        .page.active { display: block; }

        .hero-section { text-align: center; padding: 100px 40px; background: linear-gradient(135deg, rgba(255,255,255,0.9) 0%, rgba(250,250,249,0.7) 100%); border-radius: var(--border-radius-lg); margin-bottom: 80px; position: relative; overflow: hidden; }
        .hero-title { font-size: 3.8em; font-weight: 800; color: var(--primary-dark); }
        .hero-stats { display: flex; justify-content: center; gap: 60px; flex-wrap: wrap; }
        .stat-item { background: white; padding: 30px; border-radius: var(--border-radius-md); box-shadow: var(--shadow-soft); min-width: 180px; }
        .stat-number { font-size: 3em; font-weight: 700; color: var(--accent-teal); }
        .section-title { text-align: center; font-size: 2.5em; margin-bottom: 60px; color: var(--primary-dark); }
        .features-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(350px,1fr)); gap: 40px; }
        .feature-card { background: white; padding: 50px 40px; border-radius: var(--border-radius-lg); box-shadow: var(--shadow-soft); text-align: center; }
        .feature-icon { font-size: 3.5em; color: var(--accent-teal); }
        .testimonials-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px,1fr)); gap: 30px; }

        .main-converter { background: white; border-radius: var(--border-radius-lg); box-shadow: var(--shadow-strong); margin-bottom: 60px; }
        .converter-grid { display: grid; grid-template-columns: 1fr 1fr; }
        .input-panel, .preview-panel { padding: 50px; }
        .text-input { width: 100%; min-height: 300px; padding: 30px; border: 2px solid transparent; border-radius: var(--border-radius-sm); font-size:1.1em; background: white; }
        .customization-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px,1fr)); gap:25px; }
        .bionic-display { font-size:1.4em; line-height:1.8; white-space:pre-wrap; }
        .bionic-bold { font-weight: 700; color: var(--primary-dark); }
        .bionic-normal { font-weight: 400; color: var(--text-medium); }
        .reading-modes { display: flex; justify-content: center; gap:15px; padding:30px 40px; background: white; border-bottom:1px solid var(--reading-border); flex-wrap:wrap; }
        .mode-tab { padding:12px 30px; background: transparent; border:2px solid var(--reading-border); border-radius:50px; cursor:pointer; font-weight:600; }
        .mode-tab.active { background: var(--accent-gradient); border-color:var(--accent-teal); color:white; }
        .action-buttons { display: flex; gap:20px; padding:40px; background: linear-gradient(135deg, var(--reading-bg) 0%, white 100%); }
        .action-button { flex:1; padding:20px; border:none; border-radius:var(--border-radius-md); font-weight:600; cursor:pointer; display:flex; align-items:center; justify-content:center; gap:15px; }
        .action-button.primary { background: var(--accent-gradient); color:white; }
        .back-home { text-align: center; margin:40px 0; }
        .main-footer { background: var(--primary-gradient); color: white; padding: 60px 40px; margin-top: 100px; text-align: center; }
        .loading-overlay, .success-message { display: none; position: fixed; z-index:2000; }
        /* responsive quick */
        @media (max-width: 1200px) { .converter-grid { grid-template-columns:1fr; } }
        @media (max-width: 768px) { .hero-title { font-size:2.5em; } .page-container { margin-top:140px; } }
    </style>
</head>
<body>
    <!-- COMPACT FIRST PAGE (like deepseek) -->
    <div class="intro-card-wrapper">
        <div class="intro-card">
            <div class="tool-row">
                <div class="tool-info">
                    <div class="tool-name">Bionic Reader</div>
                    <div class="tool-desc">Read faster, focus better — with artificial fixation.</div>
                </div>
                <div class="tool-action">
                    <a href="#" class="try-now-btn" id="enterBionicBtn">Try Now →</a>
                </div>
            </div>
            <div class="attribution">bionicreader.app</div>
        </div>
    </div>

    <!-- FULL BIONIC READER EDITOR (from original bionik.html, condensed but fully functional) -->
    <div class="bionic-editor-full" id="bionicFullEditor">
        <nav class="main-nav">
            <div class="nav-content">
                <div class="logo" id="logoHomeBtn">
                    <span class="logo-icon">🚀</span>
                    <div>
                        <div class="logo-text">Bionic Reader Pro</div>
                        <div class="logo-subtitle">ENHANCE YOUR READING</div>
                    </div>
                </div>
                <div class="nav-links">
                    <div class="nav-link active" id="navHome">Home</div>
                    <div class="nav-link" id="navConverter">Converter</div>
                    <div class="nav-link" id="navFeatures">Features</div>
                    <div class="cta-button" id="ctaStart">⚡ Start Reading</div>
                </div>
            </div>
        </nav>

        <!-- Home Page (simplified, but with hero) -->
        <div id="homePageFull" class="page active">
            <div class="page-container">
                <section class="hero-section">
                    <h1 class="hero-title">Read <span style="color:#319795;">Faster</span>, Focus <span style="color:#319795;">Better</span></h1>
                    <p class="hero-subtitle">Transform any text into bionic format – guide your eyes with artificial fixation.</p>
                    <div class="hero-stats">
                        <div class="stat-item"><span class="stat-number">65%</span><span class="stat-label">Faster Reading</span></div>
                        <div class="stat-item"><span class="stat-number">40%</span><span class="stat-label">Better Focus</span></div>
                        <div class="stat-item"><span class="stat-number">100%</span><span class="stat-label">Free</span></div>
                    </div>
                    <button class="cta-button" id="heroStartBtn" style="padding:20px 50px;">📖 Try Bionic Reading</button>
                </section>
                <section class="features-section">
                    <h2 class="section-title">Why Bionic Reading Works</h2>
                    <div class="features-grid">
                        <div class="feature-card"><div class="feature-icon">🎯</div><h3>Guided Fixation</h3><p>Reduce back‑skipping, maintain focus.</p></div>
                        <div class="feature-card"><div class="feature-icon">⚡</div><h3>Speed Enhancement</h3><p>Read up to 65% faster with comprehension.</p></div>
                        <div class="feature-card"><div class="feature-icon">🧠</div><h3>Better Retention</h3><p>Brain processes information efficiently.</p></div>
                    </div>
                </section>
            </div>
        </div>

        <!-- Converter Page (full featured) -->
        <div id="converterPageFull" class="page">
            <div class="page-container">
                <div class="converter-header">
                    <h1 class="converter-title">Bionic Reading Converter</h1>
                    <p class="converter-subtitle">Paste text, customize, and read faster.</p>
                </div>
                <div class="main-converter">
                    <div class="converter-grid">
                        <div class="input-panel">
                            <h2 class="panel-title"><i>📝</i> Your Text</h2>
                            <textarea id="textInput" class="text-input" placeholder="Type or paste text...">Welcome to Bionic Reading. This method emphasizes the first letters of words, creating artificial fixation points. Try it yourself!</textarea>
                            <div class="customization-panel">
                                <h3><i>⚙️</i> Settings</h3>
                                <div class="customization-grid">
                                    <select id="readingMode">
                                        <option value="light">Light (25% bold)</option>
                                        <option value="medium" selected>Medium (50% bold)</option>
                                        <option value="heavy">Heavy (75% bold)</option>
                                    </select>
                                    <div>Fixation <input type="range" id="fixationLength" min="1" max="8" value="4"><span id="fixationValue">4 letters</span></div>
                                    <div>Text size <input type="range" id="textSize" min="14" max="28" value="18"><span id="textSizeValue">18px</span></div>
                                </div>
                            </div>
                        </div>
                        <div class="preview-panel">
                            <h2 class="panel-title"><i>👁️</i> Bionic Preview</h2>
                            <div class="reading-preview">
                                <div id="bionicPreview" class="bionic-display">Welcome to Bionic Reading...</div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="reading-modes">
                    <button class="mode-tab active" data-mode="standard">Standard</button>
                    <button class="mode-tab" data-mode="speed">Speed</button>
                    <button class="mode-tab" data-mode="focus">Focus</button>
                </div>
                <div class="action-buttons">
                    <button id="convertBtn" class="action-button primary">🔄 Convert</button>
                    <button id="copyBtn" class="action-button secondary">📋 Copy</button>
                    <button id="exportBtn" class="action-button secondary">💾 Export</button>
                </div>
                <div class="back-home">
                    <button class="cta-button" id="backToHomeBtn">🏠 Back to Home</button>
                </div>
            </div>
        </div>

        <footer class="main-footer">
            <div class="footer-content">© 2025 Bionic Reader Pro — read smarter.</div>
        </footer>
    </div>

    <!-- Loading & Success (hidden) -->
    <div id="loadingOverlay" class="loading-overlay"><div class="loading-spinner"></div><div>CONVERTING</div></div>
    <div id="successMessage" class="success-message"><i>✅</i> <span id="successText">Done</span></div>

    <script>
        (function() {
            // --- STATE: show editor after compact card click ---
            const body = document.body;
            const enterBtn = document.getElementById('enterBionicBtn');
            enterBtn.addEventListener('click', (e) => {
                e.preventDefault();
                body.classList.add('show-editor');
                // make sure home page is active inside editor
                showPageFull('home');
                // re-run converter init if needed
                if (typeof updatePreview === 'function') updatePreview();
            });

            // --- internal page management for the full editor ---
            const homePage = document.getElementById('homePageFull');
            const converterPage = document.getElementById('converterPageFull');
            const navHome = document.getElementById('navHome');
            const navConverter = document.getElementById('navConverter');
            const navFeatures = document.getElementById('navFeatures');
            const ctaStart = document.getElementById('ctaStart');
            const heroStartBtn = document.getElementById('heroStartBtn');
            const backToHomeBtn = document.getElementById('backToHomeBtn');
            const logoHomeBtn = document.getElementById('logoHomeBtn');

            function showPageFull(page) {
                homePage.classList.remove('active');
                converterPage.classList.remove('active');
                navHome.classList.remove('active');
                navConverter.classList.remove('active');
                if (page === 'home') {
                    homePage.classList.add('active');
                    navHome.classList.add('active');
                } else {
                    converterPage.classList.add('active');
                    navConverter.classList.add('active');
                    // initialize converter when shown
                    setTimeout(() => updatePreview(), 50);
                }
            }

            navHome.addEventListener('click', () => showPageFull('home'));
            navConverter.addEventListener('click', () => showPageFull('converter'));
            ctaStart.addEventListener('click', () => showPageFull('converter'));
            heroStartBtn.addEventListener('click', () => showPageFull('converter'));
            backToHomeBtn.addEventListener('click', () => showPageFull('home'));
            logoHomeBtn.addEventListener('click', () => showPageFull('home'));
            navFeatures.addEventListener('click', () => { showPageFull('home'); });

            // --- BIONIC CONVERSION LOGIC (copied and adapted) ---
            const textInput = document.getElementById('textInput');
            const bionicPreview = document.getElementById('bionicPreview');
            const readingMode = document.getElementById('readingMode');
            const fixationRange = document.getElementById('fixationLength');
            const fixationSpan = document.getElementById('fixationValue');
            const textSizeRange = document.getElementById('textSize');
            const textSizeSpan = document.getElementById('textSizeValue');
            const modeTabs = document.querySelectorAll('.mode-tab');

            function convertToBionic(text, fixationLen, boldLevel) {
                if (!text) return '';
                const lines = text.split('\n');
                return lines.map(line => {
                    if (line.trim() === '') return '';
                    const words = line.split(/(\s+)/);
                    return words.map(word => {
                        if (/\s/.test(word)) return word;
                        const len = word.length;
                        let boldPart = '', normalPart = '';
                        if (boldLevel === 'light') {
                            let cut = Math.min(fixationLen, Math.floor(len * 0.25));
                            boldPart = word.slice(0, cut);
                            normalPart = word.slice(cut);
                        } else if (boldLevel === 'heavy') {
                            let cut = Math.min(len, Math.floor(len * 0.75));
                            boldPart = word.slice(0, cut);
                            normalPart = word.slice(cut);
                        } else { // medium
                            let cut = Math.min(fixationLen, Math.floor(len * 0.5));
                            boldPart = word.slice(0, cut);
                            normalPart = word.slice(cut);
                        }
                        if (normalPart) return `<span class="bionic-bold">${boldPart}</span><span class="bionic-normal">${normalPart}</span>`;
                        else return `<span class="bionic-bold">${boldPart}</span>`;
                    }).join('');
                }).join('<br>');
            }

            function updatePreview() {
                const text = textInput.value;
                const mode = readingMode.value; // light, medium, heavy
                let fixation = parseInt(fixationRange.value, 10);
                const html = convertToBionic(text, fixation, mode);
                bionicPreview.innerHTML = html || 'Enter text to see preview';
                // apply text size
                let size = textSizeRange.value;
                bionicPreview.style.fontSize = size + 'px';
                textSizeSpan.innerText = size + 'px';
                fixationSpan.innerText = fixation + ' letters';
            }

            // event listeners
            textInput.addEventListener('input', updatePreview);
            readingMode.addEventListener('change', updatePreview);
            fixationRange.addEventListener('input', updatePreview);
            textSizeRange.addEventListener('input', updatePreview);

            // mode tabs
            modeTabs.forEach(tab => {
                tab.addEventListener('click', function() {
                    modeTabs.forEach(t => t.classList.remove('active'));
                    this.classList.add('active');
                    const mode = this.dataset.mode;
                    if (mode === 'standard') readingMode.value = 'medium';
                    else if (mode === 'speed') { readingMode.value = 'light'; fixationRange.value = 3; }
                    else if (mode === 'focus') { readingMode.value = 'heavy'; fixationRange.value = 5; }
                    updatePreview();
                });
            });

            // convert button just re-runs update
            document.getElementById('convertBtn').addEventListener('click', updatePreview);

            // copy button
            document.getElementById('copyBtn').addEventListener('click', async () => {
                const plain = bionicPreview.innerText;
                try {
                    await navigator.clipboard.writeText(plain);
                    showSuccessMsg('Copied!');
                } catch { showSuccessMsg('Copy failed'); }
            });

            // export HTML
            document.getElementById('exportBtn').addEventListener('click', () => {
                const content = bionicPreview.innerHTML;
                const html = `<!DOCTYPE html><html><head><style>.bionic-bold{font-weight:700;color:#1a365d;}.bionic-normal{font-weight:400;color:#4a5568;}</style></head><body>${content}</body></html>`;
                const blob = new Blob([html], {type:'text/html'});
                const a = document.createElement('a');
                a.href = URL.createObjectURL(blob);
                a.download = 'bionic-export.html';
                a.click();
                showSuccessMsg('Exported');
            });

            function showSuccessMsg(msg) {
                const box = document.getElementById('successMessage');
                document.getElementById('successText').innerText = msg;
                box.style.display = 'flex';
                setTimeout(() => box.style.display = 'none', 2000);
            }

            // init preview
            updatePreview();

            // optional loading overlay (not used heavily, but keep)
            window.showLoading = () => document.getElementById('loadingOverlay').style.display = 'flex';
            window.hideLoading = () => document.getElementById('loadingOverlay').style.display = 'none';
        })();
    </script>
</body>
</html>
