<?xml version="1.0" encoding="utf-8"?>
<svg xmlns="http://www.w3.org/2000/svg" width="1200" height="320" viewBox="0 0 1200 320" preserveAspectRatio="xMidYMid slice">
  <defs>
    <!-- Background gradient -->
    <linearGradient id="bg" x1="0" x2="1" y1="0" y2="1">
      <stop offset="0%" stop-color="#020111"/>
      <stop offset="40%" stop-color="#0d1b2a"/>
      <stop offset="100%" stop-color="#071029"/>
    </linearGradient>

    <!-- Neon text glow filter -->
    <filter id="neon">
      <feGaussianBlur stdDeviation="3" result="coloredBlur"/>
      <feMerge>
        <feMergeNode in="coloredBlur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>

    <!-- Soft vignette -->
    <radialGradient id="vignette" cx="50%" cy="40%" r="80%">
      <stop offset="0%" stop-color="rgba(255,255,255,0)"/>
      <stop offset="100%" stop-color="rgba(0,0,0,0.45)"/>
    </radialGradient>

    <!-- Star shape -->
    <symbol id="star" viewBox="-1 -1 2 2">
      <circle cx="0" cy="0" r="1" />
    </symbol>

    <!-- Grid path for futuristic lines -->
    <pattern id="grid" width="120" height="120" patternUnits="userSpaceOnUse">
      <path d="M0 100 L120 100" stroke="rgba(255,255,255,0.03)" stroke-width="1"/>
      <path d="M60 0 L60 120" stroke="rgba(255,255,255,0.02)" stroke-width="1"/>
    </pattern>
  </defs>

  <!-- background -->
  <rect width="1200" height="320" fill="url(#bg)"/>
  <rect width="1200" height="320" fill="url(#vignette)" />

  <!-- moving faint grid -->
  <g opacity="0.55">
    <rect width="1200" height="320" fill="url(#grid)">
      <animateTransform attributeName="transform"
                        type="translate"
                        from="0 0" to="-240 0"
                        dur="18s"
                        repeatCount="indefinite" />
    </rect>
  </g>

  <!-- animated stars layer (parallax) -->
  <g id="stars" fill="#9be7ff" opacity="0.9">
    <!-- multiple stars with different speeds -->
    <use href="#star" x="80"  y="40"  width="2.2" height="2.2" opacity="0.9">
      <animate attributeName="cx" values="80; -40" dur="28s" repeatCount="indefinite"/>
    </use>
    <use href="#star" x="420" y="20"  width="2.6" height="2.6" opacity="0.8">
      <animate attributeName="x" from="420" to="1260" dur="34s" repeatCount="indefinite"/>
    </use>
    <use href="#star" x="900" y="60" width="1.6" height="1.6" opacity="0.7">
      <animate attributeName="x" from="900" to="-180" dur="22s" repeatCount="indefinite"/>
    </use>
    <use href="#star" x="1100" y="140" width="1.2" height="1.2" opacity="0.6">
      <animate attributeName="x" from="1100" to="-100" dur="40s" repeatCount="indefinite"/>
    </use>
    <use href="#star" x="260" y="200" width="1.8" height="1.8" opacity="0.85">
      <animate attributeName="x" from="260" to="1400" dur="30s" repeatCount="indefinite"/>
    </use>
  </g>

  <!-- animated neon arcs (swooshes) -->
  <g stroke-linecap="round" stroke-width="2" fill="none" opacity="0.95">
    <path d="M -200 220 Q 300 20 900 220" stroke="rgba(155,231,255,0.06)">
      <animate attributeName="d"
               dur="6s"
               repeatCount="indefinite"
               values="
                 M -200 220 Q 300 20 900 220;
                 M -200 200 Q 300 40 900 200;
                 M -200 220 Q 300 20 900 220"/>
    </path>

    <path d="M -200 240 Q 300 60 900 240" stroke="rgba(138,43,226,0.06)">
      <animate attributeName="d"
               dur="7.2s"
               repeatCount="indefinite"
               values="
                 M -200 240 Q 300 60 900 240;
                 M -200 230 Q 300 80 900 230;
                 M -200 240 Q 300 60 900 240"/>
    </path>
  </g>

  <!-- central neon text with glow -->
  <g transform="translate(60,80)">
    <!-- glowing blurred shadow -->
    <text x="0" y="115" font-family="Inter, Helvetica, Arial, sans-serif" font-size="86" font-weight="800"
          fill="#00ffd1" filter="url(#neon)" style="letter-spacing:2px;">
      Café Aroma
      <animate attributeName="opacity" values="0.9;1;0.95;1" dur="3.2s" repeatCount="indefinite" />
    </text>

    <!-- main neon text (front) -->
    <text x="0" y="115" font-family="Inter, Helvetica, Arial, sans-serif" font-size="86" font-weight="800"
          fill="url(#textgrad)" style="letter-spacing:2px;">
      <!-- create a fake gradient via stroke -->
      <tspan fill="#b8f0ff">Café</tspan>
      <tspan dx="12" fill="#9be7ff"> Aroma</tspan>
    </text>

    <!-- subtle flicker effect via overlay -->
    <rect x="-6" y="56" width="520" height="72" fill="black" opacity="0">
      <animate attributeName="opacity" values="0;0.02;0;0.015;0" dur="2.4s" repeatCount="indefinite"/>
    </rect>

    <!-- neon underline -->
    <rect x="0" y="130" width="420" height="6" rx="3" fill="#00ffd1" opacity="0.12">
      <animate attributeName="width" values="0;420;380;420" dur="5s" repeatCount="indefinite" />
    </rect>
  </g>

  <!-- right-side holographic card -->
  <g transform="translate(780,36)" opacity="0.95">
    <rect x="0" y="0" width="360" height="248" rx="14" fill="rgba(255,255,255,0.02)" stroke="rgba(155,231,255,0.06)"/>
    <rect x="12" y="16" width="336" height="88" rx="8" fill="rgba(0,0,0,0.06)"/>
    <circle cx="40" cy="60" r="14" fill="#9be7ff" opacity="0.9"/>
    <rect x="68" y="48" width="230" height="18" rx="6" fill="rgba(255,255,255,0.05)"/>
    <rect x="68" y="72" width="140" height="12" rx="6" fill="rgba(255,255,255,0.03)"/>
    <g transform="translate(20,120)">
      <rect x="0" y="0" width="320" height="90" rx="8" fill="rgba(255,255,255,0.01)"/>
      <path d="M10 18 h120" stroke="rgba(155,231,255,0.07)" stroke-width="3" stroke-linecap="round"/>
      <path d="M10 44 h80"  stroke="rgba(138,43,226,0.06)" stroke-width="3" stroke-linecap="round"/>
      <animateTransform attributeName="transform" attributeType="XML" type="translate" values="0 0;0 -4;0 0" dur="3.8s" repeatCount="indefinite"/>
    </g>
  </g>

  <!-- subtle bottom glow -->
  <ellipse cx="600" cy="310" rx="520" ry="60" fill="rgba(0,102,120,0.06)">
    <animate attributeName="rx" values="520;540;520" dur="6s" repeatCount="indefinite"/>
  </ellipse>

  <!-- tiny animated scanline across -->
  <rect x="-300" y="52" width="180" height="2" fill="rgba(0,255,220,0.08)">
    <animate attributeName="x" from="-300" to="1400" dur="5.6s" repeatCount="indefinite"/>
  </rect>

  <!-- small caption (typewriter fade) -->
  <text x="60" y="170" font-family="Inter, Helvetica, Arial, sans-serif" font-size="14" fill="rgba(200,230,255,0.7)">
    Elegant UI • Session Cart • Razorpay • OTP Auth • Tailwind CSS
    <animate attributeName="opacity" values="0;0.8;0.6;0.8" dur="6s" repeatCount="indefinite"/>
  </text>
</svg>



Developed “Café Aroma”, a Django-based e-commerce site for a dine-in coffee shop. Features include custom user auth, product management, session-based cart, Razorpay payments, OTP verification, order tracking with admin updates, and SMTP-based contact form.
