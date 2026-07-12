===================================================================
 LEIJAC.COM — deployment readme
===================================================================

Seven HTML pages plus one stylesheet. Everything in this folder is
static — no build step, no dependencies, no database. Drop the
contents onto any web host and it works.

-------------------------------------------------------------------
 File list
-------------------------------------------------------------------

  index.html          Splash page (auto-redirects to menu after 30s)
  menu.html           Main navigation hub
  kaisha-annai.html   Company profile (会社案内)
  seihin-jouhou.html  Product catalog (製品情報)
  news.html           News / announcements (NEWS)
  saiyou-jouhou.html  Recruiting (採用情報)
  otoiawase.html      Contact info (お問い合わせ)
  style.css           Shared stylesheet
  README.txt          This file

-------------------------------------------------------------------
 Deployment
-------------------------------------------------------------------

Upload every file in this folder to the webroot of leijac.com.
Keep the filenames exactly as they are. The relative links between
pages (menu.html → kaisha-annai.html etc.) will just work.

index.html must sit at the root so visiting leijac.com loads the
splash page first.

No .htaccess or server config required. Any static host works —
Netlify, GitHub Pages, S3, nginx, Apache, whatever the current host
for leijac.com is.

-------------------------------------------------------------------
 What it looks like
-------------------------------------------------------------------

The site is a 1:1 homage to the "How to Digital ART" DVD-ROM
(Kadokawa, 2001, built with IBM HomePage Builder). Everything is
in Japanese.

Splash and menu run on a fixed 800x600 stage that scales to fit
the window (fullscreen-IE-in-2001 presentation). The splash logo
pieces fly in from off-screen on choppy 50ms timers, then the
page auto-advances to the menu after 30 seconds (or the beveled
>>Skip>> button). The menu is the disc's layout: navy logo block,
wireframe deco rectangles, RGB wireframe circles on a black left
rail, flat #000090 panel, numbered yellow menu items that roll
over to cyan.

Interior pages use the disc's section template: #00006f blue,
yellow text, white links, red Return arrow top-right, thick white
HR, content in alternating #0000cc / #0000a2 banded table rows.

The logo is a PNG render (inf/leijac.png, from After Effects) —
no typographic logo anywhere. The news page keeps its blinking
NEW badge (CSS opacity keyframes).

-------------------------------------------------------------------
 The fiction
-------------------------------------------------------------------

This site is an in-fiction artifact. レイジャック株式会社 is
depicted as a small Nagoya arcade game studio founded in 1989 by
服部隆造 (Hattori Ryūzō, 代表取締役社長) and 伊藤雅史
(取締役副社長). All names are fictional Japanese businessmen —
nothing ties the fiction to any real person. Their catalog contains six released arcade titles
from 1990 to 2000 plus one in-development title for 2001
(ジェット・フェニックス). Address is a real Nagoya business
district postal code (460-0008, 中区栄) but the building is
fictional. Phone number prefix (052-264) is real Nagoya but the
last four digits are fake. Dates for the Amusement Machine Show
2001 in the news page reference real event dates.

Nothing on this site references Horror Theater, Leijac Digital
Entertainment LLC (the actual modern company), Marshall NC, or
anything outside the in-fiction 2001 Japanese Leijac universe.

-------------------------------------------------------------------
 Customization
-------------------------------------------------------------------

All visual styling lives in style.css. Common edits:

  - Interior blue      BODY.interior, #00006f
  - Band rows          .band-a #0000cc / .band-b #0000a2
  - Menu panel blue    .menu-panel, #000090
  - Yellow accents     #ffff00 (menu items, rules, © lines)
  - Fly-in speed       FRAMES / tick values in index.html script
  - Splash redirect    change "30" in META Refresh on index.html

Splash layer start positions are the vfxSlide() calls in
index.html; menu button coordinates are inline styles in
menu.html (800x600 stage space, same as the disc).

===================================================================
