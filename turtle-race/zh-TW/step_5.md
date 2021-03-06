## 賽跑的烏龜

現在我們到了有趣的時刻了~ 讓我們新增一些賽跑的烏龜。 如果所有的烏龜每次都移動同樣的步數，那就沒有意思了，我們要讓它們每次移動一個隨機的步數。 在100個回合之後，跑得最遠的那個烏龜將獲得勝利。

+ 當你使用像 `forward(20)` 這樣的命令時 , 你控制的只是一隻烏龜。但你可以新增更多的烏龜。將以下程式碼新增到程式的末尾（但請確保它沒有縮排）：
    
    ![截圖](images/race-red.png)
    
    第一行程式碼建立了一個名為‘ada’的烏龜。接下來的兩行分別設定了它的顏色和形狀。現在它看起來確實是像一隻烏龜了！

+ 讓我們把烏龜放到起跑線：
    
    ![截圖](images/race-start.png)

+ 現在你需要通過一次移動一個隨機步數來讓烏龜賽跑。 您將需要調取python `random` 庫中的 `randint` 函式。 將這個`import`語句新增到你的程式的頂部:
    
    ![截圖](images/race-randint.png)

+ `randint` 函式將返回設定範圍之間的一個隨機整數（不帶小數點的整數）。烏龜將在每個回合中向前移動1、2、3、4或5步。
    
    ![截圖](images/race-random.png)

+ 只有一隻烏龜跑就沒辦法比賽了！讓我們再新增一隻烏龜：
    
    ![截圖](images/race-blue.png)
    
    請注意移動藍色烏龜的程式碼需要和移動紅色烏龜程式碼在**同一個**`for`迴圈中，以確保每個回合所有的烏龜都會向前移動。