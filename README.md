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
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Image Filter Pro | 50+ Filters & Editor</title>
    <style>
        /* === COMPACT CARD STYLES (First Page) === */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: #eef2f7;
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            font-family: 'Inter', system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
            padding: 1.5rem;
            transition: background 0.3s;
        }

        body.editor-active {
            display: block;
            background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
            padding: 0;
        }

        .options-card {
            max-width: 680px;
            width: 100%;
            background: #ffffff;
            border-radius: 42px;
            box-shadow: 0 30px 50px -20px rgba(18, 30, 55, 0.25), 0 8px 18px rgba(0,0,0,0.03);
            padding: 1.8rem 3rem 2rem 3rem;
            border: 1px solid rgba(255,255,255,0.5);
            transition: all 0.2s;
            background-image: radial-gradient(circle at 20% 30%, rgba(235, 242, 255, 0.3) 2px, transparent 2px),
                            radial-gradient(circle at 80% 70%, rgba(200, 212, 240, 0.2) 1px, transparent 2px);
            background-size: 40px 40px, 30px 30px;
            margin: 0 auto;
        }

        body.editor-active .options-card {
            display: none;
        }

        .tool-block {
            margin-top: 1.2rem;
        }

        .tool-block:first-of-type {
            margin-top: 0.2rem;
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
            color: #0f1f3a;
            letter-spacing: -0.3px;
            line-height: 1.1;
        }

        .tool-desc {
            font-size: 1.1rem;
            color: #4d5b7c;
            margin-top: 0.1rem;
            font-weight: 400;
            border-left: 2px solid #b3c3e3;
            padding-left: 0.9rem;
        }

        .try-btn {
            background: transparent;
            border: 2px solid #283659;
            color: #283659;
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

        .try-btn:hover {
            background: #1e2b46;
            color: white;
            border-color: #1e2b46;
            box-shadow: 0 12px 18px -8px #1e2b4690;
        }

        .try-btn:active {
            transform: scale(0.96);
        }

        .tool-action {
            flex: 0 0 auto;
            margin-left: 2rem;
        }

        .attribution {
            font-size: 0.75rem;
            color: #8a99be;
            text-align: right;
            margin-top: 1rem;
            opacity: 0.45;
            border-top: 1px dashed #cfd9ec;
            padding-top: 0.6rem;
        }

        @media (max-width: 600px) {
            .options-card { padding: 1.5rem; }
            .tool-name { font-size: 1.7rem; }
            .tool-row { flex-direction: column; align-items: flex-start; gap: 1rem; }
            .tool-action { margin-left: 0; width: 100%; }
            .try-btn { width: 100%; justify-content: center; }
        }

        /* === FULL FEATURE STYLES (from img fil.html) === */
        :root {
            --primary-dark: #1a365d;
            --primary-main: #2d3748;
            --primary-light: #4a5568;
            --primary-gradient: linear-gradient(135deg, #2d3748 0%, #1a365d 100%);
            --accent-purple: #805ad5;
            --accent-purple-light: #9f7aea;
            --accent-gradient: linear-gradient(135deg, #805ad5 0%, #9f7aea 100%);
            --accent-pink: #d53f8c;
            --accent-pink-light: #ed64a6;
            --pink-gradient: linear-gradient(135deg, #d53f8c 0%, #ed64a6 100%);
            --visual-blue: #3182ce;
            --visual-blue-light: #63b3ed;
            --visual-gradient: linear-gradient(135deg, #3182ce 0%, #63b3ed 100%);
            --clean-bg: #FAFAF9;
            --clean-paper: #FFFFFF;
            --clean-border: #E2E8F0;
            --text-dark: #1a202c;
            --text-medium: #4a5568;
            --text-light: #718096;
            --image-bg: #f7fafc;
            --image-border: #e2e8f0;
            --shadow-soft: 0 4px 20px rgba(0, 0, 0, 0.06);
            --shadow-medium: 0 8px 30px rgba(0, 0, 0, 0.08);
            --shadow-strong: 0 15px 50px rgba(0, 0, 0, 0.10);
            --border-radius-sm: 12px;
            --border-radius-md: 20px;
            --border-radius-lg: 30px;
            --transition-smooth: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .editor-container {
            display: none;
        }

        body.editor-active .editor-container {
            display: block;
        }

        /* Navigation */
        .main-nav {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            background: rgba(255, 255, 255, 0.95);
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
            color: var(--accent-purple);
            filter: drop-shadow(0 2px 4px rgba(128, 90, 213, 0.3));
        }

        .logo-text {
            font-size: 1.8em;
            font-weight: 300;
            letter-spacing: 1px;
            color: var(--primary-dark);
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
            position: relative;
            overflow: hidden;
            cursor: pointer;
        }

        .nav-link::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(128, 90, 213, 0.1), transparent);
            transition: left 0.6s;
        }

        .nav-link:hover::before {
            left: 100%;
        }

        .nav-link:hover {
            color: var(--accent-purple);
            background: rgba(128, 90, 213, 0.05);
        }

        .nav-link.active {
            background: var(--accent-gradient);
            color: white;
            box-shadow: 0 4px 15px rgba(128, 90, 213, 0.2);
        }

        .cta-button {
            background: var(--accent-gradient);
            color: white;
            padding: 12px 30px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            transition: var(--transition-smooth);
            border: none;
            cursor: pointer;
            display: inline-flex;
            align-items: center;
            gap: 10px;
            box-shadow: 0 4px 15px rgba(128, 90, 213, 0.2);
        }

        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(128, 90, 213, 0.3);
        }

        /* Page Management */
        .page {
            display: none;
            animation: fadeIn 0.5s ease;
        }

        .page.active {
            display: block;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .page-container {
            max-width: 1400px;
            margin: 100px auto 50px;
            padding: 0 20px;
        }

        /* ========== HOME PAGE STYLES ========== */
        .hero-section {
            text-align: center;
            padding: 100px 40px;
            background: linear-gradient(135deg, rgba(255, 255, 255, 0.9) 0%, rgba(245, 241, 250, 0.7) 100%);
            border-radius: var(--border-radius-lg);
            margin-bottom: 80px;
            position: relative;
            overflow: hidden;
            border: 1px solid rgba(0, 0, 0, 0.05);
        }

        .hero-bg {
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: radial-gradient(circle at 20% 80%, rgba(128, 90, 213, 0.1) 0%, transparent 50%),
                        radial-gradient(circle at 80% 20%, rgba(49, 130, 206, 0.1) 0%, transparent 50%),
                        radial-gradient(circle at 40% 40%, rgba(213, 63, 140, 0.05) 0%, transparent 50%);
            z-index: 1;
        }

        .hero-content {
            position: relative;
            z-index: 2;
        }

        .hero-title {
            font-size: 3.5em;
            font-weight: 300;
            margin-bottom: 30px;
            color: var(--primary-dark);
            line-height: 1.2;
        }

        .hero-title span {
            background: linear-gradient(135deg, var(--accent-purple), var(--visual-blue));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .hero-subtitle {
            font-size: 1.2em;
            color: var(--text-medium);
            max-width: 700px;
            margin: 0 auto 50px;
            line-height: 1.8;
            font-weight: 300;
        }

        .hero-stats {
            display: flex;
            justify-content: center;
            gap: 60px;
            margin: 60px 0;
            flex-wrap: wrap;
        }

        .stat-item {
            text-align: center;
            background: white;
            padding: 30px;
            border-radius: var(--border-radius-md);
            box-shadow: var(--shadow-soft);
            min-width: 180px;
            transition: var(--transition-smooth);
        }

        .stat-item:hover {
            transform: translateY(-10px);
            box-shadow: var(--shadow-medium);
        }

        .stat-number {
            font-size: 2.5em;
            font-weight: 300;
            color: var(--accent-purple);
            display: block;
            margin-bottom: 10px;
        }

        .stat-label {
            font-size: 1em;
            color: var(--text-medium);
            text-transform: uppercase;
            letter-spacing: 1px;
            font-weight: 500;
        }

        .features-section {
            margin-bottom: 100px;
        }

        .section-title {
            text-align: center;
            font-size: 2.5em;
            margin-bottom: 60px;
            color: var(--primary-dark);
            font-weight: 300;
            position: relative;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 3px;
            background: var(--accent-gradient);
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 40px;
        }

        .feature-card {
            background: var(--clean-paper);
            padding: 50px 40px;
            border-radius: var(--border-radius-lg);
            box-shadow: var(--shadow-soft);
            text-align: center;
            transition: var(--transition-smooth);
            border: 1px solid transparent;
            position: relative;
            overflow: hidden;
        }

        .feature-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 5px;
            background: var(--accent-gradient);
        }

        .feature-card:hover {
            transform: translateY(-15px);
            box-shadow: var(--shadow-strong);
            border-color: var(--accent-purple-light);
        }

        .feature-icon {
            font-size: 3.5em;
            margin-bottom: 30px;
            color: var(--accent-purple);
            display: inline-block;
            width: 80px;
            height: 80px;
            line-height: 80px;
            background: linear-gradient(135deg, rgba(128, 90, 213, 0.1) 0%, rgba(255, 255, 255, 0.1) 100%);
            border-radius: 50%;
            box-shadow: 0 4px 20px rgba(128, 90, 213, 0.15);
        }

        .feature-title {
            font-size: 1.6em;
            margin-bottom: 20px;
            color: var(--primary-dark);
            font-weight: 300;
        }

        .feature-description {
            color: var(--text-medium);
            line-height: 1.8;
            font-weight: 300;
        }

        .steps-section {
            background: linear-gradient(135deg, var(--clean-bg) 0%, var(--clean-paper) 100%);
            padding: 80px 40px;
            border-radius: var(--border-radius-lg);
            margin-bottom: 100px;
            border: 1px solid rgba(0, 0, 0, 0.05);
        }

        .steps-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1000px;
            margin: 0 auto;
            position: relative;
        }

        .steps-container::before {
            content: '';
            position: absolute;
            top: 40px;
            left: 25%;
            right: 25%;
            height: 2px;
            background: var(--accent-gradient);
            z-index: 1;
        }

        .step {
            text-align: center;
            position: relative;
            z-index: 2;
            background: white;
            padding: 40px;
            border-radius: var(--border-radius-md);
            box-shadow: var(--shadow-soft);
            width: 30%;
        }

        .step-number {
            width: 60px;
            height: 60px;
            background: var(--accent-gradient);
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.8em;
            font-weight: 600;
            margin: 0 auto 30px;
            box-shadow: 0 4px 15px rgba(128, 90, 213, 0.3);
        }

        .step-title {
            font-size: 1.4em;
            margin-bottom: 15px;
            color: var(--primary-dark);
            font-weight: 300;
        }

        .step-description {
            color: var(--text-medium);
            line-height: 1.7;
            font-weight: 300;
        }

        .categories-section {
            background: var(--clean-paper);
            border-radius: var(--border-radius-lg);
            padding: 60px 40px;
            margin-bottom: 100px;
            box-shadow: var(--shadow-soft);
        }

        .categories-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-top: 60px;
        }

        .category-card {
            text-align: center;
            padding: 40px 30px;
            background: var(--clean-bg);
            border-radius: var(--border-radius-md);
            transition: var(--transition-smooth);
            cursor: pointer;
            border: 2px solid transparent;
        }

        .category-card:hover {
            transform: translateY(-10px);
            box-shadow: var(--shadow-medium);
            border-color: var(--accent-purple-light);
        }

        .category-icon {
            font-size: 2.5em;
            margin-bottom: 20px;
            color: var(--accent-purple);
        }

        .category-title {
            font-size: 1.3em;
            color: var(--primary-dark);
            margin-bottom: 10px;
            font-weight: 500;
        }

        .category-count {
            color: var(--text-light);
            font-size: 0.9em;
        }

        .cta-section {
            text-align: center;
            padding: 80px 40px;
            background: linear-gradient(135deg, rgba(128, 90, 213, 0.05) 0%, rgba(49, 130, 206, 0.05) 100%);
            border-radius: var(--border-radius-lg);
            margin-bottom: 80px;
            border: 1px solid rgba(128, 90, 213, 0.1);
        }

        .cta-title {
            font-size: 2.5em;
            margin-bottom: 30px;
            color: var(--primary-dark);
            font-weight: 300;
        }

        .cta-description {
            font-size: 1.2em;
            color: var(--text-medium);
            max-width: 600px;
            margin: 0 auto 50px;
            line-height: 1.8;
            font-weight: 300;
        }

        /* FAQ Section */
        .faq-section {
            max-width: 800px;
            margin: 60px auto;
            padding: 0 20px;
        }

        .faq-section h3 {
            font-size: 1.4em;
            color: var(--primary-dark);
            margin: 30px 0 10px;
        }

        .faq-section p {
            color: var(--text-medium);
            margin-bottom: 20px;
            padding-left: 20px;
            border-left: 3px solid var(--accent-purple-light);
        }

        /* ========== FILTER PAGE STYLES ========== */
        .filter-header {
            text-align: center;
            margin-bottom: 60px;
        }

        .filter-title {
            font-size: 3em;
            margin-bottom: 20px;
            color: var(--primary-dark);
            font-weight: 300;
        }

        .filter-subtitle {
            font-size: 1.2em;
            color: var(--text-medium);
            max-width: 600px;
            margin: 0 auto;
            line-height: 1.8;
            font-weight: 300;
        }

        .main-filter {
            background: var(--clean-paper);
            border-radius: var(--border-radius-lg);
            box-shadow: var(--shadow-strong);
            overflow: hidden;
            margin-bottom: 60px;
            border: 1px solid rgba(0, 0, 0, 0.05);
        }

        .filter-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 0;
            min-height: 600px;
        }

        .upload-panel {
            padding: 50px;
            background: linear-gradient(135deg, var(--clean-bg) 0%, var(--clean-paper) 100%);
            border-right: 1px solid var(--clean-border);
            display: flex;
            flex-direction: column;
        }

        .panel-title {
            font-size: 1.8em;
            margin-bottom: 30px;
            color: var(--primary-dark);
            font-weight: 300;
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .upload-area {
            flex: 1;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            padding: 40px;
            border: 3px dashed var(--accent-purple-light);
            border-radius: var(--border-radius-md);
            background: white;
            transition: var(--transition-smooth);
            cursor: pointer;
            position: relative;
            overflow: hidden;
        }

        .upload-area:hover {
            border-color: var(--accent-purple);
            background: rgba(128, 90, 213, 0.02);
            transform: translateY(-5px);
        }

        .upload-area.drag-over {
            border-color: var(--visual-blue);
            background: rgba(49, 130, 206, 0.05);
        }

        .upload-icon {
            font-size: 4em;
            color: var(--accent-purple-light);
            margin-bottom: 20px;
        }

        .upload-text {
            font-size: 1.2em;
            color: var(--primary-dark);
            font-weight: 500;
            margin-bottom: 10px;
        }

        .upload-subtext {
            color: var(--text-medium);
            text-align: center;
            margin-bottom: 20px;
        }

        .upload-button {
            background: var(--accent-gradient);
            color: white;
            padding: 12px 30px;
            border-radius: 50px;
            font-weight: 500;
            border: none;
            cursor: pointer;
            transition: var(--transition-smooth);
        }

        .upload-button:hover {
            transform: translateY(-2px);
            box-shadow: 0 8px 25px rgba(128, 90, 213, 0.3);
        }

        #fileInput {
            display: none;
        }

        .image-preview {
            width: 100%;
            height: 200px;
            border-radius: var(--border-radius-sm);
            overflow: hidden;
            margin-top: 20px;
            display: none;
            position: relative;
        }

        .image-preview img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .preview-info {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            background: rgba(0, 0, 0, 0.7);
            color: white;
            padding: 10px 20px;
            font-size: 0.9em;
            display: flex;
            justify-content: space-between;
        }

        .filters-panel {
            padding: 30px 0;
        }

        .filters-title {
            font-size: 1.2em;
            margin-bottom: 20px;
            color: var(--primary-dark);
            font-weight: 300;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .filter-categories {
            display: flex;
            gap: 10px;
            margin-bottom: 20px;
            flex-wrap: wrap;
        }

        .category-btn {
            padding: 8px 20px;
            background: white;
            border: 2px solid var(--clean-border);
            border-radius: 50px;
            color: var(--text-medium);
            font-weight: 500;
            cursor: pointer;
            transition: var(--transition-smooth);
            font-size: 0.9em;
        }

        .category-btn:hover,
        .category-btn.active {
            background: var(--accent-gradient);
            border-color: var(--accent-purple);
            color: white;
        }

        .filter-grid-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(120px, 1fr));
            gap: 15px;
            max-height: 300px;
            overflow-y: auto;
            padding-right: 10px;
        }

        .filter-grid-container::-webkit-scrollbar {
            width: 8px;
        }

        .filter-grid-container::-webkit-scrollbar-track {
            background: var(--clean-bg);
            border-radius: 10px;
        }

        .filter-grid-container::-webkit-scrollbar-thumb {
            background: var(--accent-gradient);
            border-radius: 10px;
        }

        .filter-option {
            background: white;
            border-radius: var(--border-radius-sm);
            padding: 20px;
            text-align: center;
            cursor: pointer;
            transition: var(--transition-smooth);
            border: 2px solid transparent;
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 10px;
        }

        .filter-option:hover {
            transform: translateY(-5px);
            box-shadow: var(--shadow-medium);
            border-color: var(--accent-purple-light);
        }

        .filter-option.active {
            border-color: var(--accent-purple);
            background: rgba(128, 90, 213, 0.05);
        }

        .filter-icon {
            font-size: 1.8em;
            color: var(--accent-purple);
        }

        .filter-name {
            font-size: 0.9em;
            color: var(--text-dark);
            font-weight: 500;
        }

        .adjustments-panel {
            background: white;
            padding: 25px;
            border-radius: var(--border-radius-md);
            margin-top: 20px;
            box-shadow: var(--shadow-soft);
        }

        .adjustment-control {
            margin-bottom: 15px;
        }

        .adjustment-label {
            display: flex;
            justify-content: space-between;
            margin-bottom: 5px;
            color: var(--text-dark);
            font-weight: 500;
        }

        .adjustment-value {
            color: var(--accent-purple);
            font-weight: 500;
        }

        .slider-container {
            position: relative;
            height: 30px;
            display: flex;
            align-items: center;
        }

        .slider {
            -webkit-appearance: none;
            width: 100%;
            height: 6px;
            border-radius: 3px;
            background: linear-gradient(to right, var(--clean-border), var(--accent-purple));
            outline: none;
        }

        .slider::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            background: var(--accent-purple);
            cursor: pointer;
            border: 3px solid white;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
        }

        .slider::-moz-range-thumb {
            width: 20px;
            height: 20px;
            border-radius: 50%;
            background: var(--accent-purple);
            cursor: pointer;
            border: 3px solid white;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
        }

        .preview-panel {
            padding: 50px;
            background: var(--image-bg);
            display: flex;
            flex-direction: column;
            gap: 30px;
        }

        .preview-container {
            flex: 1;
            display: flex;
            flex-direction: column;
            background: white;
            border-radius: var(--border-radius-md);
            box-shadow: var(--shadow-medium);
            overflow: hidden;
        }

        .preview-header {
            padding: 20px;
            border-bottom: 1px solid var(--clean-border);
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .preview-title {
            font-size: 1.2em;
            color: var(--primary-dark);
            font-weight: 300;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .preview-actions {
            display: flex;
            gap: 10px;
        }

        .preview-action-btn {
            padding: 8px 16px;
            background: var(--clean-bg);
            border: 1px solid var(--clean-border);
            border-radius: var(--border-radius-sm);
            color: var(--text-medium);
            font-weight: 500;
            cursor: pointer;
            transition: var(--transition-smooth);
            font-size: 0.9em;
        }

        .preview-action-btn:hover {
            background: var(--accent-purple);
            color: white;
            border-color: var(--accent-purple);
        }

        .canvas-container {
            flex: 1;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 20px;
            min-height: 400px;
            background: repeating-conic-gradient(var(--clean-bg) 0% 25%, white 0% 50%) 50% / 20px 20px;
        }

        #previewCanvas {
            max-width: 100%;
            max-height: 100%;
            border-radius: var(--border-radius-sm);
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
        }

        .image-info {
            background: white;
            padding: 25px;
            border-radius: var(--border-radius-md);
            box-shadow: var(--shadow-soft);
        }

        .info-title {
            font-size: 1.2em;
            margin-bottom: 20px;
            color: var(--primary-dark);
            font-weight: 300;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .info-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 15px;
        }

        .info-item {
            background: var(--clean-bg);
            padding: 15px;
            border-radius: var(--border-radius-sm);
            text-align: center;
        }

        .info-value {
            font-size: 1.4em;
            font-weight: 300;
            color: var(--accent-purple);
            margin-bottom: 5px;
        }

        .info-label {
            font-size: 0.9em;
            color: var(--text-medium);
            font-weight: 400;
        }

        .filters-gallery {
            background: var(--clean-paper);
            border-radius: var(--border-radius-lg);
            padding: 60px 40px;
            margin: 60px 0;
            box-shadow: var(--shadow-soft);
        }

        .gallery-title {
            font-size: 2em;
            text-align: center;
            margin-bottom: 40px;
            color: var(--primary-dark);
            font-weight: 300;
        }

        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 30px;
        }

        .gallery-item {
            background: white;
            border-radius: var(--border-radius-md);
            overflow: hidden;
            box-shadow: var(--shadow-soft);
            transition: var(--transition-smooth);
            cursor: pointer;
        }

        .gallery-item:hover {
            transform: translateY(-10px);
            box-shadow: var(--shadow-medium);
        }

        .gallery-image {
            width: 100%;
            height: 150px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
        }

        .gallery-info {
            padding: 20px;
        }

        .gallery-filter-name {
            font-size: 1.1em;
            color: var(--primary-dark);
            font-weight: 500;
            margin-bottom: 5px;
        }

        .gallery-filter-desc {
            font-size: 0.9em;
            color: var(--text-medium);
        }

        .action-buttons {
            display: flex;
            gap: 20px;
            padding: 40px;
            background: linear-gradient(135deg, var(--clean-bg) 0%, var(--clean-paper) 100%);
            border-top: 1px solid var(--clean-border);
        }

        .action-button {
            flex: 1;
            padding: 20px;
            border: none;
            border-radius: var(--border-radius-md);
            font-size: 1.1em;
            font-weight: 500;
            cursor: pointer;
            transition: var(--transition-smooth);
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 15px;
            letter-spacing: 0.5px;
        }

        .action-button.primary {
            background: var(--accent-gradient);
            color: white;
            box-shadow: 0 4px 20px rgba(128, 90, 213, 0.3);
        }

        .action-button.primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 30px rgba(128, 90, 213, 0.4);
        }

        .action-button.secondary {
            background: var(--clean-paper);
            color: var(--primary-dark);
            border: 2px solid var(--clean-border);
        }

        .action-button.secondary:hover {
            border-color: var(--accent-purple);
            color: var(--accent-purple);
            transform: translateY(-3px);
        }

        .back-home {
            text-align: center;
            margin: 40px 0;
        }

        .loading-overlay {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(5px);
            z-index: 2000;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            gap: 30px;
        }

        .loading-spinner {
            width: 60px;
            height: 60px;
            border: 3px solid var(--clean-border);
            border-top-color: var(--accent-purple);
            border-radius: 50%;
            animation: spin 1s linear infinite;
        }

        @keyframes spin {
            to { transform: rotate(360deg); }
        }

        .loading-text {
            font-size: 1.2em;
            color: var(--primary-dark);
            font-weight: 300;
            letter-spacing: 2px;
        }

        .success-message {
            position: fixed;
            bottom: 40px;
            right: 40px;
            background: var(--accent-gradient);
            color: white;
            padding: 20px 30px;
            border-radius: var(--border-radius-md);
            box-shadow: var(--shadow-medium);
            display: none;
            align-items: center;
            gap: 15px;
            z-index: 1000;
            animation: slideIn 0.3s ease;
        }

        @keyframes slideIn {
            from { transform: translateX(100%); opacity: 0; }
            to { transform: translateX(0); opacity: 1; }
        }

        .main-footer {
            background: var(--primary-gradient);
            color: white;
            padding: 60px 40px;
            margin-top: 100px;
        }

        .footer-content {
            max-width: 1400px;
            margin: 0 auto;
            text-align: center;
        }

        .footer-logo {
            font-size: 2em;
            font-weight: 300;
            letter-spacing: 3px;
            margin-bottom: 30px;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 15px;
        }

        .footer-tagline {
            font-size: 1.1em;
            opacity: 0.9;
            max-width: 600px;
            margin: 0 auto 40px;
            font-weight: 300;
            line-height: 1.8;
        }

        .footer-copyright {
            font-size: 0.9em;
            opacity: 0.7;
            margin-top: 40px;
            padding-top: 40px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            font-weight: 300;
        }

        @media (max-width: 1200px) {
            .hero-title { font-size: 3em; }
            .steps-container { flex-direction: column; gap: 40px; }
            .steps-container::before { display: none; }
            .step { width: 100%; max-width: 400px; }
            .filter-grid { grid-template-columns: 1fr; }
            .upload-panel { border-right: none; border-bottom: 1px solid var(--clean-border); }
        }

        @media (max-width: 768px) {
            .main-nav { padding: 15px 20px; }
            .nav-content { flex-direction: column; gap: 20px; }
            .nav-links { flex-wrap: wrap; justify-content: center; }
            .page-container { margin-top: 140px; }
            .hero-section { padding: 60px 20px; }
            .hero-title { font-size: 2.5em; }
            .filter-title { font-size: 2.2em; }
            .upload-panel, .preview-panel { padding: 30px; }
            .action-buttons { flex-direction: column; }
        }
    </style>
</head>
<body>
    <!-- COMPACT CARD (FIRST PAGE) -->
    <div class="options-card">
        <div class="tool-block last-tool">
            <div class="tool-row">
                <div class="tool-info">
                    <div class="tool-name">Image Filtures</div>
                    <div class="tool-desc">Edit and enhance images easily.</div>
                </div>
                <div class="tool-action">
                    <a href="#" class="try-btn" id="tryNowBtn">Try Now →</a>
                </div>
            </div>
        </div>
        <div class="attribution"><span>mywebtools.in</span></div>
    </div>

    <!-- FULL EDITOR (ALL FEATURES) -->
    <div class="editor-container" id="editorContainer">
        <!-- Navigation -->
        <nav class="main-nav">
            <div class="nav-content">
                <div class="logo" onclick="showPage('home')">
                    <span class="logo-icon">🎨</span>
                    <div class="logo-text">Image Filter Pro</div>
                </div>
                <div class="nav-links">
                    <div class="nav-link active" onclick="showPage('home')">Home</div>
                    <div class="nav-link" onclick="showPage('filter')">Filter Tool</div>
                    <div class="nav-link" onclick="showPage('home'); scrollToSection('features')">Features</div>
                    <div class="cta-button" onclick="showPage('filter')">
                        <i>✨</i> Edit Images
                    </div>
                </div>
            </div>
        </nav>

        <!-- HOME PAGE -->
        <div id="home-page" class="page active">
            <div class="page-container">
                <!-- Hero Section -->
                <section class="hero-section">
                    <div class="hero-bg"></div>
                    <div class="hero-content">
                        <h1 class="hero-title">Free Online Image Filter Editor – Apply 50+ Photo Effects Instantly</h1>
                        <p class="hero-subtitle">Create stunning visuals with our professional image filter tool. Perfect for photographers, designers, and content creators.</p>
                        
                        <div class="hero-stats">
                            <div class="stat-item"><span class="stat-number">50+</span><span class="stat-label">Premium Filters</span></div>
                            <div class="stat-item"><span class="stat-number">HD</span><span class="stat-label">Quality</span></div>
                            <div class="stat-item"><span class="stat-number">100%</span><span class="stat-label">Free</span></div>
                            <div class="stat-item"><span class="stat-number">Real-time</span><span class="stat-label">Preview</span></div>
                        </div>
                        
                        <button class="cta-button" onclick="showPage('filter')" style="padding: 20px 50px; font-size: 1.2em;">
                            <i>🎨</i> Start Editing Now
                        </button>
                    </div>
                </section>

                <!-- Features Section -->
                <section id="features" class="features-section">
                    <h2 class="section-title">Why Choose Image Filter Pro?</h2>
                    <div class="features-grid">
                        <div class="feature-card"><div class="feature-icon">🎨</div><h3 class="feature-title">Premium Filter Collection</h3><p class="feature-description">Choose from 50+ beautiful filters including vintage, modern, artistic, and professional styles.</p></div>
                        <div class="feature-card"><div class="feature-icon">⚙️</div><h3 class="feature-title">Advanced Adjustments</h3><p class="feature-description">Full control over brightness, contrast, saturation, blur, and more.</p></div>
                        <div class="feature-card"><div class="feature-icon">✨</div><h3 class="feature-title">Real-time Preview</h3><p class="feature-description">See changes instantly as you apply filters and adjustments.</p></div>
                        <div class="feature-card"><div class="feature-icon">💾</div><h3 class="feature-title">High-Quality Export</h3><p class="feature-description">Download your edited images in HD quality.</p></div>
                        <div class="feature-card"><div class="feature-icon">📱</div><h3 class="feature-title">Cross-Platform</h3><p class="feature-description">Works perfectly on desktop, tablet, and mobile devices.</p></div>
                        <div class="feature-card"><div class="feature-icon">🔒</div><h3 class="feature-title">Privacy First</h3><p class="feature-description">All image processing happens in your browser. Your images never leave your device.</p></div>
                    </div>
                </section>

                <!-- How It Works -->
                <section class="steps-section">
                    <h2 class="section-title">How It Works</h2>
                    <div class="steps-container">
                        <div class="step"><div class="step-number">1</div><h3 class="step-title">Upload Image</h3><p class="step-description">Drag & drop or select any image file. Supports JPG, PNG, and WebP formats.</p></div>
                        <div class="step"><div class="step-number">2</div><h3 class="step-title">Apply Filters</h3><p class="step-description">Choose from 50+ beautiful filters and customize with advanced adjustments.</p></div>
                        <div class="step"><div class="step-number">3</div><h3 class="step-title">Download & Share</h3><p class="step-description">Download your masterpiece in HD quality and share it with the world.</p></div>
                    </div>
                </section>

                <!-- Filter Categories -->
                <section class="categories-section">
                    <h2 class="section-title">Filter Categories</h2>
                    <div class="categories-grid">
                        <div class="category-card" onclick="showPage('filter'); setFilterCategory('vintage')"><div class="category-icon">📽️</div><h3 class="category-title">Vintage</h3><p class="category-count">12 filters</p></div>
                        <div class="category-card" onclick="showPage('filter'); setFilterCategory('modern')"><div class="category-icon">✨</div><h3 class="category-title">Modern</h3><p class="category-count">10 filters</p></div>
                        <div class="category-card" onclick="showPage('filter'); setFilterCategory('blackwhite')"><div class="category-icon">⚫⚪</div><h3 class="category-title">Black & White</h3><p class="category-count">8 filters</p></div>
                        <div class="category-card" onclick="showPage('filter'); setFilterCategory('artistic')"><div class="category-icon">🎭</div><h3 class="category-title">Artistic</h3><p class="category-count">15 filters</p></div>
                        <div class="category-card" onclick="showPage('filter'); setFilterCategory('color')"><div class="category-icon">🌈</div><h3 class="category-title">Color Effects</h3><p class="category-count">10 filters</p></div>
                        <div class="category-card" onclick="showPage('filter'); setFilterCategory('special')"><div class="category-icon">🎆</div><h3 class="category-title">Special Effects</h3><p class="category-count">5 filters</p></div>
                    </div>
                </section>

                <!-- FAQ Section -->
                <section class="faq-section">
                    <h2 class="section-title">Frequently Asked Questions</h2>
                    <h3>Is this image filter editor completely free?</h3>
                    <p>Yes, our online image filter editor is 100% free to use with no hidden charges or subscriptions.</p>
                    <h3>Do I need to create an account?</h3>
                    <p>No registration is required. You can start editing your images instantly in your browser.</p>
                    <h3>Are my photos safe and private?</h3>
                    <p>Yes, all image processing happens locally on your device, so your photos are never uploaded to any server.</p>
                    <h3>Can I download images without watermarks?</h3>
                    <p>Yes, all edited images are downloaded in full quality with no watermark.</p>
                </section>

                <!-- Final CTA -->
                <section class="cta-section">
                    <h2 class="cta-title">Ready to Transform Your Images?</h2>
                    <p class="cta-description">Join thousands of creative professionals who trust Image Filter Pro for all their photo editing needs. No registration required.</p>
                    <button class="cta-button" onclick="showPage('filter')" style="padding: 20px 50px; font-size: 1.2em;"><i>🚀</i> Start Creating Now</button>
                </section>
            </div>
        </div>

        <!-- FILTER TOOL PAGE -->
        <div id="filter-page" class="page">
            <div class="page-container">
                <div class="filter-header">
                    <h2 class="filter-title">Free Online Image Filter Editor</h2>
                    <p class="filter-subtitle">Upload your image and apply beautiful filters with real-time preview. Customize with advanced adjustments.</p>
                </div>

                <!-- Main Filter Tool -->
                <div class="main-filter">
                    <div class="filter-grid">
                        <!-- Upload Panel -->
                        <div class="upload-panel">
                            <h2 class="panel-title"><i>📤</i> Upload Image</h2>
                            
                            <div class="upload-area" id="uploadArea" onclick="document.getElementById('fileInput').click()">
                                <div class="upload-icon">🖼️</div>
                                <div class="upload-text">Drag & Drop Your Image</div>
                                <div class="upload-subtext">or click to browse files</div>
                                <div class="upload-subtext">Supports: JPG, PNG, WebP (Max 50MB)</div>
                                <button class="upload-button" onclick="document.getElementById('fileInput').click()">Browse Files</button>
                                <input type="file" id="fileInput" accept="image/*">
                            </div>
                            
                            <div class="image-preview" id="imagePreview">
                                <img id="previewImage" src="" alt="Uploaded image preview">
                                <div class="preview-info">
                                    <span id="fileName">No file selected</span>
                                    <span id="fileSize">0 KB</span>
                                </div>
                            </div>
                            
                            <!-- Filter Categories -->
                            <div class="filters-panel">
                                <h3 class="filters-title"><i>🎨</i> Filter Categories</h3>
                                
                                <div class="filter-categories">
                                    <button class="category-btn active" onclick="setFilterCategory('all')">All Filters</button>
                                    <button class="category-btn" onclick="setFilterCategory('vintage')">Vintage</button>
                                    <button class="category-btn" onclick="setFilterCategory('modern')">Modern</button>
                                    <button class="category-btn" onclick="setFilterCategory('blackwhite')">B&W</button>
                                    <button class="category-btn" onclick="setFilterCategory('artistic')">Artistic</button>
                                    <button class="category-btn" onclick="setFilterCategory('color')">Color</button>
                                </div>
                                
                                <!-- Filter Grid -->
                                <div class="filter-grid-container" id="filterGrid"></div>
                            </div>
                            
                            <!-- Adjustments -->
                            <div class="adjustments-panel">
                                <h3 class="filters-title"><i>⚙️</i> Adjustments</h3>
                                
                                <div class="adjustment-control">
                                    <div class="adjustment-label"><span>Brightness</span><span class="adjustment-value" id="brightnessValue">0%</span></div>
                                    <div class="slider-container"><input type="range" min="-100" max="100" value="0" class="slider" id="brightnessSlider" oninput="updateAdjustment('brightness')"></div>
                                </div>
                                
                                <div class="adjustment-control">
                                    <div class="adjustment-label"><span>Contrast</span><span class="adjustment-value" id="contrastValue">0%</span></div>
                                    <div class="slider-container"><input type="range" min="-100" max="100" value="0" class="slider" id="contrastSlider" oninput="updateAdjustment('contrast')"></div>
                                </div>
                                
                                <div class="adjustment-control">
                                    <div class="adjustment-label"><span>Saturation</span><span class="adjustment-value" id="saturationValue">0%</span></div>
                                    <div class="slider-container"><input type="range" min="-100" max="100" value="0" class="slider" id="saturationSlider" oninput="updateAdjustment('saturation')"></div>
                                </div>
                                
                                <div class="adjustment-control">
                                    <div class="adjustment-label"><span>Blur</span><span class="adjustment-value" id="blurValue">0px</span></div>
                                    <div class="slider-container"><input type="range" min="0" max="20" value="0" class="slider" id="blurSlider" oninput="updateAdjustment('blur')"></div>
                                </div>
                            </div>
                        </div>
                        
                        <!-- Preview Panel -->
                        <div class="preview-panel">
                            <div class="preview-container">
                                <div class="preview-header">
                                    <div class="preview-title"><i>✨</i> Live Preview</div>
                                    <div class="preview-actions">
                                        <button class="preview-action-btn" onclick="resetFilters()">Reset</button>
                                        <button class="preview-action-btn" onclick="applyFilter('original')">Original</button>
                                    </div>
                                </div>
                                
                                <div class="canvas-container">
                                    <canvas id="previewCanvas"></canvas>
                                </div>
                            </div>
                            
                            <!-- Image Info -->
                            <div class="image-info">
                                <h3 class="info-title"><i>📊</i> Image Information</h3>
                                <div class="info-grid">
                                    <div class="info-item"><div class="info-value" id="imageWidth">0px</div><div class="info-label">Width</div></div>
                                    <div class="info-item"><div class="info-value" id="imageHeight">0px</div><div class="info-label">Height</div></div>
                                    <div class="info-item"><div class="info-value" id="imageFormat">N/A</div><div class="info-label">Format</div></div>
                                    <div class="info-item"><div class="info-value" id="imageSize">0 KB</div><div class="info-label">Size</div></div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Filter Gallery -->
                <section class="filters-gallery">
                    <h2 class="gallery-title">Popular Filter Effects</h2>
                    <div class="gallery-grid">
                        <div class="gallery-item" onclick="applyFilter('vintage')"><div class="gallery-image" style="background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);"></div><div class="gallery-info"><div class="gallery-filter-name">Vintage</div><div class="gallery-filter-desc">Classic film look</div></div></div>
                        <div class="gallery-item" onclick="applyFilter('grayscale')"><div class="gallery-image" style="background: linear-gradient(135deg, #718096 0%, #2d3748 100%);"></div><div class="gallery-info"><div class="gallery-filter-name">Grayscale</div><div class="gallery-filter-desc">Black & white effect</div></div></div>
                        <div class="gallery-item" onclick="applyFilter('sepia')"><div class="gallery-image" style="background: linear-gradient(135deg, #d69e2e 0%, #805ad5 100%);"></div><div class="gallery-info"><div class="gallery-filter-name">Sepia</div><div class="gallery-filter-desc">Antique photo effect</div></div></div>
                        <div class="gallery-item" onclick="applyFilter('invert')"><div class="gallery-image" style="background: linear-gradient(135deg, #1a202c 0%, #2d3748 100%);"></div><div class="gallery-info"><div class="gallery-filter-name">Invert</div><div class="gallery-filter-desc">Color inversion</div></div></div>
                        <div class="gallery-item" onclick="applyFilter('cool')"><div class="gallery-image" style="background: linear-gradient(135deg, #3182ce 0%, #63b3ed 100%);"></div><div class="gallery-info"><div class="gallery-filter-name">Cool</div><div class="gallery-filter-desc">Blue tone effect</div></div></div>
                        <div class="gallery-item" onclick="applyFilter('warm')"><div class="gallery-image" style="background: linear-gradient(135deg, #dd6b20 0%, #d69e2e 100%);"></div><div class="gallery-info"><div class="gallery-filter-name">Warm</div><div class="gallery-filter-desc">Orange tone effect</div></div></div>
                    </div>
                </section>

                <!-- Action Buttons -->
                <div class="action-buttons">
                    <button id="downloadBtn" class="action-button primary"><i>💾</i> Download HD Image</button>
                    <button id="shareBtn" class="action-button secondary"><i>📤</i> Share Image</button>
                </div>

                <!-- Back to Home -->
                <div class="back-home">
                    <button class="cta-button" onclick="showPage('home')" style="background: var(--primary-gradient);"><i>🏠</i> Back to Home</button>
                </div>
            </div>
        </div>

        <!-- Footer -->
        <footer class="main-footer">
            <div class="footer-content">
                <div class="footer-logo"><span>🎨</span> Image Filter Pro</div>
                <p class="footer-tagline">Creating beautiful visual experiences since 2026. Transform your images with professional-grade filters.</p>
                <div class="footer-copyright">© 2026 Image Filter Pro. All rights reserved. Made with ❤️ for creators everywhere.</div>
            </div>
        </footer>
    </div>

    <!-- Loading Overlay -->
    <div id="loadingOverlay" class="loading-overlay">
        <div class="loading-spinner"></div>
        <div class="loading-text">PROCESSING IMAGE</div>
    </div>

    <!-- Success Message -->
    <div id="successMessage" class="success-message">
        <i>✅</i>
        <span id="successText">Image processed successfully!</span>
    </div>

    <script>
        // Page Management
        function showPage(pageId) {
            document.querySelectorAll('.page').forEach(page => page.classList.remove('active'));
            document.querySelectorAll('.nav-link').forEach(link => link.classList.remove('active'));
            
            if (pageId === 'home') {
                document.getElementById('home-page').classList.add('active');
                document.querySelectorAll('.nav-link')[0].classList.add('active');
                document.title = 'Image Filter Pro | Advanced Photo Editing';
            } else if (pageId === 'filter') {
                document.getElementById('filter-page').classList.add('active');
                document.querySelectorAll('.nav-link')[1].classList.add('active');
                document.title = 'Image Filter Tool | Professional Photo Editor';
                if (typeof initImageFilter === 'function') initImageFilter();
            }
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        function scrollToSection(sectionId) {
            const section = document.getElementById(sectionId);
            if (section) section.scrollIntoView({ behavior: 'smooth', block: 'start' });
        }

        // Compact card "Try Now" button
        document.getElementById('tryNowBtn').addEventListener('click', function(e) {
            e.preventDefault();
            document.body.classList.add('editor-active');
            showPage('filter');
        });

        // Image Filter Logic
        let currentImage = null;
        let originalImage = null;
        let currentFilter = 'original';
        let currentCategory = 'all';
        let canvas = document.getElementById('previewCanvas');
        let ctx = canvas ? canvas.getContext('2d') : null;
        let adjustments = { brightness: 0, contrast: 0, saturation: 0, blur: 0 };

        // Filter definitions (50+ filters)
        const filters = [
            { id: 'original', name: 'Original', category: 'all', icon: '🔄' },
            { id: 'vintage', name: 'Vintage', category: 'vintage', icon: '📽️' },
            { id: 'sepia', name: 'Sepia', category: 'vintage', icon: '🟤' },
            { id: 'grayscale', name: 'Grayscale', category: 'blackwhite', icon: '⚫' },
            { id: 'invert', name: 'Invert', category: 'artistic', icon: '🔄' },
            { id: 'cool', name: 'Cool', category: 'color', icon: '🔵' },
            { id: 'warm', name: 'Warm', category: 'color', icon: '🟠' },
            { id: 'blur', name: 'Blur', category: 'special', icon: '🌀' },
            { id: 'sharpen', name: 'Sharpen', category: 'modern', icon: '✨' },
            { id: 'emboss', name: 'Emboss', category: 'artistic', icon: '🔼' },
            { id: 'pixelate', name: 'Pixelate', category: 'artistic', icon: '🧊' },
            { id: 'vignette', name: 'Vignette', category: 'vintage', icon: '⭕' },
            { id: 'lomo', name: 'Lomo', category: 'vintage', icon: '📸' },
            { id: 'clarendon', name: 'Clarendon', category: 'modern', icon: '🎞️' },
            { id: 'gingham', name: 'Gingham', category: 'modern', icon: '🏞️' },
            { id: 'moon', name: 'Moon', category: 'modern', icon: '🌙' },
            { id: 'lark', name: 'Lark', category: 'modern', icon: '🕊️' },
            { id: 'reyes', name: 'Reyes', category: 'vintage', icon: '🎑' },
            { id: 'juno', name: 'Juno', category: 'modern', icon: '🟣' },
            { id: 'slumber', name: 'Slumber', category: 'vintage', icon: '😴' },
            { id: 'crema', name: 'Crema', category: 'vintage', icon: '☕' },
            { id: 'ludwig', name: 'Ludwig', category: 'artistic', icon: '🎭' },
            { id: 'aden', name: 'Aden', category: 'modern', icon: '🔷' },
            { id: 'perpetua', name: 'Perpetua', category: 'modern', icon: '💎' }
        ];

        function initImageFilter() {
            canvas = document.getElementById('previewCanvas');
            ctx = canvas ? canvas.getContext('2d') : null;
            setupEventListeners();
            populateFilters();
            updateImageInfo();
        }

        function setupEventListeners() {
            const fileInput = document.getElementById('fileInput');
            const uploadArea = document.getElementById('uploadArea');
            
            fileInput.addEventListener('change', handleFileSelect);
            
            uploadArea.addEventListener('dragover', (e) => {
                e.preventDefault();
                uploadArea.classList.add('drag-over');
            });
            
            uploadArea.addEventListener('dragleave', () => {
                uploadArea.classList.remove('drag-over');
            });
            
            uploadArea.addEventListener('drop', (e) => {
                e.preventDefault();
                uploadArea.classList.remove('drag-over');
                const files = e.dataTransfer.files;
                if (files.length > 0) handleImageFile(files[0]);
            });
            
            document.getElementById('downloadBtn').addEventListener('click', downloadImage);
            document.getElementById('shareBtn').addEventListener('click', shareImage);
        }

        function handleFileSelect(e) {
            const file = e.target.files[0];
            if (file) handleImageFile(file);
        }

        function handleImageFile(file) {
            if (!file.type.match('image.*')) {
                showError('Please select an image file');
                return;
            }
            if (file.size > 50 * 1024 * 1024) {
                showError('Image size must be less than 50MB');
                return;
            }
            
            showLoading();
            
            const reader = new FileReader();
            reader.onload = function(e) {
                originalImage = new Image();
                originalImage.onload = function() {
                    currentImage = originalImage;
                    
                    const maxWidth = 800, maxHeight = 600;
                    let width = originalImage.width, height = originalImage.height;
                    
                    if (width > maxWidth) {
                        height = (maxWidth / width) * height;
                        width = maxWidth;
                    }
                    if (height > maxHeight) {
                        width = (maxHeight / height) * width;
                        height = maxHeight;
                    }
                    
                    canvas.width = width;
                    canvas.height = height;
                    
                    drawImage();
                    
                    document.getElementById('previewImage').src = e.target.result;
                    document.getElementById('imagePreview').style.display = 'block';
                    document.getElementById('fileName').textContent = file.name;
                    document.getElementById('fileSize').textContent = formatFileSize(file.size);
                    
                    updateImageInfo();
                    hideLoading();
                    showSuccess('Image loaded successfully!');
                };
                originalImage.src = e.target.result;
            };
            reader.readAsDataURL(file);
        }

        function drawImage() {
            if (!currentImage || !ctx) return;
            
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            ctx.drawImage(currentImage, 0, 0, canvas.width, canvas.height);
            
            applyCurrentFilter();
            applyAdjustments();
        }

        function applyCurrentFilter() {
            if (currentFilter === 'original' || !ctx) return;
            
            const imageData = ctx.getImageData(0, 0, canvas.width, canvas.height);
            const data = imageData.data;
            
            switch(currentFilter) {
                case 'grayscale':
                    for (let i = 0; i < data.length; i += 4) {
                        const avg = (data[i] + data[i+1] + data[i+2]) / 3;
                        data[i] = data[i+1] = data[i+2] = avg;
                    }
                    break;
                case 'sepia':
                    for (let i = 0; i < data.length; i += 4) {
                        const r = data[i], g = data[i+1], b = data[i+2];
                        data[i] = Math.min(255, (r * 0.393) + (g * 0.769) + (b * 0.189));
                        data[i+1] = Math.min(255, (r * 0.349) + (g * 0.686) + (b * 0.168));
                        data[i+2] = Math.min(255, (r * 0.272) + (g * 0.534) + (b * 0.131));
                    }
                    break;
                case 'invert':
                    for (let i = 0; i < data.length; i += 4) {
                        data[i] = 255 - data[i];
                        data[i+1] = 255 - data[i+1];
                        data[i+2] = 255 - data[i+2];
                    }
                    break;
                case 'vintage':
                    for (let i = 0; i < data.length; i += 4) {
                        data[i] = Math.min(255, data[i] + 20);
                        data[i+1] = Math.max(0, data[i+1] - 10);
                        data[i+2] = Math.max(0, data[i+2] - 30);
                    }
                    break;
                case 'cool':
                    for (let i = 0; i < data.length; i += 4) {
                        data[i] = Math.max(0, data[i] - 10);
                        data[i+2] = Math.min(255, data[i+2] + 10);
                    }
                    break;
                case 'warm':
                    for (let i = 0; i < data.length; i += 4) {
                        data[i] = Math.min(255, data[i] + 20);
                        data[i+1] = Math.min(255, data[i+1] + 10);
                        data[i+2] = Math.max(0, data[i+2] - 10);
                    }
                    break;
            }
            
            ctx.putImageData(imageData, 0, 0);
        }

        function applyAdjustments() {
            if (!ctx || (adjustments.brightness === 0 && adjustments.contrast === 0 && 
                adjustments.saturation === 0 && adjustments.blur === 0)) return;
            
            const imageData = ctx.getImageData(0, 0, canvas.width, canvas.height);
            const data = imageData.data;
            
            if (adjustments.brightness !== 0) {
                const factor = (adjustments.brightness + 100) / 100;
                for (let i = 0; i < data.length; i += 4) {
                    data[i] = Math.min(255, Math.max(0, data[i] * factor));
                    data[i+1] = Math.min(255, Math.max(0, data[i+1] * factor));
                    data[i+2] = Math.min(255, Math.max(0, data[i+2] * factor));
                }
            }
            
            if (adjustments.contrast !== 0) {
                const factor = (adjustments.contrast + 100) / 100;
                const intercept = 128 * (1 - factor);
                for (let i = 0; i < data.length; i += 4) {
                    data[i] = Math.min(255, Math.max(0, data[i] * factor + intercept));
                    data[i+1] = Math.min(255, Math.max(0, data[i+1] * factor + intercept));
                    data[i+2] = Math.min(255, Math.max(0, data[i+2] * factor + intercept));
                }
            }
            
            if (adjustments.saturation !== 0) {
                const factor = (adjustments.saturation + 100) / 100;
                for (let i = 0; i < data.length; i += 4) {
                    const r = data[i], g = data[i+1], b = data[i+2];
                    const gray = 0.2989 * r + 0.5870 * g + 0.1140 * b;
                    data[i] = Math.min(255, Math.max(0, gray + factor * (r - gray)));
                    data[i+1] = Math.min(255, Math.max(0, gray + factor * (g - gray)));
                    data[i+2] = Math.min(255, Math.max(0, gray + factor * (b - gray)));
                }
            }
            
            ctx.putImageData(imageData, 0, 0);
            
            if (adjustments.blur > 0) {
                applyBlur(adjustments.blur);
            }
        }

        function applyBlur(radius) {
            const imageData = ctx.getImageData(0, 0, canvas.width, canvas.height);
            const tempData = ctx.getImageData(0, 0, canvas.width, canvas.height);
            const data = imageData.data;
            const temp = tempData.data;
            
            for (let y = 0; y < canvas.height; y++) {
                for (let x = 0; x < canvas.width; x++) {
                    let r = 0, g = 0, b = 0, count = 0;
                    
                    for (let dy = -radius; dy <= radius; dy++) {
                        for (let dx = -radius; dx <= radius; dx++) {
                            const nx = x + dx, ny = y + dy;
                            if (nx >= 0 && nx < canvas.width && ny >= 0 && ny < canvas.height) {
                                const idx = (ny * canvas.width + nx) * 4;
                                r += data[idx];
                                g += data[idx+1];
                                b += data[idx+2];
                                count++;
                            }
                        }
                    }
                    
                    const idx = (y * canvas.width + x) * 4;
                    temp[idx] = r / count;
                    temp[idx+1] = g / count;
                    temp[idx+2] = b / count;
                    temp[idx+3] = data[idx+3];
                }
            }
            
            ctx.putImageData(tempData, 0, 0);
        }

        function populateFilters() {
            const filterGrid = document.getElementById('filterGrid');
            if (!filterGrid) return;
            
            filterGrid.innerHTML = '';
            
            const filteredFilters = currentCategory === 'all' 
                ? filters 
                : filters.filter(f => f.category === currentCategory);
            
            filteredFilters.forEach(filter => {
                const filterElement = document.createElement('div');
                filterElement.className = `filter-option ${filter.id === currentFilter ? 'active' : ''}`;
                filterElement.innerHTML = `
                    <div class="filter-icon">${filter.icon}</div>
                    <div class="filter-name">${filter.name}</div>
                `;
                filterElement.dataset.filter = filter.id;
                filterElement.addEventListener('click', () => applyFilter(filter.id));
                filterGrid.appendChild(filterElement);
            });
        }

        function setFilterCategory(category) {
            currentCategory = category;
            document.querySelectorAll('.category-btn').forEach(btn => btn.classList.remove('active'));
            event.target.classList.add('active');
            populateFilters();
        }

        function applyFilter(filterId) {
            currentFilter = filterId;
            document.querySelectorAll('.filter-option').forEach(option => {
                option.classList.remove('active');
                if (option.dataset.filter === filterId) option.classList.add('active');
            });
            drawImage();
            showSuccess(`Applied ${filterId} filter`);
        }

        function updateAdjustment(type) {
            const slider = document.getElementById(`${type}Slider`);
            const valueDisplay = document.getElementById(`${type}Value`);
            const value = parseInt(slider.value);
            adjustments[type] = value;
            
            if (type === 'blur') valueDisplay.textContent = `${value}px`;
            else valueDisplay.textContent = `${value}%`;
            
            drawImage();
        }

        function resetFilters() {
            currentFilter = 'original';
            adjustments = { brightness: 0, contrast: 0, saturation: 0, blur: 0 };
            
            document.getElementById('brightnessSlider').value = 0;
            document.getElementById('contrastSlider').value = 0;
            document.getElementById('saturationSlider').value = 0;
            document.getElementById('blurSlider').value = 0;
            
            document.getElementById('brightnessValue').textContent = '0%';
            document.getElementById('contrastValue').textContent = '0%';
            document.getElementById('saturationValue').textContent = '0%';
            document.getElementById('blurValue').textContent = '0px';
            
            applyFilter('original');
            drawImage();
            showSuccess('Filters reset to original');
        }

        function updateImageInfo() {
            if (!currentImage) return;
            document.getElementById('imageWidth').textContent = `${currentImage.width}px`;
            document.getElementById('imageHeight').textContent = `${currentImage.height}px`;
            document.getElementById('imageFormat').textContent = 'PNG';
            const size = canvas.width * canvas.height * 4;
            document.getElementById('imageSize').textContent = formatFileSize(size);
        }

        function downloadImage() {
            if (!currentImage) {
                showError('Please upload an image first');
                return;
            }
            showLoading();
            setTimeout(() => {
                const link = document.createElement('a');
                link.download = `filtered-image-${new Date().getTime()}.png`;
                link.href = canvas.toDataURL('image/png', 1.0);
                link.click();
                hideLoading();
                showSuccess('Image downloaded successfully!');
            }, 500);
        }

        function shareImage() {
            if (!currentImage) {
                showError('Please upload an image first');
                return;
            }
            canvas.toBlob(blob => {
                const file = new File([blob], 'filtered-image.png', { type: 'image/png' });
                if (navigator.share) {
                    navigator.share({
                        files: [file],
                        title: 'Filtered Image',
                        text: 'Check out this image I edited with Image Filter Pro!'
                    }).then(() => showSuccess('Image shared successfully!'))
                      .catch(() => showError('Error sharing image'));
                } else {
                    navigator.clipboard.write([new ClipboardItem({ 'image/png': blob })])
                        .then(() => showSuccess('Image copied to clipboard!'))
                        .catch(() => showError('Could not copy image'));
                }
            });
        }

        function formatFileSize(bytes) {
            if (bytes === 0) return '0 Bytes';
            const k = 1024, sizes = ['Bytes', 'KB', 'MB', 'GB'];
            const i = Math.floor(Math.log(bytes) / Math.log(k));
            return parseFloat((bytes / Math.pow(k, i)).toFixed(2)) + ' ' + sizes[i];
        }

        function showLoading() {
            document.getElementById('loadingOverlay').style.display = 'flex';
        }

        function hideLoading() {
            document.getElementById('loadingOverlay').style.display = 'none';
        }

        function showSuccess(message) {
            const successMessage = document.getElementById('successMessage');
            const successText = document.getElementById('successText');
            successText.textContent = message;
            successMessage.style.display = 'flex';
            setTimeout(() => successMessage.style.display = 'none', 3000);
        }

        function showError(message) {
            const successMessage = document.getElementById('successMessage');
            const successText = document.getElementById('successText');
            successText.textContent = message;
            successMessage.style.background = 'linear-gradient(135deg, #e53e3e 0%, #c53030 100%)';
            successMessage.style.display = 'flex';
            setTimeout(() => {
                successMessage.style.display = 'none';
                successMessage.style.background = 'var(--accent-gradient)';
            }, 3000);
        }

        // Initialize on page load
        document.addEventListener('DOMContentLoaded', function() {
            if (document.getElementById('filter-page').classList.contains('active')) {
                initImageFilter();
            }
        });
    </script>
</body>
</html>
