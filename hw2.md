## (1）PERT/CPM圖
```mermaid
graph LR
    A[1. 研擬計畫 1d] --- B(2. 任務分配 4d)
    A --> C[3. 取得硬體 17d]
    B --- D(4. 程式開發 70d)
    C --> E[5. 安裝硬體 10d]
    D --- F(6. 程式測試 30d)
    E --> G[7. 撰寫使用手冊 25d]
    E --> H[8. 轉換檔案 20d]
    F --- I(9. 系統測試 25d)
    G --> J[10. 使用者訓練 20d]
    H --> J
    I --- K(11. 使用者測試 25d)
    J --> K

    %% 關鍵路徑的連線樣式
    linkStyle 0 stroke:red,stroke-width:3px
    linkStyle 2 stroke:red,stroke-width:3px
    linkStyle 4 stroke:red,stroke-width:3px
    linkStyle 6 stroke:red,stroke-width:3px
    linkStyle 8 stroke:red,stroke-width:3px
    linkStyle 10 stroke:red,stroke-width:3px

    %% 關鍵路徑的節點樣式
    style A fill:#ffcccc,stroke:#ff0000,stroke-width:2px
    style B fill:#ffcccc,stroke:#ff0000,stroke-width:2px
    style D fill:#ffcccc,stroke:#ff0000,stroke-width:2px
    style F fill:#ffcccc,stroke:#ff0000,stroke-width:2px
    style I fill:#ffcccc,stroke:#ff0000,stroke-width:2px
    style K fill:#ffcccc,stroke:#ff0000,stroke-width:2px
```
---
## (2) 甘特圖
```mermaid
gantt
    title 專案甘特圖 (以日數計算，總工期 155 天)
    dateFormat  x
    axisFormat  %s

    section 關鍵路徑
    1. 研擬計畫      :crit, id1, 0, 1d
    2. 任務分配      :crit, id2, 1, 4d
    4. 程式開發      :crit, id4, 5, 70d
    6. 程式測試      :crit, id6, 75, 30d
    9. 系統測試      :crit, id9, 105, 25d
    11. 使用者測試  :crit, id11, 130, 25d

    section 其他任務
    3. 取得硬體      :id3, 1, 17d
    5. 安裝硬體      :id5, 18, 10d
    7. 撰寫使用手冊 :id7, 28, 25d
    8. 轉換檔案      :id8, 28, 20d
    10. 使用者訓練  :id10, 53, 20d
