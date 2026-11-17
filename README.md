# Mandarin Trail · 汉语小径

A **free, dependency-free, installable Progressive Web App (PWA)** to learn Mandarin from the very beginning through the **classic HSK 1–2 foundation**.

## Included

- Four progressive Pinyin lessons: initials/finals, five tones, difficult sounds, and tone sandhi.
- **300 vocabulary entries**: 150 classic HSK 1 + 150 classic HSK 2, with tone-marked Pinyin and short English explanations.
- 24 bite-sized vocabulary lessons (12 per level), flashcards, 10-question adaptive drills and a basic spaced-review schedule.
- 24 common radicals and 24 practical travel phrases, including airport, hotel, transit and food situations.
- Touch handwriting practice and **38 schematic, step-by-step character stroke diagrams**. Other characters offer a tracing canvas but not verified stroke diagrams. Handwriting is **not automatically assessed**.
- XP, streaks, a seven-day activity chart, lesson status, vocabulary progress, and JSON backup/restore.
- Offline-first: all lessons, quizzes and artwork are built in; no API, login, backend or third-party JavaScript is needed.

**Important syllabus note:** This app follows the **older HSK 2.0** vocabulary standard (300 words through level 2). It does **not** contain all vocabulary needed for the expanded HSK 3.0 exam, first launched worldwide on **13 December 2026**. For current examination preparation, consult [ChineseTest](https://www.chinesetest.cn/HSK).

## Publish to GitHub Pages (no command line needed)

1. Download and **extract** `mandarin-trail.zip` on your computer or Android phone. Do not upload the ZIP itself as the GitHub Pages site.
2. Sign in at [github.com](https://github.com) and select **New repository** (or **+ → New repository**).
3. Name it `mandarin-trail`, set visibility to **Public**, and select **Create repository**. A public repository works with GitHub Pages on a free personal GitHub account.
4. Open the repository, choose **Add file → Upload files** (if this is an empty repo, choose the **uploading an existing file** link).
5. Upload the **extracted contents**, preserving all files at the root. The `index.html`, `app.js`, `data.js`, `strokes.js`, `style.css`, `sw.js`, `manifest.webmanifest`, and `README.md` must be **at the repository root**. The PNG icons must also be at the repository root.
6. Select **Commit changes**.
7. Open **Settings → Pages → Build and deployment**. Set **Source: Deploy from a branch**, **Branch: main**, **Folder: /(root)**, and select **Save**.
8. Open the published website at `https://YOUR-USERNAME.github.io/mandarin-trail/` (substitute your GitHub username). The Pages settings will also show the exact live URL after deployment.
9. On **Android Chrome**, open the published URL while online and wait for the first full page load. Then tap the **⋮ menu → Install app**, or **Add to Home screen**, depending on Chrome's wording. Open the installed shortcut once before testing without connectivity.
10. Turn on **airplane mode**, reopen the app from your home screen and check the course, drills and handwriting grid. If it fails, reconnect, reopen the web URL once to complete caching, and test again.

### Uploading from Android only

Unzip the archive first in Android's Files app. Open GitHub in Chrome, enable **Desktop site** if GitHub hides **Add file / Upload files**, and select the extracted files, without needing any folders. Uploading a whole folder can be browser-dependent: if necessary, use a desktop browser or a Git client that supports folder uploads. A ZIP by itself **will not be expanded automatically** by GitHub.

### First run without GitHub

Opening `index.html` locally can preview the content in some browsers, but **offline installation requires a website served over HTTPS**, such as GitHub Pages. Service workers do not operate through ordinary `file://` pages. Alternatively, during development, serve the directory with `python -m http.server 8000` and open `http://localhost:8000` on the same device.

## Storage and privacy

Progress is stored using `localStorage` **on each device/browser**. It will work offline and does not sync across devices or upload to GitHub. Use **Profile → Export progress**, save the JSON file, then **Profile → Import progress** on the other device. Clearing site storage or reinstalling may erase unexported progress.

The **Listen** feature uses the phone's system speech synthesis. Speech audio is **not bundled** in this app; an installed Mandarin voice might work offline, whereas some Android TTS engines require network access. All written content and other activities are self-contained.

## Updating

Replace files in the repository and commit. When updating the app, also change `CACHE_NAME` in `sw.js` (for example to `mandarin-trail-v1.0.1`) so the offline assets refresh. Refresh the site online before switching to airplane mode.

## Project structure

```text
mandarin-trail/
  index.html
  style.css
  app.js
  data.js
  strokes.js
  sw.js
  manifest.webmanifest
  README.md
  icon-192.png
  icon-512.png
```

## References and acknowledgments

- [ChineseTest](https://www.chinesetest.cn/HSK) — current exam arrangements and official syllabus.
- [HSK Prep classic HSK 1 / HSK 2 word lists](https://tryhskprep.com/blog/hsk-2-vocabulary-list) — cross-check for the 150 + 150 historical syllabus entries. Brief English glosses in this project are separately edited.
- Stroke diagrams are **original, schematic teaching paths** for core characters. They are not the Hanzi Writer library, and they do not claim font-quality accuracy.

This app is intended for personal study, not as a certified test-preparation product. The code is released under the MIT license; the HSK name and test are owned by their respective organizations.
