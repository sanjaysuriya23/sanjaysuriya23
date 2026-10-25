<?xml version="1.0" encoding="UTF-8"?>
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 420" width="1200" height="420" role="img" aria-labelledby="sy-hero-title sy-hero-desc">
  <title id="sy-hero-title">SANJAY SURIYA E</title>
  <desc id="sy-hero-desc">Computer Science Student, AI Enthusiast, App Developer. Black and orange banner with a technical grid, orbital details and a flowing amber line.</desc>

  <defs>
    <linearGradient id="sy-hero-bg" x1="0" y1="0" x2="1" y2="1">
      <stop offset="0" stop-color="#0A0A0A"/>
      <stop offset="0.55" stop-color="#141414"/>
      <stop offset="1" stop-color="#22130A"/>
    </linearGradient>

    <radialGradient id="sy-hero-glow-a" gradientUnits="userSpaceOnUse" cx="960" cy="205" r="440">
      <stop offset="0" stop-color="#FF6A00" stop-opacity="0.6"/>
      <stop offset="0.5" stop-color="#7A2E00" stop-opacity="0.4"/>
      <stop offset="1" stop-color="#7A2E00" stop-opacity="0"/>
      <animate attributeName="cx" values="900;1020;900" dur="14s" repeatCount="indefinite"/>
    </radialGradient>

    <radialGradient id="sy-hero-glow-b" gradientUnits="userSpaceOnUse" cx="140" cy="430" r="380">
      <stop offset="0" stop-color="#FF8A1F" stop-opacity="0.3"/>
      <stop offset="1" stop-color="#FF8A1F" stop-opacity="0"/>
      <animate attributeName="cy" values="430;380;430" dur="11s" repeatCount="indefinite"/>
    </radialGradient>

    <linearGradient id="sy-hero-name" gradientUnits="userSpaceOnUse" x1="80" y1="0" x2="730" y2="0">
      <stop offset="0" stop-color="#FFFFFF"/>
      <stop offset="1" stop-color="#FFB347"/>
    </linearGradient>

    <linearGradient id="sy-hero-underline" gradientUnits="userSpaceOnUse" x1="80" y1="0" x2="680" y2="0">
      <stop offset="0" stop-color="#FFB347"/>
      <stop offset="0.5" stop-color="#FF8A1F"/>
      <stop offset="1" stop-color="#FF6A00" stop-opacity="0"/>
    </linearGradient>

    <linearGradient id="sy-hero-wave" gradientUnits="userSpaceOnUse" x1="0" y1="0" x2="1200" y2="0">
      <stop offset="0" stop-color="#FF6A00" stop-opacity="0"/>
      <stop offset="0.3" stop-color="#FF8A1F"/>
      <stop offset="0.7" stop-color="#FFB347"/>
      <stop offset="1" stop-color="#FF8A1F" stop-opacity="0"/>
    </linearGradient>

    <pattern id="sy-hero-grid-fine" width="24" height="24" patternUnits="userSpaceOnUse">
      <path d="M24 0H0V24" fill="none" stroke="#FFFFFF" stroke-opacity="0.045" stroke-width="0.6"/>
    </pattern>
    <pattern id="sy-hero-grid-major" width="120" height="120" patternUnits="userSpaceOnUse">
      <path d="M120 0H0V120" fill="none" stroke="#FFB347" stroke-opacity="0.09" stroke-width="0.8"/>
    </pattern>

    <filter id="sy-hero-blur" x="-20%" y="-300%" width="140%" height="700%">
      <feGaussianBlur stdDeviation="6"/>
    </filter>
    <filter id="sy-hero-soft" x="-100%" y="-100%" width="300%" height="300%">
      <feGaussianBlur stdDeviation="2.5"/>
    </filter>

    <clipPath id="sy-hero-clip">
      <rect width="1200" height="420" rx="18"/>
    </clipPath>
  </defs>

  <g clip-path="url(#sy-hero-clip)">
    <!-- Background layers -->
    <rect width="1200" height="420" fill="url(#sy-hero-bg)"/>
    <rect width="1200" height="420" fill="url(#sy-hero-glow-a)"/>
    <rect width="1200" height="420" fill="url(#sy-hero-glow-b)"/>
    <rect width="1200" height="420" fill="url(#sy-hero-grid-fine)"/>
    <rect width="1200" height="420" fill="url(#sy-hero-grid-major)"/>

    <!-- Orbital system -->
    <g transform="translate(960 205)">
      <circle r="150" fill="none" stroke="#FF8A1F" stroke-opacity="0.35" stroke-width="1" stroke-dasharray="2 8"/>
      <circle r="100" fill="none" stroke="#FFB347" stroke-opacity="0.22" stroke-width="1"/>
      <ellipse rx="230" ry="70" transform="rotate(-24)" fill="none" stroke="#FF8A1F" stroke-opacity="0.42" stroke-width="1"/>
      <ellipse rx="230" ry="70" transform="rotate(24)" fill="none" stroke="#FFB347" stroke-opacity="0.22" stroke-width="1"/>
      <line x1="-190" y1="0" x2="190" y2="0" stroke="#FFB347" stroke-opacity="0.15"/>
      <line x1="0" y1="-190" x2="0" y2="190" stroke="#FFB347" stroke-opacity="0.15"/>

      <!-- Node on outer ring -->
      <g>
        <animateTransform attributeName="transform" type="rotate" from="0" to="360" dur="30s" repeatCount="indefinite"/>
        <circle cx="150" cy="0" r="7" fill="#FFB347" opacity="0.6" filter="url(#sy-hero-soft)"/>
        <circle cx="150" cy="0" r="4" fill="#FFFFFF"/>
      </g>

      <!-- Node on inner ring, opposite direction -->
      <g>
        <animateTransform attributeName="transform" type="rotate" from="360" to="0" dur="20s" repeatCount="indefinite"/>
        <circle cx="100" cy="0" r="3.5" fill="#FF8A1F"/>
      </g>

      <!-- Node travelling along the tilted ellipse -->
      <g transform="rotate(-24)">
        <circle r="3" fill="#FFB347">
          <animateMotion dur="18s" repeatCount="indefinite" path="M-230 0 a230 70 0 1 0 460 0 a230 70 0 1 0 -460 0"/>
        </circle>
      </g>

      <!-- Core -->
      <circle r="18" fill="none" stroke="#FF8A1F" stroke-opacity="0.55" stroke-width="1">
        <animate attributeName="r" values="18;38" dur="4s" repeatCount="indefinite"/>
        <animate attributeName="stroke-opacity" values="0.55;0" dur="4s" repeatCount="indefinite"/>
      </circle>
      <circle r="9" fill="#FF6A00" stroke="#FFB347" stroke-width="1"/>
      <circle r="3.5" fill="#FFFFFF"/>
    </g>

    <!-- Technical corner marks -->
    <g fill="none" stroke="#FFB347" stroke-opacity="0.4" stroke-width="1.2" stroke-linecap="square">
      <path d="M32 64V32H64"/>
      <path d="M1136 32H1168V64"/>
      <path d="M32 356V388H64"/>
      <path d="M1136 388H1168V356"/>
    </g>

    <!-- Labels -->
    <text x="80" y="112" font-family="'SFMono-Regular', Consolas, 'Liberation Mono', Menlo, monospace" font-size="13" letter-spacing="3" fill="#FF8A1F">B.E. COMPUTER SCIENCE AND ENGINEERING  /  2025 — 2029</text>

    <!-- Name -->
    <text x="80" y="190" font-family="Georgia, 'Times New Roman', serif" font-size="56" font-weight="700" fill="url(#sy-hero-name)" textLength="650" lengthAdjust="spacing">SANJAY SURIYA E</text>

    <!-- Role line -->
    <text x="80" y="245" font-family="'Segoe UI', Helvetica, Arial, sans-serif" font-size="20" letter-spacing="1" fill="#FFB347">Computer Science Student<tspan fill="#FF6A00" dx="12">|</tspan><tspan dx="12">AI Enthusiast</tspan><tspan fill="#FF6A00" dx="12">|</tspan><tspan dx="12">App Developer</tspan></text>

    <!-- Glowing underline -->
    <line x1="80" y1="274" x2="680" y2="274" stroke="#FF8A1F" stroke-width="5" stroke-opacity="0.55" filter="url(#sy-hero-blur)"/>
    <line x1="80" y1="274" x2="680" y2="274" stroke="url(#sy-hero-underline)" stroke-width="2" stroke-linecap="round"/>
    <circle r="4" fill="#FFFFFF" filter="url(#sy-hero-soft)">
      <animateMotion dur="5s" repeatCount="indefinite" path="M80 274 H680"/>
    </circle>

    <text x="80" y="312" font-family="'SFMono-Regular', Consolas, 'Liberation Mono', Menlo, monospace" font-size="12" letter-spacing="2.5" fill="#FFB347" fill-opacity="0.7">PAAVAI ENGINEERING COLLEGE</text>

    <!-- Flowing path: faint static copy keeps the design intact without animation -->
    <path d="M-20 378 C 160 324, 300 416, 520 368 S 860 326, 1000 370 S 1160 398, 1220 356" fill="none" stroke="#FF8A1F" stroke-opacity="0.25" stroke-width="1.2"/>
    <path d="M-20 378 C 160 324, 300 416, 520 368 S 860 326, 1000 370 S 1160 398, 1220 356" fill="none" stroke="url(#sy-hero-wave)" stroke-width="2" stroke-linecap="round" pathLength="1000" stroke-dasharray="1000">
      <animate attributeName="stroke-dashoffset" values="1000;0;0" keyTimes="0;0.6;1" dur="9s" repeatCount="indefinite"/>
    </path>
  </g>

  <rect x="0.5" y="0.5" width="1199" height="419" rx="18" fill="none" stroke="#7A2E00" stroke-width="1"/>
</svg>
