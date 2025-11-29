# 🔧 XSD-Based XML Editor (基於 XSD 的 XML 編輯器)

![License](https://img.shields.io/badge/license-Apache%202.0-blue.svg)
![Platform](https://img.shields.io/badge/platform-Web-orange.svg)
![Language](https://img.shields.io/badge/language-HTML%20%2F%20JS%20%2F%20CSS-yellow.svg)

一個輕量級、純前端的 XML 編輯器，能夠讀取 XSD (XML Schema Definition) 檔案，並根據架構定義動態生成編輯介面。支援即時驗證、樹狀結構編輯、多國語系與主題切換。

A lightweight, purely client-side XML editor that parses XSD (XML Schema Definition) files to generate a dynamic editing interface. Features real-time validation, tree-view editing, multi-language support, and theme customization.

---

## ✨ 功能特色 (Features)

### 1. 核心編輯功能 (Core Editing)
- **無伺服器架構 (Serverless)**：純 HTML/JS/CSS 實作，無需後端，直接在瀏覽器運行。
  - *Pure HTML/JS/CSS implementation, runs directly in the browser without a backend.*
- **雙模式檢視 (Dual View)**：
  - 🌲 **樹狀編輯器 (Tree Editor)**：直覺的 GUI，透過點擊新增/刪除節點與屬性。
    - *Intuitive GUI for adding/removing nodes and attributes via clicks.*
  - 📝 **原始碼編輯器 (Source Editor)**：帶有語法高亮的原始 XML 代碼檢視。
    - *Raw XML code view with syntax highlighting.*

### 2. 智慧 XSD 解析 (Smart XSD Parsing)
- **智慧輸入控制 (Smart Inputs)**：
  - 自動偵測 `xs:enumeration` 並產生下拉選單。(*Auto-detects enumerations and generates dropdowns.*)
  - 自動偵測 `xs:date`, `xs:time`, `xs:dateTime` 並顯示日期時間選擇器。(*Auto-displays date/time pickers for date/time types.*)
- **限制條件顯示 (Constraints Display)**：
  - 在介面上直接顯示 `minOccurs`, `maxOccurs`, `pattern`, `totalDigits` 等限制。
  - *Displays constraints like min/max occurs, patterns, and digits directly on the UI.*
- **XPath 顯示 (XPath Display)**：
  - 顯示每個元素的完整 XPath 路徑，方便定位。
  - *Shows the full XPath for each element for easy navigation.*
- **說明文件 (Documentation)**：
  - 讀取 XSD 中的 `xs:documentation` 並顯示為提示。
  - *Reads and displays `xs:documentation` from XSD as tooltips.*

### 3. 使用者體驗 (User Experience)
- **多國語系 (Internationalization)**：
  - 支援繁體中文、简体中文、English、日本語、ภาษาไทย。
  - 自動偵測瀏覽器語系。(*Auto-detects browser language.*)
- **佈景主題 (Theming)**：
  - 內建多種 **莫蘭迪色系 (Morandi Colors)** 主題（紅、黃、藍、綠、粉、預設紫）。
  - *Built-in Morandi color themes (Red, Yellow, Blue, Green, Pink, Default).*
- **響應式設計 (Responsive Design)**：
  - 自動適應視窗大小，最大化編輯空間 (95% 寬度)。
  - *Adapts to window size, maximizing editing space (95% width).*

---

## 🚀 快速開始 (Getting Started)

本專案不需要編譯或安裝任何依賴套件。
*This project requires no compilation or dependencies.*

1.  **下載專案 (Clone the repository)**
    ```bash
    git clone [https://github.com/bluemoney/XSDBasedXMLEditor.git](https://github.com/bluemoney/XSDBasedXMLEditor.git)
    ```

2.  **執行 (Run)**
    直接使用瀏覽器 (Chrome, Firefox, Edge, Safari) 開啟 `index.html` 即可。
    *Simply open `index.html` in your web browser.*

---

## 📖 使用說明 (Usage Guide)

1.  **載入 XSD (Load XSD)**
    - 點擊左上角的 **「📁 載入 XSD 檔案」**，選擇您的 `.xsd` 架構檔。
    - *Click **"📁 Load XSD File"** to select your schema definition.*

2.  **編輯 XML (Edit XML)**
    - 系統會自動產生根節點。(*The root node is generated automatically.*)
    - 點擊 **「+ 子節點」** 增加元素（系統會依據 XSD 過濾合法的子元素）。(*Click **"+ Child"** to add elements, filtered by XSD rules.*)
    - 點擊 **「修改」** 來編輯內容或新增屬性。(*Click **"Edit"** to modify content or attributes.*)

3.  **驗證與匯出 (Validate & Export)**
    - 點擊 **「✓ 驗證 XML」** 檢查文件是否符合規範。(*Click **"✓ Validate XML"** to check compliance.*)
    - 點擊 **「💾 匯出 XML」** 下載編輯完成的檔案。(*Click **"💾 Export XML"** to download the file.*)

---

## 🛠️ 技術細節 (Technical Details)

* **DOMParser**: 用於解析 XSD 與 XML 字串。(*Used for parsing XSD and XML strings.*)
* **Recursion**: 使用遞迴演算法動態生成樹狀結構 DOM。(*Recursive algorithms used to generate the tree view DOM.*)
* **CSS Variables**: 使用 `:root` 變數實現動態換膚功能。(*CSS variables used for dynamic theming.*)
* **Zero Dependencies**: 完全無外部依賴。(*No external libraries required.*)

---

### **螢幕截圖 (Screenshots)**

*![image](https://github.com/bluemoney/XSDBasedXMLEditor/blob/main/screenshot_01.png)*
