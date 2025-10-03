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

    %% 關鍵路徑的連線 (使用 '---' 標記關鍵路徑，讓箭頭變粗)
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
