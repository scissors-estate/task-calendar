# 業務管理カレンダー

民泊運営スタッフ用の業務タスク管理カレンダー。共通タスク（「共」）と個人タスクを週・月単位で管理し、繰り返しタスク・完了チェック・作業時間の記録ができる。

- 公開URL: https://scissors-estate.github.io/task-calendar/
- ログイン: Googleアカウント（メンバー登録された人のみ）
- データ保存: Firebase Realtime Database（プロジェクト `scissors-task-calendar` / `tasks/`・`members/`）
- ホスティング: GitHub Pages
- 構成: `index.html` 1ファイルのみ（約3,200行）

## 編集するとき（次に変更したくなった時の手順）

1. GitHub の `index.html` を開き、最新の中身をダウンロード（Download raw file）
2. Claude のチャット「【民泊】業務管理カレンダー」に `index.html` を添付し、直したい内容を伝える
3. Claude が直した `index.html` をダウンロード
4. 画面右上のバージョン表示（例 `v2026.11.05-2`）を新しい日付に更新してもらう（反映確認の目印）
5. GitHub のリポジトリで **Add file → Upload files** から `index.html` をアップロード → **Commit changes**
6. 1〜2分後に公開URLで、バージョン表示が新しくなっているか確認（変わらなければ Ctrl+F5）

## 注意点

- 必ず **GitHub上の最新の `index.html`** から編集を始める（古いファイルを上げると、他の人の改修が消える）
- 同時に2人以上で改修しない（後からアップした方で上書きされる）
- タスクのデータは Firebase 側にあるので、`index.html` を上げ直してもタスクは消えない
- Firebase の設定（`firebaseConfig`）やデータの保存先（`tasks/`・`members/`）は変更しない

## トラブル時のチェック

- ログインできない → メンバー登録されているか（👥 メンバー）、Googleアカウントが合っているか
- 画面が真っ白 → 直前にアップした `index.html` に誤りがある。GitHub の履歴（History）から1つ前の版に戻す
- 変更が反映されない → 1〜2分待ってから Ctrl+F5（強制再読み込み）
