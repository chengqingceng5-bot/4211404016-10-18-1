# 小風攝影工作室｜攝影師作品集網站

純靜態網站（單一 `index.html`，HTML / CSS / JS 同檔），可直接部署到 Vercel。

## 專案結構

```
.
├── index.html
├── README.md
└── images/
    ├── hero.jpg
    ├── about.jpg
    ├── wedding-01.jpg ~ wedding-06.jpg     婚紗
    ├── ceremony-01.jpg ~ ceremony-06.jpg   婚禮紀錄
    └── portrait-01.jpg ~ portrait-06.jpg   形象照
```

## 替換成真實圖片（免費圖庫）

`images/` 內目前是程式產生的色塊示意圖，檔名與路徑已和 `index.html` 對應。
請到免費圖庫下載照片，用相同檔名覆蓋即可：

- Unsplash：https://unsplash.com
- Pexels：https://www.pexels.com
- Pixabay：https://pixabay.com

建議：作品圖 1200×800（3:2）、`hero.jpg` 1600×1000、`about.jpg` 800×1000，單張壓縮到 300 KB 以內。
使用前請確認各圖庫的授權條款；若換成不同內容，記得同步修改 `index.html` 內的 `alt` 文字。

## 上線前請修改

在 `index.html` 搜尋並替換：

- `hello@example.com` → 真實 Email（共 4 處：JSON-LD、表單 action、表單 JS、頁尾）
- `your_instagram` → 真實 Instagram 帳號
- 服務方案價格與交件時間 → 依實際報價調整
- `<title>` 目前依需求為「小柯攝影工作室」，頁面內品牌為「小風攝影工作室」，請統一名稱
- 若有正式網域，可加入 `<link rel="canonical">`，並把 `og:image` 改為完整網址

## 部署

### GitHub

```bash
git init
git add .
git commit -m "Initial commit: photographer portfolio"
git branch -M main
git remote add origin https://github.com/<你的帳號>/<repo名稱>.git
git push -u origin main
```

### Vercel

1. 登入 https://vercel.com，點 **Add New → Project**。
2. 匯入剛才的 GitHub repo。
3. Framework Preset 選 **Other**，Build Command 與 Output Directory 保持空白。
4. 按 **Deploy**，之後每次 push 都會自動更新。

## 關於詢問表單

靜態網站沒有後端，表單送出時會開啟訪客的郵件程式並自動帶入內容。
若想直接收到表單通知，可改接 Formspree、Getform 或 Vercel Serverless Function。
