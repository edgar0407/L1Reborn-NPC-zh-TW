# 近期更新（2026年8月）

> 本資料夾收錄本月（截至最新更新）所有新增/修改過的檔案，方便只想看「這個月改了什麼」的人瀏覽，不需要重新下載整個 trunk。
> `trunk/text/` 永遠是完整合併版本，可直接整包覆蓋進遊戲使用；本資料夾內容只是 `text/` 同名檔案的唯讀副本，**不要單獨拿這裡的檔案去覆蓋遊戲**，缺其他未變動的檔案。

---

## 2026-08-21　鍊金術師移除斷鏈

- `alchemy1-e.html`：移除「萃取黑色血痕」(`link="alchemy26"`) 連結，該頁面在整個專案中從未存在（含 RefrenceOnly 各版本），點了沒有內容，屬於既有斷鏈

## 2026-08-21　安東新增虛空金屬盔甲選項

- `anton2-e.html` / `anton2.html`：技師安東新增第二項鍛造選項「Craft Void Plate Mail.」，翻譯為「製作虛空金屬盔甲」
- 比對 Reborn-20260819 官方全量 148 個檔案，145 個與過去快照逐位元組相同（伺服器整包重出既有內容），僅 anton2 這組是真的更新

## 2026-08-19　rrafons 兌換選單改版

- `rrafons7-e.html` / `rrafons8-e.html` / `rrafons12-e.html` / `rrafons13-e.html`：香辣醬／香草兌換清單改為「品項　x1　x10」雙欄格式，全形空白補齊對齊，x1/x10 與品項名稱（綜合香辣醬／香草）加上顏色區分
- 移除 `goblinprisoner-e`、`goblintreasure1~3(-e)`、`gtreas1~3(-e)` 共 13 個孤兒檔（檔名過長被吃檔工具靜默跳過，內容已被 `gpris`/`gtrs1~3` 取代）

## 2026-08-14　官方更新：巨龍戰利品廳、秘密飛龍傳送門

- 新增巨龍戰利品廳系列對話（`drgha`、`drghdone`、`drgheads`、`drgherr`、`drghf`、`drghl`、`drghneed`、`drghused`、`drghv`）與秘密飛龍傳送門（`dsecret1~3`）
- 更新符文重鑄師（`runereforge`/`runereforges`）與羅賓孫（`robinscroll`/`robinscroll2`）清單

## 2026-08-10　補漏與選單版面調整

- 補齊漏併入主線的 `dvchm-e.html`（07-10 已翻好但只留在舊 patch 資料夾，未併入根目錄）
- 新增藥水商 Sasha 對話 `noodle-e.html`、登入畫面歡迎詞 `intro-e.tbl`
- `bscrolls1~5-e.html` 全形數字改半形，選項間對齊方式統一；`fihm-e.html` 改為個人/隊伍雙欄格式，與 dvchm 等新版選單風格一致

## 2026-08-01　官方更新：多項系統性改版

- 神秘吟遊詩人主選單改版，`bscrolls1~5` 新增 x100 兌換，新增傲慢之塔卷軸升降級功能（`toidown`/`toiscrollup`）
- 傲慢之塔困難模式（`toihm`）更新王討伐規則說明
- 鐵匠亞提利歐新增克羅諾斯之懼武器線，海柏利安之絕望移至 `adelio18`
- 鐵匠皮爾選單改版，新增古代戰士臂甲 `pual8`
- 新增哥布林王事件全套翻譯（`goblinprisoner`/`gpris`/`goblintreasure`/`gtreas`/`gtrs` 系列，後於 08-19 精簡孤兒檔）
- 新增歐林之影 NPC 與完整任務線翻譯（`orim1~10`）
- 新增食人妖精競賽導覽 `bugrace`、自由披風織工 `freedomcloak`、戒指插槽解鎖 `slot6`/`slot7`/`slot9`

---

詳細逐檔異動請參閱 git log（`git log --since=2026-08-01`）或 [devlog](../../readme.md)。
