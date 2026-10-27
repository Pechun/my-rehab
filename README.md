# my-rehab

物理治療症狀紀錄 App：https://pechun.github.io/my-rehab/

## 更新方式（給 Claude）
- **程式更新**：修改 `index.html` 時，同時把 `APP_VER` 和 `version.json` 的 `v` 改成同一個新值。手機打開時發現版本不同，會自動重新載入。
- **推送內容到手機**：在 `inbox.json` 的 `items` 加一筆，`id` 必須是新的、不重複。手機打開時會自動套用，每個 id 只套用一次。
  - `hep_add`：`exercises: [{name, dose, how}]`，加到最近一次回診的居家作業（同名跳過；沒有回診會自動建立一筆）
  - `question_add`：`questions: ["要問的問題"]`
  - `visit_add`：`date`、`notes`、`exercises`
- `inbox.json` 是公開的，只放動作說明這類內容，不放疼痛紀錄。
