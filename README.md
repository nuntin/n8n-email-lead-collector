# 📧 Email Lead Collector (n8n)

This automation flow allows you to scrape emails from any list of websites and export the result as a downloadable CSV file.

✅ Built using official n8n nodes only  
✅ No OAuth / external API required  
✅ No community nodes used

---

## 🧩 Features

- Input list of website URLs
- Scrape email addresses from HTML
- Filter duplicate & invalid emails
- Export result as CSV to `./emails.csv`
- Works on n8n v1.94.1 and above

---

## 🚀 Usage (Step-by-step)

1. Import the provided `email-lead-collector.json` into n8n
2. Click the first node (Set) → enter websites in this format:

   ```json
   [
     "https://www.djangoproject.com",
     "https://www.python.org",
     "https://www.openai.com"
   ]
   ```

3. Run the full workflow
4. Result file `emails.csv` will be saved in the current working directory

---

## ⚠️ Notes on File Saving

- This flow saves to: `./emails.csv`  
  *(current directory where n8n is running)*

### 🐳 If using Docker:

```bash
docker run -it --rm   -v $(pwd)/output:/data   -e N8N_EDITOR_BASE_URL=http://localhost:5678   -p 5678:5678 n8nio/n8n
```

Then change `File Path` in Save File node to:

```bash
/data/emails.csv
```

---

## 🇹🇭 คำอธิบายภาษาไทย

Flow นี้ใช้สำหรับดึงอีเมลจากเว็บไซต์ต่าง ๆ และบันทึกผลลัพธ์เป็นไฟล์ `.csv` โดยไม่ต้องใช้ API หรือระบบภายนอก

- ป้อน URL ของเว็บไซต์ที่ต้องการ
- ดึง email ที่พบจาก HTML โดยตรง
- บันทึกผลลัพธ์ลงใน `./emails.csv`

✅ เหมาะสำหรับนักการตลาด / นักพัฒนา / เจ้าของธุรกิจที่ต้องการ Lead  
✅ ไม่มีขั้นตอน OAuth ให้ยุ่งยาก

---

## 📁 Files

- `email-lead-collector.json` — Verified Flow file
- `README.md` — This instruction file (EN/TH)---

## 🛠 Troubleshooting

### ❌ Error: `ENOENT: no such file or directory`
- This happens when the folder path doesn't exist.
- Solution: Make sure the directory in the `Save File` node exists.
  - For local: use `./emails.csv`
  - For Docker: mount the path correctly and use `/data/emails.csv`

### ❌ No Emails Found
- Try using websites that contain visible email addresses in the page.
- Ensure "Always Output Data" is enabled in `Settings`.

---

## 🎞 Example GIF

> (Add your own screen recording here using [ScreenToGif](https://www.screentogif.com/))

You can place your GIF inside the repo and embed like:


![Demo GIF](demo.gif)


---

## 🪪 License

This project is released under the [MIT License](https://opensource.org/licenses/MIT).

You are free to use, modify, and distribute this workflow, including for commercial purposes. No warranty provided.