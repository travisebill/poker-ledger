# ♠️ 越記越多的記帳本 ♣️

線上撲克與桌遊的記帳軟體 — PWA 版本，可安裝、可離線使用。

> 原始碼由 [Gemini](https://gemini.google.com/) 生成，原始分享對話：
> <https://share.gemini.google/ZmbAfImHrKSU>

## 功能

- **遊戲類型自訂** — 預設「德州撲克現金桌」「德州撲克錦標賽」「十三張」，可自行新增
- **累計追蹤** — 買入、出金、當週水錢，頂部看板即時計算總額與淨利
- **獲利曲線圖** — 內建 Chart.js 互動式圖表
- **戰績篩選與匯出** — 依遊戲類型過濾，支援 JSON 備份 / 還原
- **本機儲存** — localStorage，資料不上傳任何伺服器

## PWA

| 項目 | 說明 |
|------|------|
| Manifest | `manifest.webmanifest`（standalone、深色主題、3 種 icon 含 maskable） |
| Service Worker | `sw.js` — app shell cache-first、導航 network-first、靜態資源 stale-while-revalidate |
| 離線 | ✅ 所有 CDN 依賴已本地化至 `vendor/`（Tailwind、Chart.js、Font Awesome、Fredoka 字型） |
| 安裝 | iOS「分享 → 加入主畫面」；Chrome/Edge 網址列安裝圖示 |

## 開發

```bash
python3 -m http.server 8899   # 需經 HTTP 才能註冊 Service Worker
# → http://127.0.0.1:8899
```

## 技術棧

Tailwind CSS（CDN 版，已本地化）· Chart.js 4 · Font Awesome 6.4 · 原生 JS + localStorage

## License

MIT
