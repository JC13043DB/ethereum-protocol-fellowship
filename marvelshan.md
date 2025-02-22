---
timezone: Asia/Shanghai
---

# Zaki

1. 自我介绍
    - Hi我是Zaki，這是第1次參加共學，大家一起努力！
2. 你认为你会完成本次残酷学习吗？
    - Let's go!!!!

## Notes

<!-- Content_START -->

### 2025.02.06

“Heroes are heroes because they are heroic in behavior, not because they won or lost.”
— Nicholas Taleb

## Prehistory

- 在 prehistory 的第一張及介紹了 Ethereum 的的起源和願景 並且從 1969 年冷戰時的 ARPANET 開始介紹，從此之後網路迅速的擴張，到目前已經是幾十億人在使用了。

- 接著是 UNIX 的起源了，不得不說到的事兩位偉大的人物，Ken Thompson 和 Dennis Ritchie，Dennis Ritchie 也可稱它為 dmr，他也早一步在 2011 年時離開了，這兩位為了未來的資訊世界發展可說是最重要並且沒有之一呀，後續 Thompson 也前往了 google 並發明了 go 語言，後續就不多說了([wiki](https://zh.wikipedia.org/zh-tw/%E8%82%AF%C2%B7%E6%B1%A4%E6%99%AE%E9%80%8A))。在 UNIX 中，帶入了像是分層系統，shell 等等的功能與概念，讓未來的資訊系統世界打好良好的網路基礎設施概念，以下簡單的解釋這些概念。

### **Unix 的階層式檔案系統（Hierarchical File System）**

Unix 採用 **階層式檔案系統（Hierarchical File System, HFS）**，這是一種樹狀結構的目錄系統，所有的檔案和目錄都從 **根目錄（`/`）** 開始，逐層向下展開。

📂 **主要概念**：

1. **根目錄 `/`**：Unix 檔案系統的最頂層，一切皆從 `/` 開始。
2. **標準目錄**：
   - `/bin`（Binary）：基本可執行程式，如 `ls`、`cp`、`mkdir`。
   - `/home`：使用者的家目錄（如 `/home/user`）。
   - `/etc`：系統設定檔，如 `/etc/passwd`（使用者帳號資訊）。
   - `/var`：動態資料，如 `/var/log`（系統日誌）。
   - `/tmp`：暫存檔案（開機後可能被刪除）。
3. **絕對路徑 & 相對路徑**：
   - **絕對路徑**：從根目錄 `/` 開始，例如 `/home/user/file.txt`。
   - **相對路徑**：相對於當前目錄，例如 `./file.txt`。
4. **檔案與目錄權限**：
   - 使用 ls -l 可查看權限（`rwxr-xr-x` 代表擁有者可讀寫執行，其他人只能讀取和執行）。

---

### **Shell 作為命令列介面（Shell as a Command-Line Interface）**

**Shell** 是 Unix/Linux 的命令列介面（CLI），用來與作業系統互動。常見的 shell 包括：

- **Bash（Bourne Again Shell）**：預設於大多數 Linux 發行版。
- **Zsh（Z Shell）**：功能更強大，許多 macOS 使用者選擇使用。
- **Fish（Friendly Interactive Shell）**：強調易用性與自動補全。

📌 **常見的 Shell 操作**：

- `pwd`：顯示當前路徑。
- `ls`：列出目錄內容（`ls -l` 顯示詳細資訊）。
- `cd /path/to/dir`：切換目錄。
- `cp source destination`：複製檔案或目錄。
- `mv old_name new_name`：移動或重新命名檔案。
- rm file / `rm -r dir`：刪除檔案或目錄（⚠️ 小心使用）。

---

### **單一用途的 Unix 工具（Single-Purpose Utilities）與組合使用**

Unix 遵循 **「一個程式只做一件事，並且做得好」** 的設計哲學，許多工具都是單一用途，但可以透過 **管線（`|`）** 和 **重導向（`>`、`>>`、`<`）** 組合來完成更複雜的任務。

📌 **常見 Unix 工具**：
| 指令 | 功能 |
|------|------|
| cat file | 顯示檔案內容 |
| grep "keyword" file | 搜尋檔案中的關鍵字 |
| sort file | 對檔案內容排序 |
| uniq file | 移除重複行 |
| wc -l file | 計算行數 |
| head -n 10 file | 顯示前 10 行 |
| tail -n 10 file | 顯示最後 10 行 |
| cut -d',' -f2 file.csv | 擷取 CSV 第二欄 |
| awk '{print $1}' file | 取出第一欄 |
| sed 's/old/new/g' file | 文字取代 |
| find /path -name "*.txt" | 在指定路徑尋找檔案 |
| xargs | 接收輸入並執行指令 |

---

- 在那個充滿阿諛我詐的戰爭時代中，資訊網路是一大通訊的利器，但是在戰爭中就有敵對的一方，讓對方知道了了傳輸資料是一件危險的事情，這時加密與解密就是相當重要的技術了，這時我們相當熟悉的電影模仿遊戲中的主角圖靈 Alan Turing 在其中也扮演了相當重要的角色，在此之後密碼學也迎來快速的發展。
  - 1974 年，Ralph Merkle 提出了 Merkle’s Puzzles，這是一種讓雙方在沒有共同秘密的情況下交換訊息並建立共享密鑰的方法。
  - 1976 年，Whitfield Diffie 和 Martin Hellman 受 Merkle 的研究啟發，發表了 **「New Directions in Cryptography」**（密碼學新方向）論文，並提出了 Diffie–Hellman 密鑰交換算法，這標誌著「無需信任的加密技術」的誕生。
  - 1977 年，Ron Rivest、Adi Shamir 和 Leonard Adleman 發明了 RSA 加密系統，這是第一個可行的公鑰密碼學實作，並在論文《A Method for Obtaining Digital Signatures and Public-Key Cryptosystems》中發表。
  - 1977 年，數學家 Martin Gardner 在《Scientific American》雜誌上介紹了 RSA-129 加密挑戰，並懸賞 $100 獎勵破解者。
  - 1994 年，一組科學家與志願者成功破解 RSA-129，並將獎金捐給自由軟體基金會，證明了「加密的完美安全性只是一種幻覺」，因為密碼技術需不斷進化來應對新威脅（如量子計算機）。
  - 現代 RSA 加密（1024 至 4096 位元）成為網路安全的基礎，保護金融交易，促進電子商務與網路銀行的發展。
- 在過去 code 是相當自由的存在，會刊登在報紙上讓每個人都能有反饋，想當初小時候都會拿報紙上的數讀在解，現在的小孩應該都沒有這種回憶了。在過去 IBM 可說是壟斷了計算機這塊的市場，在 1969 年美國的反壟斷訴訟打開了軟體必須綁定硬體的鎖鏈，接著的開源大戰也開打，從 Unix 的收費到微軟大大 Bill Gates 停止共用 BASIC source code，GNU 也因此從 Richard Stallman 的手上催生了，接著的網路世界也慢慢到我們熟知的 Linus Torvalds 開發的 kernel 奠定了未來軟體開發的藍圖。
- 講回在 WW2 結束時，各國對於密碼學的控制，美國也將此列入管制，不外乎於當時的國家安全局 NAS，當時 MIT 所發表的 RSA 一度被列為機密，後續也因為此，被公共強烈的批評，政府試圖削弱密碼學的行為被視為監控公民通信的手段，但是密碼學的研究仍在持續發展。後續在許多的密碼學家的推動下，cyberpunks 也快速地被推動著，這場運動 最終推動了去中心化數位貨幣的誕生，為後來的區塊鏈與比特幣奠定了理論基礎。
- 資訊世界快速的發展下，在 1990 年時 David Chaum 推出 DigiCash，嘗試建立匿名數位支付系統，提供隱私保護。然而，由於過於依賴傳統金融機構，最終於 1998 年破產，未能普及， Wei Dai 的 B-money 和 Nick Szabo 的 BitGold 都試圖解決數位貨幣的去中心化問題，但當時技術條件尚未成熟，未能廣泛應用，這些理念影響了 2008 年比特幣（Bitcoin）的誕生，中本聰（Satoshi Nakamoto）在白皮書中提出了區塊鏈技術，成功實現了真正的去中心化數位貨幣。
- 2008 年，中本聰（Satoshi Nakamoto）提出了比特幣，去中心化的電子現金系統，並且不依賴任何中心化的發行機構或資產作為支持，比特幣使用區塊鏈技術來確保交易的安全性和順序，並且可以在沒有銀行或中介機構的情況下進行交易，不僅是一種數字貨幣，還是一個社會經濟實驗，利用了「POW」機制，允許在無需中央控制的情況下達成交易順序的共識，但其網路也顯示出某些局限性，尤其是在應用開發方面，許多嘗試在比特幣區塊鏈上構建的應用由於網路擴展性差，變得非常複雜且不易擴展。
- 2012 年，Vitalik Buterin 和 Mihai Alisie 創辦了 Bitcoin Magazine，Vitalik 很快發現比特幣的局限性，並提出了一個可以支持各種金融應用的平臺構想，在 Gavin Wood 的協助下，乙太坊（Ethereum）的設計得到了正式確立，並開始著手建設一個去中心化的世界電腦，這個平台不僅支持數字貨幣交易，還能運行智能合約和去中心化應用（DApps），2015 年 7 月 30 日，乙太坊正式啟動，成為一個致力於建立自我主權經濟的平臺，也利用數字貨幣建立更為開放和自由的經濟體系，到目前為止市值已超過 $400 billion 美元，為非常重要的區塊鏈平台之一。



### 2025.02.07

## Architecture

以太坊的協議架構經過多年的演進，目前分為兩個主要部分：**執行層（Execution Layer, EL）**和**共識層（Consensus Layer, CL）**。這兩個層次分別負責不同的功能，並通過定義好的 API 進行互動。以下是對其架構和流程的詳細說明。

---

#### 1. **執行層（Execution Layer, EL）**
   - **功能**：負責處理實際的交易和用戶互動，執行智能合約，並維護區塊鏈的狀態（State）。
   - **核心元件**：
     - **EVM（以太坊虛擬機）**：執行智能合約的環境。
     - **交易池（TXs/newpool）**：存儲待處理的交易。
     - **State（狀態數據）**：區塊鏈的當前狀態。
     - **JSON-RPC**：提供與外部應用程序（如 Web3）的接口。
   - **p2p 網路**：使用 **devp2p** 協議與其他 EL 節點通信，傳輸交易和區塊數據。

#### 2. **共識層（Consensus Layer, CL）**
   - **功能**：提供權益證明（Proof-of-Stake, PoS）共識機制，確保所有節點遵循同一條鏈，並驅動執行層的規範鏈（Canonical Chain）。
   - **核心元件**：
     - **RANDAO**：隨機數生成機制，用於選擇驗證者。
     - **LMD-GHOST**：分叉選擇算法，決定哪條鏈是有效的。
     - **Beacon APIs**：與信標鏈（Beacon Chain）相關的接口。
     - **Validators（驗證者）**：負責驗證區塊和交易的節點。
   - **p2p 網路**：使用 **libp2p** 協議與其他 CL 節點通信，傳輸共識相關數據（如見證 Attestation）。


![image](https://github.com/user-attachments/assets/73d6c77d-069b-4f1f-a053-d87a84860668)

---

### **Eth 1.0 與 Eth 2.0 的共識機制比較**

#### 1. **Eth 1.0（PoW 機制）**
   - **共識機制**：工作量證明（Proof-of-Work, PoW）和分叉選擇規則（Fork Choice Rule）。
   - **流程**：
     1. 節點收到新區塊後，驗證 PoW 的有效性。
     2. 比較新鏈的累積工作量（Work），選擇工作量最高的鏈。
     3. 執行並驗證區塊中的交易，確保交易有效。
   - **特點**：PoW、分叉選擇和交易驗證是綁定在一起的（如 Geth 客戶端）。


![image](https://github.com/user-attachments/assets/1255ae31-c972-42a0-8ef4-4952fd0db185)

#### 2. **Eth 2.0（PoS 機制）**
   - **共識機制**：權益證明（Proof-of-Stake, PoS）和分叉選擇規則。
   - **流程**：
     1. 節點收到新區塊後，驗證 PoS 的有效性。
     2. 根據驗證者的見證（Attestation）數量決定區塊的權重，選擇權重最高的鏈。
     3. 執行並驗證區塊中的交易，確保交易有效。
   - **特點**：PoS 和分叉選擇由 CL 處理，交易驗證由 EL 處理。


![image](https://github.com/user-attachments/assets/8231039a-8770-44aa-b416-2671db6926d6)

---

### **CL 與 EL 的互動流程**

1. **區塊提案與驗證**：
   - 當 CL 收到新區塊時，會將區塊中的 EL 相關內容（如交易）通過 **Engine API** 發送給 EL。
   - EL 驗證交易的有效性，並將結果返回給 CL。
   - 如果交易有效且符合 CL 的分叉選擇規則，CL 會通知 EL 更新狀態。

2. **狀態更新**：
   - CL 決定哪條鏈是最長鏈後，會通知 EL 套用該區塊中的交易，並計算最新的狀態（State）。
   - EL 更新狀態後，將結果返回給 CL。

3. **區塊生成**：
   - 如果 CL 節點是驗證者並需要提案區塊，它會請求 EL 生成 EL 區塊（包含 EVM 交易）。
   - CL 自己生成 CL 區塊（包含驗證者的見證 Attestation）。
  
   
![image](https://github.com/user-attachments/assets/39745d7a-4f42-4eb4-8ecd-a83a252c67ae)

---

### **CL 與 EL 的獨立性**

- **開發者互動**：
  - 開發者通過 **web3.eth** 與 EL 互動（如查詢交易、狀態）。
  - 通過 **web3.beacon** 與 CL 互動（如查詢共識相關數據）。
- **p2p 網路**：
  - EL 使用 **devp2p** 網路（Eth 1.0 的 p2p 協議）。
  - CL 使用 **libp2p** 網路（Eth 2.0 的 p2p 協議）。
![image](https://github.com/user-attachments/assets/0ef94e96-7ab4-407a-8308-cc5f19433806)

![image](https://github.com/user-attachments/assets/e8b9b431-c674-436d-932e-32a30c915014)

在合併前，以太坊的執行層和共識層是獨立運行的，所有交易和區塊驗證都由執行層完成，並依賴 PoW 共識機制。

自 2020 年 12 月起，共識層（信標鏈）開始運行，採用 PoS 共識，並協調驗證者（Validator）。

合併後，以太坊正式轉向 PoS，執行層負責交易處理，共識層負責驗證區塊，兩者需協同運作。
![image](https://github.com/user-attachments/assets/6e7352fe-74bc-41d5-bcb9-ad9cf61f4164)

參考：

[Eth 2.0 的共識層和執行層分工及 The Merge 影響](https://medium.com/taipei-ethereum-meetup/eth-2-0-cl-el-separation-and-impact-of-the-merge-dbeb6828c907)

[如何跑起以太坊執行層與共識層客戶端](https://medium.com/swf-lab/%E5%A6%82%E4%BD%95%E8%B7%91%E8%B5%B7%E4%BB%A5%E5%A4%AA%E5%9D%8A%E5%9F%B7%E8%A1%8C%E5%B1%A4%E8%88%87%E5%85%B1%E8%AD%98%E5%B1%A4%E5%AE%A2%E6%88%B6%E7%AB%AF-54d0b472e7ac)

### 2025.02.08

在 Ethereum 協議設計中，有兩個特別的設計原則值得關注：**Modularity** 和 **Non-discriminant**。

#### **1. Modularity**
Modularity 使得 Ethereum 協議能夠靈活適應未來的技術變革。這種設計哲學意味著 Ethereum 的核心協議應當是高度模組化的，使開發者能夠在不影響整個應用堆疊的情況下進行局部修改。

- **靈活升級**：Ethereum 持續進行研究與工程改進，模組化架構允許開發者針對特定部分進行優化，而不會影響整體系統運作。例如 Proto-Danksharding 的引入，為 Layer 2 擴展提供了靈活的構建模組。
- **獨立性與可重用性**：許多 Ethereum 內部的技術創新，如 Dagger、Patricia Trees 和 SSZ，都被設計為獨立的庫，即使 Ethereum 本身不使用其中的某些功能，它們仍然可以被其他協議採用。
- **封裝複雜性**：Ethereum 的架構由多個子系統組成，每個子系統內部可能相當複雜，但對外提供的是高級接口，讓開發者能夠輕鬆組裝和調試不同的組件，提高開發效率與系統穩定性。

#### **2. Non-discriminant**
Ethereum 的設計哲學源自 FOSS（自由與開源軟體）和 Cypherpunk 運動，強調開放與去中心化，在協議本身對於應用場景的中立性：

- **無審查**：Ethereum 不會主動限制特定類型的應用，任何人都可以在協議之上部署智能合約，只要它們遵循協議規則。
- **關注協議本身的穩定性**：Ethereum 內部的調控機制僅針對協議的安全性與穩定性，而不會基於價值判斷來限制某些應用。例如，理論上，你可以在 Ethereum 上運行一個無限迴圈的腳本，只要你願意支付計算步驟所需的交易費用，並且不超過協議允許的 Gas 限制。
- **去中心化精神**：這種設計確保 Ethereum 平台保持對所有開發者的開放性，不會因特定應用場景或使用者需求而施加額外限制，確保區塊鏈的去中心化本質。

參考：

[模組化區塊鏈是什麼？](https://www.blocktempo.com/what-is-modular-blockchain/)

### 2025.02.09

## UTXO 
全名是Unspent Transaction Output（未花費的交易輸出）。

從較為標準的定義上而言，UTXO（未使用的交易輸出）是比特幣的核心概念之一，UTXO 是一種記錄交易輸出狀態的方式，它跟蹤了每個未使用的交易輸出，以確定哪些比特幣屬於哪個地址。

類比簡單理解，每個 UTXO 就像一張鈔票，它有特定的面值（比特幣數量）並附加了一個鎖，只能被一個私鑰打開。當你要發送比特幣時，你需要選擇一些鈔票，將它們合併成一個新的鈔票，並用收件人的鎖重新鎖上。

UTXO 核心設計思路是：它記錄交易事件，而不記錄最終狀態。要計算某個用戶有多少比特幣，就要對其錢包裡所有的 UTXO 求和，得到結果就是他的持幣數量。

## Nonce

“Nonce”一詞可能看起來充滿技術性且很覆雜，但其本質很簡單。它是一個獨特的數字，源自短語“僅使用一次的號碼”，在區塊鏈和密碼學中髮揮著重要作用。

## [Merkle Patricia Tree](https://hackmd.io/@pohanlu/Merkle_Patricia_Tree)

Ethereum 使用 **修改版的 Merkle-Patricia Trie** 來存儲狀態數據，這是一種結合 **PATRICIA Trie** 和 **Merkle Tree** 特性的數據結構，能夠高效地查找和驗證數據。  

這種 Trie 結構是確定性且可加密驗證的： 
- 狀態的根哈希（state root）是根據所有狀態數據計算出的，兩個相同的狀態必然會有相同的根哈希。  
- 透過 Merkle Proof，可以輕鬆驗證某個值是否存在於該狀態中。  
- 任何改變狀態的操作都會導致根哈希的變化，確保數據的安全性與唯一性。  
- 這種結構理論上能提供 **O(log(n))** 的插入、查找和刪除效率。  


### 1. **帳戶模型 vs UTXO 模型**  
   - 了解這兩種模型的區別，可以幫助我們理解為何比特幣和以太坊在交易處理和隱私性上有所不同。  
   - UTXO 模型提供更好的隱私性和並行處理能力，但帳戶模型更適合智能合約和去中心化應用（DApps）。  
   - 這些概念對於開發智能合約、錢包、交易機制以及 Layer 2 方案（如 Rollups）都很重要。  

### 2. **Merkle Patricia Trie (MPT) 與 Verkle Trees**  
   - 以太坊的狀態存儲依賴 MPT，而未來可能會改用 Verkle 樹，以減少節點存儲需求並提高可擴展性。  
   - MPT 的設計允許高效驗證區塊狀態，這對於輕客戶端（light clients）和 Layer 2 解決方案尤為重要。  
   - Verkle Trees 的研究代表了以太坊向「無狀態客戶端」（stateless clients）邁進的重要一步，這將有助於降低節點運行成本，進一步去中心化網絡。  

### 3. **序列化格式：RLP vs SSZ**  
   - RLP 是以太坊 1.0 使用的序列化格式，但它不支援 Merkle 化，影響了輕客戶端的可行性。  
   - SSZ（Ethereum 2.0 使用）允許更高效的 Merkle 化，使輕客戶端能夠驗證數據而不需要下載整個區塊鏈。  
   - 這些序列化格式影響智能合約的數據存儲方式，以及如何高效同步網絡狀態。  

### 4. **以太坊共識機制與最終性（Finality）**  
   - 以太坊 2.0 採用 **Casper FFG** 和 **LMD-GHOST** 來實現最終性，這與傳統 PoW 區塊鏈（如比特幣）有很大不同。  
   - 了解最終性機制，可以幫助我們理解如何避免長時間的區塊鏈回溯（reorg），以及如何確保交易不可逆。  
   - Gasper（結合 Casper FFG + LMD-GHOST）是以太坊目前使用的完整 PoS 共識協議，這與 DeFi、Staking 獎勵和安全性息息相關。  

### 5. **DHT（分散式哈希表）在以太坊網絡中的作用**  
   - 以太坊使用 DHT（類似於 BitTorrent 和 IPFS）來尋找節點，而非查找區塊。  
   - 這有助於提升 P2P 網絡的效率，並確保以太坊節點能夠快速發現其他節點進行同步。  
   - 了解 DHT 可以幫助我們優化節點發現機制，改善以太坊網絡連接和同步速度。  


參考:

[科普 | 一文讀懂UTXO概念與操作](https://news.cnyes.com/news/id/5534920)

[科普 | 想了解 BRC-20，先學比特幣的 「UTXO 模型」是什麼？](https://www.blocktempo.com/to-understand-brc-20-first-learn-the-utxo-model-adopted-by-bitcoin/)

[什麽是區塊鏈中的交易Nonce？](https://www.gate.io/zh-tw/learn/articles/what-is-a-transaction-nonce-in-blockchain/808)

[連Ethereum都在用！用一個例子徹底理解DHT](https://medium.com/taipei-ethereum-meetup/%E9%80%A3ethereum%E9%83%BD%E5%9C%A8%E7%94%A8-%E7%94%A8%E4%B8%80%E5%80%8B%E4%BE%8B%E5%AD%90%E5%BE%B9%E5%BA%95%E7%90%86%E8%A7%A3dht-f772ea2c6dcf)

[Data Partitioning - Distributed Hash Table and Consistent Hashing](https://ithelp.ithome.com.tw/articles/10226170)

[eth 1.x 與無狀態節點介紹](https://medium.com/cryptocow/eth1-x-stateless-clients-deddc3f935bb)

[Cryptography](https://ithelp.ithome.com.tw/articles/10287338)

[Casper FFG 與 Casper CBC 的瑜亮情結](https://medium.com/taipei-ethereum-meetup/history-and-state-of-ethereums-casper-research-85e8fba26002)


## Protocol history and evolution

### **Frontier - 以太坊的誕生**  

**發布時間：** 2015 年 7 月 30 日 3:26:13 AM UTC（以太坊創世區塊的時間戳）  

Frontier 是以太坊協議的首次正式發布，主要目標是讓開發者開始學習、實驗，並構建去中心化應用（DApps）和工具。  

#### **Frontier 的關鍵特性**  
- **初始 Gas 限制**：  
  - Frontier 啟動時，Gas 限制被硬性設定為 **5000**，這是為了讓礦工和用戶能夠順利運行以太坊節點並安裝客戶端。  
  - 在 **Frontier Thawing Fork**（解凍分叉）後，Gas 限制提升至 **3,141,592（約 3 百萬）**，確保網絡能夠處理更大的交易量。  

- **Canary Contracts（金絲雀合約）**：  
  - 這些合約只會返回 **0 或 1**，作為一種特殊的網絡監控機制。  
  - 如果多個 Canary Contracts 同時回傳 **1**，則表示區塊鏈需要升級，客戶端會自動停止挖礦並提醒用戶更新軟體，避免網絡長時間停滯。  

Frontier 版本主要是讓以太坊開發者熟悉這個新興平台，並為後續的升級做準備。  

---

### **Homestead - 以太坊邁向成熟**  

**發布時間：** 2016 年 3 月 14 日  

Homestead 是以太坊的 **第一個正式穩定版本**，標誌著以太坊從測試階段轉向更穩定、成熟的網絡。這次升級引入了幾個重要的改進，包括安全性強化、Gas 費用調整，以及合約創建邏輯的修正。  

### **Homestead 主要改進**  

#### **EIP-2：合約創建與交易簽名的優化**  
- **提高合約創建的 Gas 費用**：  
  - 透過交易創建合約的 Gas 費用從 **21,000 提高到 53,000**，目的是減少濫用交易來部署合約，鼓勵開發者使用 **CREATE** 操作碼來創建合約。  

- **無效的高 s 值簽名（Invalid high s-value signatures）**：  
  - 簽名中的 `s` 值若超過 `secp256k1n/2`，則交易將視為無效。  
  - 這個改變解決了 **交易可塑性（Transaction Malleability）** 問題，確保交易哈希值不會被輕易修改，提高交易追蹤的可靠性。  

- **合約創建失敗時不再留下空合約**：  
  - 若合約創建時 Gas 不足，將直接導致合約創建失敗，而不是留下一個 **空合約**，避免無效合約佔用區塊鏈狀態存儲。  

- **調整難度調整算法（Difficulty Adjustment Algorithm）**：  
  - Frontier 版本的難度調整機制存在一些問題，Homestead 修改了算法，使區塊時間更加穩定，減少難度變化過大導致的區塊時間波動。  

#### **EIP-7：新增 DELEGATECALL 操作碼**  
- `DELEGATECALL` 操作碼（0xf4）與 `CALLCODE` 類似，但它允許合約傳遞 **原始交易的發送者（msg.sender）和價值（msg.value）**。  
- 這使得 **代理合約模式（Proxy Pattern）** 變得更加靈活，開發者可以使用代理合約來轉發交易，而不影響原始發送者的身份。  

#### **EIP-8：提高網絡升級的兼容性**  
- Homestead 允許以太坊客戶端接受未來協議升級，即使數據包格式有所變化，也不會導致節點之間的連線失敗。  
- 這種「**Forward Compatibility**」機制確保網絡升級時，不會因為不同版本的客戶端不兼容而導致分裂。  

Homestead 讓以太坊從 **測試性質的 Frontier** 進入了更穩定的發展階段，為之後的智能合約應用和 DeFi 領域打下了基礎。  

### **Metropolis —— 智能合約的優化與隱私改進**  
**分為 Byzantium 和 Constantinople 兩個階段，分別於 2017 年和 2019 年發布。**  

Metropolis 旨在提高以太坊的智能合約功能、隱私性和可用性，並為 PoS 轉換做準備。  

#### **Byzantium —— 2017 年 10 月**  
- **EIP-649（降低區塊獎勵 & 延緩難度炸彈）**  
  - 區塊獎勵從 5 ETH 降至 **3 ETH**，減少通脹壓力。  
  - 延緩「難度炸彈」，避免區塊時間過快增加。  

- **EIP-658（交易狀態變更）**  
  - 引入 `status` 字段，讓交易成功與否更清晰。  

- **EIP-197 / EIP-198 / EIP-206（新密碼學指令）**  
  - 增加 zk-SNARK 支持，為以太坊上的隱私交易鋪平道路。  

#### **Constantinople —— 2019 年 2 月**  
- **EIP-145（位移操作提升效率）**  
  - 提升智能合約執行效率，降低 gas 費用。  
- **EIP-1052（智能合約驗證）**  
  - 允許合約透過 `EXTCODEHASH` 來獲取另一個合約的哈希，提高合約間交互效率。  
- **EIP-1234（進一步降低區塊獎勵 & 再次延緩難度炸彈）**  
  - 區塊獎勵從 **3 ETH 降至 2 ETH**，延緩難度炸彈。  

### **Serenity —— 以太坊 2.0**  
Serenity 是以太坊的最終形態，包含 **PoS（權益證明）、分片技術（Sharding）** 和 **更強大的虛擬機（eWASM）**。  

- **Beacon Chain（信標鏈）**：2020 年 12 月 1 日上線，作為以太坊 PoS 的骨幹。  
- **分片技術（Sharding）**：以太坊將區塊鏈拆分為多個 **分片鏈**，提升交易處理能力。  
- **eWASM**（取代 EVM）：允許以 WebAssembly 編寫智能合約，提高執行效能和靈活性。  



### **The Merge - 以太坊正式轉向 PoS**  

**發生時間：** 2022 年 9 月 15 日  

The Merge 是以太坊歷史上 **最重要的升級之一**，標誌著以太坊從 **工作量證明（Proof-of-Work, PoW）** 完全轉向 **權益證明（Proof-of-Stake, PoS）**。這次升級不僅大幅降低能源消耗，還為未來的擴展性和升級鋪平了道路。  

### **The Merge 的主要變化**  

- **棄用 PoW，改用 PoS**：  
  - **PoW Mining完全停止**，取而代之的是 **驗證者（Validators）** 負責區塊驗證。  
  - 這使得以太坊的 **能源消耗降低超過 99%**，成為更環保的區塊鏈。  

- **兩層架構：執行層（Execution Layer）+ 共識層（Consensus Layer）**：  
  - 以太坊將 **交易執行層（原本的以太坊鏈）** 與 **共識層（Beacon Chain）** 進行合併。  
  - **Beacon Chain** 早在 **2020 年 12 月 1 日** 就開始運行，並經過長時間測試，確保 PoS 共識機制的穩定性。  

- **提升安全性與去中心化**：  
  - PoS 驗證者需要 **抵押（Stake）ETH** 才能參與共識，若有惡意行為將面臨**資金懲罰（Slashing）**，這讓網絡更加安全。  
  - PoS 降低了礦池壟斷風險，讓更多個人驗證者能夠參與，提升去中心化程度。  


參考:

[以太坊歷史超迅速補充包（一）：寧靜之前](https://medium.com/swf-lab/%E4%BB%A5%E5%A4%AA%E5%9D%8A%E6%AD%B7%E5%8F%B2%E8%B6%85%E8%BF%85%E9%80%9F%E8%A3%9C%E5%85%85%E5%8C%85-%E4%B8%80-%E5%AF%A7%E9%9D%9C%E4%B9%8B%E5%89%8D-24f24753f9b6)

[簡述以太坊歷史的關鍵節點，坎昆升級前應該怎樣布局](https://m.cnyes.com/news/print/5231561?exp=a)

[以太坊的下個十年：坎昆升級](https://www.markreadfintech.com/p/bb3)

[「以太坊」坎昆升級 Proto-Danksharding](https://matters.town/a/71wfdgqk7vpa)
<!-- Content_END -->
