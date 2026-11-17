# Agent Skills

可供 Claude Code 和 Codex 使用的 skills，集中在這個 Git 專案維護。

## Skills

- [natural-zh-tw](skills/natural-zh-tw/SKILL.md)：用自然、精簡的台灣繁體中文寫作。

## 安裝

先把這個專案 clone 到固定位置，再進入專案根目錄執行：

```sh
mkdir -p ~/.claude/skills ~/.codex/skills
ln -s "$(pwd)/skills/natural-zh-tw" ~/.claude/skills/natural-zh-tw
ln -s "$(pwd)/skills/natural-zh-tw" ~/.codex/skills/natural-zh-tw
```

若目標路徑已存在，先檢查既有內容，不要直接覆蓋。符號連結指向此專案，移動或刪除專案後需要重新建立連結。重新啟動 Claude Code 或 Codex，讓新 skill 被載入。

## 更新

在這個專案編輯 `skills/natural-zh-tw/SKILL.md`，兩個工具會共用同一份內容。從 GitHub 更新時，在專案根目錄執行 `git pull`。新增 skill 時，在 `skills/` 底下建立獨立資料夾，並依照上面的方式建立連結。
