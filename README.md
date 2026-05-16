# CurioHub • 知藏

**高質感即時資訊聚合 + 智能個人知識庫 + 社群討論**

一個專為知識工作者設計的現代化平台。讓你輕鬆收集網路優質資訊、AI 智能分類整理，**並針對每篇收藏展開深入討論與想法交流**。

![Cover Image](https://via.placeholder.com/1200x600/1a1a2e/ffffff?text=CurateHub)

## ✨ 核心特色

- **即時資訊探索**：聚合多來源最新內容
- **智能一鍵收藏**：AI 自動分類 + 摘要
- **強大個人知識庫**：多層級資料夾、標籤、筆記
- **每篇連結討論區**：用戶可針對單一連結發表評論、想法、見解與延伸討論
- **極致美觀介面**：雜誌風格 + 流暢動效 + 深色模式

## 🎯 主要功能

### 資訊流與收藏
- 熱門趨勢與分類瀏覽
- 一鍵收藏 + AI 智能分類建議
- AI 生成重點摘要

### 個人知識庫
- 無限層級資料夾 + 多標籤系統
- 個人筆記與高亮
- 多視圖切換（Masonry、Grid、List）
- 全文與語義搜尋

### **全新：討論區（Discussion）**
每篇收藏的連結都擁有獨立的**討論區**，讓用戶可以：
- 發表個人見解、補充資訊或不同觀點
- 回覆他人評論（支援 threaded 討論）
- 對留言按讚
- 標記有用留言
- 討論區置頂重要留言
- AI 輔助總結討論重點（規劃中）

這讓 CurateHub 不只是個人收藏工具，更能成為**思想碰撞與知識共創**的空間。

### 其他亮點
- PWA 支援（可安裝到手機）
- 完整深色模式
- 閱讀狀態追蹤
- 每日/每週知識回顧

## 🛠️ 技術堆疊

- **Frontend**：Next.js 15 (App Router + TypeScript) + Tailwind CSS + Shadcn/ui + TanStack Query
- **Backend**：FastAPI (Python) 或 NestJS
- **Database**：PostgreSQL（新增 `comments`、`comment_replies` 表）
- **Real-time**：Socket.io 或 Supabase Realtime（即時更新討論）
- **AI**：Grok / Claude（分類、摘要、未來討論總結）
- **Auth**：Clerk 或 NextAuth.js

## 📁 專案結構（重點更新）

```bash
curatehub/
├── apps/web/
│   ├── app/
│   │   ├── (main)/             # 首頁、探索
│   │   ├── library/            # 我的知識庫
│   │   └── bookmark/[id]/      # 單篇收藏頁面 ← 新增討論區
│   └── components/
│       ├── BookmarkCard/
│       ├── DiscussionSection/  # 新增討論區元件
│       └── Comment/
├── apps/api/
│   └── routes/
│       └── comments/           # 討論區 API
└── prisma/schema.prisma        # 包含 Comment 模型
```

## 🗺️ 開發路線圖

### MVP（第一階段） - 已加入討論功能
- [ ] 多來源資訊卡片展示
- [ ] 一鍵收藏 + AI 分類
- [ ] 我的收藏頁面
- [ ] **每篇收藏的討論區（核心功能）**
  - 發表留言
  -  threaded 回覆
  - 按讚功能
- [ ] 深色模式與響應式

### 後續階段
- [ ] AI 討論重點總結
- [ ] 熱門討論排行
- [ ] 公開分享討論區連結
- [ ] 網頁剪藏擴充功能
- [ ] 團隊共享收藏與討論

## 🛠️ 本地開發環境設置

```bash
git clone https://github.com/yourusername/curatehub.git
cd curatehub

# 前端
cd apps/web
pnpm install
pnpm dev

# 後端（FastAPI）
cd ../api
pip install -r requirements.txt
uvicorn main:app --reload
```

## 📸 介面預覽（建議加入）

- 首頁資訊流
- 收藏彈窗
- **單篇收藏頁面（含討論區）** ← 重點截圖
- 行動版討論介面

## 📄 License

MIT License © 2026 CurateHub
