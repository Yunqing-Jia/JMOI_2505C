# 🛡️ LaTeX Selective Encryption Package (JMOI_2505C)
This README.md was generated with the help of ChatGPT.

A simple, customizable LaTeX package to selectively **"encrypt" sensitive text or hyperlinks** in your document—using asterisks `*`, hashes `#`, or even black boxes ▮—while keeping everything else perfectly readable.

> Want to hide personal data in your PDF before sharing it? Want anonymized previews of confidential content in a paper draft or public submission?  
**This package is for you.**

---

## ✨ Features

✅ Selective encryption of **text** and **hyperlinks**  
✅ Choose your **encryption style**: asterisk `*`, hash `#`, or black box `■`  
✅ Fully **customizable encryption color**  
✅ Encryption level can be **turned off** without modifying your source code  

---

## 📦 Files

- `selective-encryption.sty`: The core package file.
- `test.tex`: A sample document showing how to use the package.
- `test.pdf`: Output from `test.tex`, showing encrypted and unencrypted content side-by-side.

---

## 🔧 Installation

Just place `selective-encryption.sty` in the same directory as your `.tex` file, or install it in your local TeX tree.

Then, in your LaTeX document:

```latex
\usepackage[encrypt=2,color=cyan]{selective-encryption}

---

## 🔐 Usage

This package defines two main commands:
	•	\textE{...} — encrypt regular text
	•	\linkE{<url>}{<text>} — encrypt hyperlink display text or URL

You can switch encryption modes using the encrypt option:

### 🔢 Encryption Types

| `encrypt` | Effect                         | Appearance Example       |
|-----------|--------------------------------|--------------------------|
| `0`       | No encryption                  | `@Yunqing-Jia`           |
| `1`       | Encrypted with `*` symbols     | `************`           |
| `2`       | Encrypted with `#` symbols     | `############`           |
| `3`       | Encrypted with filled boxes `■` | `■■■■■■■■■■■■`          |

> ℹ️ The number of symbols matches the number of characters in the original string.
