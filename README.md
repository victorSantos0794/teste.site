<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Super Liga BT — Torneio de Duplas</title>
<link href="https://fonts.googleapis.com/css2?family=Barlow+Condensed:ital,wght@0,300;0,400;0,600;0,700;0,800;0,900;1,700&family=Barlow:wght@300;400;500;600&family=Share+Tech+Mono&display=swap" rel="stylesheet">
<style>
:root {
  --bg:#070e18; --surface:#0c1624; --card:#101e30; --card2:#0e1a2a;
  --border:#1a2e46; --border2:#253d5c;
  --accent:#00d4ff; --accent-d:#0099cc;
  --amber:#ffab00; --green:#00e676; --red:#ff3d71;
  --muted:#4e6b8a; --text:#ddeeff; --text2:#8aafc8;
  --gold:#ffd740; --silver:#b8c8d8; --bronze:#ff8f65;
  --r:8px; --r2:14px;
  --glow-a:0 0 30px rgba(0,212,255,.2);
  --trans:.22s cubic-bezier(.4,0,.2,1);
}
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0;}
html{scroll-behavior:smooth;}
body{background:var(--bg);color:var(--text);font-family:'Barlow',sans-serif;min-height:100vh;overflow-x:hidden;}
body::before{content:'';position:fixed;inset:0;z-index:0;background-image:url('data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNDQwIDkwMCI+CiAgPCEtLSBTa3kgZ3JhZGllbnQgLS0+CiAgPGRlZnM+CiAgICA8bGluZWFyR3JhZGllbnQgaWQ9InNreSIgeDE9IjAiIHkxPSIwIiB4Mj0iMCIgeTI9IjEiPgogICAgICA8c3RvcCBvZmZzZXQ9IjAlIiBzdG9wLWNvbG9yPSIjODdDRUVCIi8+CiAgICAgIDxzdG9wIG9mZnNldD0iNDAlIiBzdG9wLWNvbG9yPSIjQjhFNEY3Ii8+CiAgICAgIDxzdG9wIG9mZnNldD0iMTAwJSIgc3RvcC1jb2xvcj0iI0U4RjRGOCIvPgogICAgPC9saW5lYXJHcmFkaWVudD4KICAgIDxsaW5lYXJHcmFkaWVudCBpZD0ic2VhIiB4MT0iMCIgeTE9IjAiIHgyPSIwIiB5Mj0iMSI+CiAgICAgIDxzdG9wIG9mZnNldD0iMCUiIHN0b3AtY29sb3I9IiMxQTZCOEEiLz4KICAgICAgPHN0b3Agb2Zmc2V0PSI2MCUiIHN0b3AtY29sb3I9IiMyMTk2QTgiLz4KICAgICAgPHN0b3Agb2Zmc2V0PSIxMDAlIiBzdG9wLWNvbG9yPSIjNEREMENDIi8+CiAgICA8L2xpbmVhckdyYWRpZW50PgogICAgPGxpbmVhckdyYWRpZW50IGlkPSJzYW5kIiB4MT0iMCIgeTE9IjAiIHgyPSIwIiB5Mj0iMSI+CiAgICAgIDxzdG9wIG9mZnNldD0iMCUiIHN0b3AtY29sb3I9IiNENEE5NkEiLz4KICAgICAgPHN0b3Agb2Zmc2V0PSIxMDAlIiBzdG9wLWNvbG9yPSIjQzQ5MDUwIi8+CiAgICA8L2xpbmVhckdyYWRpZW50PgogICAgPGxpbmVhckdyYWRpZW50IGlkPSJ3YXZlMSIgeDE9IjAiIHkxPSIwIiB4Mj0iMCIgeTI9IjEiPgogICAgICA8c3RvcCBvZmZzZXQ9IjAlIiBzdG9wLWNvbG9yPSIjN0VDOEUzIiBzdG9wLW9wYWNpdHk9IjAuOSIvPgogICAgICA8c3RvcCBvZmZzZXQ9IjEwMCUiIHN0b3AtY29sb3I9IiM1QUI5RDQiIHN0b3Atb3BhY2l0eT0iMC41Ii8+CiAgICA8L2xpbmVhckdyYWRpZW50PgogICAgPHJhZGlhbEdyYWRpZW50IGlkPSJzdW4iIGN4PSI1MCUiIGN5PSI1MCUiPgogICAgICA8c3RvcCBvZmZzZXQ9IjAlIiBzdG9wLWNvbG9yPSIjRkZGMTc2Ii8+CiAgICAgIDxzdG9wIG9mZnNldD0iNjAlIiBzdG9wLWNvbG9yPSIjRkZENTRGIi8+CiAgICAgIDxzdG9wIG9mZnNldD0iMTAwJSIgc3RvcC1jb2xvcj0iI0ZGQjMwMCIgc3RvcC1vcGFjaXR5PSIwIi8+CiAgICA8L3JhZGlhbEdyYWRpZW50PgogIDwvZGVmcz4KICA8IS0tIFNreSAtLT4KICA8cmVjdCB3aWR0aD0iMTQ0MCIgaGVpZ2h0PSI5MDAiIGZpbGw9InVybCgjc2t5KSIvPgogIDwhLS0gU3VuIC0tPgogIDxjaXJjbGUgY3g9IjExMDAiIGN5PSIxNDAiIHI9IjgwIiBmaWxsPSJ1cmwoI3N1bikiIG9wYWNpdHk9IjAuODUiLz4KICA8Y2lyY2xlIGN4PSIxMTAwIiBjeT0iMTQwIiByPSI1NSIgZmlsbD0iI0ZGRTA4MiIgb3BhY2l0eT0iMC42Ii8+CiAgPCEtLSBDbG91ZHMgLS0+CiAgPGVsbGlwc2UgY3g9IjIwMCIgY3k9IjEyMCIgcng9IjEyMCIgcnk9IjM1IiBmaWxsPSJ3aGl0ZSIgb3BhY2l0eT0iMC43Ii8+CiAgPGVsbGlwc2UgY3g9IjI2MCIgY3k9IjEwNSIgcng9IjgwIiByeT0iMzAiIGZpbGw9IndoaXRlIiBvcGFjaXR5PSIwLjc1Ii8+CiAgPGVsbGlwc2UgY3g9IjE0MCIgY3k9IjExMCIgcng9IjcwIiByeT0iMjUiIGZpbGw9IndoaXRlIiBvcGFjaXR5PSIwLjY1Ii8+CiAgPGVsbGlwc2UgY3g9IjYwMCIgY3k9IjgwIiByeD0iMTAwIiByeT0iMjgiIGZpbGw9IndoaXRlIiBvcGFjaXR5PSIwLjYiLz4KICA8ZWxsaXBzZSBjeD0iNjYwIiBjeT0iNjgiIHJ4PSI3MCIgcnk9IjIyIiBmaWxsPSJ3aGl0ZSIgb3BhY2l0eT0iMC42NSIvPgogIDxlbGxpcHNlIGN4PSI5MDAiIGN5PSIxMDAiIHJ4PSI5MCIgcnk9IjI2IiBmaWxsPSJ3aGl0ZSIgb3BhY2l0eT0iMC41Ii8+CiAgPCEtLSBTZWEgLS0+CiAgPHJlY3QgeD0iMCIgeT0iMzcwIiB3aWR0aD0iMTQ0MCIgaGVpZ2h0PSIzNDAiIGZpbGw9InVybCgjc2VhKSIvPgogIDwhLS0gU2VhIHNoaW1tZXIgbGluZXMgLS0+CiAgPGxpbmUgeDE9IjAiIHkxPSI0MTAiIHgyPSIxNDQwIiB5Mj0iNDE1IiBzdHJva2U9IndoaXRlIiBzdHJva2Utd2lkdGg9IjEuNSIgb3BhY2l0eT0iMC4yIi8+CiAgPGxpbmUgeDE9IjAiIHkxPSI0NDAiIHgyPSIxNDQwIiB5Mj0iNDQ1IiBzdHJva2U9IndoaXRlIiBzdHJva2Utd2lkdGg9IjEiIG9wYWNpdHk9IjAuMTUiLz4KICA8bGluZSB4MT0iMCIgeTE9IjQ3NSIgeDI9IjE0NDAiIHkyPSI0NzgiIHN0cm9rZT0id2hpdGUiIHN0cm9rZS13aWR0aD0iMS41IiBvcGFjaXR5PSIwLjE4Ii8+CiAgPGxpbmUgeDE9IjAiIHkxPSI1MTAiIHgyPSIxNDQwIiB5Mj0iNTEyIiBzdHJva2U9IndoaXRlIiBzdHJva2Utd2lkdGg9IjEiIG9wYWNpdHk9IjAuMTIiLz4KICA8bGluZSB4MT0iMCIgeTE9IjU0NSIgeDI9IjE0NDAiIHkyPSI1NDciIHN0cm9rZT0id2hpdGUiIHN0cm9rZS13aWR0aD0iMS41IiBvcGFjaXR5PSIwLjE1Ii8+CiAgPGxpbmUgeDE9IjAiIHkxPSI1ODAiIHgyPSIxNDQwIiB5Mj0iNTgyIiBzdHJva2U9IndoaXRlIiBzdHJva2Utd2lkdGg9IjEiIG9wYWNpdHk9IjAuMTIiLz4KICA8bGluZSB4MT0iMCIgeTE9IjYyMCIgeDI9IjE0NDAiIHkyPSI2MjIiIHN0cm9rZT0id2hpdGUiIHN0cm9rZS13aWR0aD0iMS4yIiBvcGFjaXR5PSIwLjEiLz4KICA8IS0tIFdhdmUgZm9hbSAtLT4KICA8cGF0aCBkPSJNMCw2ODAgUTE4MCw2NjAgMzYwLDY4MCBRNTQwLDcwMCA3MjAsNjc4IFE5MDAsNjU4IDEwODAsNjgwIFExMjYwLDcwMCAxNDQwLDY4MCBMMTQ0MCw3MTAgTDAsNzEwIFoiIGZpbGw9InVybCgjd2F2ZTEpIi8+CiAgPHBhdGggZD0iTTAsNjk1IFEyMDAsNjc1IDQwMCw2OTUgUTYwMCw3MTUgODAwLDY5NSBRMTAwMCw2NzUgMTIwMCw2OTUgUTEzMjAsNzA3IDE0NDAsNjk1IEwxNDQwLDcyMCBMMCw3MjAgWiIgZmlsbD0id2hpdGUiIG9wYWNpdHk9IjAuMjUiLz4KICA8IS0tIFNhbmQgLS0+CiAgPHBhdGggZD0iTTAsNzAwIFEzNjAsNjcwIDcyMCw2OTAgUTEwODAsNzEwIDE0NDAsNjg1IEwxNDQwLDkwMCBMMCw5MDAgWiIgZmlsbD0idXJsKCNzYW5kKSIvPgogIDwhLS0gU2FuZCB0ZXh0dXJlIGxpbmVzIC0tPgogIDxwYXRoIGQ9Ik0wLDc1MCBRMzYwLDczMCA3MjAsNzQ4IFExMDgwLDc2NiAxNDQwLDc0NSIgc3Ryb2tlPSIjQzQ5MDUwIiBzdHJva2Utd2lkdGg9IjEuNSIgZmlsbD0ibm9uZSIgb3BhY2l0eT0iMC40Ii8+CiAgPHBhdGggZD0iTTAsNzkwIFEzNjAsNzcyIDcyMCw3ODggUTEwODAsODA2IDE0NDAsNzg1IiBzdHJva2U9IiNDNDkwNTAiIHN0cm9rZS13aWR0aD0iMSIgZmlsbD0ibm9uZSIgb3BhY2l0eT0iMC4zIi8+CiAgPHBhdGggZD0iTTAsODM1IFEzNjAsODE4IDcyMCw4MzMgUTEwODAsODUwIDE0NDAsODMwIiBzdHJva2U9IiNDNDkwNTAiIHN0cm9rZS13aWR0aD0iMSIgZmlsbD0ibm9uZSIgb3BhY2l0eT0iMC4yNSIvPgogIDwhLS0gUGFsbSB0cmVlIGxlZnQgLS0+CiAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoODAsNDIwKSI+CiAgICA8cmVjdCB4PSItOCIgeT0iMCIgd2lkdGg9IjE2IiBoZWlnaHQ9IjIyMCIgcng9IjYiIGZpbGw9IiM4QjY5MTQiIHRyYW5zZm9ybT0icm90YXRlKC01LDAsMjIwKSIvPgogICAgPGVsbGlwc2UgY3g9Ii0zMCIgY3k9Ii0xMCIgcng9IjkwIiByeT0iMjIiIGZpbGw9IiM0QTdDM0YiIHRyYW5zZm9ybT0icm90YXRlKC0yMCwtMzAsLTEwKSIvPgogICAgPGVsbGlwc2UgY3g9IjIwIiBjeT0iLTI1IiByeD0iODUiIHJ5PSIyMCIgZmlsbD0iIzVBOEM0RiIgdHJhbnNmb3JtPSJyb3RhdGUoMTAsMjAsLTI1KSIvPgogICAgPGVsbGlwc2UgY3g9Ii0xMCIgY3k9Ii00MCIgcng9Ijc1IiByeT0iMTgiIGZpbGw9IiMzQTZDMkYiIHRyYW5zZm9ybT0icm90YXRlKC0zNSwtMTAsLTQwKSIvPgogICAgPGVsbGlwc2UgY3g9IjQwIiBjeT0iLTE1IiByeD0iNzAiIHJ5PSIxNiIgZmlsbD0iIzRBN0MzRiIgdHJhbnNmb3JtPSJyb3RhdGUoMjUsNDAsLTE1KSIvPgogICAgPGVsbGlwc2UgY3g9Ii01MCIgY3k9IjEwIiByeD0iNjUiIHJ5PSIxNSIgZmlsbD0iIzVBOEM0RiIgdHJhbnNmb3JtPSJyb3RhdGUoLTE1LC01MCwxMCkiLz4KICA8L2c+CiAgPCEtLSBQYWxtIHRyZWUgcmlnaHQgLS0+CiAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMTM2MCwzOTApIj4KICAgIDxyZWN0IHg9Ii04IiB5PSIwIiB3aWR0aD0iMTYiIGhlaWdodD0iMjAwIiByeD0iNiIgZmlsbD0iIzhCNjkxNCIgdHJhbnNmb3JtPSJyb3RhdGUoNiwwLDIwMCkiLz4KICAgIDxlbGxpcHNlIGN4PSIzMCIgY3k9Ii01IiByeD0iODUiIHJ5PSIyMCIgZmlsbD0iIzRBN0MzRiIgdHJhbnNmb3JtPSJyb3RhdGUoMTgsMzAsLTUpIi8+CiAgICA8ZWxsaXBzZSBjeD0iLTIwIiBjeT0iLTIwIiByeD0iODAiIHJ5PSIxOSIgZmlsbD0iIzVBOEM0RiIgdHJhbnNmb3JtPSJyb3RhdGUoLTEyLC0yMCwtMjApIi8+CiAgICA8ZWxsaXBzZSBjeD0iMTAiIGN5PSItMzgiIHJ4PSI3MCIgcnk9IjE3IiBmaWxsPSIjM0E2QzJGIiB0cmFuc2Zvcm09InJvdGF0ZSgzMCwxMCwtMzgpIi8+CiAgICA8ZWxsaXBzZSBjeD0iLTQwIiBjeT0iLTEwIiByeD0iNjUiIHJ5PSIxNSIgZmlsbD0iIzRBN0MzRiIgdHJhbnNmb3JtPSJyb3RhdGUoLTIyLC00MCwtMTApIi8+CiAgICA8ZWxsaXBzZSBjeD0iNTAiIGN5PSI4IiByeD0iNjAiIHJ5PSIxNCIgZmlsbD0iIzVBOEM0RiIgdHJhbnNmb3JtPSJyb3RhdGUoMTUsNTAsOCkiLz4KICA8L2c+CiAgPCEtLSBEaXN0YW50IHNhaWxib2F0IC0tPgogIDxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKDc1MCw0MzApIj4KICAgIDxyZWN0IHg9Ii0xLjUiIHk9Ii02MCIgd2lkdGg9IjMiIGhlaWdodD0iNzAiIGZpbGw9IiM4QjczNTUiLz4KICAgIDxwb2x5Z29uIHBvaW50cz0iMCwtNTUgMzAsMTAgMCwxMCIgZmlsbD0id2hpdGUiIG9wYWNpdHk9IjAuODUiLz4KICAgIDxwb2x5Z29uIHBvaW50cz0iMCwtNTUgLTE4LDEwIDAsMTAiIGZpbGw9IiNGNUY1REMiIG9wYWNpdHk9IjAuNyIvPgogICAgPHJlY3QgeD0iLTE1IiB5PSI4IiB3aWR0aD0iMzAiIGhlaWdodD0iNyIgcng9IjMiIGZpbGw9IiM4QjczNTUiLz4KICA8L2c+CiAgPCEtLSBEaXN0YW50IHNhaWxib2F0IDIgLS0+CiAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoOTgwLDQ0NSkiPgogICAgPHJlY3QgeD0iLTEiIHk9Ii00MCIgd2lkdGg9IjIuNSIgaGVpZ2h0PSI1MCIgZmlsbD0iIzhCNzM1NSIvPgogICAgPHBvbHlnb24gcG9pbnRzPSIwLC0zNiAyMCw4IDAsOCIgZmlsbD0id2hpdGUiIG9wYWNpdHk9IjAuNyIvPgogICAgPHJlY3QgeD0iLTEwIiB5PSI3IiB3aWR0aD0iMjAiIGhlaWdodD0iNSIgcng9IjIuNSIgZmlsbD0iIzhCNzM1NSIvPgogIDwvZz4KICA8IS0tIEJlYWNoIHVtYnJlbGxhIC0tPgogIDxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKDQwMCw2OTApIj4KICAgIDxyZWN0IHg9Ii0yIiB5PSItNSIgd2lkdGg9IjQiIGhlaWdodD0iOTAiIGZpbGw9IiNBMDg1NkEiLz4KICAgIDxlbGxpcHNlIGN4PSIwIiBjeT0iLTUiIHJ4PSI2NSIgcnk9IjIwIiBmaWxsPSIjRTUzOTM1IiBvcGFjaXR5PSIwLjkiLz4KICAgIDxwYXRoIGQ9Ik0tNjUsLTUgUTAsLTMwIDY1LC01IiBzdHJva2U9IiNCNzFDMUMiIHN0cm9rZS13aWR0aD0iMiIgZmlsbD0ibm9uZSIvPgogICAgPGxpbmUgeDE9Ii0zMCIgeTE9Ii0xOCIgeDI9Ii01MCIgeTI9IjUiIHN0cm9rZT0iI0I3MUMxQyIgc3Ryb2tlLXdpZHRoPSIxLjUiLz4KICAgIDxsaW5lIHgxPSIzMCIgeTE9Ii0xOCIgeDI9IjUwIiB5Mj0iNSIgc3Ryb2tlPSIjQjcxQzFDIiBzdHJva2Utd2lkdGg9IjEuNSIvPgogIDwvZz4KICA8IS0tIEJlYWNoIHVtYnJlbGxhIDIgLS0+CiAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMTA1MCw3MDApIj4KICAgIDxyZWN0IHg9Ii0yIiB5PSItNSIgd2lkdGg9IjMuNSIgaGVpZ2h0PSI4MCIgZmlsbD0iI0EwODU2QSIvPgogICAgPGVsbGlwc2UgY3g9IjAiIGN5PSItNSIgcng9IjU1IiByeT0iMTciIGZpbGw9IiMxNTY1QzAiIG9wYWNpdHk9IjAuODUiLz4KICAgIDxwYXRoIGQ9Ik0tNTUsLTUgUTAsLTI2IDU1LC01IiBzdHJva2U9IiMwRDQ3QTEiIHN0cm9rZS13aWR0aD0iMiIgZmlsbD0ibm9uZSIvPgogIDwvZz4KICA8IS0tIFNlYWd1bGxzIC0tPgogIDxwYXRoIGQ9Ik0zMDAsMjUwIFEzMTAsMjQzIDMyMCwyNTAgUTMzMCwyNDMgMzQwLDI1MCIgc3Ryb2tlPSIjNjY2IiBzdHJva2Utd2lkdGg9IjEuNSIgZmlsbD0ibm9uZSIvPgogIDxwYXRoIGQ9Ik01MDAsMjAwIFE1MDgsMTk0IDUxNiwyMDAgUTUyNCwxOTQgNTMyLDIwMCIgc3Ryb2tlPSIjNzc3IiBzdHJva2Utd2lkdGg9IjEuMyIgZmlsbD0ibm9uZSIvPgogIDxwYXRoIGQ9Ik04NTAsMjMwIFE4NTcsMjI1IDg2NCwyMzAgUTg3MSwyMjUgODc4LDIzMCIgc3Ryb2tlPSIjODg4IiBzdHJva2Utd2lkdGg9IjEuMiIgZmlsbD0ibm9uZSIvPgo8L3N2Zz4=');background-size:cover;background-position:center;background-attachment:fixed;opacity:0.3;pointer-events:none;}
body::after{content:'';position:fixed;inset:0;z-index:0;background-image:linear-gradient(rgba(0,212,255,.02) 1px,transparent 1px),linear-gradient(90deg,rgba(0,212,255,.02) 1px,transparent 1px);background-size:48px 48px;pointer-events:none;}

/* HEADER */
header{position:sticky;top:0;z-index:100;display:flex;align-items:stretch;background:rgba(7,14,24,.95);backdrop-filter:blur(16px);border-bottom:1px solid var(--border);box-shadow:0 4px 40px rgba(0,0,0,.5);}
.header-brand{display:flex;align-items:center;gap:10px;padding:10px 20px;border-right:1px solid var(--border);flex-shrink:0;}
.brand-icon{width:40px;height:40px;background:linear-gradient(135deg,var(--accent),#006aff);border-radius:var(--r);display:flex;align-items:center;justify-content:center;font-size:19px;box-shadow:var(--glow-a);flex-shrink:0;}
.brand-text h1{font-family:'Barlow Condensed',sans-serif;font-size:18px;font-weight:900;letter-spacing:2.5px;text-transform:uppercase;line-height:1;}
.brand-text p{font-size:9px;color:var(--muted);letter-spacing:3px;text-transform:uppercase;margin-top:2px;}
nav{display:flex;align-items:stretch;flex:1;padding:0 8px;}
.nav-tab{display:flex;align-items:center;gap:7px;padding:0 20px;font-family:'Barlow Condensed',sans-serif;font-size:13px;font-weight:700;letter-spacing:1.5px;text-transform:uppercase;color:var(--muted);cursor:pointer;border:none;background:none;border-bottom:3px solid transparent;transition:color var(--trans),border-color var(--trans);}
.nav-tab:hover{color:var(--text);}
.nav-tab.active{color:var(--accent);border-bottom-color:var(--accent);}
.nav-tab .ti{font-size:15px;}
.tbadge{background:var(--red);color:white;font-size:9px;font-weight:700;padding:1px 5px;border-radius:10px;font-family:'Share Tech Mono',monospace;}
.header-right{display:flex;align-items:center;gap:14px;padding:0 20px;margin-left:auto;border-left:1px solid var(--border);}
.live-pill{display:flex;align-items:center;gap:7px;background:rgba(0,230,118,.08);border:1px solid rgba(0,230,118,.25);border-radius:20px;padding:5px 11px;font-family:'Share Tech Mono',monospace;font-size:11px;color:var(--green);letter-spacing:1px;}
.live-dot{width:7px;height:7px;background:var(--green);border-radius:50%;animation:blink 1.6s ease-in-out infinite;}
@keyframes blink{0%,100%{opacity:1;transform:scale(1)}50%{opacity:.3;transform:scale(.6)}}
.clock{font-family:'Share Tech Mono',monospace;font-size:13px;color:var(--muted);letter-spacing:1px;}

/* PAGES */
.page{display:none;position:relative;z-index:1;}
.page.active{display:block;}

/* SECTION LABEL */
.slbl{font-family:'Barlow Condensed',sans-serif;font-size:10px;font-weight:700;letter-spacing:4px;text-transform:uppercase;color:var(--accent);margin-bottom:12px;display:flex;align-items:center;gap:10px;}
.slbl::after{content:'';flex:1;height:1px;background:linear-gradient(90deg,var(--border),transparent);}

/* PANEL */
.panel{background:var(--card);border:1px solid var(--border);border-radius:var(--r2);overflow:hidden;}
.panel-head{display:flex;align-items:center;justify-content:space-between;padding:15px 20px;background:linear-gradient(135deg,var(--card2),var(--surface));border-bottom:1px solid var(--border);}
.panel-head h2{font-family:'Barlow Condensed',sans-serif;font-size:17px;font-weight:800;letter-spacing:2px;text-transform:uppercase;}

/* ── DASHBOARD ── */
#page-dashboard{max-width:1340px;margin:0 auto;padding:24px 22px 60px;}
.stat-strip{display:grid;grid-template-columns:repeat(auto-fit,minmax(140px,1fr));gap:10px;margin-bottom:26px;}
.stat-tile{background:var(--card);border:1px solid var(--border);border-radius:var(--r2);padding:15px 17px;transition:transform var(--trans),border-color var(--trans);animation:up .5s ease both;}
.stat-tile:hover{transform:translateY(-3px);border-color:var(--accent);}
.stat-tile .lbl{font-size:9px;letter-spacing:2.5px;text-transform:uppercase;color:var(--muted);margin-bottom:3px;}
.stat-tile .val{font-family:'Barlow Condensed',sans-serif;font-size:28px;font-weight:900;color:var(--accent);line-height:1;}
.stat-tile .sub{font-size:10px;color:var(--muted);margin-top:2px;}

.dash-grid{display:grid;grid-template-columns:1fr 350px;gap:18px;align-items:start;}
@media(max-width:840px){.dash-grid{grid-template-columns:1fr;}}

/* RANKING */
.col-hdr{display:grid;grid-template-columns:44px 1fr 68px 56px 56px 56px;padding:7px 18px;font-size:9px;letter-spacing:2px;text-transform:uppercase;color:var(--muted);border-bottom:1px solid var(--border);}
.rank-row{display:grid;grid-template-columns:44px 1fr 68px 56px 56px 56px;padding:10px 18px;border-bottom:1px solid rgba(26,46,70,.5);align-items:center;transition:background var(--trans);animation:up .45s ease both;}
.rank-row:hover{background:rgba(0,212,255,.04);}
.rank-row:last-child{border-bottom:none;}
.rank-row.r1{background:linear-gradient(90deg,rgba(255,215,64,.07),transparent);}
.rank-row.r2{background:linear-gradient(90deg,rgba(184,200,216,.05),transparent);}
.rank-row.r3{background:linear-gradient(90deg,rgba(255,143,101,.05),transparent);}
.pos-chip{width:28px;height:28px;border-radius:6px;display:flex;align-items:center;justify-content:center;font-family:'Barlow Condensed',sans-serif;font-size:14px;font-weight:900;}
.pc-g{background:rgba(255,215,64,.12);color:var(--gold);border:1px solid rgba(255,215,64,.3);}
.pc-s{background:rgba(184,200,216,.1);color:var(--silver);border:1px solid rgba(184,200,216,.25);}
.pc-b{background:rgba(255,143,101,.1);color:var(--bronze);border:1px solid rgba(255,143,101,.25);}
.pc-n{background:rgba(255,255,255,.04);color:var(--muted);border:1px solid var(--border);}
.p-name{font-family:'Barlow Condensed',sans-serif;font-size:16px;font-weight:700;}
.p-tags{display:flex;gap:4px;margin-top:3px;}
.tag{font-size:9px;font-weight:700;letter-spacing:.5px;padding:1px 5px;border-radius:3px;}
.tw{background:rgba(0,230,118,.1);color:var(--green);}
.tl{background:rgba(255,61,113,.1);color:var(--red);}
.td{background:rgba(78,107,138,.12);color:var(--muted);}
.pts-bar-wrap{width:100%;height:2px;background:var(--border);border-radius:1px;margin-top:4px;}
.pts-bar{height:100%;border-radius:1px;background:linear-gradient(90deg,var(--accent),#006aff);transition:width 1.2s cubic-bezier(.4,0,.2,1);}
.pts-big{font-family:'Barlow Condensed',sans-serif;font-size:21px;font-weight:900;color:var(--accent);text-align:center;}
.nc{text-align:center;font-family:'Share Tech Mono',monospace;font-size:13px;}
.cg{color:var(--green);}.cr{color:var(--red);}.cm{color:var(--muted);}

/* RIGHT COL */
.right-col{display:flex;flex-direction:column;gap:16px;}
.podium-wrap{background:var(--card);border:1px solid var(--border);border-radius:var(--r2);padding:16px;display:none;}
.podium-wrap.show{display:block;}
.podium{display:flex;align-items:flex-end;justify-content:center;gap:8px;height:100px;margin:12px 0 0;}
.pod-slot{flex:1;border-radius:7px 7px 0 0;display:flex;flex-direction:column;align-items:center;justify-content:flex-end;padding-bottom:7px;}
.pp1{height:100%;background:linear-gradient(180deg,rgba(255,215,64,.13),rgba(255,215,64,.04));border:1px solid rgba(255,215,64,.3);border-bottom:none;}
.pp2{height:72%;background:linear-gradient(180deg,rgba(184,200,216,.09),rgba(184,200,216,.03));border:1px solid rgba(184,200,216,.2);border-bottom:none;}
.pp3{height:52%;background:linear-gradient(180deg,rgba(255,143,101,.09),rgba(255,143,101,.03));border:1px solid rgba(255,143,101,.2);border-bottom:none;}
.pod-medal{font-size:17px;margin-bottom:3px;}
.pod-name{font-family:'Barlow Condensed',sans-serif;font-size:12px;font-weight:700;text-align:center;padding:0 3px;line-height:1.2;}
.pod-pts{font-family:'Share Tech Mono',monospace;font-size:9px;color:var(--muted);margin-top:2px;}

.rtabs{display:flex;flex-wrap:wrap;gap:4px;padding:9px 12px;background:var(--surface);border-bottom:1px solid var(--border);}
.rtab{padding:4px 9px;border-radius:5px;font-family:'Barlow Condensed',sans-serif;font-size:13px;font-weight:700;cursor:pointer;border:none;background:none;color:var(--muted);transition:all var(--trans);}
.rtab:hover{color:var(--text);}
.rtab.active{background:var(--accent);color:var(--bg);}
.rtab.done{color:var(--green);}
.rtab.partial{color:var(--amber);}

.mfeed{padding:9px;}
.mc{background:var(--surface);border:1px solid var(--border);border-radius:var(--r);padding:11px;margin-bottom:6px;transition:border-color var(--trans);}
.mc:hover{border-color:rgba(0,212,255,.3);}
.mc:last-child{margin-bottom:0;}
.mlbl{font-size:9px;letter-spacing:2px;text-transform:uppercase;color:var(--muted);margin-bottom:7px;}
.mbody{display:grid;grid-template-columns:1fr auto 1fr;align-items:center;gap:5px;}
.tea,.teb{display:flex;flex-direction:column;gap:2px;}
.teb{text-align:right;}
.tp{font-family:'Barlow Condensed',sans-serif;font-size:13px;font-weight:600;line-height:1.2;}
.sbox{display:flex;align-items:center;gap:4px;}
.sn{font-family:'Barlow Condensed',sans-serif;font-size:22px;font-weight:900;min-width:22px;text-align:center;line-height:1;}
.ssep{color:var(--muted);font-size:12px;}
.sw{color:var(--accent);}.sl{color:var(--muted);}.sz{color:var(--border);}
.wtag{font-size:8px;letter-spacing:1px;text-transform:uppercase;padding:2px 5px;border-radius:3px;background:rgba(0,212,255,.1);color:var(--accent);margin-top:2px;display:inline-block;}

/* ── PLACAR ── */
#page-placar{max-width:980px;margin:0 auto;padding:24px 22px 60px;}
.rf-bar{display:flex;flex-wrap:wrap;gap:5px;margin-bottom:16px;align-items:center;}
.rf-lbl{font-size:10px;color:var(--muted);letter-spacing:2px;text-transform:uppercase;margin-right:4px;}
.rfbtn{padding:5px 11px;border-radius:5px;font-family:'Barlow Condensed',sans-serif;font-size:13px;font-weight:700;cursor:pointer;border:1px solid var(--border);background:none;color:var(--muted);transition:all var(--trans);}
.rfbtn:hover{color:var(--text);border-color:var(--border2);}
.rfbtn.active{background:var(--accent);color:var(--bg);border-color:var(--accent);}
.placar-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(290px,1fr));gap:12px;}

.se{background:var(--card);border:1px solid var(--border);border-radius:var(--r2);overflow:hidden;transition:border-color var(--trans),box-shadow var(--trans);}
.se:hover{border-color:var(--border2);}
.se.done-se{border-color:rgba(0,230,118,.3);}
.se.done-se .se-head{background:linear-gradient(135deg,rgba(0,230,118,.07),transparent);}
.se-head{padding:9px 15px;background:var(--surface);border-bottom:1px solid var(--border);display:flex;align-items:center;justify-content:space-between;}
.se-lbl{font-family:'Barlow Condensed',sans-serif;font-size:10px;font-weight:700;letter-spacing:2px;text-transform:uppercase;color:var(--muted);}
.se-status{font-size:9px;padding:2px 7px;border-radius:10px;font-family:'Share Tech Mono',monospace;}
.st-done{background:rgba(0,230,118,.1);color:var(--green);}
.st-empty{background:rgba(78,107,138,.1);color:var(--muted);}
.se-body{padding:13px 15px;}
.se-teams{display:grid;grid-template-columns:1fr auto 1fr;align-items:center;gap:8px;margin-bottom:11px;}
.se-team{display:flex;flex-direction:column;gap:2px;}
.se-team.r{text-align:right;}
.se-player{font-family:'Barlow Condensed',sans-serif;font-size:14px;font-weight:700;line-height:1.2;}
.se-vs{font-family:'Barlow Condensed',sans-serif;font-size:12px;font-weight:700;color:var(--muted);text-align:center;}
.si-row{display:grid;grid-template-columns:1fr 28px 1fr;align-items:center;gap:7px;}
.si{width:100%;text-align:center;background:var(--surface);border:1.5px solid var(--border);color:var(--text);border-radius:var(--r);padding:9px 4px;font-family:'Barlow Condensed',sans-serif;font-size:26px;font-weight:900;outline:none;transition:border-color var(--trans),box-shadow var(--trans),color var(--trans);-moz-appearance:textfield;appearance:textfield;}
.si::-webkit-inner-spin-button,.si::-webkit-outer-spin-button{-webkit-appearance:none;}
.si:focus{border-color:var(--accent);box-shadow:var(--glow-a);background:rgba(0,212,255,.04);}
.si.win-i{border-color:var(--green);color:var(--green);}
.si.lose-i{color:var(--muted);}
.si-sep{font-family:'Barlow Condensed',sans-serif;font-size:16px;color:var(--muted);text-align:center;}
.btn-save{width:100%;margin-top:9px;padding:9px;background:linear-gradient(135deg,var(--accent),#006aff);color:var(--bg);border:none;border-radius:var(--r);font-family:'Barlow Condensed',sans-serif;font-size:13px;font-weight:800;letter-spacing:1.5px;text-transform:uppercase;cursor:pointer;transition:transform var(--trans),box-shadow var(--trans);box-shadow:var(--glow-a);}
.btn-save:hover{transform:translateY(-2px);box-shadow:0 0 24px rgba(0,212,255,.35);}
.btn-save:active{transform:translateY(0);}
.btn-clr{width:100%;margin-top:5px;padding:6px;background:none;border:1px solid var(--border);color:var(--muted);border-radius:var(--r);font-family:'Barlow Condensed',sans-serif;font-size:11px;font-weight:600;letter-spacing:1px;cursor:pointer;transition:color var(--trans),border-color var(--trans);}
.btn-clr:hover{color:var(--red);border-color:var(--red);}

/* ── ATLETAS ── */
#page-atletas{max-width:680px;margin:0 auto;padding:24px 22px 60px;}
.atletas-intro{background:rgba(0,212,255,.06);border:1px solid rgba(0,212,255,.15);border-radius:var(--r2);padding:15px 18px;margin-bottom:20px;font-size:13px;color:var(--text2);line-height:1.6;}
.atletas-intro strong{color:var(--accent);}
.atleta-row{display:grid;grid-template-columns:42px 1fr auto;align-items:center;gap:10px;background:var(--card);border:1px solid var(--border);border-radius:var(--r);padding:9px 14px;margin-bottom:7px;transition:border-color var(--trans);}
.atleta-row:hover{border-color:var(--border2);}
.atleta-num{font-family:'Barlow Condensed',sans-serif;font-size:17px;font-weight:900;color:var(--accent);width:34px;height:34px;background:rgba(0,212,255,.08);border:1px solid rgba(0,212,255,.2);border-radius:var(--r);display:flex;align-items:center;justify-content:center;}
.atleta-input{background:var(--surface);border:1.5px solid var(--border);color:var(--text);border-radius:6px;padding:7px 11px;font-family:'Barlow Condensed',sans-serif;font-size:16px;font-weight:700;width:100%;outline:none;transition:border-color var(--trans),box-shadow var(--trans);}
.atleta-input:focus{border-color:var(--accent);box-shadow:var(--glow-a);}
.atleta-input::placeholder{color:var(--muted);font-weight:400;}
.atleta-sb{padding:7px 14px;background:rgba(0,212,255,.1);border:1px solid rgba(0,212,255,.25);color:var(--accent);border-radius:6px;font-family:'Barlow Condensed',sans-serif;font-size:12px;font-weight:700;letter-spacing:1px;cursor:pointer;transition:all var(--trans);white-space:nowrap;}
.atleta-sb:hover{background:var(--accent);color:var(--bg);}
.atletas-actions{display:flex;gap:10px;margin-top:18px;}
.btn-act{flex:1;padding:11px;border-radius:var(--r);font-family:'Barlow Condensed',sans-serif;font-size:13px;font-weight:800;letter-spacing:1.5px;text-transform:uppercase;cursor:pointer;transition:transform var(--trans),box-shadow var(--trans);border:none;}
.btn-pri{background:linear-gradient(135deg,var(--accent),#006aff);color:var(--bg);box-shadow:var(--glow-a);}
.btn-pri:hover{transform:translateY(-2px);box-shadow:0 0 24px rgba(0,212,255,.4);}
.btn-dng{background:rgba(255,61,113,.1);border:1px solid rgba(255,61,113,.3);color:var(--red);}
.btn-dng:hover{background:var(--red);color:white;}

/* TOAST */
#toast{position:fixed;bottom:26px;right:26px;z-index:999;background:var(--green);color:var(--bg);padding:11px 20px;border-radius:10px;font-family:'Barlow Condensed',sans-serif;font-size:15px;font-weight:800;letter-spacing:1px;transform:translateY(80px);opacity:0;transition:transform .35s cubic-bezier(.4,0,.2,1),opacity .35s;pointer-events:none;max-width:300px;}
#toast.show{transform:translateY(0);opacity:1;}
#toast.err{background:var(--red);color:white;}

@keyframes up{from{opacity:0;transform:translateY(14px)}to{opacity:1;transform:translateY(0)}}
::-webkit-scrollbar{width:5px;}
::-webkit-scrollbar-track{background:var(--bg);}
::-webkit-scrollbar-thumb{background:var(--border);border-radius:3px;}

@media(max-width:580px){
  .header-brand{padding:11px 14px;}
  .brand-text h1{font-size:14px;}
  .nav-tab{padding:0 12px;font-size:11px;}
  .nav-tab .ti{display:none;}
  .clock{display:none;}
  .header-right{padding:0 10px;}
  .col-hdr{grid-template-columns:38px 1fr 58px 48px;}
  .rank-row{grid-template-columns:38px 1fr 58px 48px;}
  .rank-row>*:nth-child(5),.rank-row>*:nth-child(6),
  .col-hdr>span:nth-child(5),.col-hdr>span:nth-child(6){display:none;}
}
</style>
</head>
<body>

<header>
  <div class="header-brand">
    <div class="brand-icon" style="background:transparent;box-shadow:none;padding:0;overflow:hidden;border-radius:var(--r);width:120px;height:40px;"><img src="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQEBKgEoAAD/2wBDAAYEBQYFBAYGBQYHBwYIChAKCgkJChQODwwQFxQYGBcUFhYaHSUfGhsjHBYWICwgIyYnKSopGR8tMC0oMCUoKSj/2wBDAQcHBwoIChMKChMoGhYaKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCgoKCj/wAARCAMABYADASIAAhEBAxEB/8QAHwAAAQUBAQEBAQEAAAAAAAAAAAECAwQFBgcICQoL/8QAtRAAAgEDAwIEAwUFBAQAAAF9AQIDAAQRBRIhMUEGE1FhByJxFDKBkaEII0KxwRVS0fAkM2JyggkKFhcYGRolJicoKSo0NTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqDhIWGh4iJipKTlJWWl5iZmqKjpKWmp6ipqrKztLW2t7i5usLDxMXGx8jJytLT1NXW19jZ2uHi4+Tl5ufo6erx8vP09fb3+Pn6/8QAHwEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoL/8QAtREAAgECBAQDBAcFBAQAAQJ3AAECAxEEBSExBhJBUQdhcRMiMoEIFEKRobHBCSMzUvAVYnLRChYkNOEl8RcYGRomJygpKjU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6goOEhYaHiImKkpOUlZaXmJmaoqOkpaanqKmqsrO0tba3uLm6wsPExcbHyMnK0tPU1dbX2Nna4uPk5ebn6Onq8vP09fb3+Pn6/9oADAMBAAIRAxEAPwD6oFLSUtACUUtFACUYpaSgAopaKAEo60tFACUUv1ooASilooASjFLRQAlFLSUAGKKWkoAKKWigBKKWkoAKKWkoAKMUtFACYoxS0UAJRS0UAJRS0lABRilooAQCjFLSUAFFLRQAlGKWigBKMUtIaACjFLRQAlFLRQAlFLSGgAopaKAEoxSmkoAKKWkoAKMUtJQAUUtFACUUtJQAUUtIaACilooAQUGlooASgiiigAopTSUAFFLRQAlFLRQAlGKWkoAKMUtJQAUYpaSgAxRilpKACiloNACUYpaKAEoNLRQAlGKWigBKKWkoAMUYpaKAEoxS96KAEopaSgA6UYpaTvQAUUtFACUUtFACCjFLRQAlHWlooASilooASilooASilooASilpKACjFLRQAgopaKAEopaKAExRilooASilpKACjFLR3oASilpKACjFLSUAFFLRQAlFLRQAlGKWigBKKKWgBKMUtJ3oAKKWigBKKWigBKMUdKWgBKKWigBKKWigBMUdaWigBKKWkoAKMUtJQAUUtFACUUtFACUUtFACUUtFACUtFFABRRRQAUUUUAJRRRQAUUUUAFLRQKACiiigAooooAKKKKACiiigAooooAKKKKAA0UUUAFFFFABRRRQAUUUUAFFFFABRSUtABRRRQAUUUUAFFFFABRRRQAUUUUAFFJS0AFFFFABRRRQAUUUUAFFFFABRRRQAUUlLQAUUlLQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRSUtABRRRQAUUUUAFFFFABRRRQAUUUUAFFJS0AFFFJQAtFJS0AFFFFABRRRQAUUUUAFFFFABRRRQAUd6KKACiigUAFFFFABRRRQAUUUUAFFJS0AFFJS0AFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRSUUALRRRQAUGiigAooooAKKKKACiiigAooooAKKSloAKKKKACiiigAopKWgAooooAKKKKACiiigAooooAKKKKACikpaACiiigAooooAKKKKACiijvQAlFFFABS0lFAC0UlFAC0UUUAFFFGKACig0UAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRigAooooAKKKKACiiigAooooAKKKKACkFLRQAUUUUAFFFFABRRRQAUYoooAKKKKACiiigAooooAKKKBQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFACUtFFABRRRQAUUUUAFFFFABSUtFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUABooooAKKKKAEpaKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKAEooNFABRRRQAd6WikoAWiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAoFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFHeigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKAEooooAKKBRQAtFJS0AFFFFABRRRQAUUUUAFFFFABRRRQAUUUd6ACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRQaKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooNFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAJRRRQAUUUUAFLSUtABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAhooooABQaKKACloooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAMUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKBQAUUUUAFFFFABRRRQAUUUUAFFFFACUUUUAFBoooAWikpaACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigBKKKKACg0UUALRSUtABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAlFFFABQaKKAFopKWgAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiig0AFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFBoooASilpKACiig0ALRSUtABRRmigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigBKKWkoAKKKKAFopKWgAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooozQAGkpaSgAooozQAUtJS0AFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAlLRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABQKKKAEpaKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACikpaAEpaKKACiiigAooooAKKKKACiiigApKWigBKWiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooASiiigAooooAWikpaACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiig0AFFJmlzQAUUmaWgAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooASig0UAFFFFABS0lLQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABQeOTVa8vILG2kuLuWOGCMZZ3OABXk3iv4rPIz2/h1NidDdSrkn/AHV/qfyrKdaMFqB6xqGo2enQGa/uobeP+9K4X+dcTq3xS0O03CzS5vmHeNNq/m2P5V4pf3t1fzme9uZJ5SfvytuNaOkeFtZ1gBrDT7iWM/8ALRhsT/vo4FccsVObtBFWOzu/jBdlj9j0mBB/01lLH9AKqD4u6zn/AI8bDHp8/wDjUdr8JtdmAM89jbZ6gsXI/IYq5/wp7UMf8ha1z/1yb/Gl+/YaElp8X7wMBdaTA4/6ZzFT+oNdFp3xX0acgXlteWpPcqHX8wc/pXH3Pwn12FSYLixuPYOyn9RWBqPg3xBpoLXGlXJRerw4kH/juaPaV4boND3nSfFGiargWOpW8jn+Attb/vk4NbORXybJmNyrjDg9CMEVs6P4w1zSCBZahKYx/wAs5T5ifken4VccZ/MhWPpnNLXknh/4uRvtj12yaI9PPtvmX8VPI/WvSdH1mw1i3E2m3UNxH3KNkj6jqK6oVoz2EaVFIKWtQCiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigBKKKKACg0UUALRSUtABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUlAC0UUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFBoooAQ1keJNesdA057zUJQqDhUH3nb0UdzT/EesWuhaVLfXzlYkGAo+87dlHqTXzd4r8Q3viPVGur1iFHEUQPyxL6D39TXNXrcistxpF3xj4tv/FF2TcMYrRD+6tlPyr7n1PvUXhXwpqfiW4K2MYWBTiS4k4Rfb3PsK3Phz4Dk8ROt7qIeLSkPAHDTn0HovvXvFhZW9haR21nCkMEYwiIMACuenRdR80xnJ+Ffh5pGihJJoxfXg6yzjKg/7K9B+prtQAAAMACilFd0IKKsiQoooqwCkpaKVgMnV/D+lauhXULC3nz/ABMnzf8AfQ5rgtb+ENjMGfRryW0fqI5f3ifn1H616nSYrOVGMt0B81eIPBmt6ES95aF7cf8ALeD50/HuPxrL027utNuVubC4kt5l6PG2D+Pr+NfVJUHg8j0rjvEXw90bWJTNEjWNyTlntwAG+q9PxrlnhGtYMdznfCXxQWRktvEaCNjwLuMYT/gS9vqK9QgljnhSWF1kjcblZTkEeorz0fCfSP4r6/J/3lH/ALLW54X8KzeG32WWq3E1kTzb3CBgv+6RjFb0faLSYHVUUUldAhaKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooASig0UAFFFFAC0UlLQAUUUUAFFBooAKKKBQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRmgAqOeaOCGSaZxHGilmZjgADvTyQK8j+MfinJGg2UhA4a6ZT+Sf1P4VlVqKnG4HJePvFL+JtWLIWXT4CVgjPf1cj1P6CrHw78GHxJffaLtWXS4G/eN0Mrf3B/U1ieF9EuPEWswWFtxu+aSTHEaDq39B719JaTp9tpWnQWVlGI4IV2qP6n3NcdGm6sueRWxLb28VtDHFBGscca7UVRgKPQVLS0V6CSRIUUUUwCiiigAooooAKKK4/xz43s/DUfkRqLnUXGVhB4Qdi57D26mpnNQV2B1V1cw2sLS3EqRRqMl3YKB+JrjtS+JvhyyYolzLduO1vGWH5nArxfxBr+pa7P5upXLy85VBxGn0XpVXTdH1HVWxptjcXPOC0afKPqelcEsXKT9xFWPWn+L+mhj5emXjD1LIP61bsvizoMzBbmK8tSe7xhh/46TXh15bzWd3Na3KGOeFijrnOCKs22i6pd6eb61sJ57QMVMka7sEdcgc1CxNS4WPpfR9e0vWULaZfQXOOoRvmH1HUVp5FfJVtLNbTrNbySQzIeHRirKfrXrPgX4lPujsfEbg5IVLwDGP8AfH9a3pYpN2kKx68KKajKyqVIYEZBHenV2CCiiimAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAJRRRQAUGiigBaKSloAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigApKWmt0zSYGF4012Pw9oNxfSYMgGyFD/G56D+v4V8z3NxLc3Uk87tJNIxd2PJZiea7v4x642peIBYQtm2sPl46GU/eP4dPzqD4R+Hf7Z8RC7uUzZ2OJD6NJ/Cv4dfwFebWbqz5UUj074XeGhoGhLLcJjULsCSbI5Qfwp+Hf3zXaimgAU6u+nHljYkKKKK0AKKKKACiiigApM0tMc4HWk3YDmPiD4qj8MaP5ibXvpyUt4z0z3Y+w/wAK+ebi7lvLmSe4kaaeVtzs3LMxra+JGttrviq7lVibeAm3gA6bVPJ/E5NdP8GPC6X1zJrd7Hvht32W6noZO7fh29/pXm1G60+VbFbGt4F+GyGOO+8SISWw0dnnAA9X9T7fnXqUNvDbwrFBGkUSDCoihQB7AVKvSnYrtp0owVkTc+dPizpj2PjS7fbiK6VZ0Prxg/qDXTfAzVViub7SZmx52LiHJ6kDDD8sH8DXWfFjw6dY0EXVsm68ssyKAOXT+Jf6/hXh+nXk2nX9veWkmyeFw8Z9/f27GuKf7mrd7DPe/F3gXS/EETyrGtpqGMrcRrjJ/wBsfxD9a8K1zR7zQtSeyv4vLlXkHqrr/eU9xX0H4P8AE9p4k01Z4CEuUAE8BPMbf4ehqn8RPDUfiPQ5FjUC/gBkt3HXPdfof8K2rUY1I80dwuch8I/FzCVNC1CTcrD/AEV2PT/pn/h+VetZr5JSWe2uFkjZop4m3Ke6sD/jX074R1hdd8PWWoLgNKnzgdnHDD8waMNVbXK+gM2qKB0ortEFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFACUUtJQAUtJQaAFopKWgAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACsbxbrCaH4fvL9iN8aYjB/ic8KPzrZPSvG/jlrJa4stIib5Yx9olA9Two/maxrVOSLYI81lZ5pGaQmSV23E9SzE/419F+AdBXw/wCGrW1ZQLhx5s59Xbr+XT8K8a+F+kjWfFlr5i7oLUfaZPTj7o/PH5V9EVz4SF7zY2FFFFdwgooooAKKKKACiiigArK8UXZsPD2o3SnDRW7sPrjj9a1a5v4jgnwRrG3r5B/mKip8LYHzWYsgknJxX0z4JtbWw8M6fZ2skTmKFS+xgfmIyxOPcmvmvBqS3nltpBJbyNFIOQ0blSPxFeVRrezbbRTPq7NLXgfh74navpbJHfn+0bYcESHEg+jd/wAa9h8M+JtO8R2fn6dNuK8SRNw8Z9CP69K9GnXjPYVjabkV4r8TvAs1nNLq2iQl7RiXmgQcxHuyjuvt2+le1ZprKD1p1aaqLUEfKel6peaZeJd6fcPBOvAdD1HoR3Hsa9R8P/FgFVi1yyYN3ntuQfqp/pW94r+GemaxJJc2Df2feMcsUXMbn1K9vqK861P4d+ItPZttkLqMdHtnDZ/A4P6VxOFWltsMxPFrWdz4ivrjTJA9rM/mqdpXGRkjB9816h8Cbsvo2pWTHIgnDr7Bx/iDXkl5bTWkxhuoZYJgASki7SPfFenfAcH7RrR7bYf/AGapw7bq6gz1wCloor1SQooooAKKKKACiiigAooooAKKKKACiiigAooooASilpKACiiigBaKSloAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigBrEAEngCvlzxfqTav4l1G9ySssxCZ/uDhf0FfRPja+Om+FNVulOHSBgv8AvHgfqa+ZkjMpWNBl2IVfqeBXBi5aqI0e1/BPSfsvh2bUXTEl7J8pP/PNeB+u6vSao6HYrpmjWVlGAFghWP8AEDn9avV10o8sUgYtFFFaCCiiigAooooAKKKKACs/X7T+0NFvrTGTPA8Y+pU4rQprDPSpkrqwHyYzlcowKuMqR6EV7h4e0HQPF/hSwu7mwg+0NGEkkhHluHXg8j6Z5rzn4qaE2jeKZpY0Itb3M8ZxwG/iX8+fxFW/hP4rXRdRfT7+TbYXTAhyeIpOgP0PAP4V5tNKE3GRQ7xr8Ob3RY5LzTHe9sBywx+9jHqQPvD3FcjompXuj6hHe6bMYpk6HqGHow7ivqgDcnYgj8CK8T+K3hKPR7xdT06MLZXL4kQDiKTrx6A1dajyLngCPUvBviGDxJo0d5EBHMPkmizkxv6fTuK3q+fvhhrZ0fxPDHI+La8xBIM8An7rfgePxr6BHSunD1faRE0FNfpxS54rhfij4sTRtMawtJB/aNyuODzEh6sfQ9hWlSajG7EeSfEHVBqvi3ULmI7oQ4ijI7qoxn8816T8C7NotDv71h/x8T7V91QY/mTXkNraS3t3BbWqF5pnCRqO5NfTHhzSotF0Oz0+HBEEYUkfxN1Y/ic1xYaLnNzGzSpaSlr0EIKKKKYBRRRQAUUUUAFFFFABRRRQAUUUUAFFFFACUUGigAoNAooAKWkpaACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAoPSig0mB598a7z7P4OEIODcXCRn6DLf0ryXwNbi+8YaRARkG4VyPZfm/pXovx8cjStJj/vXDH8l/+vXE/CCPzPHl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yQQqNqIBy3+yo71k+LPEWn+ENIV2RfMI2W9tGAu4+w7KO5r591/XL/XtRa71KYyOfuqOFjX0UdhRzqgrR3A67xf8QdR13zILQtZWB48tD87j/aYfyH61yen2F1qd2ttp9vLcTt0SNc4HqfQe5rqvAvgG98QBLu9L2mmHo2P3ko/2R2Hua9u0TRbDRLQW2m20cEY6kD5nPqx6k1EKM6z5psNjzTwv8KCSk/iOYev2WBv/AEJ/6D869R03TbLTbVbewtoreFeiIuB+PrVulrthSjDZCE2j0opaK1AKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooASiiigAooooAWikpaACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKQjPWlpKQCY9qMD0FOxxSYpcqATAoAx0FOxRRYBAKWiiqAKKKKACiiigApCOKWigBuKUCloxSsgEIzRjApaKLAFFFFMAooooAQ0EA0tJSATHtQKWlosAUUUUwCiiigAooooAKKKKAGlcnmjaKdSUrAJijApcUUWAMUYpaKLAJijFLRRYBpWlpcUUWAaRmjFOpMUNAIAKWiloQBRRRTAKKKKAEI7UYApaKVgEApaKKYDSuTmjaKdRQKwmBSYFOooCwmBRgelLRQFhMUUtFAxKTaM5706igLDCucUBBin0YoFYbtFKBilooGFFFFABRRRQAmAaTABp1FACYFGBS0UBZDQopSMjGaWigBoUUbRTqKQrDSOO9AFOpKBgAKCM0UUwAcDFLRRQAUUUUAFFFFACY5z3paKKAExmjFLRQFgooooAQ0jAHrTqKAGBQBTsUtFArCYpaKKBiUUtFADSoJyQKAKXFLQAUUUUAFFFFABRRRQA0qCckZpdo9KWigVhhT8KXHHFOpkrLHGzu21VBJPoKl7DPnf4sTbvHeoAdEWND+CA/1rvvgSD/AGDqL9musfki15H4mvv7V1/UL8fduJ2Zf93oP0Ar3D4PWLWfgu3eRdr3Ujz/AIE4H6AV59HWq2M7ms3xFq9roekz3962Ioxwo6u3ZR7mtAnArwD4q+KjrWuGytmP2CxYoMdHk6M34dB+PrXXWq8kQOd8R6tda/qk1/fv87cKg+7GvZRXcfDL4fC+8vV9ciP2XO63t3H+t/22/wBn0Hesz4XeF18Q6qbm9j3abaEFh2lk6hfp3P8A9evfVAVQqgADgAdq58PR5/fkDGRRrEgVAAo6AdBT6WgV3JWEFFFFMAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooASilpKACiiigApaSloAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAK5P4nar/ZXg+9ZGxNcD7PH65bg/pmusrxf44ar5+q2emRtlbZDLIP8AbbgfkB+tY158sGNHnmn2T6hfW1nAMyTyLEuO2TivqOxtY7OzgtoBiKFFjUewGK8S+Del/bfFDXbrmKxiLg/7bcD9MmvdaxwkLR5n1BnO+PNX/sTwtf3iMBKseyP/AH24H88/hXzNBHJPcRwxDfNIwRR/eYnA/U17D8dNRBXT9KQ9zcyAe3yr/WuS+FGjjUfGVs7ruitFNw31HC/qc/hWVZ89TkQ0e1+EdFi0DQbWxiC7o1zIw/ic/eP51tikUHGDS4rvguVWJFoooqgCiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAoopKACilpKAAUUUUALRSUtABRRRQAUUfWigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAhuJFhiaR22ooLMfQCvlrxBqjavrt9fuTm4mLKPReij8gK95+K+pnTPBl4EOJrnFsmOvzdf0zXz5p9lJfX9vZwjMk8ixJ+JxXn4mV5KJSPePgzpv2Pwkt1IuJb2Qy/8AHC/yz+Nd4elVdOtY7Gxt7SFcRQRrGo9gMVj+PdX/sXwpqF2pxL5flxf77cD+efwrqi+SAjw/wAd6p/bPivULpGzEH8mL/cXj9eT+Nel/BPS/s+h3WpOvz3cm1Dj+BOP5k/lXicO+V0iiG6RyEUerE4FfUug2CaXotlYxgAQRKnHcgcn881y4Zc9RzYMv0UUV6AgooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAMUUUUAFFFFABRRRQAUUUUAFFFFACUUGigAooFFAC0UgpaACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKDRWfrur2Wiae95qMwihXj1LH0A7mlJpK7A8o+N+p+fq1npqH5LaMzOP8AabgfoP1rM+DekC98V/a3UGKyjMnP99uF/TcfwrmfEOpNrGt3t++R58hZQey9APyxXsnwc0v7D4W+1yJtlvZDJ77Bwv8AIn8a86n+9rXKO6IwK8e+PGrZbTtJjb1uZQPyX/2avYm6V8yeO9R/tnxXqN2rZj8zyo/9xflH8s/jW+KlyxsJF/4VaV/anjKzLruitQbl/wAPu/qR+VfRajArzH4G6T5GkXmpyLh7qXy0J/uJ/wDXJ/KvTqrDQtG4MdRRRXSIKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooASig0UAHeiiigBaKSloAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigBCcCvnf4k+In13xHOiufsdo5hgUHgkHDN9Sf0r6Eugxt5fL+/tO364r5KdXEjLJ98Ehs/3s81xYuTskNHaeB/Bd34lkEzH7PpqNh5mHL+qoO/1r6BtYIrW2iggQJFEoRFHYAYArzv4eeNNAi0DT9NmuFsrmCIRssw2qzdyG6cnn8a9EhljmjDxOsiNyGU5B/Grw8YxWgMyfGuonSvCup3iHDxwkIfRjwP1NfNMcbSFI0GZGIVfcmvpnxXYpqfh3UbSU4WWFhn0IGQfzAr5lQEIGzhgMgj1FYYt3khpH1D4e01NJ0SxsYwAIIlQ47nufxOa0apaLK8+j2E0pJeSCNm+pUE1drvj8KsSFFFFUAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAhooooAKDRRQAUtJS0AFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAh54ryLx78Nbm41CbUtACP5rb5bVm2nd3ZT0/CvXqQjPWs6lNTVmCPlrUNKvtMfZqFrNbNnH71CAfx6GpdM1rUdJfdp17Nbn0jb5T9V6Gvpu4t4biJop4kljPVXUMD+BrjNc+Geg6kWe3jksJjzut2wv/fJ4/LFccsLKLvFlXPO7z4m61daRNZSpbeZKpjNwoKsFPB46Z965TRLCXVdUtdPtgWedwgx2Hc/QCvQpfg9dCYiLV4DGT1eEhvyBxXdeCvBFh4XDTRs1xfONrTuMYHoo7CkqNSclzhc6e2hW3tooY+EjUIPoBipKWivQWiJCiiimAUUUUAFFFBoAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKAENFBooAKKKDQAtFJS0AFFFFABRRRQAUUUCgAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooATFLRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFACUUUUAFBooNAC0UlLQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAJRS0lAB3ooooAWikpaACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKAEpaKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKAEopaSgAo7UUUALRSUtABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABQaKKAEopTSUAFFFBoAWikpaACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiig0AJRSmkoABQaKKAClpKWgAooooAKKKKACiiigAooooAKKSloAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACikpaACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKDSUALRQKKACiiigAooooAKKKKACiiigAooooAKKSloAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAoopKAFopKWgAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAoooNACGig0UAFFFFABS0lLQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAJRRRQAUUUUALRSUtABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAlFBooAKKKKAClpKWgAooooAKKKKACiigUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFACGjvRRQACiiigBaKSloAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKAEooooAKKKKAFooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKAENFBooAO9LSUtABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUhpaSgAooooAWik70tABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFIAooooAKKKKYBRRRSAKKKKYCUGiigANJS0lACiloooAKKKKACikpaACg0lLQAUho70UALSUUUALmikpaACiiigANFFFABRRRQAUUUlAC0UGgUABooooAKM0UlAC0UlLQAUUUlAC0UUlAC0UUlAC0UlFAC0UUUAFFFFABRRSZoAWikooAWiiigANJS0UAFFJRQAtGaKTNAC0UUlAC0UUUAFFFFABmiiigAooooAKKKKACiiigAooNFABRRSUALRRRQAUUGigAopKWgAooooAKKKKACiikoAXNFFJQAtFFFABRSUtABRRRQAUUUlAC0UUlAC96KKKACikpaACijNFAB0oopKAFooooAKKKKACiijNABRRSUALRSUtABRRRQAUUUgoAWiiigAopKKACloooAKKKQUALRRSUALRRRQAUUUUAFFJRQAtGaM0CgAopKWgAopKWgAooooAKKKKACjtRScUALRSUtABRRSUALmiikoAWikzRQAtFFFABRRSUALmiikoAWikooAWiikoAWikooAWjNJS0AFJRRSAKKKWmAlFFFABSClNJQB//2Q==" style="width:100%;height:100%;object-fit:contain;object-position:center;" alt="Super Liga BT"></div>
    <div class="brand-text">
      <h1>Super Liga BT</h1>
      <p>Torneio de Duplas · Beach Tennis</p>
    </div>
  </div>
  <nav>
    <button class="nav-tab active" onclick="goTab('dashboard')" id="tab-dashboard">
      <span class="ti">📊</span> Dashboard
    </button>
    <button class="nav-tab" onclick="goTab('placar')" id="tab-placar">
      <span class="ti">⚡</span> Placar
      <span class="tbadge" id="pbadge" style="display:none">0</span>
    </button>
    <button class="nav-tab" onclick="goTab('atletas')" id="tab-atletas">
      <span class="ti">👥</span> Atletas
    </button>
  </nav>
  <div class="header-right">
    <div class="live-pill"><div class="live-dot"></div>AO VIVO</div>
    <div class="clock" id="clock">--:--:--</div>
  </div>
</header>

<!-- DASHBOARD -->
<div class="page active" id="page-dashboard">
  <div id="page-dashboard-inner" style="max-width:1340px;margin:0 auto;padding:24px 22px 60px;">
    <div class="slbl">Estatísticas do Torneio</div>
    <div class="stat-strip" id="statStrip"></div>
    <div class="dash-grid">
      <div>
        <div class="slbl">Ranking Geral</div>
        <div class="panel">
          <div class="panel-head">
            <h2>Classificação</h2>
            <span style="font-size:9px;color:var(--muted);font-family:'Share Tech Mono',monospace">PTS · V · D · E</span>
          </div>
          <div class="col-hdr">
            <span>#</span><span>Atleta</span>
            <span style="text-align:center">Pts</span>
            <span style="text-align:center">V</span>
            <span style="text-align:center">D</span>
            <span style="text-align:center">E</span>
          </div>
          <div id="rankingList"></div>
        </div>
      </div>
      <div class="right-col">
        <div class="podium-wrap" id="podiumWrap">
          <div class="slbl">Pódio</div>
          <div class="podium" id="podium"></div>
        </div>
        <div>
          <div class="slbl">Partidas</div>
          <div class="panel">
            <div class="panel-head" style="padding:10px 16px;">
              <h2 style="font-size:14px;">Por Rodada</h2>
              <span id="ovProg" style="font-size:9px;color:var(--muted);font-family:'Share Tech Mono',monospace"></span>
            </div>
            <div class="rtabs" id="dashRTabs"></div>
            <div class="mfeed" id="dashMFeed"></div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>

<!-- PLACAR -->
<div class="page" id="page-placar">
  <div style="max-width:980px;margin:0 auto;padding:24px 22px 60px;">
    <div class="rf-bar" id="rfBar">
      <span class="rf-lbl">Rodada:</span>
      <button class="rfbtn active" onclick="filterRound('all',this)">Todas</button>
    </div>
    <div class="placar-grid" id="placarGrid"></div>
  </div>
</div>

<!-- ATLETAS -->
<div class="page" id="page-atletas">
  <div class="atletas-intro">
    ✏️ <strong>Edite os nomes dos 12 atletas.</strong><br>
    Os nomes aparecem automaticamente no Ranking, Placar e Partidas.
    Pressione <strong>Enter</strong> para avançar ao próximo atleta.
  </div>
  <div id="atletasList"></div>
  <div class="atletas-actions">
    <button class="btn-act btn-pri" onclick="saveAllAtletas()">💾 Salvar todos</button>
    <button class="btn-act btn-dng" onclick="confirmReset()">🗑 Zerar placares</button>
  </div>
</div>

<div id="toast"></div>

<script>
// ═══════════════════ SCHEDULE ═══════════════════
const SCH = [
  [["J12","J1","J2","J4"],  ["J3","J10","J7","J8"],  ["J5","J11","J6","J9"]],
  [["J12","J2","J3","J5"],  ["J4","J11","J8","J9"],  ["J6","J1","J7","J10"]],
  [["J12","J3","J4","J6"],  ["J5","J1","J9","J10"],  ["J7","J2","J8","J11"]],
  [["J12","J4","J5","J7"],  ["J6","J2","J10","J11"], ["J8","J3","J9","J1"]],
  [["J12","J5","J6","J8"],  ["J7","J3","J11","J1"],  ["J9","J4","J10","J2"]],
  [["J12","J6","J7","J9"],  ["J8","J4","J1","J2"],   ["J10","J5","J11","J3"]],
  [["J12","J7","J8","J10"], ["J9","J5","J2","J3"],   ["J11","J6","J1","J4"]],
  [["J12","J8","J9","J11"], ["J10","J6","J3","J4"],  ["J1","J7","J2","J5"]],
  [["J12","J9","J10","J1"], ["J11","J7","J4","J5"],  ["J2","J8","J3","J6"]],
  [["J12","J10","J11","J2"],["J1","J8","J5","J6"],   ["J3","J9","J4","J7"]],
  [["J12","J11","J1","J3"], ["J2","J9","J6","J7"],   ["J4","J10","J5","J8"]],
];

// ═══════════════════ STATE ═══════════════════
function defaultNames(){const n={};for(let i=1;i<=12;i++)n[`J${i}`]=`Jogador ${i}`;return n;}
let state={names:defaultNames(),scores:{}};

function loadState(){
  try{
    const s=localStorage.getItem('whist_w12');
    if(s){state=JSON.parse(s);}
    for(let i=1;i<=12;i++){if(!state.names[`J${i}`])state.names[`J${i}`]=`Jogador ${i}`;}
    if(!state.scores)state.scores={};
  }catch(e){}
}

function saveState(){localStorage.setItem('whist_w12',JSON.stringify(state));}
loadState();

// ═══════════════════ NAV ═══════════════════
let curTab='dashboard';
let activeVR=0;
let rfRound='all';

function goTab(tab){
  document.querySelectorAll('.page').forEach(p=>p.classList.remove('active'));
  document.querySelectorAll('.nav-tab').forEach(t=>t.classList.remove('active'));
  document.getElementById(`page-${tab}`).classList.add('active');
  document.getElementById(`tab-${tab}`).classList.add('active');
  curTab=tab;
  if(tab==='dashboard')renderDashboard();
  if(tab==='placar')renderPlacar();
  if(tab==='atletas')renderAtletas();
}

// ═══════════════════ STATS ═══════════════════
function computeStats(){
  const p={};
  for(let i=1;i<=12;i++){
    const k=`J${i}`;
    p[k]={key:k,name:state.names[k]||k,pts:0,wins:0,losses:0,draws:0,played:0};
  }
  for(let r=0;r<SCH.length;r++){
    for(let m=0;m<SCH[r].length;m++){
      const sc=state.scores[r]&&state.scores[r][m];
      if(sc==null)continue;
      const[k1,k2,k3,k4]=SCH[r][m];
      const{a,b}=sc;
      p[k1].pts+=a;p[k2].pts+=a;p[k3].pts+=b;p[k4].pts+=b;
      [k1,k2,k3,k4].forEach(k=>p[k].played++);
      if(a>b){p[k1].wins++;p[k2].wins++;p[k3].losses++;p[k4].losses++;}
      else if(b>a){p[k3].wins++;p[k4].wins++;p[k1].losses++;p[k2].losses++;}
      else{[k1,k2,k3,k4].forEach(k=>p[k].draws++);}
    }
  }
  return Object.values(p).sort((a,b)=>{
    if(b.pts!==a.pts)return b.pts-a.pts;
    if(b.wins!==a.wins)return b.wins-a.wins;
    return parseInt(a.key.slice(1))-parseInt(b.key.slice(1));
  });
}

// ═══════════════════ DASHBOARD ═══════════════════
function renderDashboard(){
  const stats=computeStats();
  renderStats(stats);
  renderRanking(stats);
  renderPodium(stats);
  renderDashRTabs();
  renderDashMatches(activeVR);
  updateBadge();
}

function renderStats(stats){
  let played=0;
  for(let r=0;r<SCH.length;r++)
    for(let m=0;m<SCH[r].length;m++)
      if(state.scores[r]&&state.scores[r][m]!=null)played++;
  const totalPts=stats.reduce((s,p)=>s+p.pts,0);
  const leader=stats[0];
  const items=[
    {lbl:'Rodadas',val:11,sub:'no torneio'},
    {lbl:'Disputadas',val:played,sub:'de 33 partidas'},
    {lbl:'Líder',val:leader.pts>0?leader.name.split(' ').pop():'—',sub:`${leader.pts} pts`},
    {lbl:'Total de Pts',val:totalPts,sub:'acumulados'},
    {lbl:'Atletas',val:12,sub:'Beach Tennis'},
  ];
  document.getElementById('statStrip').innerHTML=items.map((it,i)=>`
    <div class="stat-tile" style="animation-delay:${i*.07}s">
      <div class="lbl">${it.lbl}</div>
      <div class="val">${esc(String(it.val))}</div>
      <div class="sub">${it.sub}</div>
    </div>`).join('');
}

function renderRanking(stats){
  const max=Math.max(...stats.map(p=>p.pts),1);
  const chips=['pc-g','pc-s','pc-b'];
  const medals=['🥇','🥈','🥉'];
  document.getElementById('rankingList').innerHTML=stats.map((p,i)=>{
    const pos=i+1;
    const chip=i<3?chips[i]:'pc-n';
    const medal=i<3?medals[i]:pos;
    const pct=(p.pts/max*100).toFixed(1);
    return `<div class="rank-row r${pos}" style="animation-delay:${i*.04}s">
      <div><div class="pos-chip ${chip}">${medal}</div></div>
      <div>
        <div class="p-name">${esc(p.name)}</div>
        <div class="p-tags">
          <span class="tag tw">${p.wins}V</span>
          <span class="tag tl">${p.losses}D</span>
          <span class="tag td">${p.draws}E</span>
        </div>
        <div class="pts-bar-wrap"><div class="pts-bar" style="width:${pct}%"></div></div>
      </div>
      <div class="pts-big">${p.pts}</div>
      <div class="nc cg">${p.wins}</div>
      <div class="nc cr">${p.losses}</div>
      <div class="nc cm">${p.draws}</div>
    </div>`;
  }).join('');
}

function renderPodium(stats){
  const wrap=document.getElementById('podiumWrap');
  if(stats.every(p=>p.pts===0)){wrap.classList.remove('show');return;}
  wrap.classList.add('show');
  const order=[stats[1],stats[0],stats[2]];
  const cls=['pp2','pp1','pp3'];const medals=['🥈','🥇','🥉'];
  document.getElementById('podium').innerHTML=order.map((p,i)=>`
    <div class="pod-slot ${cls[i]}">
      <div class="pod-medal">${medals[i]}</div>
      <div class="pod-name">${esc(p.name)}</div>
      <div class="pod-pts">${p.pts} pts</div>
    </div>`).join('');
}

function renderDashRTabs(){
  document.getElementById('dashRTabs').innerHTML=SCH.map((_,r)=>{
    const full=SCH[r].every((_,m)=>state.scores[r]&&state.scores[r][m]!=null);
    const any=SCH[r].some((_,m)=>state.scores[r]&&state.scores[r][m]!=null);
    const cls=r===activeVR?'active':(full?'done':(any?'partial':''));
    return `<button class="rtab ${cls}" onclick="selVR(${r})">R${r+1}</button>`;
  }).join('');
  let done=0;
  for(let r=0;r<SCH.length;r++)for(let m=0;m<SCH[r].length;m++)if(state.scores[r]&&state.scores[r][m]!=null)done++;
  document.getElementById('ovProg').textContent=`${done}/33`;
}

function selVR(r){activeVR=r;renderDashRTabs();renderDashMatches(r);}

function renderDashMatches(r){
  document.getElementById('dashMFeed').innerHTML=SCH[r].map((match,m)=>{
    const[k1,k2,k3,k4]=match;
    const sc=state.scores[r]&&state.scores[r][m];
    const pA=sc!=null?sc.a:'—',pB=sc!=null?sc.b:'—';
    let cA='sz',cB='sz';
    if(sc!=null){
      if(sc.a>sc.b){cA='sw';cB='sl';}
      else if(sc.b>sc.a){cB='sw';cA='sl';}
      else{cA=cB='sw';}
    }
    const wA=sc!=null&&sc.a>sc.b?'<span class="wtag">VENC.</span>':'';
    const wB=sc!=null&&sc.b>sc.a?'<span class="wtag">VENC.</span>':'';
    return `<div class="mc">
      <div class="mlbl">Partida ${m+1} · Rodada ${r+1}</div>
      <div class="mbody">
        <div class="tea"><div class="tp">${esc(state.names[k1]||k1)}</div><div class="tp">${esc(state.names[k2]||k2)}</div>${wA}</div>
        <div class="sbox"><div class="sn ${cA}">${pA}</div><div class="ssep">:</div><div class="sn ${cB}">${pB}</div></div>
        <div class="teb"><div class="tp">${esc(state.names[k3]||k3)}</div><div class="tp">${esc(state.names[k4]||k4)}</div>${wB}</div>
      </div>
    </div>`;
  }).join('');
}

// ═══════════════════ PLACAR ═══════════════════
function renderPlacar(){
  buildRFBar();
  buildGrid();
  updateBadge();
}

function buildRFBar(){
  const bar=document.getElementById('rfBar');
  bar.querySelectorAll('.rfbtn').forEach((b,i)=>{if(i>0)b.remove();});
  bar.querySelector('.rfbtn').className='rfbtn'+(rfRound==='all'?' active':'');
  SCH.forEach((_,r)=>{
    const btn=document.createElement('button');
    btn.className='rfbtn'+(rfRound===String(r)?' active':'');
    btn.textContent=`R${r+1}`;
    btn.onclick=()=>filterRound(String(r),btn);
    bar.appendChild(btn);
  });
}

function filterRound(val,btn){
  rfRound=val;
  document.querySelectorAll('.rfbtn').forEach(b=>b.classList.remove('active'));
  btn.classList.add('active');
  buildGrid();
}

function buildGrid(){
  const grid=document.getElementById('placarGrid');
  grid.innerHTML='';
  SCH.forEach((round,r)=>{
    if(rfRound!=='all'&&rfRound!==String(r))return;
    round.forEach((match,m)=>{
      const[k1,k2,k3,k4]=match;
      const sc=state.scores[r]&&state.scores[r][m];
      const has=sc!=null;
      const aVal=has?sc.a:'';
      const bVal=has?sc.b:'';
      const card=document.createElement('div');
      card.className='se'+(has?' done-se':'');
      card.id=`se-${r}-${m}`;
      card.innerHTML=`
        <div class="se-head">
          <div class="se-lbl">Rodada ${r+1} · Partida ${m+1}</div>
          <div class="se-status ${has?'st-done':'st-empty'}">${has?'✅ Salvo':'Pendente'}</div>
        </div>
        <div class="se-body">
          <div class="se-teams">
            <div class="se-team">
              <div class="se-player">${esc(state.names[k1]||k1)}</div>
              <div class="se-player">${esc(state.names[k2]||k2)}</div>
            </div>
            <div class="se-vs">VS</div>
            <div class="se-team r">
              <div class="se-player">${esc(state.names[k3]||k3)}</div>
              <div class="se-player">${esc(state.names[k4]||k4)}</div>
            </div>
          </div>
          <div class="si-row">
            <input class="si" id="sa-${r}-${m}" type="number" min="0" max="9999"
              value="${aVal}" placeholder="0"
              oninput="styleI(${r},${m})"
              onkeydown="kNav(event,${r},${m},'a')">
            <div class="si-sep">:</div>
            <input class="si" id="sb-${r}-${m}" type="number" min="0" max="9999"
              value="${bVal}" placeholder="0"
              oninput="styleI(${r},${m})"
              onkeydown="kNav(event,${r},${m},'b')">
          </div>
          <button class="btn-save" onclick="saveScore(${r},${m})">⚡ Salvar</button>
          ${has?`<button class="btn-clr" onclick="clearScore(${r},${m})">✕ Limpar</button>`:''}
        </div>`;
      grid.appendChild(card);
      if(has)setTimeout(()=>styleI(r,m),0);
    });
  });
}

function styleI(r,m){
  const iA=document.getElementById(`sa-${r}-${m}`);
  const iB=document.getElementById(`sb-${r}-${m}`);
  if(!iA||!iB)return;
  const a=parseFloat(iA.value),b=parseFloat(iB.value);
  iA.className='si';iB.className='si';
  if(!isNaN(a)&&!isNaN(b)&&iA.value!==''&&iB.value!==''){
    if(a>b){iA.classList.add('win-i');iB.classList.add('lose-i');}
    else if(b>a){iB.classList.add('win-i');iA.classList.add('lose-i');}
  }
}

function kNav(e,r,m,side){
  if(e.key==='Enter'||e.key==='\t'){
    if(side==='a'){e.preventDefault();document.getElementById(`sb-${r}-${m}`)?.focus();}
    else saveScore(r,m);
  }
}

function saveScore(r,m){
  const iA=document.getElementById(`sa-${r}-${m}`);
  const iB=document.getElementById(`sb-${r}-${m}`);
  if(!iA||!iB)return;
  const av=iA.value.trim(),bv=iB.value.trim();
  if(av===''||bv===''){showToast('⚠️ Preencha os dois placares',true);return;}
  const na=parseFloat(av),nb=parseFloat(bv);
  if(isNaN(na)||isNaN(nb)||na<0||nb<0){showToast('⚠️ Valores inválidos',true);return;}
  if(!state.scores[r])state.scores[r]={};
  state.scores[r][m]={a:na,b:nb};
  saveState();
  buildGrid();
  const[k1,k2,k3,k4]=SCH[r][m];
  const w=na>nb?`${state.names[k1]} & ${state.names[k2]}`:(nb>na?`${state.names[k3]} & ${state.names[k4]}`:'Empate');
  showToast(`✅ R${r+1}·P${m+1} — ${w}`);
  updateBadge();
  if(curTab==='dashboard')renderDashboard();
}

function clearScore(r,m){
  if(state.scores[r]){delete state.scores[r][m];if(!Object.keys(state.scores[r]).length)delete state.scores[r];}
  saveState();buildGrid();updateBadge();showToast('🗑 Placar removido');
  if(curTab==='dashboard')renderDashboard();
}

function updateBadge(){
  let done=0;
  for(let r=0;r<SCH.length;r++)for(let m=0;m<SCH[r].length;m++)if(state.scores[r]&&state.scores[r][m]!=null)done++;
  const pend=33-done;
  const b=document.getElementById('pbadge');
  if(pend>0&&pend<33){b.style.display='inline';b.textContent=pend;}
  else b.style.display='none';
}

// ═══════════════════ ATLETAS ═══════════════════
function renderAtletas(){
  document.getElementById('atletasList').innerHTML=Array.from({length:12},(_,i)=>{
    const k=`J${i+1}`;
    return `<div class="atleta-row">
      <div class="atleta-num">${i+1}</div>
      <input class="atleta-input" id="nm-${k}"
        value="${esc(state.names[k]||`Jogador ${i+1}`)}"
        placeholder="Nome do atleta"
        onkeydown="if(event.key==='Enter'){saveAtleta('${k}');document.getElementById('nm-J${i+2}')?.focus();}">
      <button class="atleta-sb" onclick="saveAtleta('${k}')">Salvar</button>
    </div>`;
  }).join('');
}

function saveAtleta(key){
  const inp=document.getElementById(`nm-${key}`);
  const val=inp.value.trim();
  if(!val){showToast('⚠️ Nome vazio',true);return;}
  state.names[key]=val;saveState();
  showToast(`✅ ${key.replace('J','Jogador ')} → ${val}`);
  if(curTab==='dashboard')renderDashboard();
  if(curTab==='placar')renderPlacar();
}

function saveAllAtletas(){
  let n=0;
  for(let i=1;i<=12;i++){
    const k=`J${i}`;
    const inp=document.getElementById(`nm-${k}`);
    if(!inp)continue;
    const val=inp.value.trim();
    if(val&&val!==state.names[k]){state.names[k]=val;n++;}
  }
  saveState();showToast(`✅ ${n} nome(s) atualizados!`);
  if(curTab==='dashboard')renderDashboard();
  if(curTab==='placar')buildGrid();
}

function confirmReset(){
  if(!confirm('⚠️ Apagar TODOS os placares?\n\nOs nomes dos atletas serão mantidos.\n\nConfirmar?'))return;
  state.scores={};saveState();showToast('🗑 Placares removidos');
  if(curTab==='placar')renderPlacar();
  if(curTab==='dashboard')renderDashboard();
}

// ═══════════════════ CLOCK ═══════════════════
function tick(){
  const n=new Date();
  document.getElementById('clock').textContent=n.toLocaleTimeString('pt-BR',{hour:'2-digit',minute:'2-digit',second:'2-digit'});
}
setInterval(tick,1000);tick();

// ═══════════════════ TOAST ═══════════════════
let tt=null;
function showToast(msg,err=false){
  const t=document.getElementById('toast');
  t.textContent=msg;t.className='show'+(err?' err':'');
  clearTimeout(tt);tt=setTimeout(()=>t.className='',3200);
}

function esc(s){return String(s||'').replace(/&/g,'&amp;').replace(/</g,'&lt;').replace(/>/g,'&gt;').replace(/"/g,'&quot;');}

// ═══════════════════ INIT ═══════════════════
renderDashboard();
updateBadge();
</script>
</body>
</html>

