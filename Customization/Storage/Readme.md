# Storage（倉庫管理員對話統一版）

## 這裡是什麼

Reborn 官方翻譯裡，35 個倉庫管理員 NPC 的對話格式很不統一：開場白各說各話、按鈕文字有「取出/領取/索回/託付」四種說法、功能完整度也不一致（有的有「確認血盟倉庫使用記錄」，大多數沒有）。

這個資料夾把這 35 個檔案統一成同一種格式，並修掉順手發現的幾個 bug。**這裡的檔案是自訂/提案性質，不是官方翻譯，不會覆蓋 `trunk/text/` 裡的正式檔案**，需要你自己確認過再套用。

## 統一後的格式

參考舊版（`E:\SynologyDrive\Games\Lineage天堂\對話\text-倉庫`）的結構：

1. **開頭先放快速操作區**（NPC 名字之後、開場白之前）：
   ```
   個人倉庫：存入 / 領出
   血盟倉庫：存入 / 領出
   ```
   熟悉倉庫怎麼用的玩家可以直接點，不用先看完開場白。
2. **開場白往下放**——每個 NPC 原本的開場白/規則說明，內容保留 Reborn 現有翻譯，只是位置移到快速操作區後面。
3. **底部維持完整按鈕區**（統一措辭）：
   ```
   個人倉庫：存放物品 / 取出物品
   血盟倉庫：使用血盟倉庫 / 確認血盟倉庫使用記錄
   ```

按鈕文字統一為「存放物品／取出物品」，取代原本「領取物品／取回物品／索回物品／寄放物品」等 4 種不同說法。「確認血盟倉庫使用記錄」（`action="history"`）原本只有 3 個 NPC 有，這次全部補上——這個 action 在 Reborn 確實有支援（`pXXX` 血盟倉庫子頁也在用同一個 action），但因為只在少數幾個 NPC 主頁面上驗證過會動，套用到遊戲前**建議先挑一兩個實測看看**。

## 順手修掉的 bug（原本 Reborn 版本就有）

- **血盟倉庫連結指錯人**：`borgin`、`dorin`、`gotham`、`haidrim`、`kuhatin`、`nodim`、`tarkin`、`tofen`、`Kriom`、`karim` 這 10 個檔案的血盟倉庫連結原本都指向 `paxellon`（複製 axellon 檔案時忘記改），已經改回各自對應的 `pXXX` 頁面（例如 `pborgin`、`pdorin`…）。
- **`tigus-e.html`、`zidar-e.html`**：血盟倉庫連結原本指向 `pgawl`（另一個 NPC 的頁面），已修正為 `ptigus`、`pzidar`。
- **`tigus-e.html`、`zidar-e.html`、`rayearth1-e.html`**：AI 翻譯標記寫成明文「烏薩奇說: AI英翻中」而不是 HTML 註解，玩家在遊戲裡會看到這行字；`rayearth1-e.html` 底部還多貼了一整段英文原文對照，同樣會顯示出來。這次都拿掉了。
- **`brogin-e.html`**：開場白裡有一段疑似編碼錯誤的亂碼「這堛澈O管費是從國庫的公款支出」，判斷應該是「這裡的保管費是從國庫的公款支出」，已修正。

## 未修的已知問題（沒有把握，先記錄）

- **`kasham-e.html`、`luku-e.html`** 的血盟倉庫連結指向 `pkasham`、`pluku`，但整個專案（含 RefrenceOnly）都找不到這兩個檔案——不確定是伺服器端真的有這兩頁只是還沒拉進來翻譯，還是本來就是斷鏈。這次維持原本連結，沒有動。
- **`brogin-e.html`** 沒有對應的 `pbrogin` 血盟倉庫子頁，它的血盟倉庫存/取是直接用 `action="deposit-pledge"`／`retrieve-pledge` 寫在主頁面上（跟其他人用連結到子頁的方式不同）。這次維持這個做法，統一版裡也沒有幫它另外做子頁連結。

## 檔案清單

```
Kriom-c.html      axellon-c.html    bahof-c.html      borgin-c.html
brogin-c.html     dorin-c.html      garin-c.html      gawl-c.html
gotham-c.html     haidrim-c.html    hakim-c.html      hirim-c.html
jianku-c.html     juke-c.html       kamu-c.html       karim-c.html
karudim-c.html    kasham-c.html     kuhatin-c.html    kuron-c.html
kusian-c.html     kuud-c.html       luku-c.html       nodim-c.html
ogi-c.html        orclon-c.html     rayearth1-c.html  sauram-c.html
tarkin-c.html     thram-c.html      tigus-c.html      timpukin-c.html
tofen-c.html      tulak-c.html      zidar-c.html
```

檔名沿用原 NPC 名（不含 `-e.html`），存成 `-c.html`，跟正式套用的 `-e.html` 區分開來，避免不小心被吃檔工具直接抓走。要套用時，把對應內容複製進 `trunk/text/` 底下同名的 `-e.html` 檔案即可。
