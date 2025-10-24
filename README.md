<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Cute Moving Rabbit</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <main class="stage" id="stage" aria-label="Animated rabbit stage">
    <!-- SVG rabbit (scalable, accessible) -->
    <div id="rabbit" class="rabbit" role="img" aria-label="Cute rabbit">
      <svg viewBox="0 0 200 150" width="200" height="150" aria-hidden="true">
        <!-- Body -->
        <g id="rabbit-group" transform="translate(0,0)">
          <ellipse id="body" cx="100" cy="95" rx="46" ry="36" fill="#fffaf6" stroke="#e6d7cc" stroke-width="2"/>
          <!-- Head -->
          <circle id="head" cx="140" cy="60" r="26" fill="#fffaf6" stroke="#e6d7cc" stroke-width="2"/>
          <!-- Ears -->
          <g id="ears" transform="translate(0,0)">
            <g id="left-ear" transform="translate(125,18)">
              <path d="M5 0 C 4 -22  -6 -24 -8 0 C -6 8 4 10 5 0 Z" fill="#fffaf6" stroke="#e6d7cc" stroke-width="2"/>
              <path d="M3 -2 C 2 -16 -2 -18 -3 -2 C -2 4 2 6 3 -2 Z" fill="#ffdfea" opacity="0.9"/>
            </g>
            <g id="right-ear" transform="translate(155,18)">
              <path d="M-5 0 C -4 -22  6 -24 8 0 C 6 8 -4 10 -5 0 Z" fill="#fffaf6" stroke="#e6d7cc" stroke-width="2"/>
              <path d="M-3 -2 C -2 -16 2 -18 3 -2 C 2 4 -2 6 -3 -2 Z" fill="#ffdfea" opacity="0.9"/>
            </g>
          </g>
          <!-- Eyes -->
          <g id="face">
            <ellipse cx="132" cy="56" rx="3.4" ry="4.6" fill="#222"/>
            <ellipse cx="148" cy="56" rx="3.4" ry="4.6" fill="#222"/>
            <!-- blush -->
            <ellipse cx="132" cy="68" rx="5.5" ry="3.2" fill="#ffd7dd" opacity="0.8"/>
            <ellipse cx="148" cy="68" rx="5.5" ry="3.2" fill="#ffd7dd" opacity="0.8"/>
            <!-- nose & mouth -->
            <path d="M140 66 q3 4 0 6 q-3 -2 0 -6" fill="#ffb6c1" stroke="#cc6b80" stroke-width="1"/>
          </g>
          <!-- Tail -->
          <circle id="tail" cx="60" cy="88" r="10" fill="#fff" stroke="#e6d7cc" stroke-width="2"/>
        </g>
      </svg>
    </div>

    <!-- UI / controls -->
    <div class="ui">
      <div>Controls: ← → to move • Space / Click to hop</div>
      <button id="toggleAuto">Toggle Auto-move</button>
    </div>
  </main>

  <script src="script.js"></script>
</body>
</html>
