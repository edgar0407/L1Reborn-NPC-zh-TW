# 近期更新（2026年8月）

> 本資料夾收錄本月（截至最新更新）所有新增/修改過的檔案，方便只想看「這個月改了什麼」的人瀏覽，不需要重新下載整個 trunk。
> `trunk/text/` 永遠是完整合併版本，可直接整包覆蓋進遊戲使用；本資料夾內容只是 `text/` 同名檔案的唯讀副本，**不要單獨拿這裡的檔案去覆蓋遊戲**，缺其他未變動的檔案。

---

## 2026-08-28　webstore-e.html 文字潤飾 + 分類清單加空行

- 開頭說明句改成「這是網站會員名下所有帳號與角色可共同存取的儲存空間。」，
  修正「網站會員下所有的帳號」容易誤讀、拿掉半形「&」與缺漏句號的問題
- `全部取出` → `全部物品`，跟上面符文/武器/材料/其他等分類標籤同樣是名詞式命名，風格一致
- 「依類型取出」3 列分類之間各加一個空行，比照 fihm/fvhm 的 Tier 間距做法

## 2026-08-28　luck1/luck2 遺忘之島連結文字簡化

- `luck1-e.html`（3 處）、`luck2-e.html`（1 處）：`action="teleport escape-forgotten-island"` 連結文字統一從「離開這個遺忘之島。」簡化成「離開遺忘之島」

## 2026-08-28　webstore-e.html 開頭說明文字改寫

- `帳號共用倉庫` → `帳號共用倉庫(Web Storage)`，標題加註英文原名
- 原本兩行「可從任何已連結的遊戲帳號將物品存入此處。並從其他已連結的角色中取出。」
  改成一行「這是一個儲存空間供網站會員下所有的帳號 & 角色可共同存取」
- 「存放上限依網站帳號贊助等級而定。」補上免費額度「(免費有25個)」，
  這個數字原本只出現在 `webstoreno-e.html` 裡，現在主頁面也直接看得到

## 2026-08-28　luck1-e.html 補上離開遺忘之島捷徑連結

- `luck1-e.html`：把 `luck2-e.html` 的「離開這個遺忘之島。」連結（`action="teleport escape-forgotten-island"`）複製 3 行放到頁面最上方，比照 escapefi1 的做法

## 2026-08-28　webstore-e.html「依類型取出」補上對齊

- `webstore-e.html`：原本用「.」串接的「符文 . 武器」「材料 . 其他」等 6 個分類連結，改成 2 欄
  （左欄補齊全形空白對齊，`防具與飾品`最長 5 字，其餘補到相同寬度）：
  符文/武器、防具與飾品/消耗品、材料/其他 各一列

## 2026-08-28　商店村傳送捷徑改成 3 行 + 空行分隔

- `gltztele-e.html`、`ortztele-e.html`、`sktztele-e.html`：最上方「傳送至商店村」捷徑連結改成連續 3 行，
  後面加 2 個空行再接「傳送到天堂競技場」捷徑

## 2026-08-28　補完 glt/ort/skt 商店村傳送員全部子頁

- 翻譯：`gltztele2-e.html`、`ortztele1-e.html`、`ortztele2-e.html`、`sktztele1-e.html`（原本都未翻譯）
- `gltztele-e.html`、`ortztele-e.html`：頂部各加上 2 行捷徑（傳送至該村商店村、傳送到天堂競技場），比照 sktztele 的做法
- `sktztele-e.html`：補上 `sktztele1` 的捷徑（傳送至商店村），現在跟商店村/天堂競技場兩個捷徑都在最上方了
- 至此 glt/ort/skt 三個商店村傳送員系列（tele/tele1/tele2/teleC）全部翻譯完成

## 2026-08-28　sktztele2 傳送連結搬到 sktztele 最上方

- `sktztele2-e.html`：翻譯（原本未翻譯，天堂競技場傳送確認頁）
- `sktztele-e.html`：把 `sktztele2` 的實際傳送連結（`action="teleport arcade"`）複製一份放到頁面最上方，原本頁面下方的內容不變
- 發現 `glt`/`ort`/`skt` 三個商店村傳送員其實都各自還有 `XXXtele1`（傳送至商店村確認頁）、`XXXtele2`（傳送至天堂競技場確認頁）兩個子頁，`sktzteleC`（拒絕進入的理由頁）已經翻好了，`sktztele1`、`gltztele1/2`、`ortztele1/2` 目前都還沒翻，先記錄，等使用者確認是否要一併處理

## 2026-08-28　翻譯 3 個商店村傳送員（glt/ort/skt）

- `gltztele-e.html`（古魯丁）、`ortztele-e.html`（歐瑞）、`sktztele-e.html`（銀騎士之村）：
  原本整份都是未翻譯的英文，比照已翻譯好的 `grtztele-e.html`（奇岩村）用詞風格翻譯
- 順手確認 `action="teleportURL"` 不是連結到單一檔案，而是全庫近 90 個檔案共用的
  通用傳送 action，實際目的地由伺服器依觸發的 NPC/場景決定；這 3 個傳送員頁面本身
  已經是「商店村傳送」連結所在的最上層頁面，沒有更早一層需要搬過去
- 順便發現同系列的 `XXXtzguard-e.html`（商店村警衛，負責反方向「返回OO村」）都已經
  翻好了，可作為之後類似組合的參考

- `fihm-e.html`：「挑戰狀態」「停用挑戰」原本被誤補齊成跟 Tier 清單一樣寬（多補了 10 格空白），
  改回只跟彼此對齊（比照 toihm 原始寫法，1 個全形空白即可，因為兩個標籤本來就等長）
- `fihm-e.html`、`fvhm-e.html`：Tier 1~3 之間各加一個空行，不要緊貼

## 2026-08-28　fihm-e.html 用詞調整、比照 toihm/fvhm 風格

- 標題與內文「被遺忘之島」統一改成「遺忘之島」（含標題、選單說明、頁尾限制說明）
- 列名比照 fvhm/dvchm 用詞：「狀態」→「挑戰狀態」、「關閉清除」→「停用挑戰」
- 比對英文原文（`Difficulty, EXP, and drops increase per tier.`），確認現有「難度、經驗值與掉落率均會提升」已完整涵蓋，未提及傷害倍率，故未新增（fvhm/dvchm 的傷害/經驗/掉落分項數值是它們自己才有的內容，fihm 英文原文沒有對應資訊，不硬套）
- 品項名稱變動後重新計算對齊寬度

## 2026-08-28　escapefi1 補上逃離遺忘之島捷徑連結

- `escapefi1-e.html`：把 `escapefi2-e.html` 的「逃離遺忘之島」連結（`action="teleport escape-forgotten-island"`）複製 3 行放到頁面最上方
- 順手修正原檔裡的編碼亂碼：「我是因為被懲罰所以才在這堙v→「我是因為被懲罰所以才在這裡」、「我要在這堿搧蛣L數的冒險家」→「我要在這裡看著無數的冒險家」

## 2026-08-28　rrafons 兌換頁改版：清單移到最上方 + 物品名稱對齊官方譯名

- `rrafons7-e.html` / `rrafons8-e.html` / `rrafons12-e.html` / `rrafons13-e.html`：
  版面改成「置中標題 → 兌換清單 → 分隔線 → NPC 開場白」，清單和兌換連結搬到最上方，
  原本兩頁開場白字數差異造成的換行不會再影響清單起始位置
- 比對 `mapping/real-desc.tsv` 官方物品譯名，修正 3 個誤譯：
  - 綜合香辣醬清單：`種子夾心薄餅`→`煎餅`、`糖醋水果`→`水果糖醋肉`、
    `怪物眼球牛排`→`漂浮之眼肉排`（皆為官方對照表直接收錄的完整料理名）
  - 香草清單：`龜龍餅乾`→`龍龜餅乾`（原本兩字顛倒，官方怪物名是「龍龜」）、
    `艾雷卡多姆燉菜`→`伊萊克頓燉菜`、`烤蠍子`→`烤毒蠍`（比照官方怪物譯名「毒蠍」）
  - 物品名稱變動後，兩份清單的對齊寬度重新計算過

## 2026-08-25　修復同批 10 個壞掉/未翻譯的對話檔

比對 entgate 那次發現的損壞模式（`<html>`/`<body>` 標籤被錯放進按鈕文字裡）在全庫掃描，抓出同樣壞掉的另外 8 個檔案，加上 2 個結構壞掉又從未翻譯的檔案：

- `dogfight8-e.html`：修復結構，補回「領取獎金」按鈕文字
- `doil4b-e.html`：修復結構，移除損壞產生的多餘斷鏈按鈕
- `eggg2-e.html` / `eggg3-e.html`：修復結構，移除損壞產生的重複/空白按鈕（實際有效選項不變）
- `eris4-e.html`：修復結構（原本 `<a>` 標籤互相巢狀，不合法 HTML），還原成兩個獨立按鈕
- `fraoun-e.html`：修復結構，並依英文原文補回遺漏的「武器／盾牌／藥水／食物」品項連結段落
- `gr_trick1-e.html`：修復結構，補回「前往隱藏地城...」按鈕文字
- `luudiel1-e.html`：修復結構，補回兩個按鈕文字（正文為既有精簡翻譯，未擴寫）
- `l_hunt.html` / `u_hunt.html`：這兩個原本完全是英文未翻譯、結構也壞掉，直接同步成已經翻譯正確的 `l_hunt-e.html` / `u_hunt-e.html` 內容

## 2026-08-25　被遺忘之島困難模式補上雙欄對齊

- `fihm-e.html`：08-10 已改成個人/隊伍雙欄格式，但「狀態」「關閉清除」「Tier 1~3」幾個標籤長度不一，沒有補齊對齊；這次比照 rrafons 的對齊規則補上全形空白，讓每一列的個人/隊伍連結對齊同一欄位

## 2026-08-22　修復扭曲的空間（entgate）壞掉的對話檔

- `entgate-e.html`：原檔 HTML 結構壞掉（`<html>`/`<body>` 標籤被錯放進按鈕文字裡，`action="1"` 重複、連結對不上文字），依英文原文與內容幾乎相同的 `entgate2-e.html` 重新翻譯修正
- 檢查同系列 `entgate2-e.html`、`entgate3-e.html` 與英文原文比對，內容意譯但語意正確，未發現結構性問題

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
