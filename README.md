# E-commerce_MiDo-Bakery
組長 陳廷瑋 C111118143

組員 簡世昌 C111118142
***

```mermaid
gantt
    title schedule

    section 任務1
    研擬計畫:        a1, 2024-10-03, 1d

    section 任務2
    任務分配:        a2, after a1, 1d

    section 任務3
    產品設定:        a3, after a2, 5d

    section 任務4
    首頁設定:        a4, after a3, 10d

    section 任務5
    客服設定:        a5, after a3, 15d

    section 任務6
    銷售頁設定:      a6, after a5, 10d

    section 任務7
    金流設定:        a7, after a6, 15d

    section 任務8
    物流設定:        a8, after a7, 15d

    section 任務9
    粉專設定:        a9, after a8, 10d

    section 任務10
    系統測試:       a10, after a9, 10d

```

&nbsp;
&nbsp;

```mermaid
graph TD
    1[研擬計畫] --> 2[任務分配]
    2    --> 3[產品設定]
    3    --> 4[首頁設定]
    3    --> 5[客服設定]
    5    --> 6[銷售頁設定]
    6    --> 7[金流設定]
    7    --> 8[物流設定]
    8    --> 9[粉專設定]
    9    --> 10[系統測試]

    style 5 fill:#ffff99,stroke:#333,stroke-width:2px

```

&nbsp;
&nbsp;

```mermaid
   graph TD
    no1["研擬計畫 | 編號:1 | 開始:第1天 | 結束:第1天 | 需時:1天"] --> no2["任務分配 | 編號:2 | 開始:第2天 | 結束:第2天 | 需時:1天"]
    no2 --> no3["產品設定 | 編號:3 | 開始:第3天 | 結束:第7天 | 需時:5天"]

    no3 --> no4["首頁設定 | 編號:4 | 開始:第8天 | 結束:第17天 | 需時:10天"]
    no3 --> no5["客服設定 | 編號:5 | 開始:第8天 | 結束:第22天 | 需時:15天"]

    no5 --> no6["銷售頁設定 | 編號:6 | 開始:第23天 | 結束:第32天 | 需時:10天"]
    no6 --> no7["金流設定 | 編號:7 | 開始:第33天 | 結束:第47天 | 需時:15天"]
    no7 --> no8["物流設定 | 編號:8 | 開始:第48天 | 結束:第62天 | 需時:15天"]
    no8 --> no9["粉專設定 | 編號:9 | 開始:第63天 | 結束:第72天 | 需時:10天"]
    no9 --> no10["系統測試 | 編號:10 | 開始:第73天 | 結束:第82天 | 需時:10天"]

    style no5 fill:#ffff99,stroke:#333,stroke-width:2px
```

***

# 功能性需求
1.用戶註冊和登入：系統能夠允許用戶註冊帳號，並通過帳號和密碼進行登入。  
2.多語言支持：系統能夠根據用戶偏好顯示不同語言的內容。  
3.搜尋功能：系統應允許用戶根據特定條件（如名稱、類別等）進行資料搜索。   

# 非功能性需求
1.安全性：實施多重身份驗證機制，並使用加密技術保護數據。  
2.兼容性：支持主流的作業系統（如Windows、macOS、Linux）和瀏覽器（如Chrome、Firefox、Safari）。  
3.可靠性：保證在故障情況下數據不丟失，並能自動恢復正常運行。  

# 功能分解圖
![image](功能分解圖.png)  

# 使用案例圖
![image](使用案例圖.png)

# 使用案例1：用戶登入系統
說明：後台人員輸入帳號密碼，才可進入後台操作  
## 流程：
1.後台人員輸入帳號和密碼。  
2.系統驗證有無錯誤並分別身分。  
3.正確後轉入系統畫面，錯誤則轉入登入畫面並顯示錯誤訊息。

# 使用案例2：後台人員操控資料
說明：商品人員操控販售類資料，服務人員操控服務類資料  
## 流程：
1.商品人員可操控商品管理頁面，訂單管理頁面，購物車管理頁面。  
* 商品管理頁面：商品瀏覽、商品搜尋、商品分類。  
* 訂單管理頁面：加入購物車、修改數量、移除商品。  
* 購物車管理頁面：建立訂單、支付流程、訂單取消。  
  
2.服務人員可操控客服服務頁面，回饋系統頁面。
* 客服功能：線上客服、常見問題。  
* 回饋系統：商品評分、顧客評分、問卷調查。  
  
# 使用案例3：線上購物平台操作
說明：顧客可至平台購買商品，遇到問題也可詢問客服，也可以根據使用心得回饋平台。  
## 流程：
1.顧客進入登入系統，輸入帳號和密碼。  
2.顧客進入購物平台，可依照分類或者自行搜索商品。  
3.購物完畢後，可進入購物車修改商品數量及移除商品。  
4.如果對於商品或服務有問題，可以透過客服來詢問。  
5.收到貨物後，可依照服務滿意度和商品品質，進行回饋並改正。  
***

# 系統環境圖 (System DFD)
![image](系統環境圖.png)  

# 資料流向圖0 (DFD 0)
![image](資料流向圖0.png)
***

# UML類別圖 (Class Diagram)
![image](UML類別圖.png)

# 使用案例一：使用者登入 (User Login)
## 循序圖
```mermaid
sequenceDiagram
    participant 使用者
    participant 商店系統

    使用者 ->> 商店系統: 登入請求 (Login Request)
    activate 商店系統
    商店系統 -->> 商店系統: 驗證帳號和密碼 (Verify credentials)
    商店系統 -->> 使用者: 登入成功 (Login Success)
    deactivate 商店系統
```
## 活動圖
```mermaid
graph TD
    A(開始 Start) --> B[輸入帳號和密碼 Enter credentials]
    B --> C{驗證帳號和密碼 Verify credentials}
    C -->|成功 Success| D[登入成功 Login Success]
    C -->|失敗 Failure| E[顯示錯誤信息 Show Error Message]
    D --> F(結束 End)
    E --> F
```
# 使用案例二：購物車結帳 (Checkout Shopping Cart)
## 循序圖
```mermaid
sequenceDiagram
    participant 使用者
    participant 商店系統
    participant 購物車
    participant 結帳
    participant 訂單資訊

    使用者 ->> 商店系統: 選擇商品並加入購物車 (Select items and add to cart)
    使用者 ->> 購物車: 查看購物車 (View cart)
    使用者 ->> 結帳: 進入結帳頁面 (Enter checkout page)
    結帳 ->> 使用者: 填寫結帳信息 (Fill in checkout information)
    使用者 ->> 訂單資訊: 提交訂單 (Submit order)
    訂單資訊 -->> 訂單資訊: 生成訂單 (Generate order)
    訂單資訊 ->> 使用者: 訂單生成成功 (Order confirmation)
```
## 活動圖
```mermaid
graph TD
    A(開始 Start) --> B[瀏覽商品 Browse products]
    B --> C[加入購物車 Add to cart]
    C --> D[查看購物車 View cart]
    D --> E[進入結帳 Enter checkout]
    E --> F[填寫結帳信息 Fill in checkout info]
    F --> G[提交訂單 Submit order]
    G --> H[生成訂單 Generate order]
    H --> I(結束 End)
```
# 使用案例三：商品評價 (Submit Review for Product)
## 循序圖
```mermaid
sequenceDiagram
    participant 使用者
    participant 商店系統
    participant 評價

    使用者 ->> 商店系統: 選擇商品 (Select product)
    使用者 ->> 評價: 提交評價 (Submit review)
    評價 -->> 評價: 儲存評價 (Save review)
    評價 ->> 使用者: 評價成功 (Review successful)
```
## 活動圖
```mermaid
graph TD
    A(開始 Start) --> B[選擇商品 Select product]
    B --> C[填寫評價信息 Enter review details]
    C --> D[提交評價 Submit review]
    D --> E[儲存評價 Save review]
    E --> F(結束 End)
```
***
