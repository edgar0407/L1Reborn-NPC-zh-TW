# 近期更新（2026年9月）

> 本資料夾收錄本月（截至最新更新）所有新增/修改過的檔案，方便只想看「這個月改了什麼」的人瀏覽，不需要重新下載整個 trunk。
> `trunk/text/` 永遠是完整合併版本，可直接整包覆蓋進遊戲使用；本資料夾內容只是 `text/` 同名檔案的唯讀副本，**不要單獨拿這裡的檔案去覆蓋遊戲**，缺其他未變動的檔案。

---

## 2026-09-04　官方更新：亞丁的冒險改版 + 精靈護手／真‧冥皇武器重鑄 + L4困難模式

- **亞丁的冒險（Adventures of Aden）改版**：`adventurehub-e.html`、`restoredadventures-e.html`/`.html`（三檔內容相同，新舊入口都指向同一頁）
  整合為單一冒險選單，收錄水晶洞窟（冰之女王／冰之惡魔）、哈汀的秘辛、歐林海上遠征、守護獨角獸、阿茲莫丹血盟地下城，以及獨立迷你攻城戰報名入口
- **水晶洞窟**：`cqueen-e.html`/`.html`（冰之女王路線）、`cdemon-e.html`/`.html`（冰之惡魔路線）——1-6人隊伍，限時清除五間冰封密室
- **歐林海上遠征**（新增party小遊戲，沿用既有「歐林」譯名）：`orimvoyage-e.html`/`.html`（主頁）、`orimattack-e.html`（攻擊符文）、
  `orimdefense-e.html`（防禦符文）、`orimportal-e.html`（登船符文）、`orimreturnrune-e.html`（歸返符文）、
  `orimcannonp-e.html`/`.html`（左舷砲台）、`orimcannons-e.html`/`.html`（右舷砲台）、`orimstatus-e.html`（狀態/獎勵查詢）——反派新譯名「歐丁」（Oldin）
- **精靈護手系統**（叛逃者NPC新增分支，`defecter2-e.html` 補上連結）：`defecter14-e.html`（總覽）、`defecter15-e.html`（力量）、
  `defecter16-e.html`（精準）、`defecter17-e.html`（洞察）——消耗+7精靈手套（冰/暗/火/風四元素之一）與對應+7手套（反王肯恩／死亡騎士／賽尼斯）精煉成60級精靈護手
- **真‧冥皇武器重鑄**（新NPC，沿用既有「真‧冥皇」譯名系列）：`fidref1-e.html`（總覽）、`fidref02`~`fidref09-e.html`（風刃短刀／真‧冥皇執行劍／
  紅影雙刀／聖晶魔杖／野獸王的鋼爪／蓋亞之怒／克羅諾斯之懼／海柏利安的絕望，八款既有黑暗妖精武器可互相重鑄，武器名稱沿用 `adelio2`~`adelio18` 系列既有譯名）
- **L4困難模式**（新增）：`l4warden-e.html`、`l4wardenc-e.html`——官方原文標題為戲謔式的「L4 FUCK YOU HARD MODE」，中文採委婉但保留自嘲語氣的「L4 找死模式」（使用者確認譯名）
- `autopot-e.html`：官方改版自動補藥選單，新增「多餘藥水」自動使用功能（使用上限50%~90%可調）與「測試／重新整理」按鈕，「使用時機」等既有翻譯沿用

## 2026-09-05　補翻舊漏檔：法師梅林（奇岩地下城/浮士德）

- `merlin1-e.html`、`merlin2-e.html`：使用者提供原文關鍵字找出的舊漏翻檔案（來自 `RefrenceOnly/Reborn/` 基礎快照，非本次官方更新內容），
  講述奇岩地下城（Giran Dungeon）曾是監獄、囚犯浮士德（Faust）出賣靈魂、亞丁國王以乙太結界封印該地的背景故事
- 新譯名：Giran Dungeon→奇岩地下城（沿用既有 Giran=奇岩）、Faust→浮士德、Aetheric Field→乙太結界
- `autopot-e.html`：使用者校正用詞，標題「自動補藥」→「自動喝水」，「多餘藥水」→「低階藥水」
- `telephantasm-e.html`：使用者手動於最上方加入3行「前往夢幻之島」捷徑連結，比照 escapefi1/luck1 等既有頁面格式
- `merlin1-e.html`：比對過 `RefrenceOnly/Justice` 快照後（發現 Justice 版 merlin1 檔案內容與 merlin2 錯置，不可直接沿用），
  於最上方加入3行 merlin2 的傳送連結（`teleport giranD`／「請將我送往監獄。」）捷徑，比照 telephantasm-e.html 格式

## 2026-09-14　符文稀有度用詞改回英文 + 網頁倉庫新增分類 + 寶石兌換改版 + 倉庫NPC翻新

- `runegambler.html`/`runegambler-e.html`（符文賭博師）、`runereforge.html`/`runereforge-e.html`（符文重鑄師 維爾）：
  稀有度名稱由中文改回官方原文，非凡→Uncommon、稀有→Rare、史詩→Epic、傳說→Legendary（「下一稀有度」等泛指用法維持中文不動）
- `webstore-e.html`（網頁倉庫）：依類型取出新增4個分類（原3行4類→5行10類），新譯名：Dolls→魔法娃娃、Scrolls and Books→卷軸與書籍、
  Chests and Event→寶箱與活動、Pets and Quest→寵物與任務物品
- `dio1-e.html`（珠寶商 迪歐，寶石兌換）：新增一段「以稀有度為列」的對照表放最上方，每列可直接點擊升級／降級（紅寶升品紅、
  品紅升高品紅⋯四色皆同款簡稱），取代原本「藍寶石/高級/最高級」等籠統字樣；原本的圖示升降級連結列移到頁面最下方保留；
  對照表四色改用正確的顏色（紅寶石系紅色、藍寶石系藍色、綠寶石系綠色）
- **倉庫管理員類 NPC 翻新**（`nodim-e.html` 諾丁、`rayearth1-e.html`/`prayearth-e.html` 雷亞斯 等）：統一套用新版倉庫頁格式——
  頂端「個人倉庫：存入　／　領出」「血盟倉庫：存入　／　領出」快速連結、底部補回「確認血盟倉庫使用記錄」；
  順便修正諾丁血盟倉庫連結誤指到另一個NPC「艾塞隆」頁面的錯誤，改回指向自己的頁面
- `Customization/Storage/text/` 底下 35 個倉庫管理員 NPC 草稿統一改名為 `*-e.html`（比對確認遊戲實際讀取的是這個檔名），
  並套用同樣的新版倉庫頁格式間距（全形空白＋全形斜線＋全形空白）
- `trunk/text/kuhatin-e.HTML` 副檔名大寫的問題已修正為小寫 `kuhatin-e.html`
