
# Vue 3 + Tailwind CSS - 深色模式設置指南
教學用-vue3的tailwind dark mode

這個指南提供了如何在使用 Vite 的 Vue 3 項目中設置 Tailwind CSS 並啟用深色模式的步驟。

## 先決條件

確保你已經安裝了 Node.js 和 npm。這個項目使用 Vite 作為開發和構建工具。

## 安裝步驟

### 步驟 1：克隆項目

如果你是從現有項目開始，請確保你已經克隆了項目並且處於項目的根目錄中。

### 步驟 2：安裝依賴

安裝項目依賴：

```bash
npm install
```

### 步驟 3：配置 Tailwind CSS
在 tailwind.config.js 中啟用深色模式：
```
// tailwind.config.js
module.exports = {
  darkMode: 'class', // 可選 'media' 或 'class'
  // ...其他配置
};
```

### 步驟 4：創建深色模式的 CSS 文件
創建一個名為 dark-mode.css 的 CSS 文件並添加你的深色模式樣式：
```
/* dark-mode.css */
.dark {
  --tw-bg-opacity: 1;
  background-color: rgba(17, 24, 39, var(--tw-bg-opacity)); /* 背景色為暗灰色 bg-gray-900 */
}
```

### 步驟 5：導入深色模式的 CSS 文件
在主 CSS 文件中導入 dark-mode.css 文件。確保這個導入語句在所有其他樣式規則之前：
```
/* src/style.css */
@import './dark-mode.css'; /* 確保這是最先被導入的 */
@tailwind base;
@tailwind components;
@tailwind utilities;
```

### 步驟 6：添加深色模式切換功能
在 Vue 組件中，例如 App.vue，添加切換深色模式的方法：
```
<template>
  <button @click="toggleDarkMode">切換深色模式</button>
</template>

<script>
export default {
  methods: {
    toggleDarkMode() {
      document.body.classList.toggle('dark');
    }
  }
};
</script>
```

### 步驟 7：啟動開發服務器
使用以下命令啟動項目：
```
npm run dev
```

開啟你的瀏覽器，訪問 http://127.0.0.1:5173/ 以查看你的應用。

### 結論
按照以上步驟，你現在應該已經在 Vue 3 項目中成功添加了 Tailwind CSS 和深色模式的支持。你可以根據需求進一步自定義 dark-mode.css 文件，為深色模式添加更多樣式。









