# Maze-Game
## Game Engine: Unity 2018.4.6f1
## Game Source Code: https://drive.google.com/file/d/1g8EBNAmDV4q5DAWhInQeyu2DYDmCL496/view?usp=sharing
## Game Download: https://drive.google.com/file/d/1zAWJlnMEmwhvcIZSArBsnjLEN4T-G-PW/view?usp=sharing
## Demo Video: https://www.youtube.com/watch?v=0Be38HmieRI

### 基礎操作方式:
1. 遊戲主角是用 WASD 鍵移動，Space 鍵跳。
2. 通關條件要先撿到三棵小樹，然後在指定地方植樹，等樹長高後逃出迷宮外，而植樹是 R 鍵。

### 額外說明:
3. 可以動態調整光源亮度:
遊戲中會有 spotlight 照著主角，沒事的時候是淺綠色。但是當主角靠近陷阱的時候，
spotlight 會在綠色和紅色之間交替。程式中是用了 Mathf.PingPong()和 Color.Lerp()實作。
4. 小地圖:
另外創建一個攝影機，在主角的頭頂上垂直攝影，把畫面儲存為一個 Texture。在 UI
界面建立一個 Raw image，再把 Texture 貼上 Raw image 上，就成為了一張小地圖。
5. 迷宮陷阱:
遊戲中每棵小樹旁都有「水晶小槍」的迷宮陷阱。它的特點是會一直注視著主角。
當主角進作了它的攻擊範圍，就會射出「小水晶」(子彈)攻擊主角。
6. 加入 GUI 元件:
除了小地圖的顯示，還有主角的血量、已收集小樹的數字顯示。
遊戲程式設計 HW1 迷宮
樊浩賢 106062363
8. 使用 Prefab 動態生成物件:
「水晶小槍」射出的子彈就是用 Prefab 動態生成。
10. 使用粒子特效:
a. 子彈射出來會有附加藍色粒子效果，粒子會慢慢隨著時間變小、消失。
b. 碰到物件後要爆炸，「小水晶」會爆成碎片後隨著時間慢慢消失。
