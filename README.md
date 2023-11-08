# Vue 3 + Tailwind CSS - 深色模式設置指南

這個專案展示了如何在 Vue 3 應用程序中結合使用 Tailwind CSS 來實現深色模式的功能。

## 特點

- Vue 3 框架
- Tailwind CSS 風格
- 可切換的深色模式
- 響應式設計

## 開始使用

要開始使用這個專案，請先確保您已經安裝了 Node.js 和 npm/yarn。

### 安裝依賴

克隆專案到您的本地機器後，運行以下命令安裝所需的依賴包：

```bash
npm install
# 或者使用 yarn
yarn install
```
運行開發服務器
安裝完依賴後，您可以啟動開發服務器來預覽應用：
```
npm run serve
# 或者使用 yarn
yarn serve
```
開啟瀏覽器並訪問 http://localhost:8080 來查看應用。

建置生產版本
當您準備將應用部署到生產環境時，您可以運行以下命令來建置優化後的版本：

```
npm run build
# 或者使用 yarn
yarn build
```

## 深色模式切換
深色模式的切換是透過 Tailwind CSS 的 dark 模式類別來控制的。透過 Vue 的響應式數據來綁定對應的類別到最頂層的 div 元素上。

您可以查看 src/App.vue 文件來了解如何實現深色模式的切換。