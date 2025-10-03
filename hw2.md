## (1）PERT/CPM圖
```mermaid
graph LR
    A[1. 研拟計畫 1d] === B(2. 任務分配 4d)
    A --> C[3. 取得硬體 17d]
    B === D(4. 程式開發 70d)
    C --> E[5. 安裝硬體 10d]
    D === F(6. 程式測試 30d)
    E --> G[7. 撰寫使用手冊 25d]
    E --> H[8. 轉換檔案 20d]
    F === I(9. 系統測試 25d)
    G --> J[10. 使用者訓練 20d]
    H --> J
    I === K(11. 使用者測試 25d)
    J --> K

    %% 关键路径连线样式：使用红色加粗 (linkStyle)
    linkStyle 0 stroke:red,stroke-width:3px
    linkStyle 2 stroke:red,stroke-width:3px
    linkStyle 4 stroke:red,stroke-width:3px
    linkStyle 6 stroke:red,stroke-width:3px
    linkStyle 8 stroke:red,stroke-width:3px

    %% 关键路径节点样式：使用浅红填充 (style)
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
    title 專案甘特圖
    dateFormat  YYYY-MM-DD
    section 計畫
    研擬計畫          :a1, 2025-09-01, 1d
    任務分配          :a2, after a1, 4d
    section 硬體
    取得硬體          :a3, after a1, 17d
    安裝硬體          :a5, after a3, 10d
    撰寫使用手冊      :a7, after a5, 25d
    轉換檔案          :a8, after a5, 20d
    section 軟體
    程式開發          :a4, after a2, 70d
    程式測試          :a6, after a4, 30d
    系統測試          :a9, after a6, 25d
    section 使用者
    使用者訓練        :a10, after a7 a8, 20d
    使用者測試        :a11, after a9 a10, 25d
