# Claude Code 四大觀念課程

國土三組 Claude Code 教育訓練網頁：四堂課（筆記系統、API 規範 Skill、流程斜線指令、外部連接與安全防線）、補充觀念、第 5 堂實作 LAB、錯誤影響對照，以及 18 張圖解與 26 題自我測驗。

- 內容查核基準：Claude Code v2.1.274（2026-09-17）官方文件
- 單一檔案 `index.html`，不需要建置；作答紀錄只存在瀏覽者自己的瀏覽器

## 發布到 GitHub Pages

> **注意：GitHub Pages 網站預設對外公開。** 即使 repo 是 private，網站仍可被任何人瀏覽；只有 GitHub Enterprise Cloud 能把 Pages 設為僅限組織成員。
> 另外，private repo 使用 Pages 需要 GitHub Pro／Team／Enterprise 方案；Free 組織只能用 public repo。

1. 在組織建立 repo，例如 `claude-code-course`。
2. 上傳 `index.html`、`README.md`（`.nojekyll` 可一併上傳，非必要）。
3. 進入 repo 的 **Settings → Pages**，在 **Build and deployment → Source** 選 **Deploy from a branch**，分支選 `main`、資料夾選 `/ (root)`，按 **Save**。
4. 約 1～2 分鐘後，網址為 `https://<組織名稱>.github.io/claude-code-course/`（組織名稱會轉為小寫）。

用指令上傳：

```bash
git clone https://github.com/<組織名稱>/claude-code-course.git
cd claude-code-course
# 將 index.html、README.md、.nojekyll 複製到此資料夾
git add index.html README.md .nojekyll
git commit -m "docs: 發布 Claude Code 四大觀念課程網頁"
git push origin main   # 若 main 已設分支保護，改用 feature 分支並建立 PR
```

## 更新內容

直接修改 `index.html` 後提交即可；Pages 會自動重新部署。Claude Code 更新頻繁，建議每季對照 [Claude Code changelog](https://code.claude.com/docs/en/changelog) 重新查核一次。

## 內容來源

- Claude Code 官方文件：https://code.claude.com/docs
- GitHub Docs：https://docs.github.com
- LAB 關卡 5 的結果為 2026-09-17 以 Claude Code v2.1.274 實際執行的紀錄
