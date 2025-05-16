# 🎨 wall color
✨ 簡介：

`wall` 是一個用 Bash 撰寫的小工具，能夠在終端機中輸出「置中」顯示、帶有背景色的文字。

非常適合用在腳本提示、警告訊息或狀態顯示。

---
# 使用方式
- 基本用法
```bash
wall -[顏色] "你的文字"
```
- 範例
```bash
wall -pink "Hello World!"
wall -red "⚠️ WARNING: Something is wrong."
```
- 進階用法
若你希望自訂字體顏色或加粗文字，可搭配 echo -n 與定義好的變數使用：
```bash
echo -n "${RED}"; wall -green "成功訊息"; echo -n "${NC}"
```
- 你需要在腳本中事先定義顏色變數，例如：
```bash
RED='\033[38;2;255;0;0m'
NC='\033[0m'
```
🎨 支援的顏色
| 參數        | 顏色說明 |
| --------- | ---- |
| `-yellow` | 黃色背景 |
| `-pink`   | 粉紅背景 |
| `-gray`   | 灰色背景 |
| `-red`    | 紅色背景 |
| `-green`  | 綠色背景 |
| `-blue`   | 藍色背景 |
| `-purple` | 紫色背景 |
| `-cyan`   | 青色背景 |

![Screenshot_2025-05-16-13-16-15-01_84d3000e3f4017145260f7618db1d683](https://github.com/user-attachments/assets/71f1517b-cf4b-4a1a-8894-8aacc7f43b42)

🌐 語言支援
首次打開Hellp幫助文檔時會詢問語言（中文或英文），~~之後會自動記住設定~~（暫時無法確定）。

📌 專案狀態
開發狀態：開發中 🚧

👤 製作者
- `Clyde Cole`

[GitHub: Clyde Cole](https://github.com/ClydeCole)

---
# ⚠️ 注意事項：
本版本仍處於早期開發階段，架構與指令格式仍可能更動

尚未處理輸入錯誤與極端情況

暫時無法解決輸出文本後終端縮放導致顯示出錯
