
## 🎯 **Effects - 效果快狠準**

----------

# ✨ **一、口訣先背起來**

> **「陰影用 shadow」**  
> **「模糊用 blur」**  
> **「透明用 opacity」**  
> **「亮暗用 brightness」**  
> **「hover 加效果」**

----------

# 🎭 **二、陰影 - 80% 只用這些**

類別

大小

用途

口訣

`shadow-sm`

小

輕量卡片

⭐⭐⭐

**`shadow`**

**標準**

**一般卡片**

⭐⭐⭐⭐⭐

`shadow-md`

中

浮起卡片

⭐⭐⭐⭐

`shadow-lg`

大

下拉選單

⭐⭐⭐⭐

`shadow-xl`

更大

Modal

⭐⭐⭐

`shadow-2xl`

超大

通知

⭐⭐

`shadow-inner`

內陰影

凹陷效果

⭐⭐

`shadow-none`

無

移除陰影

⭐⭐⭐

**🎯 90% 只用：**  `shadow`, `shadow-md`, `shadow-lg`, `shadow-none`

----------

# 🌫️ **三、模糊/透明 - 氛圍用**

## ✅ **模糊**

    html
    
    blur-none     = 不模糊
    blur-sm       = 4px 模糊
    blur          = 8px 模糊（標準）
    blur-md       = 12px
    blur-lg       = 16px
    blur-xl       = 24px
    blur-2xl      = 40px
    blur-3xl      = 64px

## ✅ **透明度**

    html
    
    opacity-0    = 0%   隱藏
    opacity-20   = 20%  很淡
    opacity-50   = 50%  半透明
    opacity-70   = 70%  稍透
    opacity-100  = 100% 不透明

**🎯 80% 只用：**  `opacity-0`, `opacity-50`, `opacity-100`, `blur`, `blur-lg`

----------

# 🎨 **四、實戰大全 - 直接複製貼上**

## ✅ **1. 卡片陰影層級**

    html
    
    <!-- 輕量卡片 -->
    <div class="bg-white shadow-sm p-6 rounded-lg">
     陰影較淡，適合背景不干擾
    </div>
    <!-- 標準卡片（最常用） -->
    <div class="bg-white shadow p-6 rounded-lg">
     一般卡片都用這個
    </div>
    <!-- 浮起卡片（hover時） -->
    <div class="bg-white shadow hover:shadow-md transition p-6 rounded-lg">
     滑過會浮起來
    </div>
    <!-- Modal / 下拉選單 -->
    <div class="bg-white shadow-xl p-6 rounded-lg">
     最高層級內容
    </div>

## ✅ **2. 模糊背景（毛玻璃）**

    html
    
    <!-- 背景模糊 + 半透明 -->
    <div class="backdrop-blur-md bg-white/30 p-6 rounded-lg">
     <p class="text-gray-900">毛玻璃效果</p>
    </div>
    <!-- 圖片上的模糊文字區 -->
    <div class="relative">
     <img src="hero.jpg" class="w-full h-96 object-cover">
     <div class="absolute inset-0 bg-black/50 backdrop-blur-sm flex items-center justify-center">
     <h2 class="text-white text-4xl font-bold">背景模糊的文字區</h2>
     </div>
    </div>
    <!-- 導覽列毛玻璃 -->
    <nav class="sticky top-0 backdrop-blur-md bg-white/70 border-b border-gray-200/50 px-6 py-4">
     半透明導覽列
    </nav>

## ✅ **3. Hover 效果**

    html
    
    <!-- 按鈕 hover 透明度 -->
    <button class="bg-blue-500 hover:opacity-90 text-white px-6 py-2 rounded transition">
     透明度變化
    </button>
    <!-- 圖片 hover 縮放 + 陰影 -->
    <div class="group overflow-hidden rounded-lg">
     <img src="product.jpg" class="w-full h-64 object-cover transition group-hover:scale-105 group-hover:shadow-lg">
     <div class="p-4 bg-white">
     <h3>商品名稱</h3>
     </div>
    </div>
    <!-- 卡片 hover 浮起 -->
    <div class="bg-white shadow hover:shadow-xl transition p-6 rounded-lg">
     hover 時陰影變大
    </div>
    <!-- 選單 hover 背景變深 -->
    <a href="#" class="block px-4 py-2 hover:bg-gray-100 transition">
     選項文字
    </a>

## ✅ **4. 載入/禁用狀態**

    html
    
    <!-- 載入中按鈕 -->
    <button disabled class="bg-blue-400 opacity-50 cursor-not-allowed px-6 py-2 rounded">
     載入中...
    </button>
    <!-- 禁用輸入框 -->
    <input disabled class="bg-gray-50 opacity-60 border border-gray-200 rounded px-4 py-2">
    <!-- 半透明遮罩 -->
    <div class="fixed inset-0 bg-black/50 flex items-center justify-center">
     <div class="bg-white p-8 rounded-lg">
     彈窗內容
     </div>
    </div>

## ✅ **5. 發光效果（焦點）**

    html
    
    <!-- 輸入框焦點發光 -->
    <input class="border border-gray-300 rounded px-4 py-2 focus:border-blue-500 focus:ring-2 focus:ring-blue-200 focus:outline-none">
    <!-- 按鈕發光 -->
    <button class="bg-blue-500 hover:bg-blue-600 text-white px-6 py-2 rounded focus:ring-4 focus:ring-blue-300 focus:outline-none">
     點擊發光
    </button>
    <!-- 自定義顏色發光 -->
    <div class="shadow-lg shadow-blue-500/50 p-6 rounded-lg">
     藍色光暈
    </div>

## ✅ **6. 亮度/對比/濾鏡**

    html
    
    <!-- 圖片 hover 變亮 -->
    <img src="product.jpg" class="hover:brightness-110 transition">
    <!-- 深色遮罩 -->
    <img src="product.jpg" class="brightness-50">
    <!-- 灰階（已失效） -->
    <img src="old.jpg" class="grayscale">
    <!-- 組合濾鏡 -->
    <div class="backdrop-blur backdrop-brightness-75 p-6">
     背景變暗 + 模糊
    </div>

----------

# 🎮 **五、Transition - 讓效果順暢**

## ✅ **最常用組合**

    html
    
    <!-- 全部屬性都過渡 -->
    transition
    <!-- 指定屬性 -->
    transition-shadow   只過渡陰影
    transition-colors   只過渡顏色 
    transition-opacity  只過渡透明度
    transition-transform 只過渡縮放/位移
    <!-- 加上時間 -->
    duration-200  0.2秒（最快）
    duration-300  0.3秒（標準）
    duration-500  0.5秒（慢）
    duration-700  0.7秒（很慢）
    <!-- 曲線 -->
    ease-linear   等速
    ease-in       慢快
    ease-out      快慢
    ease-in-out   慢快快慢

## ✅ **標準寫法**

    html
    
    <button class="bg-blue-500 hover:bg-blue-600 transition duration-300 ease-in-out">
     順暢變色
    </button>
    <div class="shadow hover:shadow-lg transition-shadow duration-300">
     順暢陰影
    </div>
    <img src="product.jpg" class="hover:scale-105 transition-transform duration-300">

----------

# ⚡ **六、響應式效果**

    html
    
    <!-- 手機：無陰影，桌機：有陰影 -->
    <div class="shadow-none md:shadow-md p-6">
     響應式陰影
    </div>
    <!-- 手機：不模糊，桌機：模糊背景 -->
    <nav class="backdrop-blur-none md:backdrop-blur-md bg-white/70">
     響應式毛玻璃
    </nav>

----------

# 🎯 **七、記憶小抄**

t

    ext
    
    陰影：
    shadow      = 標準
    shadow-md   = 中 
    shadow-lg   = 大
    shadow-none = 無
    模糊：
    blur        = 8px 標準
    blur-lg     = 16px
    backdrop-blur = 背景模糊
    透明度：
    opacity-0   = 0%
    opacity-50  = 50%
    opacity-100 = 100%
    過渡：
    transition
    duration-300
    ease-in-out
    濾鏡：
    brightness-50  亮度50%
    grayscale      黑白

----------

# 🚀 **八、80% 情況只會用到這些**

    html
    
    <!-- 1. 標準卡片陰影 -->
    shadow
    <!-- 2. hover 浮起 -->
    shadow hover:shadow-md transition-shadow
    <!-- 3. 禁用狀態 -->
    opacity-50 cursor-not-allowed
    <!-- 4. 遮罩層 -->
    bg-black/50
    <!-- 5. 毛玻璃導覽列 -->
    backdrop-blur-md bg-white/70
    <!-- 6. 圖片 hover 放大 -->
    hover:scale-105 transition-transform
    <!-- 7. 按鈕 hover 透明度 -->
    hover:opacity-90 transition
    <!-- 8. 焦點發光 -->
    focus:ring-2 focus:ring-blue-200 focus:outline-none

----------

# 💡 **九、實戰組合包**

    html
    
    <!-- 卡片 hover 浮起（最常見） -->
    <div class="bg-white shadow hover:shadow-lg transition-shadow duration-300 p-6 rounded-lg">
     🃏 滑過我會浮起來
    </div>
    <!-- 毛玻璃卡片 -->
    <div class="backdrop-blur-md bg-white/30 border border-white/20 shadow-lg p-6 rounded-lg">
     🥛 毛玻璃效果
    </div>
    <!-- 圖片 hover 縮放 -->
    <div class="overflow-hidden rounded-lg">
     <img src="product.jpg" class="w-full h-64 object-cover hover:scale-110 transition-transform duration-500">
    </div>
    <!-- 彈窗遮罩 -->
    <div class="fixed inset-0 bg-black/50 backdrop-blur-sm flex items-center justify-center">
     <div class="bg-white shadow-xl p-8 rounded-lg">
     📦 Modal 內容
     </div>
    </div>
    <!-- 導覽列毛玻璃 -->
    <nav class="sticky top-0 backdrop-blur-md bg-white/80 border-b border-gray-200/50 px-6 py-4">
     🧊 半透明導覽列
    </nav>
    <!-- 載入中狀態 -->
    <button disabled class="bg-blue-400 opacity-50 cursor-not-allowed px-6 py-2 rounded">
     ⏳ 處理中...
    </button>

----------

# 🎪 **十、濾鏡大全（少用但酷）**

    html
    
    <!-- 亮度 -->
    brightness-50   <!-- 50% 亮度 -->
    brightness-150  <!-- 150% 亮度 -->
    <!-- 對比 -->
    contrast-50     <!-- 低對比 -->
    contrast-150    <!-- 高對比 -->
    <!-- 其他 -->
    grayscale      黑白
    sepia          復古
    invert         負片
    saturate-150   飽和度

