# PGY Mentor Alert — GitHub CSV Data-Driven Version

## 架構

Excel（主資料） → 匯出 CSV → GitHub `/data/` → `index.html` fetch CSV → Dashboard

## 固定 CSV

- `data/pgy_master.csv`：PGY 名單、到職日、訓練狀態
- `data/learning_journey.csv`：24M 應完成項目與完成狀態
- `data/assessment.csv`：Mini-CEX / DOPS / BPD 等評核
- `data/mentor_alert.csv`：導師提醒

## 更新方式

1. 在 Excel 更新主資料。
2. 匯出成上述固定檔名的 CSV。
3. 上傳 GitHub，覆蓋 `/data/` 內同名 CSV。
4. GitHub Pages 重新整理即可取得最新資料。
5. `index.html` 不需要因為一般資料更新而修改。

## 注意

目前前端的勾選操作只暫存在目前瀏覽器工作階段；若要讓「勾選後」永久寫回 GitHub CSV，需要另外建立寫回機制（例如 GitHub API + 權限），不能由純 GitHub Pages 前端直接安全寫檔。
