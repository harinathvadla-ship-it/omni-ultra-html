# ⚡ LiteHost - Tiiny Host Clone

LiteHost is a lightweight, single-file HTML hosting dashboard optimized for mobile environments and WebViews (like AppsGeyser). It allows users to upload standalone `.html` files and deploy them instantly to the web with zero configuration, bypassing strict native mobile storage blocks.

---

## 🚀 Features

* **Instant Deployments:** Upload your custom HTML pages and get a live, shareable public HTTPS link in seconds.
* **WebView Optimized:** Uses client-side file reading to stream payloads, preventing Android "Failed to Fetch" or CORS security blockages.
* **Dual-Cluster Routing:** Built-in automatic fallback routing. If the primary hosting node is unreachable, it seamlessly switches to a backup network cluster.
* **Fully Responsive:** Modern, clean, user-friendly UI designed perfectly for Android smartphone screens.

---

## 🛠️ How It Works

Instead of handling heavy binary data streams which native mobile browsers often restrict, LiteHost uses a secure client-side extraction layer:

1. **File Selection:** The user selects a local `.html` file from their phone's file picker.
2. **Stream Conversion:** A `FileReader()` operation reads the file as plain text data inside the isolated app sandbox.
3. **Secure Piping:** The raw text code is piped directly to an open, secure web hosting server API.
4. **Live Link Generation:** The server responds with a live, permanent URL displaying your code as a fully rendered website.

---

## 📲 How to Use in AppsGeyser

To compile this into an APK using AppsGeyser:

1. Host this repository on **GitHub Pages** (Settings -> Pages -> Set branch to `main`).
2. Copy your live GitHub Pages link (e.g., `https://yourusername.github.io/litehost/`).
3. Go to the AppsGeyser Dashboard and create an app using the **Website** or **Browser** template.
4. Paste your GitHub Pages link into the App configuration box.
5. Build, install the APK on your phone, and start deploying!

---

## 🌐 Dependencies & Services

This project relies on the following direct web endpoints for hosting execution:
* Primary Node: `https://ttm.sh` (Anonymous temporary storage pipeline)
* Backup Node: `https://bashupload.com` (Plain text streaming terminal)
