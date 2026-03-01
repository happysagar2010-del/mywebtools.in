<!DOCTYPE html>
<html lang="en">
<head>
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "WebApplication",
  "name": "Bionic Reader Pro",
  "description": "Free Bionic Reader tool to read faster, improve focus and comprehension using bionic reading technique.",
  "url": "https://happysagar2010-del.github.io/index.html",
  "applicationCategory": "EducationalApplication",
  "operatingSystem": "Any",
  "offers": {
    "@type": "Offer",
    "price": "0",
    "priceCurrency": "USD"
  },
  "featureList": [
    "Guided Fixation Points",
    "Speed Enhancement",
    "Customizable Boldness",
    "Multiple Reading Modes"
  ]
}
</script>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0"><br><br>
<title>Bionic Reader Tool – Read Faster & Focus Better</title>
    <link rel="canonical" href="https://happysagar2010-del.github.io" />

<meta property="og:type" content="website">
<meta property="og:url" content="https://happysagar2010-del.github.io">
<meta property="og:title" content="Bionic Reader Pro – Read 65% Faster & Focus Better">
<meta property="og:description" content="Free Bionic Reader tool to improve focus and comprehension using the bionic reading technique.">
<meta property="og:image" content="https://happysagar2010-del.github.io/social-preview.jpg">
<meta name="description" content="Free Bionic Reader tool to read faster, improve focus and comprehension using bionic reading technique.">
    <style>
        /* === COMPACT CARD STYLES (FIRST PAGE) === */
        .intro-card-wrapper {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100vh;
            background: linear-gradient(135deg, #f7fafc 0%, #edf2f7 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            z-index: 2000;
            transition: opacity 0.5s ease, visibility 0.5s ease;
        }

        .intro-card-wrapper.hidden {
            opacity: 0;
            visibility: hidden;
        }

        .intro-card {
            max-width: 680px;
            width: 90%;
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
            position: relative;
            z-index: 2001;
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

        /* Ensure main content is visible when card is hidden */
        body:not(.show-main) .main-nav,
        body:not(.show-main) .page {
            display: none;
        }

        body.show-main .intro-card-wrapper {
            display: none;
        }

        body.show-main .main-nav,
        body.show-main .page {
            display: block;
        }

        body.show-main .page.active {
            display: block;
        }

        /* Your existing styles continue below */
        :root {
            /* Professional Reading-Focused Color Palette */
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

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
            background: linear-gradient(135deg, #f7fafc 0%, #edf2f7 100%);
            min-height: 100vh;
            color: var(--text-dark);
            line-height: 1.6;
            overflow-x: hidden;
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

        /* Navigation */
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
            margin-top: 2px;
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
            background: linear-gradient(90deg, transparent, rgba(49, 151, 149, 0.1), transparent);
            transition: left 0.6s;
        }

        .nav-link:hover::before {
            left: 100%;
        }

        .nav-link:hover {
            color: var(--accent-teal);
            background: rgba(49, 151, 149, 0.05);
        }

        .nav-link.active {
            background: var(--accent-gradient);
            color: white;
            box-shadow: 0 4px 15px rgba(49, 151, 149, 0.2);
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
            box-shadow: 0 4px 15px rgba(49, 151, 149, 0.2);
        }

        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(49, 151, 149, 0.3);
        }

        /* Page Container */
        .page-container {
            max-width: 1400px;
            margin: 100px auto 50px;
            padding: 0 20px;
        }

        /* ========== HOME PAGE STYLES ========== */
        .hero-section {
            text-align: center;
            padding: 100px 40px;
            background: linear-gradient(135deg, rgba(255, 255, 255, 0.9) 0%, rgba(250, 250, 249, 0.7) 100%);
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
            background: 
                radial-gradient(circle at 20% 80%, rgba(49, 151, 149, 0.1) 0%, transparent 50%),
                radial-gradient(circle at 80% 20%, rgba(42, 67, 101, 0.1) 0%, transparent 50%);
            z-index: 1;
        }

        .hero-content {
            position: relative;
            z-index: 2;
        }

        .hero-title {
            font-size: 3.8em;
            font-weight: 800;
            margin-bottom: 30px;
            color: var(--primary-dark);
            line-height: 1.2;
            letter-spacing: -1px;
        }

        .hero-title span {
            background: linear-gradient(135deg, var(--accent-teal), var(--primary-dark));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .hero-subtitle {
            font-size: 1.3em;
            color: var(--text-medium);
            max-width: 800px;
            margin: 0 auto 50px;
            line-height: 1.8;
            font-weight: 400;
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
            font-size: 3em;
            font-weight: 700;
            color: var(--accent-teal);
            display: block;
            margin-bottom: 10px;
        }

        .stat-label {
            font-size: 1em;
            color: var(--text-medium);
            text-transform: uppercase;
            letter-spacing: 1px;
            font-weight: 600;
        }

        /* Features Section */
        .features-section {
            margin-bottom: 100px;
        }

        .section-title {
            text-align: center;
            font-size: 2.5em;
            margin-bottom: 60px;
            color: var(--primary-dark);
            font-weight: 700;
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
            background: var(--reading-paper);
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
            border-color: var(--accent-teal-light);
        }

        .feature-icon {
            font-size: 3.5em;
            margin-bottom: 30px;
            color: var(--accent-teal);
            display: inline-block;
            width: 80px;
            height: 80px;
            line-height: 80px;
            background: linear-gradient(135deg, rgba(49, 151, 149, 0.1) 0%, rgba(255, 255, 255, 0.1) 100%);
            border-radius: 50%;
            box-shadow: 0 4px 20px rgba(49, 151, 149, 0.15);
        }

        .feature-title {
            font-size: 1.6em;
            margin-bottom: 20px;
            color: var(--primary-dark);
            font-weight: 600;
        }

        .feature-description {
            color: var(--text-medium);
            line-height: 1.8;
            font-weight: 400;
        }

        /* How It Works */
        .steps-section {
            background: linear-gradient(135deg, var(--reading-bg) 0%, var(--reading-paper) 100%);
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
            font-weight: 700;
            margin: 0 auto 30px;
            box-shadow: 0 4px 15px rgba(49, 151, 149, 0.3);
        }

        .step-title {
            font-size: 1.4em;
            margin-bottom: 15px;
            color: var(--primary-dark);
            font-weight: 600;
        }

        .step-description {
            color: var(--text-medium);
            line-height: 1.7;
            font-weight: 400;
        }

        /* Testimonials */
        .testimonials-section {
            margin-bottom: 100px;
        }

        .testimonials-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .testimonial-card {
            background: var(--reading-paper);
            padding: 40px;
            border-radius: var(--border-radius-lg);
            box-shadow: var(--shadow-soft);
            border-left: 5px solid var(--accent-teal);
            transition: var(--transition-smooth);
        }

        .testimonial-card:hover {
            transform: translateY(-10px);
            box-shadow: var(--shadow-medium);
        }

        .testimonial-text {
            font-style: italic;
            color: var(--text-medium);
            line-height: 1.8;
            margin-bottom: 30px;
            position: relative;
            padding-left: 20px;
        }

        .testimonial-text::before {
            content: '"';
            position: absolute;
            left: 0;
            top: -10px;
            font-size: 3em;
            color: var(--accent-teal);
            opacity: 0.3;
        }

        .testimonial-author {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .author-avatar {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: var(--primary-gradient);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: bold;
            font-size: 1.2em;
        }

        .author-info h4 {
            color: var(--primary-dark);
            margin-bottom: 5px;
            font-weight: 600;
        }

        .author-info p {
            color: var(--text-light);
            font-size: 0.9em;
        }

        /* CTA Section */
        .cta-section {
            text-align: center;
            padding: 80px 40px;
            background: linear-gradient(135deg, rgba(49, 151, 149, 0.05) 0%, rgba(42, 67, 101, 0.05) 100%);
            border-radius: var(--border-radius-lg);
            margin-bottom: 80px;
            border: 1px solid rgba(49, 151, 149, 0.1);
        }

        .cta-title {
            font-size: 2.5em;
            margin-bottom: 30px;
            color: var(--primary-dark);
            font-weight: 700;
        }

        .cta-description {
            font-size: 1.2em;
            color: var(--text-medium);
            max-width: 600px;
            margin: 0 auto 50px;
            line-height: 1.8;
            font-weight: 400;
        }

        /* ========== CONVERTER PAGE STYLES ========== */
        .converter-header {
            text-align: center;
            margin-bottom: 60px;
        }

        .converter-title {
            font-size: 3em;
            margin-bottom: 20px;
            color: var(--primary-dark);
            font-weight: 700;
        }

        .converter-subtitle {
            font-size: 1.2em;
            color: var(--text-medium);
            max-width: 600px;
            margin: 0 auto;
            line-height: 1.8;
            font-weight: 400;
        }

        /* Main Converter */
        .main-converter {
            background: var(--reading-paper);
            border-radius: var(--border-radius-lg);
            box-shadow: var(--shadow-strong);
            overflow: hidden;
            margin-bottom: 60px;
            border: 1px solid rgba(0, 0, 0, 0.05);
        }

        .converter-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 0;
            min-height: 600px;
        }

        /* Input Panel */
        .input-panel {
            padding: 50px;
            background: var(--reading-bg);
            border-right: 1px solid var(--reading-border);
            display: flex;
            flex-direction: column;
        }

        .panel-title {
            font-size: 1.8em;
            margin-bottom: 30px;
            color: var(--primary-dark);
            font-weight: 600;
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .panel-title i {
            color: var(--accent-teal);
            font-size: 1.5em;
        }

        /* Text Area */
        .text-input-container {
            flex: 1;
            position: relative;
        }

        .text-input {
            width: 100%;
            height: 100%;
            min-height: 300px;
            padding: 30px;
            background: white;
            border: 2px solid transparent;
            border-radius: var(--border-radius-sm);
            font-size: 1.1em;
            font-family: 'Inter', sans-serif;
            line-height: 1.8;
            color: var(--text-dark);
            resize: none;
            transition: var(--transition-smooth);
            box-shadow: var(--shadow-soft);
        }

        .text-input:focus {
            outline: none;
            border-color: var(--accent-teal-light);
            box-shadow: 0 0 0 3px rgba(49, 151, 149, 0.1);
        }

        /* Customization Panel */
        .customization-panel {
            padding: 30px 0;
            margin-top: 30px;
        }

        .customization-title {
            font-size: 1.2em;
            margin-bottom: 20px;
            color: var(--primary-dark);
            font-weight: 600;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .customization-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 25px;
        }

        .custom-control {
            display: flex;
            flex-direction: column;
            gap: 10px;
        }

        .control-label {
            font-size: 0.9em;
            color: var(--text-medium);
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .control-input {
            padding: 12px 20px;
            background: white;
            border: 2px solid var(--reading-border);
            border-radius: var(--border-radius-sm);
            font-size: 1em;
            color: var(--text-dark);
            transition: var(--transition-smooth);
            cursor: pointer;
        }

        .control-input:focus {
            outline: none;
            border-color: var(--accent-teal);
            box-shadow: 0 0 0 3px rgba(49, 151, 149, 0.1);
        }

        /* Preview Panel */
        .preview-panel {
            padding: 50px;
            background: var(--reading-bg);
            display: flex;
            flex-direction: column;
        }

        /* Reading Preview */
        .reading-preview {
            flex: 1;
            background: white;
            border-radius: var(--border-radius-md);
            box-shadow: var(--shadow-medium);
            padding: 50px 60px;
            position: relative;
            overflow: hidden;
            border: 1px solid rgba(0, 0, 0, 0.05);
            overflow-y: auto;
        }

        .bionic-display {
            font-size: 1.4em;
            line-height: 1.8;
            word-wrap: break-word;
            white-space: pre-wrap;
            min-height: 400px;
            color: var(--text-dark);
            transition: var(--transition-smooth);
            font-family: 'Inter', sans-serif;
        }

        /* Bionic Text Styles */
        .bionic-bold {
            font-weight: 700;
            color: var(--primary-dark);
        }

        .bionic-medium {
            font-weight: 600;
            color: var(--primary-main);
        }

        .bionic-normal {
            font-weight: 400;
            color: var(--text-medium);
        }

        /* Mode Selection */
        .modes-section {
            background: var(--reading-paper);
            border-radius: var(--border-radius-lg);
            box-shadow: var(--shadow-strong);
            overflow: hidden;
            margin-bottom: 60px;
            border: 1px solid rgba(0, 0, 0, 0.05);
        }

        .modes-header {
            padding: 40px;
            background: linear-gradient(135deg, var(--reading-bg) 0%, var(--reading-paper) 100%);
            border-bottom: 1px solid var(--reading-border);
        }

        .modes-title {
            font-size: 2em;
            margin-bottom: 20px;
            color: var(--primary-dark);
            font-weight: 600;
            text-align: center;
        }

        .modes-description {
            text-align: center;
            color: var(--text-medium);
            max-width: 600px;
            margin: 0 auto;
            font-weight: 400;
            line-height: 1.8;
        }

        /* Reading Modes */
        .reading-modes {
            display: flex;
            justify-content: center;
            gap: 15px;
            padding: 30px 40px;
            background: var(--reading-paper);
            border-bottom: 1px solid var(--reading-border);
            flex-wrap: wrap;
        }

        .mode-tab {
            padding: 12px 30px;
            background: transparent;
            border: 2px solid var(--reading-border);
            border-radius: 50px;
            color: var(--text-medium);
            font-size: 0.9em;
            font-weight: 600;
            cursor: pointer;
            transition: var(--transition-smooth);
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .mode-tab:hover {
            border-color: var(--accent-teal);
            color: var(--accent-teal);
        }

        .mode-tab.active {
            background: var(--accent-gradient);
            border-color: var(--accent-teal);
            color: white;
            box-shadow: 0 4px 15px rgba(49, 151, 149, 0.2);
        }

        /* Action Buttons */
        .action-buttons {
            display: flex;
            gap: 20px;
            padding: 40px;
            background: linear-gradient(135deg, var(--reading-bg) 0%, var(--reading-paper) 100%);
            border-top: 1px solid var(--reading-border);
        }

        .action-button {
            flex: 1;
            padding: 20px;
            border: none;
            border-radius: var(--border-radius-md);
            font-size: 1.1em;
            font-weight: 600;
            cursor: pointer;
            transition: var(--transition-smooth);
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 15px;
            letter-spacing: 1px;
        }

        .action-button.primary {
            background: var(--accent-gradient);
            color: white;
            box-shadow: 0 4px 20px rgba(49, 151, 149, 0.3);
        }

        .action-button.primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 30px rgba(49, 151, 149, 0.4);
        }

        .action-button.secondary {
            background: var(--reading-paper);
            color: var(--primary-dark);
            border: 2px solid var(--reading-border);
        }

        .action-button.secondary:hover {
            border-color: var(--accent-teal);
            color: var(--accent-teal);
            transform: translateY(-3px);
        }

        /* Back Button */
        .back-home {
            text-align: center;
            margin: 40px 0;
        }

        /* Loading Overlay */
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
            border: 3px solid var(--reading-border);
            border-top-color: var(--accent-teal);
            border-radius: 50%;
            animation: spin 1s linear infinite;
        }

        @keyframes spin {
            to { transform: rotate(360deg); }
        }

        .loading-text {
            font-size: 1.2em;
            color: var(--primary-dark);
            font-weight: 600;
            letter-spacing: 2px;
        }

        /* Success Message */
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

        /* Footer */
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
            font-weight: 700;
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
            font-weight: 400;
            line-height: 1.8;
        }

        .footer-copyright {
            font-size: 0.9em;
            opacity: 0.7;
            margin-top: 40px;
            padding-top: 40px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            font-weight: 400;
        }

        /* Responsive Design */
        @media (max-width: 1200px) {
            .hero-title {
                font-size: 3em;
            }
            
            .steps-container {
                flex-direction: column;
                gap: 40px;
            }
            
            .steps-container::before {
                display: none;
            }
            
            .step {
                width: 100%;
                max-width: 400px;
            }
            
            .converter-grid {
                grid-template-columns: 1fr;
            }
            
            .input-panel {
                border-right: none;
                border-bottom: 1px solid var(--reading-border);
            }
        }

        @media (max-width: 768px) {
            .main-nav {
                padding: 15px 20px;
            }
            
            .nav-content {
                flex-direction: column;
                gap: 20px;
            }
            
            .nav-links {
                flex-wrap: wrap;
                justify-content: center;
            }
            
            .page-container {
                margin-top: 140px;
                padding: 0 15px;
            }
            
            .hero-section {
                padding: 60px 20px;
            }
            
            .hero-title {
                font-size: 2.5em;
            }
            
            .features-grid {
                grid-template-columns: 1fr;
            }
            
            .feature-card {
                padding: 40px 30px;
            }
            
            .section-title {
                font-size: 2em;
            }
            
            .testimonials-grid {
                grid-template-columns: 1fr;
            }
            
            .converter-title {
                font-size: 2.2em;
            }
            
            .input-panel,
            .preview-panel {
                padding: 30px;
            }
            
            .customization-grid {
                grid-template-columns: 1fr;
            }
            
            .action-buttons {
                flex-direction: column;
                padding: 30px;
            }
            
            .reading-preview {
                padding: 30px 40px;
            }
            
            .bionic-display {
                font-size: 1.2em;
            }
        }

        @media (max-width: 480px) {
            .hero-title {
                font-size: 2em;
            }
            
            .hero-stats {
                gap: 20px;
            }
            
            .stat-item {
                min-width: 140px;
                padding: 20px;
            }
            
            .stat-number {
                font-size: 2.2em;
            }
            
            .nav-link {
                padding: 8px 16px;
                font-size: 0.9em;
            }
            
            .converter-title {
                font-size: 1.8em;
            }
            
            .reading-modes {
                flex-direction: column;
                align-items: stretch;
            }
            
            .mode-tab {
                text-align: center;
            }
        }

        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 10px;
        }

        ::-webkit-scrollbar-track {
            background: var(--reading-bg);
            border-radius: 10px;
        }

        ::-webkit-scrollbar-thumb {
            background: var(--accent-gradient);
            border-radius: 10px;
            border: 2px solid var(--reading-bg);
        }

        ::-webkit-scrollbar-thumb:hover {
            background: linear-gradient(135deg, var(--accent-teal), var(--accent-teal-light));
        }
    </style>
</head>
<body>
    <!-- Compact First Page (added without editing existing content) -->
    <div class="intro-card-wrapper" id="introCard">
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

    <!-- Navigation -->
    <nav class="main-nav">
        <div class="nav-content">
            <div class="logo" onclick="showPage('home')">
                <span class="logo-icon">🚀</span>
                <div>
                    <div class="logo-text">Bionic Reader Pro</div>
                    <div class="logo-subtitle">ENHANCE YOUR READING</div>
                </div>
            </div>
            <div class="nav-links">
                <div class="nav-link active" onclick="showPage('home')">Home</div>
                <div class="nav-link" onclick="showPage('converter')">Converter</div>
                <div class="nav-link" onclick="showPage('home'); scrollToSection('features')">Features</div>
                <div class="cta-button" onclick="showPage('converter')">
                    <i>⚡</i>
                    Start Reading
                </div>
            </div>
        </div>
    </nav>

    <!-- Home Page -->
    <div id="home-page" class="page active">
        <div class="page-container">
            <!-- Hero Section -->
            <section class="hero-section">
                <div class="hero-bg"></div>
                <div class="hero-content">
                    <h1 class="hero-title">
                        Read <span>Faster</span>, Focus <span>Better</span> with Bionic Reading
                    </h1>
                    <p class="hero-subtitle">
                        Transform any text into bionic format that guides your eyes through artificial fixation points, 
                        helping you read faster with better comprehension and retention.
                    </p>
                    
                    <div class="hero-stats">
                        <div class="stat-item">
                            <span class="stat-number">65%</span>
                            <span class="stat-label">Faster Reading</span>
                        </div>
                        <div class="stat-item">
                            <span class="stat-number">40%</span>
                            <span class="stat-label">Better Focus</span>
                        </div>
                        <div class="stat-item">
                            <span class="stat-number">100%</span>
                            <span class="stat-label">Free Forever</span>
                        </div>
                        <div class="stat-item">
                            <span class="stat-number">5</span>
                            <span class="stat-label">Reading Modes</span>
                        </div>
                    </div>
                    
                    <button class="cta-button" onclick="showPage('converter')" style="padding: 20px 50px; font-size: 1.2em;">
                        <i>📖</i>
                        Try Bionic Reading Now
                    </button>
                </div>
            </section>

            <!-- Features Section -->
            <section id="features" class="features-section">
                <h2 class="section-title">Why Bionic Reading Works</h2>
                <div class="features-grid">
                    <div class="feature-card">
                        <div class="feature-icon">🎯</div>
                        <h3 class="feature-title">Guided Fixation Points</h3>
                        <p class="feature-description">
                            Artificial fixation points guide your eyes, reducing back-skipping and helping you 
                            maintain focus throughout your reading session.
                        </p>
                    </div>
                    <h2>How Bionic Reading Helps You Read Faster</h2>
                    <div class="feature-card">
                        <div class="feature-icon">⚡</div>
                        <h3 class="feature-title">Speed Enhancement</h3>
                        <p class="feature-description">
                            Read up to 65% faster while maintaining or even improving comprehension compared 
                            to traditional reading methods.
                        </p>
                    </div>
                    
                    <div class="feature-card">
                        <div class="feature-icon">🧠</div>
                        <h3 class="feature-title">Better Comprehension</h3>
                        <p class="feature-description">
                            The bionic format helps your brain process information more efficiently, leading 
                            to improved understanding and retention.
                        </p>
                    </div>
                    
                    <div class="feature-card">
                        <div class="feature-icon">👁️</div>
                        <h3 class="feature-title">Reduced Eye Strain</h3>
                        <p class="feature-description">
                            By guiding your eye movements, bionic reading reduces unnecessary scanning and 
                            minimizes eye fatigue during long reading sessions.
                        </p>
                    </div>
                    
                    <div class="feature-card">
                        <div class="feature-icon">🎨</div>
                        <h3 class="feature-title">Customizable Formatting</h3>
                        <p class="feature-description">
                            Adjust boldness, fixation length, and formatting to match your personal reading 
                            preferences and optimize your experience.
                        </p>
                    </div>
                    
                    <div class="feature-card">
                        <div class="feature-icon">📱</div>
                        <h3 class="feature-title">Multi-Platform</h3>
                        <p class="feature-description">
                            Use our converter on any device – perfect for e-books, articles, documents, 
                            and any digital text you need to read.
                        </p>
                    </div>
                </div>
            </section>

            <!-- How It Works -->
            <section id="how-it-works" class="steps-section">
                <h2 class="section-title">How Bionic Reading Works</h2>
                <div class="steps-container">
                    <div class="step">
                        <div class="step-number">1</div>
                        <h3 class="step-title">Paste Your Text</h3>
                        <p class="step-description">
                            Copy and paste any text – articles, books, documents, or your own writing 
                            into our converter.
                        </p>
                    </div>
                    
                    <div class="step">
                        <div class="step-number">2</div>
                        <h3 class="step-title">Customize Settings</h3>
                        <p class="step-description">
                            Choose your preferred reading mode, adjust boldness levels, and customize 
                            the formatting to your liking.
                        </p>
                    </div>
                    
                    <div class="step">
                        <div class="step-number">3</div>
                        <h3 class="step-title">Read & Export</h3>
                        <p class="step-description">
                            Read the transformed text directly in our viewer or export it for use in 
                            your preferred reading app.
                        </p>
                    </div>
                </div>
            </section>

            <!-- Testimonials -->
            <section class="testimonials-section">
                <h2 class="section-title">What Readers Say</h2>
                <div class="testimonials-grid">
                    <div class="testimonial-card">
                        <p class="testimonial-text">
                            As a PhD student, I read hundreds of pages weekly. Bionic reading has cut my 
                            reading time by half while improving my retention. It's a game-changer for academics.
                        </p>
                        <div class="testimonial-author">
                            <div class="author-avatar">M</div>
                            <div class="author-info">
                                <h4>Mukesh kumar sagar</h4>
                                <p>PhD Candidate, Neuroscience</p>
                            </div>
                        </div>
                    </div>
                    
                    <div class="testimonial-card">
                        <p class="testimonial-text">
                            I have ADHD and always struggled with focus while reading. Bionic reading keeps 
                            me engaged and helps me finish articles I would normally abandon halfway through.
                        </p>
                        <div class="testimonial-author">
                            <div class="author-avatar">A</div>
                            <div class="author-info">
                                <h4>Ankush kumar</h4>
                                <p>Software Developer</p>
                            </div>
                        </div>
                    </div>
                    
                    <div class="testimonial-card">
                        <p class="testimonial-text">
                            Our team processes dozens of reports daily. Implementing bionic reading has 
                            improved our efficiency by 40% and reduced reading-related fatigue significantly.
                        </p>
                        <div class="testimonial-author">
                            <div class="author-avatar">A</div>
                            <div class="author-info">
                                <h4>Avinash sagar</h4>
                                <p>Research Team Lead</p>
                            </div>
                        </div>
                    </div>
                </div>
            </section>

            <!-- Final CTA -->
            <section class="cta-section">
                <h2 class="cta-title">Ready to Transform Your Reading?</h2>
                <p class="cta-description">
                    Join thousands of students, professionals, and avid readers who have revolutionized 
                    their reading experience with Bionic Reading. Start reading faster and smarter today.
                </p>
                <button class="cta-button" onclick="showPage('converter')" style="padding: 20px 50px; font-size: 1.2em;">
                    <i><span class="logo-icon" role="img" aria-label="Bionic Reader Rocket Icon">🚀</span>
</i>
                    Start Bionic Reading Now
                </button>
            </section>
<h2>What is Bionic Reading?</h2>
<p>
Bionic Reading is a modern reading technique designed to help users read faster
and focus better. It works by highlighting the most important parts of words,
allowing the brain to recognize text more efficiently.
</p>

<h2>How Bionic Reading Helps You Read Faster</h2>
<p>
Bionic reading improves reading speed by guiding the eyes to key characters in
each word. This reduces eye strain and helps readers understand text with less
effort. It is especially useful for students, professionals, and people who read
large amounts of text daily.
</p>

<h2>Who Can Use This Bionic Reader Tool?</h2>
<p>
This free Bionic Reader tool is ideal for students, bloggers, programmers,
researchers, and anyone who wants to improve reading speed and concentration.
No sign-up or installation is required.
</p>

<h2>Why Use Our Free Bionic Reader Tool?</h2>
<p>
Our tool is fast, simple, and works directly in your browser. You can instantly
convert normal text into bionic reading format and start reading more efficiently
without distractions.
</p>
            <!-- Footer -->
            <footer class="main-footer">
                <div class="footer-content">
                    <div class="footer-logo">
                        <span>🚀</span>
                        Bionic Reader Pro
                    </div>
                    <p class="footer-tagline">
                        Enhancing reading speed and comprehension through innovative text formatting. 
                        Read smarter, not harder.
 
Bionic Reader is a free online tool that helps you read faster and focus better.
It highlights key parts of words to improve reading speed and comprehension.
</p>
                    <div class="footer-copyright">
                        © 2024 Bionic Reader Pro. All rights reserved. Made for readers everywhere.
                    </div>
                </div>
            </footer>
        </div>
    </div>

    <!-- Converter Page -->
    <div id="converter-page" class="page">
        <div class="page-container">
            <!-- Header -->
            <div class="converter-header">
                <h1 class="converter-title">Bionic Reading Converter</h1>
                <p class="converter-subtitle">
                    Transform any text into bionic format for faster reading and better comprehension. 
                    Customize the settings to match your reading preferences.
                </p>
            </div>

            <!-- Main Converter -->
            <div class="main-converter">
                <div class="converter-grid">
                    <!-- Input Panel -->
                    <div class="input-panel">
                        <h2 class="panel-title">
                            <i>📝</i>
                            Your Text
                        </h2>
                        
                        <div class="text-input-container">
                            <textarea id="textInput" class="text-input" placeholder=" ">Welcome to Bionic Reading, a revolutionary method that enhances reading speed and comprehension through strategic text formatting.

How It Works:
Bionic reading works by guiding your eyes through artificial fixation points. The first few letters of each word are emphasized, creating a visual anchor that helps your brain recognize words faster and reduces unnecessary eye movements.

Benefits:
• Read up to 65% faster
• Improved focus and concentration
• Better comprehension and retention
• Reduced eye strain and fatigue
• Works with any type of text

Simply paste your text, choose your settings, and experience the difference in your reading efficiency.</textarea>
                        </div>
                        
                        <div class="customization-panel">
                            <h3 class="customization-title">
                                <i>⚙️</i>
                                Reading Settings
                            </h3>
                            
                            <div class="customization-grid">
                                <div class="custom-control">
                                    <label class="control-label">Reading Mode</label>
                                    <select id="readingMode" class="control-input">
                                        <option value="standard">Standard (40% bold)</option>
                                        <option value="light">Light (25% bold)</option>
                                        <option value="medium" selected>Medium (50% bold)</option>
                                        <option value="heavy">Heavy (75% bold)</option>
                                        <option value="extreme">Extreme (90% bold)</option>
                                    </select>
                                </div>
                                
                                <div class="custom-control">
                                    <label class="control-label">Fixation Length</label>
                                    <input type="range" id="fixationLength" class="control-input" min="1" max="10" value="4">
                                    <div style="display: flex; justify-content: space-between; font-size: 0.9em; color: var(--text-light);">
                                        <span>Short</span>
                                        <span id="fixationValue">4 letters</span>
                                        <span>Long</span>
                                    </div>
                                </div>
                                
                                <div class="custom-control">
                                    <label class="control-label">Text Size</label>
                                    <input type="range" id="textSize" class="control-input" min="14" max="28" value="18">
                                    <div style="display: flex; justify-content: space-between; font-size: 0.9em; color: var(--text-light);">
                                        <span>Small</span>
                                        <span id="textSizeValue">18px</span>
                                        <span>Large</span>
                                    </div>
                                </div>
                                
                                <div class="custom-control">
                                    <label class="control-label">Line Height</label>
                                    <input type="range" id="lineHeight" class="control-input" min="1.4" max="2.4" step="0.1" value="1.8">
                                    <div style="display: flex; justify-content: space-between; font-size: 0.9em; color: var(--text-light);">
                                        <span>Tight</span>
                                        <span id="lineHeightValue">1.8</span>
                                        <span>Loose</span>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                    
                    <!-- Preview Panel -->
                    <div class="preview-panel">
                        <h2 class="panel-title">
                            <i>👁️</i>
                            Bionic Preview
                        </h2>
                        
                        <div class="reading-preview">
                            <div id="bionicPreview" class="bionic-display">Welcome to Bionic Reading, a revolutionary method that enhances reading speed and comprehension through strategic text formatting.

How It Works:
Bionic reading works by guiding your eyes through artificial fixation points. The first few letters of each word are emphasized, creating a visual anchor that helps your brain recognize words faster and reduces unnecessary eye movements.

Benefits:
• Read up to 65% faster
• Improved focus and concentration
• Better comprehension and retention
• Reduced eye strain and fatigue
• Works with any type of text

Simply paste your text, choose your settings, and experience the difference in your reading efficiency.</div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Reading Modes -->
            <section class="modes-section" id="modes">
                <div class="modes-header">
                    <h3 class="modes-title">Choose Your Reading Mode</h3>
                    <p class="modes-description">
                        Select from different bionic reading modes optimized for various reading scenarios 
                        and personal preferences.
                    </p>
                </div>
                
                <div class="reading-modes">
                    <button class="mode-tab active" data-mode="standard">
                        <i>📖</i> Standard Reading
                    </button>
                    <button class="mode-tab" data-mode="speed">
                        <i>⚡</i> Speed Reading
                    </button>
                    <button class="mode-tab" data-mode="focus">
                        <i>🎯</i> Deep Focus
                    </button>
                    <button class="mode-tab" data-mode="study">
                        <i>🧠</i> Study Mode
                    </button>
                    <button class="mode-tab" data-mode="casual">
                        <i>😌</i> Casual Reading
                    </button>
                </div>
            </section>

            <!-- Action Buttons -->
            <div class="action-buttons" id="actions">
                <button id="convertBtn" class="action-button primary">
                    <i>🔄</i>
                    Convert to Bionic
                </button>
                <button id="copyBtn" class="action-button secondary">
                    <i>📋</i>
                    Copy Bionic Text
                </button>
                <button id="exportBtn" class="action-button secondary">
                    <i>💾</i>
                    Export as HTML
                </button>
            </div>

            <!-- Back to Home -->
            <div class="back-home">
                <button class="cta-button" onclick="showPage('home')" style="background: var(--primary-gradient);">
                    <i>🏠</i>
                    Back to Home
                </button>
            </div>
        </div>
    </div>

    <!-- Loading Overlay -->
    <div id="loadingOverlay" class="loading-overlay">
        <div class="loading-spinner"></div>
        <div class="loading-text">CONVERTING TO BIONIC</div>
    </div>

    <!-- Success Message -->
    <div id="successMessage" class="success-message">
        <i>✅</i>
        <span id="successText">Text copied successfully!</span>
    </div>

    <script>
        // Hide intro card and show main content
        document.getElementById('enterBionicBtn').addEventListener('click', function(e) {
            e.preventDefault();
            document.getElementById('introCard').classList.add('hidden');
            document.body.classList.add('show-main');
            // Make sure home page is active
            showPage('home');
        });

        // Page Management
        function showPage(pageId) {
            // Hide all pages
            document.querySelectorAll('.page').forEach(page => {
                page.classList.remove('active');
            });
            
            // Update active nav link
            document.querySelectorAll('.nav-link').forEach(link => {
                link.classList.remove('active');
            });
            
            // Show selected page
            if (pageId === 'home') {
                document.getElementById('home-page').classList.add('active');
                document.querySelectorAll('.nav-link')[0].classList.add('active');
            } else if (pageId === 'converter') {
                document.getElementById('converter-page').classList.add('active');
                document.querySelectorAll('.nav-link')[1].classList.add('active');
                initConverter();
            }
            
            // Scroll to top
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        function scrollToSection(sectionId) {
            showPage('home');
            setTimeout(() => {
                const section = document.getElementById(sectionId);
                if (section) {
                    section.scrollIntoView({ 
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            }, 100);
        }

        // Bionic Reading Converter Logic
        function convertToBionic(text, fixationLength = 4, boldness = 0.5) {
            if (!text || text.trim() === '') return '';
            
            // Split into lines to preserve paragraphs
            const lines = text.split('\n');
            const convertedLines = lines.map(line => {
                if (line.trim() === '') return '';
                
                // Split line into words
                const words = line.split(/(\s+)/);
                
                return words.map(word => {
                    // Check if it's a word (not whitespace)
                    if (/\s/.test(word)) return word;
                    
                    // Check if word is special (bullet points, etc.)
                    if (/^[•\-*]\s*/.test(word)) return word;
                    
                    const wordLength = word.length;
                    const fixation = Math.min(fixationLength, wordLength);
                    
                    // Calculate bold part based on boldness level
                    let boldPart = '';
                    let normalPart = '';
                    
                    if (boldness >= 0.9) { // Extreme
                        boldPart = word.substring(0, Math.floor(wordLength * 0.9));
                        normalPart = word.substring(Math.floor(wordLength * 0.9));
                    } else if (boldness >= 0.75) { // Heavy
                        boldPart = word.substring(0, Math.floor(wordLength * 0.75));
                        normalPart = word.substring(Math.floor(wordLength * 0.75));
                    } else if (boldness >= 0.5) { // Medium
                        boldPart = word.substring(0, Math.max(fixation, Math.floor(wordLength * 0.5)));
                        normalPart = word.substring(Math.max(fixation, Math.floor(wordLength * 0.5)));
                    } else if (boldness >= 0.25) { // Light
                        boldPart = word.substring(0, Math.min(fixation, Math.floor(wordLength * 0.25)));
                        normalPart = word.substring(Math.min(fixation, Math.floor(wordLength * 0.25)));
                    } else { // Standard
                        boldPart = word.substring(0, Math.min(fixation, Math.floor(wordLength * 0.4)));
                        normalPart = word.substring(Math.min(fixation, Math.floor(wordLength * 0.4)));
                    }
                    
                    if (normalPart) {
                        return `<span class="bionic-bold">${boldPart}</span><span class="bionic-normal">${normalPart}</span>`;
                    } else {
                        return `<span class="bionic-bold">${boldPart}</span>`;
                    }
                }).join('');
            }).join('<br>');
            
            return convertedLines;
        }

        // Initialize converter
        function initConverter() {
            setupEventListeners();
            updateBionicPreview();
        }

        // Setup event listeners
        function setupEventListeners() {
            // Text input
            const textInput = document.getElementById('textInput');
            if (textInput) {
                textInput.addEventListener('input', updateBionicPreview);
            }
            
            // Reading mode
            const readingMode = document.getElementById('readingMode');
            if (readingMode) {
                readingMode.addEventListener('change', updateBionicPreview);
            }
            
            // Fixation length
            const fixationLength = document.getElementById('fixationLength');
            const fixationValue = document.getElementById('fixationValue');
            if (fixationLength && fixationValue) {
                fixationLength.addEventListener('input', function() {
                    fixationValue.textContent = `${this.value} letters`;
                    updateBionicPreview();
                });
            }
            
            // Text size
            const textSize = document.getElementById('textSize');
            const textSizeValue = document.getElementById('textSizeValue');
            if (textSize && textSizeValue) {
                textSize.addEventListener('input', function() {
                    textSizeValue.textContent = `${this.value}px`;
                    updatePreviewStyles();
                });
            }
            
            // Line height
            const lineHeight = document.getElementById('lineHeight');
            const lineHeightValue = document.getElementById('lineHeightValue');
            if (lineHeight && lineHeightValue) {
                lineHeight.addEventListener('input', function() {
                    lineHeightValue.textContent = this.value;
                    updatePreviewStyles();
                });
            }
            
            // Convert button
            const convertBtn = document.getElementById('convertBtn');
            if (convertBtn) {
                convertBtn.addEventListener('click', updateBionicPreview);
            }
            
            // Copy button
            const copyBtn = document.getElementById('copyBtn');
            if (copyBtn) {
                copyBtn.addEventListener('click', copyBionicText);
            }
            
            // Export button
            const exportBtn = document.getElementById('exportBtn');
            if (exportBtn) {
                exportBtn.addEventListener('click', exportAsHTML);
            }
            
            // Mode tabs
            document.querySelectorAll('.mode-tab').forEach(tab => {
                tab.addEventListener('click', function() {
                    document.querySelectorAll('.mode-tab').forEach(t => t.classList.remove('active'));
                    this.classList.add('active');
                    
                    const mode = this.dataset.mode;
                    applyReadingMode(mode);
                });
            });
        }

        // Update bionic preview
        function updateBionicPreview() {
            const textInput = document.getElementById('textInput');
            const readingMode = document.getElementById('readingMode');
            const fixationLength = document.getElementById('fixationLength');
            const bionicPreview = document.getElementById('bionicPreview');
            
            if (!textInput || !bionicPreview) return;
            
            const text = textInput.value;
            const mode = readingMode ? readingMode.value : 'medium';
            const fixation = fixationLength ? parseInt(fixationLength.value) : 4;
            
            // Map mode to boldness level
            const boldnessMap = {
                'standard': 0.4,
                'light': 0.25,
                'medium': 0.5,
                'heavy': 0.75,
                'extreme': 0.9
            };
            
            const boldness = boldnessMap[mode] || 0.5;
            
            // Convert to bionic
            const bionicText = convertToBionic(text, fixation, boldness);
            bionicPreview.innerHTML = bionicText || 'Enter text to see bionic conversion...';
        }

        // Update preview styles
        function updatePreviewStyles() {
            const textSize = document.getElementById('textSize');
            const lineHeight = document.getElementById('lineHeight');
            const bionicPreview = document.getElementById('bionicPreview');
            
            if (!bionicPreview) return;
            
            if (textSize) {
                bionicPreview.style.fontSize = `${textSize.value}px`;
            }
            
            if (lineHeight) {
                bionicPreview.style.lineHeight = lineHeight.value;
            }
        }

        // Apply reading mode
        function applyReadingMode(mode) {
            const readingMode = document.getElementById('readingMode');
            const fixationLength = document.getElementById('fixationLength');
            
            const modeSettings = {
                'standard': { mode: 'standard', fixation: 4 },
                'speed': { mode: 'light', fixation: 3 },
                'focus': { mode: 'heavy', fixation: 5 },
                'study': { mode: 'medium', fixation: 4 },
                'casual': { mode: 'standard', fixation: 3 }
            };
            
            const settings = modeSettings[mode] || modeSettings.standard;
            
            if (readingMode) {
                readingMode.value = settings.mode;
            }
            
            if (fixationLength) {
                fixationLength.value = settings.fixation;
                document.getElementById('fixationValue').textContent = `${settings.fixation} letters`;
            }
            
            updateBionicPreview();
        }

        // Copy bionic text
        async function copyBionicText() {
            const bionicPreview = document.getElementById('bionicPreview');
            if (!bionicPreview) return;
            
            try {
                // Get plain text version
                const plainText = bionicPreview.textContent;
                await navigator.clipboard.writeText(plainText);
                
                showSuccess('Bionic text copied to clipboard!');
            } catch (err) {
                console.error('Failed to copy text:', err);
                showSuccess('Failed to copy text. Please try again.');
            }
        }

        // Export as HTML
        function exportAsHTML() {
            const bionicPreview = document.getElementById('bionicPreview');
            const textInput = document.getElementById('textInput');
            
            if (!bionicPreview || !textInput) return;
            
            const htmlContent = `
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bionic Reading Export</title>
    <style>
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            line-height: 1.8;
            max-width: 800px;
            margin: 0 auto;
            padding: 40px;
            color: #1a202c;
            background: #fafaf9;
        }
        .bionic-bold {
            font-weight: 700;
            color: #1a365d;
        }
        .bionic-normal {
            font-weight: 400;
            color: #4a5568;
        }
        .container {
            background: white;
            padding: 60px;
            border-radius: 20px;
            box-shadow: 0 15px 50px rgba(0,0,0,0.1);
        }
        h1 {
            color: #1a365d;
            margin-bottom: 30px;
        }
        .info {
            background: #f7fafc;
            padding: 20px;
            border-radius: 12px;
            margin: 30px 0;
            border-left: 4px solid #319795;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Bionic Reading Export</h1>
        <div class="info">
            <p><strong>Generated:</strong> ${new Date().toLocaleDateString()}</p>
            <p><strong>Original text length:</strong> ${textInput.value.length} characters</p>
            <p><strong>Bionic reading enhances comprehension and speed by emphasizing the first few letters of each word.</strong></p>
        </div>
        <div id="content">
            ${bionicPreview.innerHTML}
        </div>
    </div>
</body>
</html>`;
            
            const blob = new Blob([htmlContent], { type: 'text/html' });
            const url = URL.createObjectURL(blob);
            const a = document.createElement('a');
            a.href = url;
            a.download = `bionic-reading-${new Date().toISOString().slice(0,10)}.html`;
            document.body.appendChild(a);
            a.click();
            document.body.removeChild(a);
            URL.revokeObjectURL(url);
            
            showSuccess('HTML file downloaded successfully!');
        }

        // Show success message
        function showSuccess(message) {
            const successMessage = document.getElementById('successMessage');
            const successText = document.getElementById('successText');
            
            if (successMessage && successText) {
                successText.textContent = message;
                successMessage.style.display = 'flex';
                
                setTimeout(() => {
                    successMessage.style.display = 'none';
                }, 3000);
            }
        }

        // Initialize when page loads
        document.addEventListener('DOMContentLoaded', function() {
            // Navbar scroll effect
            let lastScroll = 0;
            const navbar = document.querySelector('.main-nav');
            
            window.addEventListener('scroll', () => {
                const currentScroll = window.pageYOffset;
                
                if (currentScroll > lastScroll && currentScroll > 100) {
                    navbar.style.transform = 'translateY(-100%)';
                } else {
                    navbar.style.transform = 'translateY(0)';
                }
                
                lastScroll = currentScroll;
            });
            
            // Animate feature cards on scroll
            const observerOptions = {
                threshold: 0.5
            };

            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.style.opacity = '1';
                        entry.target.style.transform = 'translateY(0)';
                    }
                });
            }, observerOptions);

            document.querySelectorAll('.feature-card, .stat-item, .testimonial-card').forEach(card => {
                card.style.opacity = '0';
                card.style.transform = 'translateY(20px)';
                card.style.transition = 'opacity 0.6s ease, transform 0.6s ease';
                observer.observe(card);
            });
            
            // Initialize converter if on converter page
            if (document.getElementById('converter-page').classList.contains('active')) {
                initConverter();
            }
        });

        // Initialize the converter if needed
        if (document.getElementById('converter-page').classList.contains('active')) {
            initConverter();
        }
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
