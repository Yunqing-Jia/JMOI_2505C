# JMOI_2505C | 🛡️ LaTeX Selective Encryption Package
This README.md was generated with the help of ChatGPT.

A simple, customizable LaTeX package to selectively **"encrypt" sensitive text or hyperlinks** in your document—using asterisks `*`, hashes `#`, or even filled boxes ▮ — while keeping everything else perfectly readable.

> Want to hide personal data in your PDF before sharing it? Want anonymized previews of confidential content in a paper draft or public submission?  

**This package is for you.**

---

## ✨ Features

✅ Selective encryption of **text** and **hyperlinks**  
✅ Choose your **encryption style**: asterisk `*`, hash `#`, or filled box `■`  
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
```

---

## 🔐 Usage

This package defines two main commands:
- **`\textE{...}`** — Encrypt regular text.
  - This command encrypts regular text in the document.
  - The content inside the curly braces will be replaced by the encrypted symbol based on the chosen encryption types.
  - **Example**:
    ```latex
    \textE{Encrypted text example}
    ```
    - With `encrypt=1`, this would display as `**********`.

- **`\linkE{<url>}{<text>}`** — Encrypt hyperlink display text or URL.
  - This command encrypts the hyperlink's display text or the URL itself.
  - It works similarly to the `\textE{...}` command but for links.
  - **Example**:
    ```latex
    \linkE{https://github.com/}{Github}
    ```
    - With `encrypt=2`, the output will display as `######` in place of the link text, while also masking the URL.

### 🔢 Encryption Types

You can switch encryption types using the encrypt option:

| `encrypt` | Effect                         | Appearance Example       |
|-----------|--------------------------------|--------------------------|
| `0`       | No encryption                  | `@Github`           |
| `1`       | Encrypted with `*` symbols     | `*******`           |
| `2`       | Encrypted with `#` symbols     | `#######`           |
| `3`       | Encrypted with filled boxes `■` | `■■■■■■■`          |

> ℹ️ The number of symbols matches the number of characters in the original string.

### 🎨 Color

Use the color option to change the encryption symbol color:

```latex
\usepackage[encrypt=3,color=blue]{selective-encryption}
```
### 🧪 Example

```latex
\documentclass{article}
%\usepackage[encrypt=0,color=black]{selective-encryption} % default value - no encryption
%\usepackage[encrypt=1,color=cyan]{selective-encryption} % encrypt = 1 : encrypted by *
%\usepackage[encrypt=2,color=cyan]{selective-encryption} % encrypt = 2 : encrypted by #
\usepackage[encrypt=3,color=cyan]{selective-encryption} % encrypt = 3 : encrypted by ■

\begin{document}

\section{Latex Selective Encryption Package}

\subsection{No encryption}

\textbf{$@$JMOI\_2505C Project}

\href{https://github.com/}{Github}

\subsection{With encryption}

\textbf{\textE{$@$JMOI\_2505C Project}}

\linkE{https://github.com/}{Github}

\end{document}
```

- Compile this with XeLaTeX to see the difference.


---

## 📂 Repository Structure

```
Latex-Selective-Encryption-Package/
│
├── selective-encryption.sty   % The encryption package
├── test.tex                   % Usage demo
├── test.pdf                   % Rendered PDF output
└── README.md                  % You're reading it!
```

---

## 📌 Use Cases

- Publishing reports with redacted content
- Hiding sensitive information in public slides
- Creating versions of a document with different privacy levels

---

## 📄 License

This package is released under the MIT License. Free to use, modify, and distribute.

---

## ✏️ Author

Created by Yunqing Jia

GitHub: [@Yunqing-Jia](https://github.com/Yunqing-Jia)
