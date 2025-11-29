# **🔧 XSD-Based XML Editor**

一個輕量級、純前端的 XML 編輯器，能夠讀取 XSD (XML Schema Definition) 檔案，並根據架構定義動態生成編輯介面。支援即時驗證、樹狀結構編輯、多國語系與主題切換。

A lightweight, browser-based XML editor that parses XSD files to generate a dynamic editing interface. Features real-time validation, tree-view editing, multi-language support, and theme customization.

🔗 **Project URL:** [https://github.com/bluemoney/XSDBasedXMLEditor](https://github.com/bluemoney/XSDBasedXMLEditor)

## **✨ 特色 (Features)**

* **無伺服器架構 (Serverless)**：純 HTML/JS/CSS 實作，無需後端，直接在瀏覽器運行。  
* **XSD 智能解析 (Smart XSD Parsing)**：  
  * 自動讀取 XSD 結構，限制子元素的新增選項。  
  * 支援 xs:enumeration，自動產生下拉選單。  
  * 支援 xs:date, xs:time, xs:dateTime，自動顯示日期/時間選擇器。  
  * 顯示詳細的約束條件：minOccurs, maxOccurs, pattern, totalDigits 等。  
  * 顯示完整的 **XPath** 路徑與 **Documentation** 定義。  
* **雙模式編輯 (Dual View)**：  
  * 🌲 **樹狀編輯器 (Tree Editor)**：直覺的 GUI，透過點擊新增/刪除節點與屬性。  
  * 📝 **原始碼編輯器 (Source Editor)**：帶有語法高亮的原始 XML 代碼檢視。  
* **即時驗證 (Validation)**：根據 XSD 規則檢查必要屬性、資料類型與結構完整性。  
* **多國語系支援 (i18n)**：  
  * 繁體中文 (Traditional Chinese)  
  * 简体中文 (Simplified Chinese)  
  * English  
  * 日本語 (Japanese)  
  * ภาษาไทย (Thai)  
  * *自動偵測瀏覽器語系*  
* **佈景主題 (Theming)**：  
  * 內建多種 **莫蘭迪色系 (Morandi Colors)** 主題（紅、黃、藍、綠、粉、預設紫）。  
  * 按鈕與介面顏色隨主題動態切換。  
* **響應式設計 (RWD)**：自適應視窗大小，最大化編輯空間 (95% 寬度)。

## **🚀 快速開始 (Getting Started)**

### **安裝 (Installation)**

本專案不需要編譯或安裝。

1. Clone 此專案：  
   Bash  
   git clone https://github.com/bluemoney/XSDBasedXMLEditor.git

2. 直接使用瀏覽器 (Chrome, Firefox, Edge, Safari) 開啟 xsdView.html 即可使用。

### **使用方式 (Usage)**

1. **載入 XSD**：點擊左上角的 **「📁 載入 XSD 檔案」**，選擇您的 .xsd 架構檔。  
2. **編輯 XML**：  
   * 系統會自動產生根節點。  
   * 點擊 **「+ 子節點」** 增加元素（系統會依據 XSD 過濾合法的子元素）。  
   * 點擊 **「修改」** 來編輯內容或新增屬性。  
   * 若欄位有定義 enumeration 或日期格式，會自動出現對應的輸入控制項。  
3. **查看資訊**：右側面板會顯示當前節點的 XSD 定義、XPath 與限制條件。  
4. **驗證**：點擊 **「✓ 驗證 XML」** 檢查文件是否符合規範。  
5. **匯出**：點擊 **「💾 匯出 XML」** 下載編輯完成的檔案。

## **🛠️ 技術細節 (Technical Details)**

* **核心邏輯**：使用原生 DOMParser 解析 XSD 與 XML 字串。  
* **UI 渲染**：使用遞迴 (Recursion) 動態生成樹狀結構 DOM。  
* **樣式**：使用 CSS Variables (:root) 實現動態換膚功能。  
* **依賴**：完全無外部依賴 (Zero Dependencies)。

## **🤝 貢獻 (Contributing)**

歡迎提交 Pull Request 或 Issue！

1. Fork 本專案。  
2. 建立您的 Feature Branch (git checkout \-b feature/AmazingFeature)。  
3. 提交您的修改 (git commit \-m 'Add some AmazingFeature')。  
4. 推送到 Branch (git push origin feature/AmazingFeature)。  
5. 開啟 Pull Request。

## **📄 授權 (License)**

本專案採用 **Apache-2.0** 授權條款。詳細內容請參閱 [LICENSE](https://www.google.com/search?q=LICENSE) 檔案。

Copyright (c) 2024 [bluemoney](https://www.google.com/search?q=https://github.com/bluemoney).

---

### **螢幕截圖 (Screenshots)**

*![image](https://github.com/bluemoney/XSDBasedXMLEditor/blob/main/screenshot_01.png)*
