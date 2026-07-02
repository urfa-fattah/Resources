THE READING ROOM — how this folder works
==========================================

1. Drop your file (PDF, DOCX, PPTX, image, etc.) straight into this
   /resources folder — the same one this README is in.

2. Name it course-first, with a dash or space after the course code,
   e.g.:
     CSE-1101-lecture-3-boolean-algebra.pdf
     CSE-1102-lab-sheet-2.pdf
     MATH-1101-past-paper-2024.pdf
   The website reads the part before the first dash/space/underscore
   and matches it against the Year-1 course list automatically.
   Anything it doesn't recognise is filed under "Unfiled" instead of
   being hidden.

3. Open manifest.json (in this same folder) and add the exact
   filename to the array, e.g.:

     [
       "CSE-1101-lecture-3-boolean-algebra.pdf",
       "CSE-1102-lab-sheet-2.pdf"
     ]

   Keep it valid JSON — every filename in double quotes, commas
   between entries, no trailing comma after the last one.

4. Reload the website, or click "Refresh library" — the file shows
   up filed under its course, with a PDF reader built in.

Notes:
- Nothing is uploaded anywhere. The page reads these files directly
  off disk (or off whatever static server is hosting this folder).
- If you're opening index.html directly as a file:// URL, some
  browsers block fetch() for local files. Easiest fix: serve the
  project folder with a tiny local server, e.g. from a terminal in
  the project folder run  python -m http.server 8000  and open
  http://localhost:8000 — or upload the whole folder (index.html +
  resources/) to any static host (GitHub Pages, Netlify, Vercel).
