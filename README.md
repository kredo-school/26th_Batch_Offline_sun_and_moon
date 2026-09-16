# sun-and-moon
A shared app for five members to log daily progress and support each other in achieving their goals.<br>
チームメンバー５人の目標達成のため、日々の生活を記録・管理するアプリケーション。

## Git / GitHub Rules

### Branch
- mainへの直接pushは禁止
→ 必ず下記のようにbranchを切ってから作業する。<br>
- 新機能：feature/機能名 (例：feature/profile-page)
- バグ修正：fix/修正内容 (例：fix/login-error)

### Commit
「何を変更したのか」わかるようにメッセージを残す。
- feat: 新機能
新しい機能を追加したとき。(例：feat: ユーザープロフィール画面を追加)
- fix: バグ修正
バグを直したとき。(例：fix: ログイン後に画面遷移しない問題を修正)
- refactor: リファクタリング
動作を変えずに、コードを整理したとき。(例：refactor: 日次ログ取得処理を関数に分離)
- style: UI・フォーマット修正
UIや見た目の修正。(例：style: スマホ表示の余白を調整)
- docs: ドキュメント
READMEなど、説明文を変更したとき。(例：docs: READMEにセットアップ方法を追加)
- chore: 設定・パッケージ
開発環境やライブラリなどを変更したとき。(例：chore: react-hook-formを追加)

### Pull Request
- mainへの変更は必ずPR経由
- 1人以上のレビュー後にmerge
- 1PR = 1機能を目安
- merge後はブランチを削除

## Coding Rules

### 命名規則
* 変数・関数：`camelCase`
* Reactコンポーネント：`PascalCase`
* TypeScriptの型：`PascalCase`
* 定数：`UPPER_SNAKE_CASE`
```ts
const userName = "test";
function getDailyLogs() {}
type DailyLog = {};
const MAX_LOG_LENGTH = 500;
```
### ファイル名
Reactコンポーネント：
```text
DailyLogForm.tsx
UserProfile.tsx
```

その他：
```text
auth.ts
dailyLog.ts
```
### React / Next.js

1つのコンポーネントに処理を詰め込みすぎない。
役割ごとにコンポーネントを分割する。

```text
DailyLogList.tsx
DailyLogForm.tsx
WeeklyGoal.tsx
```

### 関数

1つの関数にはできるだけ1つの役割を持たせる。
関数名から処理内容が分かるようにする。

```ts
getDailyLogs()
createDailyLog()
updateWeeklyGoal()
```

### コメント

コードを読めば分かる内容はコメントしない。
処理の理由や、特殊な実装をした理由を書く。

### Formatter / Linter

コードの書式・命名・品質チェックはESLintに従う。
PRを出す前に、

```bash
npm run lint
```

を実行する。
