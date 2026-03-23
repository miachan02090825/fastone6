**1. 觸發條件 (Trigger)**： 當使用者輸入包含「Figma 網址」或上傳「設計截圖」時觸發。

**2. 執行步驟 (Execution Steps)**：

1. **結構拆解**：分析截圖中的 **視覺層級 (Visual Hierarchy)**，識別出導覽列、英雄區 (Hero)、內容區與頁尾。
2. **顏色提取**：自動抓取畫面的主色與輔助色，建立 Tailwind Config 變數。
3. **佈局轉換**：將 Figma 的 Auto-layout 邏輯對應為 `flex` 或 `grid` 佈局。
4. **程式碼生成**：先產出完整的 HTML 結構，再注入 Tailwind CSS 類名。
5. **預覽優化**：檢查在行動裝置 (Mobile) 上的顯示是否會跑版，若會，則自動加入 `md:` 前綴