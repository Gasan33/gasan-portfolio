Gasan Omer — portfolio
======================

WHAT CHANGED IN THIS BUILD
  The 33 screenshots used to be embedded inside index.html as base64
  data URIs. That is what produced the 414 "URI too long" errors: a
  2 MB HTML file with megabyte-long attributes gets mangled by hosts,
  CDNs and editors, and the broken remains are then requested as if
  they were file paths.

  They are now real files in assets/. index.html dropped from 1972 KB
  to 153 KB and the images load lazily.

HOW TO DEPLOY
  Upload the WHOLE folder (index.html + assets/). Keep them together —
  the paths are relative.

  Netlify:  drag this folder onto netlify.com
  Vercel:   vercel deploy
  Any host: upload as-is, no build step

LOCAL PREVIEW
  python3 -m http.server 8000     then open http://localhost:8000

STILL MISSING
  Gasan_Omer_CV.pdf — drop it next to index.html. Until it is there the
  Download CV button turns itself into "Request CV" and opens email.
