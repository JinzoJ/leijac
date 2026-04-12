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

The site is styled as a 2001 Japanese corporate website built with
IBM HomePage Builder. Everything is in Japanese. The layout is a
fixed 960px three-panel frame with a LEIJAC logo mirrored on both
side panels and a center content column in royal blue.

Decorative wireframe circles cascade in on page load: right side
top-to-bottom, then left side bottom-to-top. Each circle fades in
over 0.6 seconds on a staggered delay. Circles stay on after the
cascade completes.

The news page has a blinking NEW badge on the two most recent
entries (pulses via CSS opacity keyframes).

Links are green (#00ff00), matching the period convention.

-------------------------------------------------------------------
 The fiction
-------------------------------------------------------------------

This site is an in-fiction artifact. レイジャック株式会社 is
depicted as a small Nagoya arcade game studio founded in 1989 by
フランシスコ・アドリアン (代表取締役社長) and 伊藤雅史
(取締役副社長). Their catalog contains six released arcade titles
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

  - Blue shade         body background, #04042a
  - Royal blue center  #14148c
  - Yellow accents     #ffeb3b
  - Link green         #00ff00
  - Circle fade delay  search for "animation-delay" in HTML files
  - Splash redirect    change "30" in META Refresh on index.html

The circle delays are inline in each page's HTML so you can tweak
the cascade per page without touching the stylesheet.

===================================================================
