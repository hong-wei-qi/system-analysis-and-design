### PERT/CPM 圖
![PERT/CPM 圖](./w2_PERT_CPM.png)

``` mermaid
graph TD
    subgraph 專案時程圖 (Project Schedule Diagram)
        A[1. 研擬計畫 (1天)] --> B(2. 任務分配 (4天))
        A --> C(3. 取得硬體 (17天))

        B --> D(4. 程式開發 (70天))

        C --> E(5. 安裝硬體 (10天))

        D --> F(6. 程式測試 (30天))

        E --> G(7. 撰寫使用手冊 (25天))
        E --> H(8. 轉換檔案 (20天))

        F --> I(9. 系統測試 (25天))

        G & H --> J(10. 使用者訓練 (20天))

        I & J --> K(11. 使用者測試 (25天))
    end
```

```mermaid
gantt
    title 甘特圖

    section 規劃與發展
    研擬計畫        : Task1, 2025-10-01, 1d
    任務分配        : Task2, after Task1, 4d
    取得硬體        : Task3, after Task1, 17d
    程式開發        : Task4, after Task2, 70d
    section 實施與測試
    安裝硬體        : Task5, after Task3, 10d
    程式測試        : Task6, after Task4, 30d
    撰寫使用手冊    : Task7, after Task5, 25d
    轉換檔案        : Task8, after Task5, 20d
    section 最後階段
    系統測試        : Task9, after Task6, 25d
    使用者訓練      : Task10, after Task7, 20d
    使用者測試      : Task11, after Task9, 25d
```

### 關鍵路徑
**1 > 2 > 4 > 6 > 9 > 11**

*在專案管理中，專案網路圖上耗時最長的活動序列，決定了專案的總工期。*
