Note：
**設定同步更新**資料刪除後不保留
目前繞過壞掉的npx，往後要輸入一律改成用專案內建的 **`npm run`** 指令替代。%%因為 `npx` 指令在電腦裡有損毀%%
%%**本地專案路徑**：Desktop\quartz-blog%%`

%%
 `Symlink` 改回 `Copy` 
	`Symlink`（符號連結）本質上只是在 `quartz-blog` 裡面放了一個「指向你 Obsidian 資料夾的捷徑」
	* 改回 Copy ：你隨時可以把這個捷徑檔案刪除，然後自己建立一個真正的、普通的 `content` 資料夾，再把筆記手動複製進去。
	* **想徹底重新設定的做法**：你也可以隨時在終端機再次輸入 `node quartz/bootstrap-cli.mjs create`，Quartz 就會跳出一樣的畫面，讓你重新選擇一次。
%%

%%
local指令
	cd Desktop/quartz-blog 確保在此資料夾
	node quartz/bootstrap-cli.mjs build --serve
	網址 http://localhost:8080
	Done in an hour!
%%


- 官網下載node.js v24.18.0 LTS
## CMD

npx quartz create(**`npm error could not determine executable to run`**)
npm install -g npm@12.0.1 %%更新npm%%

cd Desktop 
mkdir quartz-blog %%make directory 建立quartz-blog資料夾 %%
cd quartz-blog
git clone https://github.com/jackyzha0/quartz.git . %%透過git直接下到當前資料夾%%
npm install %%安裝專案所需套件%%
node quartz/bootstrap-cli.mjs create %%Quartz 最新版本Quartz 5更改為bootstrap-cli.mjs%%
Obsidian
Symlink an existing folder
(Enter) path to existing content folder
Enter the base URL for your Quartz site (e.g. mysite.github.io/quartz) %% KCOxO.github.io/Roadmap 。走到這會自動去 GitHub 上載入一個專門的第三方套件 quartz-themes到(Desktop\quartz-blog) %%






%%
## 三種差異

- `Copy an existing folder`（複製現有資料夾）
	-Quartz 會把你現有的 Obsidian 筆記資料夾「整個複製一份」進來。
	-最安全，Quartz 不會不小心改動到你原本在 Obsidian 的原始檔案。
	-只有在「這一次執行設定」時幫你複製過去
-  `Symlink an existing folder`（建立符號連結）
	-**之後你只要在 Obsidian 裡面寫筆記、儲存，Quartz 這裡就會**自動同步更新，你不需要手動一直複製貼上。
	-如果以後在 Quartz 裡不小心刪除檔案，Obsidian 本地的原始檔案也會跟著不見。
-  `Empty Quartz`（空白的 Quartz）
	-建立一個完全空白、只有幾篇預設範例筆記的資料夾。
	-手動打開電腦的檔案總管，把筆記一邊一邊手動複製進 `C:\Users\K\Desktop\quartz-blog\content`。

進階方法：把 Quartz 直接塞進 Obsidian
- **優點一：在 Obsidian 內部就能直接管理網站檔案**  
    除了筆記外，Quartz 還有很多設定檔（例如調整網站標題、顏色、側邊欄的 `quartz.config.ts`）。如果用做法 B，這些網站設定檔會直接出現在你的 Obsidian 左側目錄中。你可以直接在 Obsidian 裡一邊寫筆記，一邊點開設定檔修改網站外觀，不需要在兩個資料夾之間跳來跳去。
- **優點二：完全避開 Windows 捷徑（Symlink）可能失效的風險**  
    Windows 的 Symlink 有時候會因為系統權限、外接硬碟代號改變、或是雲端硬碟（如 OneDrive/iCloud）同步而失效。做法 B 因為所有檔案都在同一個資料夾裡，絕對不會有捷徑斷掉的問題。

---
%%

