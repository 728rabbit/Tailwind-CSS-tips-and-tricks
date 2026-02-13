
## 🎯 **Tailwind 其他常用補完計畫**

----------

# 🧩 **一、Sizing - 尺寸進階**

## ✅ **寬高常用但容易漏**

    html
    
    <!-- 最小/最大寬度 -->
    min-w-0        <!-- 允許壓縮到0 -->
    min-w-full     <!-- 最小100% -->
    max-w-xs       <!-- 20rem/320px -->
    max-w-sm       <!-- 24rem/384px -->
    max-w-md       <!-- 28rem/448px -->
    max-w-lg       <!-- 32rem/512px -->
    max-w-xl       <!-- 36rem/576px -->
    max-w-2xl      <!-- 42rem/672px -->
    max-w-4xl      <!-- 56rem/896px -->
    max-w-7xl      <!-- 80rem/1280px - 網站容器常用！-->
    <!-- 常用場景 -->
    <div class="max-w-7xl mx-auto px-4">
     <!-- 整個網站容器，大螢幕不無限延伸 -->
    </div>
    <!-- 高度相關 -->
    min-h-screen   <!-- 至少滿版 -->
    h-full         <!-- 高度100% -->
    max-h-96       <!-- 最大高度384px，可滾動區 -->

----------

# 📦 **二、Positioning - 定位**

## ✅ **絕對定位家族**

    html
    
    <!-- 定位類型 -->
    relative       <!-- 父層要有這個 -->
    absolute       <!-- 子層絕對定位 -->
    fixed         <!-- 固定視窗 -->
    sticky        <!-- 黏著定位（超好用！） -->
    <!-- 位置方向 -->
    inset-0       <!-- top:0; right:0; bottom:0; left:0 - 滿版遮罩 -->
    top-0         <!-- 貼齊上方 -->
    left-0        <!-- 貼齊左方 -->
    right-0       <!-- 貼齊右方 -->
    bottom-0      <!-- 貼齊下方 -->
    inset-x-0     <!-- left:0; right:0 -->
    inset-y-0     <!-- top:0; bottom:0 -->
    top-1/2       <!-- 50% 搭配 transform 置中 -->
    left-1/2
    -inset-4      <!-- 負值往外擴 -->

## ✅ **實戰聖經**

    html
    
    <!-- 1. 置中神器（永遠置中） -->
    <div class="relative">
     <div class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2">
     完全置中
     </div>
    </div>
    <!-- 2. 浮動按鈕 -->
    <button class="fixed bottom-6 right-6 bg-blue-500 text-white p-4 rounded-full shadow-lg">
     ↑
    </button>
    <!-- 3. 黏著標題 -->
    <h2 class="sticky top-0 bg-white py-4 border-b">
     滑過我會黏住
    </h2>
    <!-- 4. 圖片上的標籤 -->
    <div class="relative">
     <img src="product.jpg">
     <span class="absolute top-2 left-2 bg-red-500 text-white px-2 py-1 text-xs rounded">
     SALE
     </span>
    </div>
    <!-- 5. 滿版遮罩 -->
    <div class="fixed inset-0 bg-black/50 flex items-center justify-center">
     Modal
    </div>

----------

# 🔢 **三、Z-index - 圖層**

    html
    
    z-0     <!-- 0 -->
    z-10    <!-- 10 -->
    z-20    <!-- 20 --> 
    z-30    <!-- 30 -->
    z-40    <!-- 40 -->
    z-50    <!-- 50 - Modal常用 -->
    z-auto  <!-- auto -->
    <!-- 實戰 -->
    z-50    <!-- Modal -->
    z-40    <!-- 遮罩 -->
    z-30    <!-- 下拉選單 -->
    z-20    <!-- Header -->
    z-10    <!-- 一般內容 -->
    z-0     <!-- 背景 -->

----------

# 🖼️ **四、Object Fit - 圖片處理**

## ✅ **圖片必備**

    html
    
    <!-- 80% 情況用這個 -->
    object-cover   <!-- 填滿、裁切、不變形 -->
    object-contain <!-- 完整顯示、留白 -->
    <!-- 搭配 -->
    object-center  <!-- 置中（預設） -->
    object-top     <!-- 對齊上方（人像） -->
    object-bottom  <!-- 對齊下方 -->
    <!-- 標準寫法 -->
    <img src="photo.jpg" class="w-full h-64 object-cover object-center rounded-lg">

----------

# 🔄 **五、Transform - 變形**

## ✅ **最常用**

    html
    
    <!-- 縮放 -->
    scale-95      <!-- 0.95倍 -->
    scale-100     <!-- 1倍 -->
    scale-105     <!-- 1.05倍 hover常用 -->
    scale-110     <!-- 1.1倍 -->
    <!-- 旋轉 -->
    rotate-45     <!-- 45度 -->
    rotate-90     <!-- 90度 -->
    rotate-180    <!-- 180度 -->
    <!-- 位移 -->
    translate-x-1/2  <!-- 50% -->
    translate-y-1/2
    -translate-x-1/2 <!-- 負50% -->
    <!-- 組合 -->
    transform      <!-- 開啟變形（Tailwind 3+ 可省略） -->
    transform-gpu  <!-- 硬體加速 -->

----------

# 🎬 **六、Animation - 動畫**

## ✅ **內建動畫**

    html
    
    animate-spin      <!-- 旋轉載入 -->
    animate-ping      <!-- 雷達波 -->
    animate-pulse     <!-- 呼吸燈 -->
    animate-bounce    <!-- 彈跳 -->
    animate-none      <!-- 關閉 -->
    <!-- 載入 spinner -->
    <svg class="animate-spin h-5 w-5 text-white">
     <!-- 圖示 -->
    </svg>
    <!-- 通知紅點 -->
    <span class="absolute -top-1 -right-1 h-3 w-3 bg-red-500 rounded-full animate-ping"></span>

----------

# 📋 **七、Lists - 列表**

    html
    
    list-none      <!-- 無項目符號 -->
    list-disc      <!-- 實心圓點 -->
    list-decimal   <!-- 數字 -->
    list-inside    <!-- 符號在內 -->
    list-outside   <!-- 符號在外（預設） -->
    <!-- 實戰 -->
    <ul class="list-disc list-inside space-y-2">
     <li>第一項</li>
     <li>第二項</li>
    </ul>

----------

# 🔍 **八、Interactivity - 互動**

    html
    
    cursor-pointer   <!-- 手指 -->
    cursor-default   <!-- 預設 -->
    cursor-not-allowed <!-- 不能點 -->
    cursor-wait     <!-- 載入中 -->
    select-none     <!-- 不能選取 -->
    select-text     <!-- 可選取（預設） -->
    resize          <!-- 可拉大 -->
    resize-none     <!-- 固定大小 -->
    resize-y        <!-- 垂直可拉 -->
    resize-x        <!-- 水平可拉 -->

----------

# 🧹 **九、Clear/Overflow - 清除/溢出**

    html
    
    overflow-hidden   <!-- 裁切 -->
    overflow-auto     <!-- 捲軸 -->
    overflow-scroll   <!-- 強制捲軸 -->
    overflow-visible  <!-- 顯示超出 -->
    truncate         <!-- 文字超出行省略（單行） -->
    line-clamp-2     <!-- 2行後省略（超好用！） -->
    line-clamp-3     <!-- 3行省略 -->
    line-clamp-none  <!-- 不省略 -->
    <!-- 實戰 -->
    <p class="line-clamp-2">
     這段文字超過兩行就會顯示...非常適合卡片描述
    </p>

----------

# 🎯 **十、Filters - 進階濾鏡**

    html
    
    <!-- 背濾鏡（毛玻璃） -->
    backdrop-blur-sm
    backdrop-blur
    backdrop-blur-md
    backdrop-blur-lg
    <!-- 亮度 -->
    backdrop-brightness-75
    backdrop-brightness-50
    <!-- 灰階 -->
    backdrop-grayscale
    backdrop-grayscale-0

----------

# 🚀 **十一、80% 情況下會用到的補完清單**

    html
    
    <!-- 1. 網站容器 -->
    max-w-7xl mx-auto px-4
    <!-- 2. 圖片處理 -->
    object-cover object-center
    <!-- 3. 置中神器 -->
    absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2
    <!-- 4. 黏著標題 -->
    sticky top-0 bg-white z-10
    <!-- 5. 文字省略 -->
    line-clamp-2
    <!-- 6. 載入動畫 -->
    animate-spin
    <!-- 7. 手指游標 -->
    cursor-pointer
    <!-- 8. 滾動區 -->
    overflow-auto max-h-96
    <!-- 9. 下拉選單圖層 -->
    z-50
    <!-- 10. 禁用狀態 -->
    cursor-not-allowed opacity-50
