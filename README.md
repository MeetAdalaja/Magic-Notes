# Magic Notes — Vanilla JS Notes App

A lightweight **note‑taking web app** built with **HTML, CSS, and vanilla JavaScript**.  
Add notes, search through them instantly, and delete what you don’t need — all stored in your browser via **localStorage** (no server, no sign‑in).

[![Live Demo](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-2ea44f)](https://meetadalaja.github.io/Magic-Notes/)
[![Last commit](https://img.shields.io/github/last-commit/MeetAdalaja/Magic-Notes)](https://github.com/MeetAdalaja/Magic-Notes/commits/master)
[![Repo size](https://img.shields.io/github/repo-size/MeetAdalaja/Magic-Notes)](https://github.com/MeetAdalaja/Magic-Notes)
![Stack](https://img.shields.io/badge/HTML-CSS-JavaScript-informational)

---

## ✨ Features

- 📝 **Create notes** with a title and content
- 🗂️ **Search** notes instantly by keyword
- 🗑️ **Delete** notes you no longer need
- 🔒 **Private & offline**: data is saved locally via `localStorage`
- ⚡ **Zero dependencies**: pure HTML/CSS/JS

> Optional enhancements (see [Roadmap](#-roadmap)) include edit‑in‑place, color labels, and `localStorage` backup/export to JSON.

---

## 🖥️ Live Demo

**▶️ https://meetadalaja.github.io/Magic-Notes/**

If the page looks empty at first load, add your first note and it will appear in the list/grid.

---

## 🗂️ Project Structure

```text
Magic-Notes/
├─ js/            # App logic (render, storage, search, events)
├─ index.html     # App UI (markup + script includes)
└─ styles.css     # (If present) basic styling
```

> Your repository may keep styles inline in `index.html`; if you prefer, move them into a `styles.css` file and link it.

---

## ⚙️ Run Locally

No build tools needed.

```bash
# Option A: just open the file
double-click index.html

# Option B: run a tiny static server (prevents some browser security quirks)
# Python 3
python -m http.server 8000
# then open http://localhost:8000
```

---

## 🚀 Deploy (GitHub Pages)

Pages is already configured for this repository. To redeploy:

1. Commit & push to `master` (or the Pages source branch in repo settings)
2. Wait for GitHub Pages to build
3. Your site will be live at **https://meetadalaja.github.io/Magic-Notes/**

> To change the domain, add a `CNAME` file or configure a custom domain in the repository’s **Settings → Pages**.

---

## 🧩 Implementation Notes

- Notes are serialized to `localStorage` (e.g., `localStorage.setItem('notes', JSON.stringify([...]))`)
- On load, the app reads existing notes and renders them
- The search field filters the in‑memory list and re‑renders the results
- Deleting a note updates local state and persists back to `localStorage`

---

## ✅ Roadmap

- [ ] **Edit** an existing note (inline or modal)
- [ ] **Color labels / tags** and filter by tag
- [ ] **Export/Import** notes as JSON
- [ ] **Keyboard shortcuts** (e.g., `Ctrl+Enter` to add, `/` to focus search)
- [ ] **Responsive** grid and better empty states

---

## 🐞 Troubleshooting

- **Notes don’t persist?** Check your browser privacy settings — some modes block `localStorage`
- **Nothing renders?** Open DevTools → Console for errors (missing `js` include, typos, etc.)
- **Search is slow with many notes?** Debounce the input handler or limit DOM updates per keystroke

---

## 📄 License

Add a `LICENSE` file (e.g., MIT) if you want others to reuse or adapt your code.  
Without a license, the default is “all rights reserved.”

---

## 🙏 Credits

Built by **Meet Adalaja**.  
Icons/badges are from Shields.io; no external JS frameworks are used.
