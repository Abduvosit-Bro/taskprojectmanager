# 学生向けプロジェクト・タスク管理システム
## (Task & Project Manager for Students)

---

## 1. プロジェクトの概要 (Overview)
**背景:**
学生生活において、課題、プロジェクト、アルバイト、サークル活動など、複数のタスクを同時に管理することは困難です。
既存のツールは機能が多すぎて複雑だったり、学生特有のニーズ（多言語対応など）を満たしていないことがありました。

**目的:**
学生が直感的に使え、学業とプライベートを効率的に管理できる、多言語対応のタスク管理プラットフォームを提供すること。

---

## 2. 主な機能 (Key Features)

### 🌐 多言語サポート (Multilingual Support)
- **日本語とウズベク語**の完全対応。
- UI言語を瞬時に切り替え可能。
- 留学生や多国籍なチームでの利用に最適。

### 🤖 AI自動翻訳 (AI Translation)
- タスクやプロジェクトの説明文を**AIが自動翻訳**。
- オフライン時はローカル辞書による翻訳フォールバック機能が作動。
- 言語の壁を越えたコラボレーションを実現。

### 📅 スマートカレンダー (Smart Calendar)
- 提出期限やイベントをカレンダー形式で視覚的に管理。
- FullCalendarを採用し、ドラッグ＆ドロップで直感的に操作可能。

### 📊 プロジェクト管理 (Project Management)
- タスクをプロジェクトごとに整理。
- 1つのタスクを**複数のプロジェクトに紐付け**可能（多対多のリレーション）。
- 進捗状況をステータス（未着手、進行中、完了）で可視化。

### 🔔 リアルタイム通知 (Real-time Notifications)
- 期限が迫ったタスクや新しい割り当てを通知。
- CeleryとRedisを使用した非同期処理で、スムーズなユーザー体験を提供。

---

## 3. 技術スタック (Tech Stack)

**Backend:**
- **Django 5 & DRF:** 堅牢でスケーラブルなAPIサーバー。
- **Flexible Database:** 本番環境は **PostgreSQL**、開発環境は **SQLite** に対応（Docker不要）。
- **Async Tasks:** Celery + Redis（ローカル開発用のEagerモードもサポート）。
- **Auth:** JWTによるセキュアな認証。

**Frontend:**
- **React + TypeScript:** モダンで型安全なUI開発。
- **Vite:** 高速なビルドツール。
- **Tailwind CSS:** 柔軟で美しいスタイリング。
- **TanStack Query:** 効率的なデータフェッチとキャッシング。

---

## 4. インフラとデプロイ (Infrastructure & Deployment)

**開発環境 (Development):**
- **Docker-less Support:** Dockerなしでも簡単にセットアップ可能（SQLite & Celery Eager）。
- **Git & GitHub:** バージョン管理とCI/CD連携。

**本番環境 (Production):**
- **Backend:** Render.com (Gunicorn, WhiteNoise, PostgreSQL)。
- **Frontend:** Vercel (Vite Build, Edge Network)。
- **Security:** CORS設定、環境変数による機密情報の管理。

---

## 5. デモンストレーション (Demo)
*(ここで実際の画面を見せる、またはリンクを紹介する)*

1.  **ログイン & ダッシュボード:** 直感的なホーム画面。
2.  **タスク作成:** タイトル入力とAI翻訳の実演。
3.  **カレンダービュー:** 月表示/週表示の切り替え。
4.  **言語切り替え:** 日本語 ⇔ ウズベク語のスイッチ。

---

## 6. 今後の展望 (Future Roadmap)
- **モバイルアプリ化:** React Nativeによるスマホ対応。
- **チームコラボレーション機能:** コメント機能、ファイル共有の強化。
- **AI機能の拡張:** タスクの優先度自動提案、学習スケジュールの最適化。

---

## 7. まとめ (Conclusion)
**Task & Project Manager** は、単なるTo-Doリストではなく、学生の成功をサポートする多言語対応のパートナーです。
最新のWeb技術を駆使し、使いやすさと機能性を両立させました。

**ご清聴ありがとうございました！ (Thank you!)**
