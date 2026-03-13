# Emaya-Languages
One Word To Say
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>இமையா — Emaya in All Languages</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #0d0d0d;
    --surface: #161616;
    --card: #1e1e1e;
    --border: rgba(255,255,255,0.07);
    --text: #f0ede6;
    --muted: #888;
    --accent: #e8c97e;
  }
  * { box-sizing: border-box; margin: 0; padding: 0; }
  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'DM Sans', sans-serif;
    min-height: 100vh;
    overflow-x: hidden;
  }

  /* Hero */
  .hero {
    text-align: center;
    padding: 72px 24px 48px;
    position: relative;
  }
  .hero::before {
    content: '';
    position: absolute;
    top: 0; left: 50%;
    transform: translateX(-50%);
    width: 600px; height: 300px;
    background: radial-gradient(ellipse at 50% 0%, rgba(232,201,126,0.12) 0%, transparent 70%);
    pointer-events: none;
  }
  .hero-label {
    font-size: 11px;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 16px;
    font-weight: 500;
  }
  .hero-name {
    font-family: 'Playfair Display', serif;
    font-size: clamp(52px, 10vw, 96px);
    font-weight: 700;
    letter-spacing: -0.02em;
    line-height: 1;
    margin-bottom: 8px;
    background: linear-gradient(135deg, #f0ede6 0%, #e8c97e 60%, #f0ede6 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }
  .hero-tamil {
    font-size: clamp(28px, 5vw, 48px);
    color: var(--accent);
    font-weight: 300;
    margin-bottom: 24px;
    opacity: 0.9;
  }
  .hero-sub {
    font-size: 14px;
    color: var(--muted);
    letter-spacing: 0.05em;
  }

  /* Sections */
  .container { max-width: 1100px; margin: 0 auto; padding: 0 20px 80px; }
  .section-title {
    font-size: 10px;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--accent);
    font-weight: 500;
    margin: 40px 0 16px;
    padding-bottom: 10px;
    border-bottom: 1px solid var(--border);
  }

  /* Grid */
  .grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(240px, 1fr));
    gap: 10px;
  }
  .card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 14px 16px;
    display: flex;
    align-items: center;
    gap: 14px;
    transition: border-color 0.2s, transform 0.2s;
    cursor: default;
  }
  .card:hover {
    transform: translateY(-2px);
    border-color: rgba(255,255,255,0.15);
  }
  .swatch {
    width: 38px; height: 38px;
    border-radius: 8px;
    flex-shrink: 0;
    opacity: 0.9;
  }
  .lang-name {
    font-size: 10px;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    color: var(--muted);
    margin-bottom: 3px;
    font-weight: 500;
  }
  .native-text {
    font-size: 19px;
    font-weight: 400;
    color: var(--text);
    line-height: 1.2;
  }
  .hex-code {
    font-size: 10px;
    color: #555;
    margin-top: 2px;
    font-family: monospace;
    letter-spacing: 0.05em;
  }

  /* Footer */
  footer {
    text-align: center;
    padding: 32px 20px;
    border-top: 1px solid var(--border);
    color: var(--muted);
    font-size: 12px;
    letter-spacing: 0.05em;
  }
  footer span { color: var(--accent); }
</style>
</head>
<body>

<div class="hero">
  <p class="hero-label">A name across all languages</p>
  <div class="hero-name">EMAYA</div>
  <div class="hero-tamil">இமையா</div>
  <p class="hero-sub">Written in 80+ world languages &amp; scripts</p>
</div>

<div class="container" id="root"></div>

<footer>Made with love for <span>இமையா</span> &mdash; Emaya</footer>

<script>
const sections = [
  { label: "South Asian languages", entries: [
    { lang: "Tamil ✓", native: "இமையா", hex: "#E63946" },
    { lang: "Hindi", native: "इमाया", hex: "#F4A261" },
    { lang: "Bengali", native: "এমায়া", hex: "#2A9D8F" },
    { lang: "Telugu", native: "ఇమాయా", hex: "#E76F51" },
    { lang: "Kannada", native: "ಇಮಾಯಾ", hex: "#264653" },
    { lang: "Malayalam", native: "ഇമായ", hex: "#6D6875" },
    { lang: "Gujarati", native: "ઇમાયા", hex: "#B5838D" },
    { lang: "Punjabi (Gurmukhi)", native: "ਇਮਾਯਾ", hex: "#E9C46A" },
    { lang: "Marathi", native: "इमाया", hex: "#606C38" },
    { lang: "Odia", native: "ଇମାୟା", hex: "#DDA15E" },
    { lang: "Sinhala", native: "ඉමායා", hex: "#81B29A" },
    { lang: "Nepali", native: "इमाया", hex: "#C77DFF" },
    { lang: "Urdu", native: "اِمایا", hex: "#BC6C25" },
    { lang: "Sindhi", native: "اِمايا", hex: "#FF9F1C" },
    { lang: "Pashto", native: "ایمایا", hex: "#CBDFBD" },
    { lang: "Dhivehi (Maldivian)", native: "އިމާޔާ", hex: "#0096C7" },
    { lang: "Sanskrit", native: "इमाया", hex: "#C77DFF" },
  ]},
  { label: "East & Southeast Asian languages", entries: [
    { lang: "Chinese (Mandarin)", native: "伊玛雅", hex: "#BB3E03" },
    { lang: "Chinese (Cantonese)", native: "伊瑪雅", hex: "#AE2012" },
    { lang: "Japanese", native: "イマヤ", hex: "#CA6702" },
    { lang: "Korean", native: "이마야", hex: "#9B2226" },
    { lang: "Thai", native: "อีมายา", hex: "#0A9396" },
    { lang: "Vietnamese", native: "Y-ma-ya", hex: "#006D77" },
    { lang: "Khmer", native: "អ៊ីម៉ាយ៉ា", hex: "#3D405B" },
    { lang: "Burmese", native: "အီမာယာ", hex: "#5C4033" },
    { lang: "Lao", native: "ອີມາຢາ", hex: "#7B2FBE" },
    { lang: "Mongolian", native: "Имааяа", hex: "#FFBE0B" },
    { lang: "Tibetan", native: "ཨི་མ་ཡ", hex: "#06D6A0" },
    { lang: "Tagalog (Filipino)", native: "Imaya", hex: "#FF6B6B" },
    { lang: "Javanese", native: "ꦲꦶꦩꦪ", hex: "#4ECDC4" },
    { lang: "Indonesian", native: "Imaya", hex: "#023047" },
    { lang: "Malay", native: "Imaya", hex: "#8ECAE6" },
  ]},
  { label: "Middle Eastern & Central Asian languages", entries: [
    { lang: "Arabic", native: "إيمايا", hex: "#005F73" },
    { lang: "Persian (Farsi)", native: "ایمایا", hex: "#94D2BD" },
    { lang: "Hebrew", native: "אימאיה", hex: "#EE9B00" },
    { lang: "Turkish", native: "İmaya", hex: "#E63946" },
    { lang: "Azerbaijani", native: "İmaya", hex: "#FF6700" },
    { lang: "Uzbek", native: "Imaya", hex: "#3A86FF" },
    { lang: "Kazakh", native: "Имая", hex: "#8338EC" },
    { lang: "Kyrgyz", native: "Имая", hex: "#F72585" },
    { lang: "Tajik", native: "Имоя", hex: "#7209B7" },
    { lang: "Turkmen", native: "Imaya", hex: "#4CC9F0" },
    { lang: "Kurdish (Kurmanji)", native: "Îmaya", hex: "#2DC653" },
  ]},
  { label: "African languages", entries: [
    { lang: "Amharic", native: "ኢማያ", hex: "#023E8A" },
    { lang: "Tigrinya", native: "እማያ", hex: "#48CAE4" },
    { lang: "Somali", native: "Imaaya", hex: "#55A630" },
    { lang: "Swahili", native: "Imaya", hex: "#219EBC" },
    { lang: "Hausa", native: "Imaya", hex: "#FFB703" },
    { lang: "Yoruba", native: "Imaya", hex: "#FB8500" },
    { lang: "Igbo", native: "Ịmaya", hex: "#38B000" },
    { lang: "Zulu", native: "Imaya", hex: "#2B9348" },
    { lang: "Xhosa", native: "Imaya", hex: "#74C69D" },
    { lang: "Shona", native: "Imaya", hex: "#D62828" },
    { lang: "Afrikaans", native: "Imaya", hex: "#F77F00" },
    { lang: "Malagasy", native: "Imaya", hex: "#9D4EDD" },
    { lang: "Wolof", native: "Imaya", hex: "#F4D35E" },
    { lang: "Twi (Akan)", native: "Imaya", hex: "#00B4D8" },
  ]},
  { label: "European languages", entries: [
    { lang: "Spanish", native: "Imaya", hex: "#EF233C" },
    { lang: "French", native: "Imaya", hex: "#4361EE" },
    { lang: "Portuguese", native: "Imaya", hex: "#7B2D8B" },
    { lang: "Italian", native: "Imaya", hex: "#38B000" },
    { lang: "German", native: "Imaya", hex: "#F77F00" },
    { lang: "Dutch", native: "Imaya", hex: "#D62839" },
    { lang: "Swedish", native: "Imaya", hex: "#006DAA" },
    { lang: "Norwegian", native: "Imaya", hex: "#EF476F" },
    { lang: "Danish", native: "Imaya", hex: "#C9184A" },
    { lang: "Finnish", native: "Imaya", hex: "#0077B6" },
    { lang: "Polish", native: "Imaya", hex: "#80B918" },
    { lang: "Czech", native: "Imaya", hex: "#FF595E" },
    { lang: "Slovak", native: "Imaya", hex: "#6A4C93" },
    { lang: "Hungarian", native: "Imaja", hex: "#1982C4" },
    { lang: "Romanian", native: "Imaya", hex: "#FFCA3A" },
    { lang: "Greek", native: "Ιμάγια", hex: "#FF006E" },
    { lang: "Russian", native: "Имайа", hex: "#7209B7" },
    { lang: "Ukrainian", native: "Імайа", hex: "#3A86FF" },
    { lang: "Serbian (Cyrillic)", native: "Имаја", hex: "#8338EC" },
    { lang: "Bulgarian", native: "Имая", hex: "#FB5607" },
    { lang: "Georgian", native: "იმაია", hex: "#F2CC8F" },
    { lang: "Armenian", native: "Էմայա", hex: "#D62828" },
    { lang: "Basque", native: "Imaya", hex: "#D00000" },
    { lang: "Welsh", native: "Imaya", hex: "#00A651" },
    { lang: "Irish (Gaelic)", native: "Imaya", hex: "#FF6B35" },
    { lang: "Albanian", native: "Imaja", hex: "#E63946" },
    { lang: "Latvian", native: "Imaja", hex: "#8D0801" },
    { lang: "Lithuanian", native: "Imaja", hex: "#007F5F" },
    { lang: "Estonian", native: "Imaja", hex: "#0072CE" },
  ]},
  { label: "Pacific & other languages", entries: [
    { lang: "Hawaiian", native: "ʻImaya", hex: "#FF9F1C" },
    { lang: "Māori", native: "Imaya", hex: "#2D6A4F" },
    { lang: "Samoan", native: "Imaya", hex: "#52B788" },
    { lang: "Tongan", native: "ʻImaya", hex: "#40916C" },
    { lang: "Fijian", native: "Imaya", hex: "#1B4332" },
  ]},
  { label: "Special & accessibility scripts", entries: [
    { lang: "Braille (Blind language)", native: "⠊⠍⠁⠽⠁", hex: "#1B4332" },
    { lang: "Sign language (ASL) — fingerspell", native: "I-M-A-Y-A", hex: "#344E41" },
    { lang: "Morse code", native: "·· –– ·– –·– ·–", hex: "#3A5A40" },
    { lang: "Latin (Classical)", native: "Imaia", hex: "#4A4E69" },
  ]},
];

const root = document.getElementById("root");
sections.forEach(({ label, entries }) => {
  const sl = document.createElement("div");
  sl.className = "section-title";
  sl.textContent = label;
  root.appendChild(sl);
  const grid = document.createElement("div");
  grid.className = "grid";
  entries.forEach(({ lang, native, hex }) => {
    const card = document.createElement("div");
    card.className = "card";
    card.innerHTML = `
      <div class="swatch" style="background:${hex}"></div>
      <div>
        <div class="lang-name">${lang}</div>
        <div class="native-text">${native}</div>
        <div class="hex-code">${hex}</div>
      </div>`;
    grid.appendChild(card);
  });
  root.appendChild(grid);
});
</script>
</body>
</html>
