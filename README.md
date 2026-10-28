# Online Examination Management System

A simple offline-friendly exam system that runs entirely in the browser (HTML, CSS, JavaScript). No server or database needed.

## Run it
- **Locally:** open `index.html` in a browser (keep `index.html`, `script.js` and `style.css` in the same folder).
- **On GitHub Pages:** push these files to a repository, then go to **Settings → Pages**, choose the `main` branch and the `/ (root)` folder, and save. Your site will be at `https://<username>.github.io/<repository>/`.

## Default login
- Administrator: `admin` / `admin123` (change it in **School & Exam** settings after first login).

## How it works
1. Admin sets the school, exam title, date, start time and duration.
2. Admin adds questions (type them, paste them, or import from a text-based PDF).
3. Admin creates student accounts.
4. **Export exam package** creates `exam-package.pdf`. Load it on each student device with **Load an exam package**, then log out.
5. Students sign in and take the exam. They must answer every question before they can submit.
6. Each student downloads an `answers-<username>.pdf` file; the admin imports these in **Results**.

## Notes
- Data is stored in each browser (localStorage / IndexedDB), so it stays on that device.
- Exam package and answer files are PDFs that also carry the app data. Do not edit or re-save them.
- Importing questions from an ordinary PDF loads the pdf.js library from cdnjs, so it needs internet the first time.

## Question format
```
1. What is the brain of the computer?
A) RAM
B) CPU
C) Mouse
D) Monitor
Answer: B
```
