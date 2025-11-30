# ⚡ Instant Python Web Server
A super-simple, zero-config web server written in Python.  
Perfect for quickly hosting static files, testing HTML/CSS/JS, or running a lightweight local server.

---

## 🚀 Features
- Minimal (only 7 lines of code)
- No dependencies — uses Python’s built-in modules
- Works on any OS (Windows, Linux, macOS)
- Automatically serves files from the current folder
- Great for beginners & quick testing

---

## 📦 Code

```python
import http.server
import socketserver

PORT = 8000

handler = http.server.SimpleHTTPRequestHandler
with socketserver.TCPServer(("", PORT), handler) as httpd:
    print(f"Serving at http://localhost:{PORT}")
    httpd.serve_forever()
