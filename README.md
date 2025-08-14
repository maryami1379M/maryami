:root {
  --bg: #0f172a;
  --card: #111827;
  --text: #e5e7eb;
  --muted: #9ca3af;
  --accent: #22c55e;
  --danger: #ef4444;
  --border: #1f2937;
}

* { box-sizing: border-box; }
html, body { margin: 0; padding: 0; background: var(--bg); color: var(--text); font-family: system-ui, sans-serif; }
.container { max-width: 900px; margin: 0 auto; padding: 16px; }

h1 { margin: 0 0 8px; font-weight: 800; }
input, textarea, button {
  width: 100%; padding: 10px 12px; border-radius: 12px; border: 1px solid var(--border);
  background: #0b1220; color: var(--text); outline: none;
}
input::placeholder, textarea::placeholder { color: var(--muted); }
button { cursor: pointer; background: var(--accent); border: none; color: #05130a; font-weight: 700; }
button.danger { background: var(--danger); color: #190404; }

#note-form { display: grid; gap: 10px; grid-template-columns: 1fr 1fr; }
#note-form #content { grid-column: 1 / -1; }
#note-form button { grid-column: span 1; }
#note-form #clear-all { grid-column: span 1; }

#list { list-style: none; padding: 0; margin: 16px 0 80px; display: grid; gap: 12px; }
.card {
  background: var(--card); border: 1px solid var(--border); border-radius: 16px; padding: 12px;
  display: grid; gap: 8px;
}
.card header { display: flex; alig-items: center; justify-content: space-between; gap: 8px; }
.tags { display: flex; gap: 6px; flex-wrap: wrap; }
.tag { font-size: 12px; padding: 4px 8px; border-radius: 999px; background: #0b1526; border: 1px solid var(--border); color: var(--muted); }
.actions { display: flex; gap: 6px; }
.actions button { padding: 6px 8px; border-radius: 10px; }
.muted { color: var(--muted); font-size: 14px; }

#search { width: 100%; margin-top: 6px; }

footer { position: sticky; bottom: 0; background: linear-gradient(to top, rgba(15,23,42,0.95), rgba(15,23,42,0.7)); border-top: 1px solid var(--border); }
footer .container { display: grid; gap: 8px; grid-template-columns: 1fr 1fr; }
#io { grid-column: 1 / -1; }

@media (max-width: 720px) {
  #note-form { grid-template-columns: 1fr; }
  footer .container { grid-template-columns: 1fr; }
}

