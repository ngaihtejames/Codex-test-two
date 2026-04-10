# 🚀 Colab Turbo Downloader

A **high-performance, beginner-friendly file downloader** built for **Google Colab** with seamless **Google Drive integration**.

> ⚡ Fill the inputs → click **Runtime → Run all** → your file downloads automatically.

---

## ✨ Features

- 🧠 **No code required** — form-based UI (edit one cell only)
- ☁️ **Google Drive integration** — save files directly to your Drive
- 📊 **Storage dashboard** — total, used, free space + usage %
- ⚠️ **Low storage warning** before download starts
- 📂 **Lightweight Drive file browser**
- 🚀 **Multi-threaded downloads** (HTTP range requests)
- 🔁 **Retry + backoff** for network/server issues
- 💾 **Memory-efficient streaming** (no RAM overload)
- 🔄 **Automatic fallback** for unsupported servers
- 📊 **Live progress bar** (bytes, speed)

---

## 📁 Repository Structure

```
.
├── downloader.ipynb   # Main Colab notebook (UI + downloader)
├── README.md          # Project documentation
├── requirements.txt   # Dependencies
└── .gitignore         # Ignore rules
```

---

## ⚡ Quick Start (Google Colab)

1. Open **`downloader.ipynb`** in Google Colab  
2. In the **🔧 Downloader Settings** cell, enter:
   - 🔗 Download URL  
   - 📄 Output file name (optional)  
   - ⚙️ Parallel connections  
   - 📁 Save folder (Google Drive)  
3. (Optional) Enable **Advanced Settings**  
4. Click **Runtime → Run all**  
5. Approve Google Drive mount when prompted  
6. Wait for:
```
✅ Download complete
```

---

## ⚠️ Notes & Limitations

- Some servers **do not support range requests** → auto fallback to single-stream mode  
- If **content-length is missing**, percentage may be less precise  
- **Login-protected URLs** may not work  
- Very large downloads depend on Colab runtime/network stability  

---

## 📦 Requirements

```
requests>=2.31.0
tqdm>=4.66.0
```

(Colab typically has these preinstalled)

---

## 📜 License

Add a license (MIT recommended) before publishing.
