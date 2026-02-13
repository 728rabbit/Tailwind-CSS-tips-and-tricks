
## 🚀 **Flexbox & Grid 快狠準應用**

----------

# 🎯 **一、Flexbox - 一維排版**

## ✅ **最常用組合（背起來！）**

    html
    
    <!-- 水平置中 + 垂直置中 + 等距 -->
    <div class="flex items-center justify-between">
     <div>左</div>
     <div>中</div>
     <div>右</div>
    </div>

類別

意思

常用度

`flex`

開啟 Flex

⭐⭐⭐⭐⭐

`items-center`

垂直置中

⭐⭐⭐⭐⭐

`justify-between`

左右貼邊，中間等距

⭐⭐⭐⭐⭐

`justify-center`

水平置中

⭐⭐⭐⭐⭐

`flex-col`

垂直排列

⭐⭐⭐⭐

`gap-{size}`

間距

⭐⭐⭐⭐⭐

----------

## 📦 **Flexbox 實戰大全**

### **1. 導覽列 - 標配**

    html
    
    <nav class="flex items-center justify-between px-6 py-4">
     <div class="text-xl font-bold">Logo</div>
     <div class="flex gap-8">
     <a>首頁</a>
     <a>產品</a>
     <a>關於</a>
     </div>
     <button class="bg-blue-500 text-white px-4 py-2 rounded">
     登入
     </button>
    </nav>

### **2. 卡片水平排列**

html

    <div class="flex flex-wrap gap-6">
     <div class="w-64">卡片1</div>
     <div class="w-64">卡片2</div>
     <div class="w-64">卡片3</div>
    </div>

### **3. 表單標籤 + 輸入框**

    html
    
    <div class="flex items-center gap-4">
     <label class="w-24">姓名</label>
     <input class="flex-1 border p-2 rounded">
     <!-- flex-1 佔滿剩餘寬度 -->
    </div>

### **4. 置中神器**

    html
    
    <div class="flex items-center justify-center h-screen">
     <div class="bg-white p-8 rounded-lg shadow-lg">
     垂直水平置中的內容
     </div>
    </div>

----------

# 🎯 **二、Grid - 二維排版**

## ✅ **最常用組合（背起來！）**

    html
    
    <!-- 三欄等寬，有間距 -->
    <div class="grid grid-cols-3 gap-4">
     <div>1</div>
     <div>2</div>
     <div>3</div>
    </div>

類別

意思

常用度

`grid`

開啟 Grid

⭐⭐⭐⭐⭐

`grid-cols-{n}`

幾欄

⭐⭐⭐⭐⭐

`gap-{size}`

間距

⭐⭐⭐⭐⭐

`col-span-{n}`

跨幾欄

⭐⭐⭐⭐

`grid-rows-{n}`

幾列

⭐⭐

----------

## 📦 **Grid 實戰大全**

### **1. 商品列表 - 響應式**

    html
    
    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
     <div class="bg-white p-4 rounded">商品1</div>
     <div class="bg-white p-4 rounded">商品2</div>
     <div class="bg-white p-4 rounded">商品3</div>
     <div class="bg-white p-4 rounded">商品4</div>
    </div>
    <!-- 手機:1欄 平板:2欄 桌機:4欄 -->

### **2. 儀表板 - 跨欄**

    html
    
    <div class="grid grid-cols-4 gap-4">
     <!-- 左側邊欄 - 佔1欄 -->
     <div class="col-span-1 bg-gray-100">側邊欄</div>
      
     <!-- 主要內容 - 佔3欄 -->
     <div class="col-span-3">
     <div class="grid grid-cols-3 gap-4">
     <div class="bg-white p-4">卡片1</div>
     <div class="bg-white p-4">卡片2</div>
     <div class="bg-white p-4">卡片3</div>
     </div>
     </div>
    </div>

### **3. 圖片牆**

    html
    
    <div class="grid grid-cols-3 md:grid-cols-4 lg:grid-cols-6 gap-2">
     <img src="1.jpg" class="w-full h-40 object-cover">
     <img src="2.jpg" class="w-full h-40 object-cover">
     <img src="3.jpg" class="w-full h-40 object-cover">
     <!-- 更多圖片... -->
    </div>

### **4. 文章 + 側邊欄**

    html
    
    <div class="grid grid-cols-1 lg:grid-cols-3 gap-8">
     <!-- 主要內容 - 桌機佔2欄 -->
     <article class="lg:col-span-2">
     <h1 class="text-2xl font-bold">文章標題</h1>
     <p>內容...</p>
     </article>
      
     <!-- 側邊欄 - 桌機佔1欄 -->
     <aside class="space-y-4">
     <div class="bg-gray-50 p-4">推薦文章</div>
     <div class="bg-gray-50 p-4">廣告</div>
     </aside>
    </div>

----------

# ⚡ **三、Flex vs Grid 怎麼選？**

情境

用哪個

原因

導覽列、選單

**Flex**

一維，從左到右

表單、輸入框

**Flex**

標籤＋輸入框對齊

垂直置中

**Flex**

items-center 最快

商品牆

**Grid**

二維，行列整齊

儀表板

**Grid**

複雜跨欄排版

卡片列表

**都行**

Grid 更整齊

----------

# 🎮 **四、記憶口訣**

text

Flex 一維一條龍
水平垂直都能中
選單表單導覽列
items-center 最威風
Grid 二維棋盤格
幾欄幾列自己刻
響應跨欄超好切
col-span 最特別

----------

# 🔥 **五、終極懶人包**

**80% 情況用這三組：**

    html
    
    <!-- 1. Flex 置中王 -->
    <div class="flex items-center justify-between">
     <!-- 左右兩邊，中間有空 -->
    </div>
    <!-- 2. Grid 響應王 -->
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
     <!-- 手機1欄 平板2欄 桌機4欄 -->
    </div>
    <!-- 3. Flex 表單王 -->
    <div class="flex items-center gap-4">
     <label class="w-24">標籤</label>
     <input class="flex-1 border p-2 rounded">
    </div>
