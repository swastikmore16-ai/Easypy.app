EasyPy — Full Website Project
================================

FOLDER STRUCTURE
-----------------
easypy-project/
  index.html          -> the page structure (links to the CSS and JS below)
  css/styles.css       -> all styling
  js/script.js          -> all interactivity (lessons, quizzes, language
                          switching, lead form, certificate generator, etc.)
  assets/favicon.png    -> browser tab icon (your logo)
  assets/logo.png       -> logo shown in the top navigation bar

This is a completely static website — no build step, no server, no
database required. It runs entirely in the browser.

ABOUT FONTS
------------
The site uses Google Fonts (Inter, Noto Sans, Noto Sans Devanagari,
JetBrains Mono), loaded via a standard <link> tag in index.html pointing to
fonts.googleapis.com. This is the normal, recommended way to use Google
Fonts on any live website — it works automatically once the site is online,
no extra files needed. (If you ever want the fonts fully self-hosted with
zero external calls, that's a separate ask — let me know.)

HOW TO DEPLOY
--------------
Netlify (easiest):
  1. Go to https://app.netlify.com/drop
  2. Drag the whole "easypy-project" folder onto the page
  3. You get a live link instantly; attach a custom domain later from
     Site settings > Domain management if you buy one.

GitHub Pages:
  1. Create a new repository on GitHub
  2. Upload everything INSIDE easypy-project (index.html, css/, js/,
     assets/) to the root of the repo — keep the folder structure exactly
     as it is
  3. Repo Settings > Pages > Deploy from branch > main / root
  4. Your site goes live at https://yourusername.github.io/reponame

Any regular web host (Hostinger, GoDaddy, etc.):
  1. Open their File Manager or connect via FTP
  2. Upload index.html, css/, js/, and assets/ into the public_html (or
     www) folder, keeping the same folder structure
  3. Done — visiting your domain now loads the site

IMPORTANT — TWO THINGS TO SWITCH ON AFTER DEPLOYING
------------------------------------------------------
This site currently saves lesson progress using a storage feature that
ONLY works inside Claude.ai. Once hosted on your own domain, that specific
auto-save quietly stops (site won't break, it just won't remember progress
between visits). The lead-capture form and ad slot are wired up and ready,
but need your own free account IDs to actually work:

1. LEAD CAPTURE (name + email form) — via Formspree, free:
   - Sign up at https://formspree.io, create a form, copy its Form ID
   - Open js/script.js, find "YOUR_FORMSPREE_ID" (appears once), replace
     it with your real ID, save, re-upload js/script.js

2. ADS — via Google AdSense, free (needs approval after you're live):
   - Apply at https://www.google.com/adsense with your live site URL
   - Once approved, you get a Publisher ID (ca-pub-...) and a Slot ID
   - Open index.html, find "YOUR_ADSENSE_PUBLISHER_ID" and uncomment the
     <script> tag right above it
   - Open js/script.js, find "YOUR_ADSENSE_PUBLISHER_ID" and
     "YOUR_ADSENSE_SLOT_ID" inside the ad slot comment, fill in your real
     values, and uncomment those two lines
   - Save both files, re-upload

Until you do these two things, the site works perfectly for learning —
the lead form just won't reach your inbox yet, and the ad slot stays
empty/placeholder.

WHAT'S INSIDE THE SITE
------------------------
- 8 Python lessons (Intro, Variables, Data Types, Input/Output,
  Conditionals, Loops, Lists, Functions), each fully written in English,
  Hindi, and Marathi (no mixed scripts)
- A "mother tongue bridge" card on every lesson connecting the Python
  concept to how you'd naturally say it
- A "Predict the Output" self-test before each quiz
- A 2-question quiz per lesson with instant feedback
- Progress tracking sidebar
- A name/email capture step before lessons start (Formspree-ready)
- A downloadable completion certificate (PNG) once all lessons are done
- An ad slot in the sidebar (AdSense-ready)
- Copy-code buttons on every code example

WANT MORE?
-----------
Go back to the Claude conversation this was built in and ask for more —
additional lessons, more languages, a real in-browser Python code runner,
a revision/cheat-sheet page, etc.
