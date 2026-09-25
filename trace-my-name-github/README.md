# Trace My Name

A name-tracing activity for handwriting practice. Students trace their name with a finger, stylus or mouse. The page scores how accurately they traced and checks Zaner-Bloser letter formation.

It is one self-contained web page (`index.html`). There is nothing to install or build.

## Features

- **Zaner-Bloser print letters** built from real stroke paths, with green start dots, direction arrows and optional stroke numbers. Slanted print and cursive are also available. Cursive is scored by shape only.
- **Scoring**
  - Tracing accuracy combines *Stayed on the path* and *Finished the letters*.
  - Letter formation checks each letter's starting point and stroke direction.
- **Fading support:** row 1 dotted, row 2 faint, rows 3–4 lines only with a model to copy. An optional warm-up page of lines and curves comes first.
- **Watch me:** animates how each letter is formed, as a pen path, outline edges or both. There is also an optional strip that animates each letter of the student's name.
- **Letter heights in real inches** (½ in to 3 in, plus Fill screen), with a ruler check to match each screen.
- **Accessibility**
  - high contrast, wide tracing path, thick pen
  - left-handed layout, palm rejection, read-aloud directions
  - reduced motion, ALL CAPS, one letter at a time
- **Student view:** big writing area, progress dots, three large buttons and a short results pop-up. Leaving it takes a press-and-hold and the teacher code if one is set.
- **Progress tracking:** time, pen lifts and stylus pressure for each try, a daily chart, CSV export and a PDF progress report.
- **PDF downloads:** a printable practice worksheet, a progress report and today's results.
- **Light, Dark or Match device** appearance.

## Use it

Open `index.html` in a browser, or publish it with GitHub Pages:

1. In the repository, go to **Settings → Pages**.
2. Under **Build and deployment**, pick **Deploy from a branch**, choose `main` and `/ (root)`, and save.
3. After a minute the site is live at `https://<your-username>.github.io/<repository-name>/`.

## Where data is saved

When the page runs on GitHub Pages or from a file, student progress is saved **only in that browser on that device**. It uses the browser's local storage and is never sent anywhere. Clearing the browser's data erases it, and progress does not move between devices. Download a CSV or PDF report regularly to keep records.

Settings and the teacher code are also saved per device. The code keeps students out of settings. It is not a security feature.

Use first names or initials, and follow your school's rules on student data.

## Browser needs

- A current version of Chrome, Edge, Safari or Firefox.
- An internet connection. The page loads fonts from Google Fonts and the PDF tool (pdf-lib) from jsDelivr.
- Tablets, touch Chromebooks, interactive whiteboards, phones and computers with a mouse are all supported.

## Known limits

- Scoring on the lines-only rows expects the name in the same place and size as the hidden model. A name written well somewhere else can score lower.
- The formation check covers starting points and stroke direction, not stroke order.
- The letter strokes follow Zaner-Bloser closely but are hand-drawn approximations, not official letter shapes.
- Accent marks are not traced (José is traced as Jose), and letters without stroke data are skipped.
- Pressure is recorded only with styluses that report it, such as Apple Pencil.
