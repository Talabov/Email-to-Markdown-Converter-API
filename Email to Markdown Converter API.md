# 📧 Email to Markdown Converter API
---

🚀 **Need a ready-to-deploy version?**

Includes Docker, setup guide, sample responses, and full API structure.

👉 [Buy it on Gumroad](https://talabov.gumroad.com/)

---

A production-ready Flask REST API that parses `.eml` email files and converts the contents into clean Markdown or plain text. HTML is sanitized, scripts/tables removed — perfect for email parsing or analysis pipelines.

---

## ✅ Key Features

- 📥 Upload `.eml` email files via POST
- 🧹 Extracts subject, sender, recipient, and body
- 🧼 Converts HTML email body to readable Markdown
- 🔄 Plain-text fallback supported
- 🛡 Strips `<style>`, `<script>`, and tables
- 🧪 Postman-tested, modular project structure
- 🗃 2MB file size limit

---

## 🚀 Endpoints

### Convert to JSON (Markdown)

**POST** `/convert-json`

**Request (form-data):**
- `file`: `.eml` file

**Response:**
```json
{
  "subject": "Subject line here",
  "from": "sender@example.com",
  "to": "receiver@example.com",
  "markdown": "Converted email content here"
}
```

---

### Convert to Plain Text

**POST** `/convert-plain`

**Request (form-data):**
- `file`: `.eml` file

**Response:**
Plain text content of the email body.

---

## ⛔ Error Handling

```json
{
  "error": "No file part"
}
```

```json
{
  "error": "Invalid file"
}
```

```json
{
  "error": "Email body not found"
}
```

---

## ⚙️ Requirements

```bash
pip install -r requirements.txt
```

- Flask  
- beautifulsoup4

---

## 🖥 How to Run

```bash
python app.py
```

Server runs at:
```
http://127.0.0.1:5000/
```

---

## 🧪 Example Screenshots

- ✅ Upload `.eml` via Postman
- ✅ Markdown JSON response
- ✅ Plain text response
- ⚠️ Error handling examples

> Screenshots available in the `/screens/` folder

---

## 💼 Ready-to-Use Version

You can get a ZIP with full code, setup instructions, and working examples:

👉 [Buy it on Gumroad](https://talabov.gumroad.com/)

---

## 📬 Contacts

- Email: talabov.ali72@gmail.com  
- Telegram: [@talabovali](https://t.me/talabovali)

---

**Need this in another language/stack (Node.js, Go, etc)?**  
Custom dev available — just reach out.
