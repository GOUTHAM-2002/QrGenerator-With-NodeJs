# 📱 QR Code Generator - Node.js

A simple, lightweight **QR code generator** built with Node.js. Convert any text or URL into a scannable QR code image with just a few lines of code.

![Node.js](https://img.shields.io/badge/Node.js-16.x+-339933?style=for-the-badge&logo=node.js&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)

---

## 🎯 Overview

This project demonstrates how to programmatically generate QR codes using Node.js. Perfect for learning backend development, creating URL shorteners, building authentication systems, or any application that needs QR code functionality.

---

## ✨ Features

- **Generate QR codes from text or URLs**
- **Save QR codes as PNG images**
- **Store input URLs to a text file** for logging
- **Simple command-line interface**
- **Lightweight and fast** - minimal dependencies
- **Easy to integrate** into larger projects

---

## 🚀 Quick Start

### Prerequisites

- **Node.js** (v16.x or higher) - [Download here](https://nodejs.org/)
- **npm** (comes with Node.js)

### Installation

1. **Clone the repository**
```bash
   git clone https://github.com/GOUTHAM-2002/QrGenerator-With-NodeJs.git
   cd QrGenerator-With-NodeJs
```

2. **Install dependencies**
```bash
   npm install
```

3. **Run the generator**
```bash
   node index.js
```

---

## 📖 Usage

### Basic Example
```javascript
// index.js
const qr = require('qrcode');
const fs = require('fs');

// Your URL or text
const inputURL = "https://github.com/GOUTHAM-2002";

// Generate QR code
qr.toFile('qr_code.png', inputURL, (err) => {
  if (err) throw err;
  console.log('QR Code generated successfully!');
});

// Save URL to text file
fs.writeFileSync('URL.txt', inputURL);
```

### Running the Script
```bash
node index.js
```

This will:
- Generate a `qr_code.png` image in your project folder
- Save the input URL to `URL.txt`

---

## 📂 Project Structure
```
QrGenerator-With-NodeJs/
├── node_modules/        # Dependencies
├── index.js             # Main QR generator script
├── solution.js          # Alternative implementation (if needed)
├── URL.txt              # Stores the last generated URL
├── qr_code.png          # Generated QR code image (output)
├── package.json         # Project metadata and dependencies
├── package-lock.json    # Locked dependency versions
└── README.md            # You are here
```

---

## 🛠️ Dependencies

This project uses the following npm packages:

- **[qrcode](https://www.npmjs.com/package/qrcode)** - QR code generation library
- **fs** (built-in) - File system operations

Install all dependencies with:
```bash
npm install
```

---

## 🎨 Customization

### Change QR Code Size
```javascript
const options = {
  width: 300,  // Width in pixels
  color: {
    dark: '#000000',  // Black dots
    light: '#FFFFFF'  // White background
  }
};

qr.toFile('qr_code.png', inputURL, options, (err) => {
  if (err) throw err;
});
```

### Generate QR Code to Terminal
```javascript
qr.toString(inputURL, { type: 'terminal' }, (err, string) => {
  if (err) throw err;
  console.log(string);
});
```

### Output as Data URL (for web applications)
```javascript
qr.toDataURL(inputURL, (err, url) => {
  if (err) throw err;
  console.log(url);  // Base64 encoded image
});
```

---

## 💡 Use Cases

- **URL Shorteners**: Generate QR codes for shortened links
- **Authentication**: Two-factor authentication (2FA) systems
- **Marketing**: Create scannable codes for campaigns
- **Event Management**: Generate tickets with QR codes
- **Product Labeling**: Link to product information pages
- **WiFi Sharing**: Encode WiFi credentials

---

## 🧪 Example Output

After running the script, you'll get:

**qr_code.png**  
![QR Code Example](https://via.placeholder.com/200x200?text=QR+Code)

**URL.txt**
```
https://github.com/GOUTHAM-2002
```

---

## 🔧 Troubleshooting

### Module not found error
```bash
npm install
```

### Permission denied (Linux/Mac)
```bash
chmod +x index.js
```

### PNG not generating
Make sure you have write permissions in the project directory.

---

## 🚀 Enhancements & Future Ideas

- [ ] Add command-line arguments for custom URLs
- [ ] Support multiple output formats (SVG, PDF)
- [ ] Create a web interface with Express.js
- [ ] Add batch QR code generation
- [ ] Implement QR code decoding
- [ ] Add logo/image overlay to QR codes
- [ ] Create REST API endpoints

---

## 🤝 Contributing

Contributions are welcome! Feel free to:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

---

## 👤 Author

**Goutham N**

- GitHub: [@GOUTHAM-2002](https://github.com/GOUTHAM-2002)
- Email: goutham3336@gmail.com

---

## 🌟 Show Your Support

If you found this project helpful, give it a ⭐ on GitHub!

---

## 📚 Resources

- [QRCode npm package documentation](https://www.npmjs.com/package/qrcode)
- [Node.js File System docs](https://nodejs.org/api/fs.html)
- [QR Code specification](https://en.wikipedia.org/wiki/QR_code)

---

**Built with ❤️ and Node.js**
