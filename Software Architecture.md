# Introduction
1. 什麼是軟件架構
	+ SEI：是整個程序或計算系統的結構（Structure），包含了程序的元素（Software Elements）和那些外部能看見的元素屬性（Properties）和元素之間的關係（Relationship）。
	+ IEEE：是那些給一個系統做出的建設性的設計（Design）和演化（Evolution）。
	+ 定義：
		+ 關於軟件設計（Software design）
		+ 關於視圖（Views）：高層視圖、設計決策
		+ 系統的組織結構（Structure/Organization）：元素和關係（Elements/Relationship）
		+ 屬性（Properties）
2. 軟件架構做什麼
	+ 架構定義了結構（Architecture defines structure）：
		+ 定義組件接口
		+ 定義組件的交流和依賴
		+ 定義組件的職責
	+ 架構說明組件的交流
		+ 數據傳遞機制
		+ 控制流
	+ 架構傳遞非功能性需求（NFRs）
		+ 包括了技術約束，商務約束和質量約束
	+ 架構是個抽象
3. 軟件架構如何而來
	+ 不僅僅侷限于需求
	+ 可能是商業和技術決定的集合
	+ 經常受以下因素影響：
		+ 系統利益相關者
		+ 開發組織
		+ 架構師
		+ 系統環境
4. 架構的視圖
	+ 邏輯視圖：定義必要的元素和體系中的關係
	+ 過程視圖：描述元素之間的交流依賴
	+ 物理視圖：主要的進程和元素是怎麼映射到硬件
	+ 開發視圖：捕捉內部的元素聯繫
5. 架構活動和過程
	+ 架構活動包括四大步驟（P.26）
		+ 發現架構重要需求（ASRs，Architecturally Significant Requirements）
		+ 架構設計（Architecture Design)
		+ 視圖和文檔（Documenting）
		+ 架構評估（Architecture Evaluation）
	+ Lifecycle
		+ 架構分析
		+ 架構評估
		+ 架構實現
		+ 架構合成
		+ 架構維護

# Quality Attributes
1. 選件要求
	+ 功能需求（Functional Requirements）
		+ 描述了如何給利益相關者產生價值
		+ 描述了系統的職責
	+ 質量需求（NFRs）
		+ 質量需求用於檢驗功能需求和整個產品的質量
	+ 約束（Constrains）
2. 質量屬性
	+ 軟件開發各個階段傳遞出的需求
	+ 場景（Modeling Quality Attribute Scenarios）（P.15)
		+ Stimulus：刺激，是一個系統需要考慮到的發生的情況
		+ Source of stimulus：人或其他實體產生這個刺激
		+ Response：收到刺激後的活動反應
		+ Response measure：反應衡量標準
		+ Environment：當接收到刺激后系統的狀況，是正在運行還是過載
		+ Artifact：系統中的一個部件，當需求應用於的一個部份，可能是整個系統
    + 質量設計決定七大分類（P.17）
    + 質量屬性（P.19）
    	+ Availablity：可用性
    		+ 和整個程序的可靠性（Reliability）有關
        + Interoperability：互用性
        	+ 描述多個系統通過接口交換特定信息的屬性，包括交換和正確推斷消息
        + Modifiability：可更改性
        	+ 用於評估一個更改所消耗的時間和金錢
        + Performance：性能
        	+ 關於系統需要處理需求的時間
        	+ 氛圍處理時間和阻塞時間
        + Security：安全性
        	+ 衡量系統保護數據和信息的能力
        + Testability：可測試性
        	+ 能夠發現各個部件的輸入和觀察到它們的輸出
        + Usability：可用性
        	+ 用戶去完成一個特定任務的容易性評估
        + X-ability
	+ Scenario（情景刻畫）表格
		+ Source
		+ Stimulus
		+ Artifact
		+ Environment
		+ Response
		+ Response Measure
3. 架構重要需求（ASRs，Architecturally Significant Requirements）
	+ 如何獲得 ASRs：
		+ 從需求文檔（Requirement Documents）
		+ 從訪談利益相關人員（Stakeholders）
		+ 理解商業目標（Business Goals）
		+ 從效能樹（Utility Tree）

# Architecture Patterns
1. 架構模式（Architecture Patterns）
	+ 是在不斷嘗試中找到的一種設計決策的集合
	+ 可複用
	+ 描述一種架構的類別
	+ 包含了：
		+ 上下文（Context）
		+ 問題（Problem）
		+ 解決方式（Solution）：元素、關係和約束
2. 模塊模式（Module Patterns）
	+ 分層模式（Layered Pattern）
3. 連接件模式（Component-Connector Patterns）
	+ 代理模式（Broker Pattern）
	+ MVC 模式（Model-View-Controller Pattern）
	+ 管道過濾模式（Pipe-and-Filter Pattern）
	+ 客戶端服務器模式（Client-Server Pattern）
	+ 點對點模式（Peer-to-Peer Pattern）
	+ 面向服務的模式（Service-Oriented Pattern）
	+ 發佈訂閱模式（Publish-Subscribe Pattern）
	+ 共享數據模式（Shared-Data Pattern）
4. 分配模式（Allocation Patterns）
	+ 多鏈模式(Multi-Tier Pattern)
		+ Client、Web、EJB、Backend
    + 映射-歸納模式（Map-Reduce Pattern）
    	+ Map to parition and merge
5. 模式和策略（Patterns & Tactics）
	+ 區別於 Pattern，Tacitc 更簡單，密度更小。
	+ Pattern 會互相包含和交叉。
	+ Pattern 通常包含多個設計方案。
	+ Pattern 和 Tactic 共同構建了整個架構基礎的工具。
	+ Pattern 看的角度不同。
	+ Pattern 會包含一定的 Tactic。
6. 描述
	+ Overview
	+ Elements
	+ Relations
	+ Constraints
	+ Weaknesses

# Designing Architecture
1. 設計方法（Design Strategy）
	+ 分解（Decomposition）
	+ 迭代（Iteration）
	+ 生成和測試（Generate and Test）
2. ADD（Attribute-Driven Design）
	+ 確認需求（Confirm there is sufficient requirements infomation）
	+ 選擇一個系統元素分解（Choose an element of the system to decompose）
	+ 為該元素確認架構必要需求（Identify the ASRs for the chosen element）
		+ H, M, L 的二維數組：（對利益相關者的重要性，對架構實現的影響）即（Importance，Difficulty）
	+ 選擇一個符合架構必要需求的設計理念（Choose a design concept that satisfies the ASRs）
		+ 確認設計關注點（Identify design concerns）
		+ 為次要關注點列出不同的模式和策略（List alternative patterns/tactics for subordinate concerns）
		+ 選擇合適的模式和策略（Select patterns/tactics from the list）
		+ 決定架構必要需求和模式策略之間的關係（Determine relationship between patterns/tactics and ASRs）
		+ 捕獲架構視圖（Capture preliminary architecture views）
		+ 評估并解決不一致問題（Evaluate and resolve inconsistencies）
    + 列出架構元素和分配職責（Instantiate architectural elements and allocate responsibilities）
    + 為元素定義接口（Define interfaces for instantiated elements）
    + 確認需求、為元素構造約束（Verify and refine requirements and make them constraints for instantiated elements）
    + 重複以上步驟（Repeat until satisfied）
	+ ** 總的來說，選擇一個部份去設計，考慮所有的必要架構需求，建立并測試這個設計，評估滿足質量屬性的輸入輸出 **

# Documenting Architecture
1. 文檔的好處和不足
	+ 好處
        + 更好地交流
        + 幫助理解決策
        + 更新設計者的思維
        + 鍛鍊設計架構的能力
    + 不足
    	+ 沒有標準化
    	+ 大型系統時間長
    	+ 註釋缺失
2. Views and Beyond（視圖和之外的東西）
	+ Views
		+ Style、Pattern、View 的區別：
			+ Style：關注組件和組件之間的交互和職責限制，不包含具體的上下文和問題（Problem & Context）
			+ Pattern：關注問題和上下文
			+ View：
        + Views：
    		+ Module Views（模塊視圖）：強調靜態
    		+ C&C Views（連接件視圖）：強調動態
    		+ Allocation Views（部署視圖）：周圍環境
        + Documenting Views（如何寫文檔）：
            + 建立一個利益相關者的視圖表格：不同的利益相關者對不同視圖有不同的關注點
            + 合併視圖
            + 優先級和分佈：80/20 原則
    + Beyond
    	+ 文檔模板
    		+ 版本控制
    		+ Roadmap
        + 文檔目錄
        + 文檔指引

# Evaluating Architecture
1. 為什麼要評估
	+ 大型項目經常遲交
	+ 重新設計
	+ 提早發現問題
	+ 提供一個項目技術管理
	+ 儘早評估
2. 體繫結構權衡分析方法（ATAM，Architecture Tradeoff Analysis Method）
	+ 評估方式：設計者、夥伴、外界人士
	+ 階段：
		+ Phase 0：參與者和準備階段（Partnership & Preparation）
			+ 前提：有體系結構文檔
			+ 結果：評估計劃──誰、什麼時間、提供什麼樣子的評估報告
        + Phase 1：評估（Evaluation）
        	+ 參與者：評估小組和決策者
        	+ 結果：關於架構的簡要的描述演講、商業目標、質量屬性、功能樹、風險和非風險點、敏感的觀點、利益相關的觀點
        	+ Step 1：表述這個方法，Present the ATAM
        	+ Step 2：表述商業動機，Present the business drivers──包括最重要的功能性需求、約束、商業目的、主要利益相關、架構驅動
        	+ Step 3：表述架構，Present architecture──表述架構的技術約束和系統
        	+ Step 4：確定使用的架構方法，Identify Architectural Approaches
        	+ Step 5：生成質量屬性效用樹，Generate quality attribute utility tree──決定性的一步，重新劃分優先級
        	+ Step 6：分析架構方法，Analyze architectural approaches
        + Phase 2：評估第二環節
        	+ 參與者：涉及到利益獲得者
        	+ 結果：一個優先級場景的列表、危險和商業動機
        	+ Step 1：展示，Present the ATAM & Previous Results
        	+ Step 7：頭腦風暴、場景劃分優先級，Brainstorm & Prioritize Scenarios
        	+ Step 8：分析架構方法，Analyze architectural approaches──根據優先級重新分析
        	+ Step 9：展示，Present Results
        + Phase 3：後續工作（Follow up）
        	+ 參與者：評估小組和主要利益相關者
        	+ 結果：最終的評估報告

# Software Product Line
1. 什麼是產品線
	+ 很多相關近似的商品
	+ Products：Custom Assets 和 Core Assets
	+ 共享同一個通用的、符合特定需求的軟件特定系統
	+ Core Assets：
		+ Reuse（復用）：在 SPL 中大量使用
		+ 提供特定的信息知識和經驗
		+ 提供大量不同的（Variation）特點適應不同特性
		+ 實現的需求在 SPL 的圈子中
    + Custom Assets：
    	+ 對於特定的產品
    	+ 滿足用戶特定的需求
    	+ 實現 SPL 圈子中的需求
    	+ 集成 Core Assets
2. Reuse & Variation
	+ 復用：代碼復用是最容易的
	+ 變動：讓代碼更加靈活，現在設計，未來復用
3. PLA（Product Line Architecture）
	+ 定義公用的功能和可改變的功能
4. Variation Mechanisms
	+ Forms of variation 6
		+ Include or omit elements
		+ Variable number of each element
		+ Interface Satisfaction
		+ Parameterisation
		+ “Hook” interfaces
		+ Reflection
	+ Software entity varied 3
		+ Architecture level – High-level abstract structures
		+ Design level – Lower-level abstract structures
		+ File level – low-level concrete source structures
    + Binding time 5
    	+ Coding-time – when you create a coding workspace
    	+ Compile-time – when you build object code
    	+ Link-time – when you create your application
    	+ Initialization-time – when your application starts
    	+ Run-time – while your application is running
5. Product line approach
	+ 3 Essential Activities
		+ Software Engineering
		+ Technical Management
		+ Organizational Management
	+ 29 Practice Areas
	+ 12 (22) Practice Patterns
	+ V Cycle
6. Extractive
	+ 分析產品核心的部份
	+ 提取核心和異同
	+ 重新組裝

# Model Driven Architecture
1. Model Driven Development（MDD）模塊驅動開發
	+ 分離開功能定義和功能實現
2. 什麼是 MDA
	+ MDA 遵循 OMG
	+ 建模語言之間的標準──MOF
	+ 層次：
		+ CIM（Computation independent model），計算獨立模型，關注系統的環境和需求
		+ PIM（Platform independent model），平台獨立模型，關注整個架構的實現和計算，和平台無關
		+ PSM（platform specific model），平台特定模型，關注在特定平台上的計算，和平台有關
    + 目標：
    	+ 可移植性（Portability）
    	+ 交互性（Interoperability）
    	+ 可重用性（Reusablility）
    + 不足：
    	+ 多義性
    	+ 複雜性
    	+ 從頭構建和剪裁通用模塊語言的平衡
3. Architecture Description Language（ADL）

# Service Oriented Architecture
1. Why SOA
	+ 優勢：從已有的服務上建立商業過程，組件的復用和解耦
	+ 技術：XML、Web Services、Service Bus
	+ Service Find-Bind-Execute Digram
		+ 三者關係（註冊，尋找，綁定）
		+ Service Consumer
		+ Service Provider
		+ Registry
2. SOA 不是 Web 服務
	+ SOA 是一種架構方式
	+ Web Service 是實現手段之一
3. WSDL & SOAP
	+ Envelope
	+ Header
	+ Body
4. Enterprise Service Bus（ESB）
	+ ESB 提供一個環境和平台但是並不能實現 SOA
5. 實現
	+ 自下而上：確定需求調用已有服務和添加新的內容構建服務。
    + 自上而下：分析已有服務，在基礎上構建新的服務。
