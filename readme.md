# 🧾 Quick Bill POS — Arun Traders (v8.2)

**Quick Bill POS** is a fast, offline-first, single-file Progressive Web Application (PWA) tailored for retail stores, grocery shops, and wholesale traders. Built with zero backend dependencies, it combines rapid keypad billing, thermal Bluetooth ESC/POS printing, customer credit ledgers, inventory management, and instant WhatsApp receipt sharing in a sleek, responsive interface.

---

## ✨ Key Features

### 🧮 Rapid Billing & POS Modes
- **Quick Bill Mode:** Custom on-screen Numeric & QWERTY keypads designed for touchscreens and mobile devices, complete with auto-switching focus (`Item Name → Rate → Qty`), smart quantity replacement, and Caps Lock ON by default.
- **Smart 2-Row Suggestion Tray:** Dynamic-width, high-contrast item tiles automatically sorted by **most sold items first** based on historical sales volume.
- **Item Wise POS:** Visual product grid with category filter pills and real-time search for one-tap cart additions.
- **Live App Stats Drawer:** Real-time sidebar metrics tracking **Total Items**, **Customers**, **Total Bills**, and **Lifetime Revenue**.

### 🖨️ Thermal Printing & Digital Sharing
- **Web Bluetooth ESC/POS Printing:** Direct wireless printing to 58mm and 80mm thermal receipt printers with customizable shop headers and live canvas receipt previews.
- **Direct WhatsApp Receipt Share:** Generates a high-DPI PNG image of the thermal receipt and shares it directly to the customer's WhatsApp via the Web Share API (with automatic download + `wa.me` fallback on desktop).
- **Dynamic UPI QR Code Generator:** Instant payment QR code generation (`upi://pay`) for digital checkouts with support for multiple UPI IDs.

### 👥 Customer Credit Ledger & Inventory
- **Customer Management:** Track customer dues, credit limits, partial/full payment settlements, and printable customer statements.
- **Inventory Management:** Manage purchase rates, sale rates, barcodes, and categories with full **CSV Import (with interactive column mapping)** and **CSV Export**.
- **Sales Reports & Analytics:** Filterable KPIs (Gross Sales, Net Profit, Avg Bill Value, Payment Mode breakdown, and Top 5 Best-Selling Products) across Today, Yesterday, Week, Month, or custom date ranges.

### 🎨 Customization & Offline Reliability
- **Offline-First Storage:** Powered by browser **IndexedDB** with an automatic in-memory fallback for restricted or private browsing environments.
- **JSON & CSV Backup/Restore:** Full one-click database export and restore functionality.
- **6 Built-in Color Themes:** Dark (Original), Nordic Mint, Cyber Violet, Obsidian Cyan, Warm Espresso, and Clean Light.
- **Installable PWA:** Includes dynamic Web App Manifest and Service Worker registration for home-screen installation on Android, iOS, Windows, and macOS.

---

## 🚀 Getting Started

### 1. Run Locally
Because **Quick Bill POS** is built as a self-contained single-file web application:
1. Clone or download this repository.
2. Open `quickbill_v6_6.html` (or rename it to `index.html`) directly in any modern browser (Chrome, Edge, Safari, Brave).

### 2. Host as an Installable App (PWA)
To enable **Web Bluetooth Printing** and **Install App** functionality:
1. Host the HTML file on any static HTTPS server (e.g., **GitHub Pages**, **Vercel**, **Netlify**, or **Cloudflare Pages**).
2. Open the hosted URL on your mobile device or desktop browser.
3. Open the left navigation drawer and tap **📲 Install App** (or use your browser's *"Add to Home Screen"* option).

---

## 🛠️ Tech Stack

- **Frontend:** HTML5, Vanilla JavaScript (ES6+), Tailwind CSS (CDN)
- **Icons & Fonts:** Font Awesome 6, Google Fonts (`Inter`)
- **Storage:** IndexedDB API (`QuickBill_ArunTraders_V8_2`) + `localStorage`
- **Hardware & APIs:** Web Bluetooth API (ESC/POS), HTML5 Canvas Receipt Renderer, QRious, Web Share API

---

## 📋 Default Keyboard & Billing Workflow

1. **Select Customer (Optional):** Tap the customer pill in the top header to search or quick-create a customer ledger.
2. **Add Items:**
   - Tap a product from the **2-row suggestion tray**, *or*
   - Enter the **Rate** on the numeric keypad, press **Enter (`X`)**, enter **Qty**, and press **Enter (`X`)** to add to the cart.
3. **Checkout & Share:**
   - Tap **Save** to open the checkout summary.
   - Choose **Cash**, **UPI** (displays live scannable QR), or **Credit**.
   - Tap **WhatsApp** to share the receipt image directly, or **Save & Print** to send to your paired Bluetooth thermal printer.

---

## 👨‍💻 Developer & Credits

- **Developer:** Arun Kumar SC
- **Contact:** +91 8105104599
- **Store:** Arun Traders, Pavagada
- ❤️ *Special thanks to my family — Aaryan & Atharv.*