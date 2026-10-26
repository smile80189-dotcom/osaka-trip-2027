# osaka-trip-2027
<!DOCTYPE html>
<html lang="zh-TW">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>大阪 5 天 4 夜繪本之旅 🏯✨</title>
  
  <!-- Google Fonts: 粉圓體 (Huninn) -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Zen+Maru+Gothic:wght@400;700;900&display=swap" rel="stylesheet">
  
  <!-- Tailwind CSS CDN -->
  <script src="https://cdn.tailwindcss.com"></script>
  
  <!-- FontAwesome Icons -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

  <script>
    tailwind.config = {
      theme: {
        extend: {
          colors: {
            paper: '#FFFCF6',
            ink: '#3E3A39',
            coral: '#F2A497',
            yamabuki: '#F6D27A',
            mizuiro: '#A8D3E6',
            wakatake: '#B9DAA5',
            sand: '#F7F0E3'
          },
          fontFamily: {
            huninn: ['"Zen Maru Gothic"', 'sans-serif'],
          },
          boxShadow: {
            'picture-book': '3px 4px 0px #3E3A39',
            'picture-book-lg': '5px 6px 0px #3E3A39',
            'picture-book-sm': '2px 2px 0px #3E3A39',
          }
        }
      }
    }
  </script>

  <style>
    body {
      background-color: #FFFCF6;
      color: #3E3A39;
      font-family: 'Zen Maru Gothic', sans-serif;
      overflow-x: hidden;
    }

    /* 手繪風格黑框與粗線邊框 */
    .pb-border {
      border: 3px solid #3E3A39;
      border-radius: 24px;
    }

    .pb-border-sm {
      border: 2px solid #3E3A39;
      border-radius: 16px;
    }

    /* 浮輕微動畫 */
    @keyframes gentle-float {
      0%, 100% { transform: translateY(0px) rotate(0deg); }
      50% { transform: translateY(-8px) rotate(1.5deg); }
    }

    @keyframes gentle-bounce {
      0%, 100% { transform: scale(1); }
      50% { transform: scale(1.04); }
    }

    .animate-float {
      animation: gentle-float 4s ease-in-out infinite;
    }

    .tab-bounce {
      animation: gentle-bounce 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275);
    }

    /* 支援減少動態效果 (Accessibility) */
    @media (prefers-reduced-motion: reduce) {
      .animate-float, .tab-bounce, .transition-all {
        animation: none !important;
        transition: none !important;
      }
    }

    /* 自訂 Checkbox 手繪風格 */
    .custom-checkbox {
      appearance: none;
      width: 22px;
      height: 22px;
      border: 3px solid #3E3A39;
      border-radius: 8px;
      outline: none;
      cursor: pointer;
      position: relative;
      background-color: #FFFFFF;
      transition: all 0.2s;
    }

    .custom-checkbox:checked {
      background-color: #F2A497;
    }

    .custom-checkbox:checked::after {
      content: '✓';
      position: absolute;
      color: #3E3A39;
      font-weight: 900;
      font-size: 14px;
      top: -3px;
      left: 3px;
    }

    /* Tab active style */
    .day-tab.active {
      background-color: #F6D27A;
      transform: translateY(-2px);
      box-shadow: 3px 4px 0px #3E3A39;
    }

    /* 全頁可編輯輔助框視覺提醒 */
    [contenteditable="true"]:hover {
      outline: 2px dashed #F2A497;
      border-radius: 4px;
    }
    [contenteditable="true"]:focus {
      outline: 2px solid #3E3A39;
      background-color: rgba(246, 210, 122, 0.2);
      border-radius: 4px;
    }

    /* Custom scrollbar */
    ::-webkit-scrollbar {
      width: 8px;
      height: 8px;
    }
    ::-webkit-scrollbar-track {
      background: #FFFCF6;
    }
    ::-webkit-scrollbar-thumb {
      background: #A8D3E6;
      border: 2px solid #3E3A39;
      border-radius: 10px;
    }
  </style>
</head>
<body class="pb-28">

  <!-- 頂端固定導覽列 -->
  <nav class="fixed top-0 left-0 right-0 z-40 bg-[#FFFCF6]/90 backdrop-blur-md border-b-4 border-[#3E3A39] px-4 py-3">
    <div class="max-w-md mx-auto flex justify-between items-center">
      <a href="#home" class="flex items-center gap-2 font-black text-lg text-ink">
        <span class="bg-coral text-white p-1 px-2 rounded-xl border-2 border-ink text-xs">2027</span>
        <span contenteditable="true">大阪繪本小旅行</span>
      </a>
      <span class="text-xs font-bold bg-yamabuki px-2 py-1 rounded-full border-2 border-ink"><i class="fa-solid fa-pen text-[10px] mr-1"></i>點文字即可編輯</span>
    </div>
  </nav>

  <!-- 主容器 (手機優先 max-w-md) -->
  <main class="max-w-md mx-auto pt-20 px-4 space-y-8">

    <!-- 首頁 Hero 區塊 -->
    <section id="home" class="bg-sand p-6 pb-8 pb-border shadow-picture-book-lg text-center relative overflow-hidden mt-2">
      <div class="absolute top-2 left-3 text-coral opacity-60"><i class="fa-solid fa-cloud text-2xl"></i></div>
      <div class="absolute top-6 right-4 text-mizuiro opacity-60"><i class="fa-solid fa-sparkles text-xl"></i></div>
      
      <!-- 手繪風 SVG 插圖：大阪城與櫻花太陽 -->
      <div class="relative w-40 h-40 mx-auto mb-3 animate-float">
        <svg viewBox="0 0 200 200" class="w-full h-full">
          <circle cx="150" cy="50" r="30" fill="#F2A497" stroke="#3E3A39" stroke-width="4" />
          <path d="M 20,70 Q 35,50 50,70 Q 65,50 80,70 Q 90,85 75,95 Q 60,100 45,95 Q 25,100 20,70 Z" fill="#FFFFFF" stroke="#3E3A39" stroke-width="4"/>
          <polygon points="50,170 150,170 140,130 60,130" fill="#A8D3E6" stroke="#3E3A39" stroke-width="4"/>
          <line x1="75" y1="130" x2="70" y2="170" stroke="#3E3A39" stroke-width="3"/>
          <line x1="125" y1="130" x2="130" y2="170" stroke="#3E3A39" stroke-width="3"/>
          <rect x="65" y="100" width="70" height="30" rx="4" fill="#F7F0E3" stroke="#3E3A39" stroke-width="4"/>
          <path d="M 55,100 Q 100,85 145,100" fill="#B9DAA5" stroke="#3E3A39" stroke-width="4"/>
          <rect x="75" y="70" width="50" height="20" rx="3" fill="#F6D27A" stroke="#3E3A39" stroke-width="4"/>
          <path d="M 65,70 Q 100,50 135,70 Z" fill="#B9DAA5" stroke="#3E3A39" stroke-width="4"/>
          <circle cx="100" cy="45" r="7" fill="#F6D27A" stroke="#3E3A39" stroke-width="3"/>
        </svg>
      </div>

      <h1 class="text-2xl font-black text-ink mb-1" contenteditable="true">大阪 5 天 4 夜關西遊</h1>
      <p class="text-sm font-bold text-ink/70 mb-4" contenteditable="true">2027.01.13 ~ 2027.01.17 🇯🇵</p>

      <!-- 倒數計時器 -->
      <div class="bg-paper p-3 pb-border-sm shadow-picture-book-sm inline-block w-full">
        <p class="text-xs font-bold text-ink/70 mb-1" contenteditable="true">距離出發還有 ✈️</p>
        <div class="flex justify-center items-center gap-2 font-black text-lg text-ink">
          <div class="bg-yamabuki px-3 py-1 rounded-xl border-2 border-ink" id="cd-days">--</div> <span class="text-sm">天</span>
          <div class="bg-mizuiro px-3 py-1 rounded-xl border-2 border-ink" id="cd-hours">--</div> <span class="text-sm">時</span>
          <div class="bg-coral px-3 py-1 rounded-xl border-2 border-ink text-white" id="cd-mins">--</div> <span class="text-sm">分</span>
        </div>
      </div>
    </section>

    <!-- 航班資訊卡片 -->
    <section id="flight" class="space-y-3">
      <div class="flex items-center gap-2">
        <span class="w-4 h-8 bg-coral rounded-full border-2 border-ink"></span>
        <h2 class="text-xl font-black text-ink" contenteditable="true">航班資訊</h2>
      </div>

      <div class="bg-paper p-5 pb-border shadow-picture-book space-y-4">
        <div class="flex justify-between items-center pb-3 border-b-2 border-dashed border-ink/30">
          <div class="flex items-center gap-2">
            <div class="w-8 h-8 rounded-lg bg-yamabuki border-2 border-ink flex items-center justify-center font-black text-xs">
              虎
            </div>
            <div>
              <p class="font-black text-sm" contenteditable="true">台灣虎航 Tigerair</p>
              <p class="text-xs text-ink/60 font-bold" contenteditable="true">直飛雙程班機</p>
            </div>
          </div>
          <span class="text-xs font-black bg-wakatake px-2.5 py-1 rounded-full border-2 border-ink" contenteditable="true">已確認</span>
        </div>

        <!-- 去程 -->
        <div class="space-y-2">
          <div class="flex items-center justify-between text-xs font-black text-ink/70">
            <span contenteditable="true">去程 ‧ 2027.01.13 (三)</span>
            <span class="bg-mizuiro/50 px-2 py-0.5 rounded-md border border-ink/40" contenteditable="true">3h 25m</span>
          </div>
          <div class="flex justify-between items-center bg-sand p-3 rounded-2xl border-2 border-ink">
            <div class="text-center">
              <p class="text-xl font-black" contenteditable="true">07:00</p>
              <p class="text-xs font-bold text-ink/70" contenteditable="true">TPE 桃園</p>
            </div>
            <div class="flex-1 flex flex-col items-center px-3">
              <i class="fa-solid fa-plane text-coral text-sm"></i>
              <div class="w-full border-b-2 border-dotted border-ink my-1"></div>
            </div>
            <div class="text-center">
              <p class="text-xl font-black" contenteditable="true">10:25</p>
              <p class="text-xs font-bold text-ink/70" contenteditable="true">KIX 關西</p>
            </div>
          </div>
        </div>

        <!-- 回程 -->
        <div class="space-y-2">
          <div class="flex items-center justify-between text-xs font-black text-ink/70">
            <span contenteditable="true">回程 ‧ 2027.01.17 (日)</span>
            <span class="bg-mizuiro/50 px-2 py-0.5 rounded-md border border-ink/40" contenteditable="true">3h 20m</span>
          </div>
          <div class="flex justify-between items-center bg-sand p-3 rounded-2xl border-2 border-ink">
            <div class="text-center">
              <p class="text-xl font-black" contenteditable="true">11:30</p>
              <p class="text-xs font-bold text-ink/70" contenteditable="true">KIX 關西</p>
            </div>
            <div class="flex-1 flex flex-col items-center px-3">
              <i class="fa-solid fa-plane text-coral text-sm rotate-180"></i>
              <div class="w-full border-b-2 border-dotted border-ink my-1"></div>
            </div>
            <div class="text-center">
              <p class="text-xl font-black" contenteditable="true">13:50</p>
              <p class="text-xs font-bold text-ink/70" contenteditable="true">TPE 桃園</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- 住宿資訊 -->
    <section id="hotel" class="space-y-3">
      <div class="flex items-center justify-between">
        <div class="flex items-center gap-2">
          <span class="w-4 h-8 bg-mizuiro rounded-full border-2 border-ink"></span>
          <h2 class="text-xl font-black text-ink" contenteditable="true">住宿飯店</h2>
        </div>
        <a href="https://www.google.com/maps/search/?api=1&query=Hotel+Hankyu+RESPIRE+OSAKA" target="_blank" class="text-xs font-black bg-yamabuki px-3 py-1.5 rounded-xl border-2 border-ink shadow-picture-book-sm active:translate-y-0.5 flex items-center gap-1">
          <i class="fa-solid fa-location-dot text-coral"></i> 地圖
        </a>
      </div>

      <div class="bg-paper p-4 pb-border shadow-picture-book flex items-center gap-4">
        <div class="w-16 h-16 rounded-2xl bg-yamabuki border-2 border-ink flex-shrink-0 flex items-center justify-center text-3xl">
          🏨
        </div>
        <div>
          <span class="text-xs font-black bg-coral text-white px-2 py-0.5 rounded-md border border-ink" contenteditable="true">連續入住 4 晚</span>
          <h3 class="font-black text-base mt-1" contenteditable="true">大阪龍仕柏飯店</h3>
          <p class="text-xs font-bold text-ink/70" contenteditable="true">Hotel Hankyu RESPIRE OSAKA</p>
          <p class="text-xs text-ink/60 mt-0.5" contenteditable="true">梅田站直結 ‧ 逛街交通超便利</p>
        </div>
      </div>
    </section>

    <!-- 每日行程 區塊 (日期切換 + 時間軸) -->
    <section id="itinerary" class="space-y-4 pt-2">
      <div class="flex items-center justify-between">
        <div class="flex items-center gap-2">
          <span class="w-4 h-8 bg-yamabuki rounded-full border-2 border-ink"></span>
          <h2 class="text-xl font-black text-ink" contenteditable="true">每日行程</h2>
        </div>
        <span class="text-xs font-bold bg-sand px-2.5 py-1 rounded-full border-2 border-ink">點擊日期切換</span>
      </div>

      <!-- 日期分頁按鈕 (5天) -->
      <div class="grid grid-cols-5 gap-1.5" id="day-tabs">
        <button onclick="switchDay(1)" id="tab-d1" class="day-tab active pb-border-sm py-2 px-1 text-center bg-paper cursor-pointer transition-all">
          <p class="text-[10px] font-black opacity-70">1/13</p>
          <p class="text-xs font-black">D1</p>
        </button>
        <button onclick="switchDay(2)" id="tab-d2" class="day-tab pb-border-sm py-2 px-1 text-center bg-paper cursor-pointer transition-all">
          <p class="text-[10px] font-black opacity-70">1/14</p>
          <p class="text-xs font-black">D2</p>
        </button>
        <button onclick="switchDay(3)" id="tab-d3" class="day-tab pb-border-sm py-2 px-1 text-center bg-paper cursor-pointer transition-all">
          <p class="text-[10px] font-black opacity-70">1/15</p>
          <p class="text-xs font-black">D3</p>
        </button>
        <button onclick="switchDay(4)" id="tab-d4" class="day-tab pb-border-sm py-2 px-1 text-center bg-paper cursor-pointer transition-all">
          <p class="text-[10px] font-black opacity-70">1/16</p>
          <p class="text-xs font-black">D4</p>
        </button>
        <button onclick="switchDay(5)" id="tab-d5" class="day-tab pb-border-sm py-2 px-1 text-center bg-paper cursor-pointer transition-all">
          <p class="text-[10px] font-black opacity-70">1/17</p>
          <p class="text-xs font-black">D5</p>
        </button>
      </div>

      <!-- 動態主題抬頭卡片 -->
      <div id="day-header" class="bg-wakatake p-4 pb-border shadow-picture-book flex items-center justify-between">
        <div>
          <span id="day-date-badge" class="text-xs font-black bg-paper px-2 py-0.5 rounded-md border border-ink" contenteditable="true">2027.01.13 (三)</span>
          <h3 id="day-title" class="text-lg font-black text-ink mt-1" contenteditable="true">Day 1 ‧ 大阪市區漫步</h3>
        </div>
        <div id="day-svg" class="w-12 h-12 flex items-center justify-center text-2xl">
          🛍️
        </div>
      </div>

      <!-- 時間軸卡片內容 -->
      <div id="timeline-container" class="space-y-4 relative pl-4 border-l-4 border-dashed border-ink/40 ml-2">
        <!-- D1 內容預設展示 -->
      </div>
    </section>

    <!-- 分帳與記帳功能 區塊 -->
    <section id="expense" class="space-y-3 pt-2">
      <div class="flex items-center justify-between">
        <div class="flex items-center gap-2">
          <span class="w-4 h-8 bg-coral rounded-full border-2 border-ink"></span>
          <h2 class="text-xl font-black text-ink">旅程分帳記帳</h2>
        </div>
        <span class="text-xs font-black bg-sand px-2.5 py-1 rounded-full border-2 border-ink">即時統計</span>
      </div>

      <!-- 記帳表單 -->
      <div class="bg-paper p-5 pb-border shadow-picture-book space-y-3">
        <h3 class="font-black text-sm text-ink flex items-center gap-2">
          <i class="fa-solid fa-pen-to-square text-coral"></i> 新增消費紀錄
        </h3>
        
        <div class="grid grid-cols-2 gap-2 text-xs font-bold">
          <div>
            <label class="block text-ink/70 mb-1">消費日</label>
            <select id="exp-date" class="w-full p-2 bg-sand rounded-xl border-2 border-ink outline-none">
              <option value="Day 1 (1/13)">Day 1 (1/13)</option>
              <option value="Day 2 (1/14)">Day 2 (1/14)</option>
              <option value="Day 3 (1/15)">Day 3 (1/15)</option>
              <option value="Day 4 (1/16)">Day 4 (1/16)</option>
              <option value="Day 5 (1/17)">Day 5 (1/17)</option>
            </select>
          </div>

          <div>
            <label class="block text-ink/70 mb-1">消費類別</label>
            <select id="exp-cat" class="w-full p-2 bg-sand rounded-xl border-2 border-ink outline-none">
              <option value="餐饮美食">🍜 餐飲美食</option>
              <option value="交通票券">🚃 交通票券</option>
              <option value="購物買物">🛍️ 購物買物</option>
              <option value="景點門票">🎟️ 景點門票</option>
              <option value="其他雜項">🎈 其他雜項</option>
            </select>
          </div>

          <div>
            <label class="block text-ink/70 mb-1">消費名稱</label>
            <input type="text" id="exp-name" placeholder="例：鴨與蔥拉麵" class="w-full p-2 bg-sand rounded-xl border-2 border-ink outline-none">
          </div>

          <div>
            <label class="block text-ink/70 mb-1">金額 (NTD / JPY)</label>
            <input type="number" id="exp-amount" placeholder="1000" class="w-full p-2 bg-sand rounded-xl border-2 border-ink outline-none">
          </div>
        </div>

        <button onclick="addExpense()" class="w-full py-2.5 bg-yamabuki font-black text-sm text-ink rounded-xl border-2 border-ink shadow-picture-book-sm active:translate-y-0.5 cursor-pointer mt-2">
          ＋ 新增這筆花費
        </button>
      </div>

      <!-- 每日花費總額統計 -->
      <div class="bg-sand p-4 rounded-2xl pb-border-sm shadow-picture-book-sm space-y-2">
        <h3 class="font-black text-xs text-ink/80 flex items-center justify-between border-b border-ink/20 pb-1">
          <span>📅 每日花費總額匯總</span>
          <span class="text-coral font-black" id="exp-grand-total">總計: 0</span>
        </h3>
        <div id="daily-expense-totals" class="grid grid-cols-2 gap-2 text-xs font-black">
          <!-- JS 動態計算渲染 -->
        </div>
      </div>

      <!-- 消費列表 -->
      <div class="bg-paper p-4 pb-border shadow-picture-book space-y-2">
        <h3 class="font-black text-xs text-ink/70">消費細項清單</h3>
        <div id="expense-list" class="space-y-2 text-xs font-bold">
          <!-- JS 渲染 -->
        </div>
      </div>
    </section>

    <!-- 採購清單區塊 -->
    <section id="shopping" class="space-y-3 pt-2">
      <div class="flex items-center justify-between">
        <div class="flex items-center gap-2">
          <span class="w-4 h-8 bg-yamabuki rounded-full border-2 border-ink"></span>
          <h2 class="text-xl font-black text-ink">採購紀念清單</h2>
        </div>
        <span class="text-xs font-black bg-wakatake px-2.5 py-1 rounded-full border-2 border-ink" id="shop-progress">0/0 完成</span>
      </div>

      <div class="bg-paper p-5 pb-border shadow-picture-book space-y-3">
        <!-- 新增採購品項 -->
        <div class="flex gap-2">
          <input type="text" id="shop-input" placeholder="輸入想買的藥妝/伴手禮..." class="flex-1 p-2 text-xs font-bold bg-sand rounded-xl border-2 border-ink outline-none">
          <button onclick="addShoppingItem()" class="px-4 bg-coral text-white font-black text-xs rounded-xl border-2 border-ink shadow-picture-book-sm active:translate-y-0.5 cursor-pointer">
            加入
          </button>
        </div>

        <!-- 採購清單網格 -->
        <div class="space-y-2 text-xs font-bold" id="shopping-list">
          <!-- JS 渲染 -->
        </div>
      </div>
    </section>

    <!-- 攜帶物品清單區塊 -->
    <section id="packing" class="space-y-3 pt-2">
      <div class="flex items-center justify-between">
        <div class="flex items-center gap-2">
          <span class="w-4 h-8 bg-wakatake rounded-full border-2 border-ink"></span>
          <h2 class="text-xl font-black text-ink" contenteditable="true">行李整理清單</h2>
        </div>
        <span id="packing-progress" class="text-xs font-black bg-yamabuki px-2.5 py-1 rounded-full border-2 border-ink">0/0 完成</span>
      </div>

      <!-- 隨身行李 -->
      <div class="bg-paper p-5 pb-border shadow-picture-book space-y-3">
        <div class="flex items-center gap-2 text-coral border-b-2 border-ink/20 pb-2">
          <i class="fa-solid fa-bag-shopping font-black"></i>
          <h3 class="font-black text-sm text-ink" contenteditable="true">隨身背包 / 登機包</h3>
        </div>
        <div class="grid grid-cols-2 gap-2 text-xs font-bold" id="carryon-list">
          <!-- JS 渲染 -->
        </div>
      </div>

      <!-- 托運行李 -->
      <div class="bg-paper p-5 pb-border shadow-picture-book space-y-3">
        <div class="flex items-center gap-2 text-mizuiro border-b-2 border-ink/20 pb-2">
          <i class="fa-solid fa-suitcase-rolling font-black text-ink"></i>
          <h3 class="font-black text-sm text-ink" contenteditable="true">托運行李箱</h3>
        </div>
        <div class="grid grid-cols-1 gap-2 text-xs font-bold" id="checked-list">
          <!-- JS 渲染 -->
        </div>
      </div>
    </section>

    <!-- 行程費用預算區塊 -->
    <section id="budget" class="space-y-3 pt-2">
      <div class="flex items-center gap-2">
        <span class="w-4 h-8 bg-coral rounded-full border-2 border-ink"></span>
        <h2 class="text-xl font-black text-ink" contenteditable="true">行程費用與預算</h2>
      </div>

      <div class="bg-paper p-5 pb-border shadow-picture-book space-y-4">
        <!-- 總計金額 -->
        <div class="bg-sand p-4 rounded-2xl border-2 border-ink flex justify-between items-center">
          <div>
            <p class="text-xs font-bold text-ink/70" contenteditable="true">預估每人費用總計</p>
            <p class="text-2xl font-black text-coral" id="total-cost">NT$ --</p>
          </div>
          <div class="w-12 h-12 rounded-full bg-yamabuki border-2 border-ink flex items-center justify-center text-xl">
            💰
          </div>
        </div>

        <!-- 費用明細 -->
        <div class="space-y-2 text-xs font-bold" id="budget-items">
          <!-- JS 渲染 -->
        </div>

        <p class="text-[10px] text-ink/60 text-center font-bold pt-2 border-t-2 border-dashed border-ink/20" contenteditable="true">
          💡 票券明細：票券+行程 (16,184 = 1,689 + 9,500 + 2,010 + 2,985)
        </p>
      </div>
    </section>

  </main>

  <!-- 底部固定選單 (釘選功能列: 行程、地圖、首頁、記帳、行李) -->
  <div class="fixed bottom-0 left-0 right-0 z-50 bg-[#FFFCF6] border-t-4 border-[#3E3A39] py-2 px-4 shadow-[0_-4px_10px_rgba(0,0,0,0.05)]">
    <div class="max-w-md mx-auto flex justify-around items-center">
      <a href="#itinerary" class="flex flex-col items-center text-ink hover:text-coral transition-colors">
        <div class="w-9 h-9 rounded-2xl bg-yamabuki border-2 border-ink flex items-center justify-center shadow-picture-book-sm active:translate-y-0.5">
          <i class="fa-solid fa-calendar-days text-sm"></i>
        </div>
        <span class="text-[10px] font-black mt-1">行程</span>
      </a>

      <a href="https://maps.google.com/?q=Osaka" target="_blank" class="flex flex-col items-center text-ink hover:text-coral transition-colors">
        <div class="w-9 h-9 rounded-2xl bg-mizuiro border-2 border-ink flex items-center justify-center shadow-picture-book-sm active:translate-y-0.5">
          <i class="fa-solid fa-map-location-dot text-sm"></i>
        </div>
        <span class="text-[10px] font-black mt-1">地圖</span>
      </a>

      <a href="#home" class="flex flex-col items-center text-ink hover:text-coral transition-colors">
        <div class="w-11 h-11 rounded-2xl bg-coral text-white border-2 border-ink flex items-center justify-center shadow-picture-book-sm active:translate-y-0.5 -mt-3">
          <i class="fa-solid fa-house text-base"></i>
        </div>
        <span class="text-[10px] font-black mt-0.5">首頁</span>
      </a>

      <a href="#expense" class="flex flex-col items-center text-ink hover:text-coral transition-colors">
        <div class="w-9 h-9 rounded-2xl bg-wakatake border-2 border-ink flex items-center justify-center shadow-picture-book-sm active:translate-y-0.5">
          <i class="fa-solid fa-receipt text-sm"></i>
        </div>
        <span class="text-[10px] font-black mt-1">記帳</span>
      </a>

      <a href="#packing" class="flex flex-col items-center text-ink hover:text-coral transition-colors">
        <div class="w-9 h-9 rounded-2xl bg-sand border-2 border-ink flex items-center justify-center shadow-picture-book-sm active:translate-y-0.5">
          <i class="fa-solid fa-suitcase text-sm"></i>
        </div>
        <span class="text-[10px] font-black mt-1">行李</span>
      </a>
    </div>
  </div>

  <!-- 底部手繪頁尾 -->
  <footer class="mt-8 text-center text-xs font-bold text-ink/60 space-y-1">
    <p contenteditable="true">Have a nice trip in Osaka! 🇯🇵✨</p>
    <p class="text-[10px]" contenteditable="true">繪本風旅遊手冊 ‧ 2027</p>
  </footer>

  <script>
    // 1. 出發倒數計時器
    const targetDate = new Date('2027-01-13T07:00:00').getTime();

    function updateCountdown() {
      const now = new Date().getTime();
      const diff = targetDate - now;

      if (diff > 0) {
        const days = Math.floor(diff / (1000 * 60 * 60 * 24));
        const hours = Math.floor((diff % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
        const mins = Math.floor((diff % (1000 * 60 * 60)) / (1000 * 60));

        document.getElementById('cd-days').innerText = days;
        document.getElementById('cd-hours').innerText = hours.toString().padStart(2, '0');
        document.getElementById('cd-mins').innerText = mins.toString().padStart(2, '0');
      } else {
        document.getElementById('cd-days').innerText = '0';
        document.getElementById('cd-hours').innerText = '00';
        document.getElementById('cd-mins').innerText = '00';
      }
    }
    updateCountdown();
    setInterval(updateCountdown, 60000);

    // 2. 每日行程資料集 (包含 Google Map 搜尋連結)
    const itineraryData = {
      1: {
        date: "2027.01.13 (三)",
        title: "Day 1 ‧ 大阪市區漫步",
        badgeColor: "bg-wakatake",
        icon: "🛍️",
        events: [
          { time: "07:00 - 10:25", title: "搭乘台灣虎航前往大阪", type: "交通", tagColor: "bg-mizuiro", desc: "桃園機場 (TPE) ➔ 關西國際機場 (KIX)", map: "Kansai+International+Airport" },
          { time: "11:30 - 12:30", title: "關西機場前往大阪市區", type: "交通", tagColor: "bg-mizuiro", desc: "搭乘 JR Haruka 或南海電鐵特急前往梅田/難波" },
          { time: "13:00", title: "大阪龍仕柏飯店 Check in", type: "住宿", tagColor: "bg-yamabuki", desc: "放置行李、稍作休息 (Hotel Hankyu RESPIRE OSAKA)", map: "Hotel+Hankyu+RESPIRE+OSAKA" },
          { time: "13:30", title: "午餐：鴨と葱拉麵", type: "美食", tagColor: "bg-coral text-white", must: true, desc: "品嚐極致鮮美鴨肉湯頭與精選日本蔥拉麵 🍜", map: "Ramen+Kamo+to+Negi+Osaka" },
          { time: "15:00 - 18:00", title: "梅田 / 心齋橋市區逛街購物", type: "景點", tagColor: "bg-wakatake", desc: "逛百貨、藥妝店、服飾店與買紀念品", map: "Shinsaibashi-suji+Shopping+Street" },
          { time: "18:30", title: "晚餐：燒肉但馬屋", type: "美食", tagColor: "bg-coral text-white", must: true, desc: "享用頂級熟成和牛燒肉盛宴 🥩", map: "Tajimaya+Osaka" },
          { time: "20:30", title: "返回飯店休息", type: "住宿", tagColor: "bg-yamabuki", desc: "整理戰利品，準備明天環球影城體力！" }
        ]
      },
      2: {
        date: "2027.01.14 (四)",
        title: "Day 2 ‧ 環球影城全日夢幻之旅",
        badgeColor: "bg-yamabuki",
        icon: "🎢",
        events: [
          { time: "07:30 - 08:15", title: "出發前往日本環球影城 (USJ)", type: "交通", tagColor: "bg-mizuiro", desc: "從梅田搭乘 JR 櫻島線前往 Universal City 站", map: "Universal+Studios+Japan" },
          { time: "08:30 - 18:30", title: "環球影城一日遊", type: "必去景點", tagColor: "bg-coral text-white", must: true, desc: "超級任天堂世界 🍄、哈利波特魔法世界 🧹、歡樂遊行", map: "Universal+Studios+Japan" },
          { time: "19:30", title: "晚餐：TSUKADA 壽喜燒", type: "美食", tagColor: "bg-coral text-white", must: true, desc: "熱騰騰濃郁高湯與優質牛肉壽喜燒 🍲", map: "TSUKADA+Sukiyaki+Osaka" },
          { time: "21:30", title: "返回飯店休息", type: "住宿", tagColor: "bg-yamabuki", desc: "泡澡舒緩雙腿疲勞 🛀" }
        ]
      },
      3: {
        date: "2027.01.15 (五)",
        title: "Day 3 ‧ 京都天橋立 & 伊根舟屋一日遊",
        badgeColor: "bg-mizuiro",
        icon: "🌊",
        events: [
          { time: "07:45", title: "日本橋車站集合出發", type: "集合", tagColor: "bg-sand", desc: "搭乘一日遊專車前往海之京都", map: "Nippombashi+Station" },
          { time: "10:30 - 12:30", title: "日本三景：天橋立", type: "必去景點", tagColor: "bg-coral text-white", must: true, desc: "搭纜車登上傘松公園，觀賞「飛龍觀」絕景 🐉", map: "Amanohashidate" },
          { time: "13:30 - 15:30", title: "伊根舟屋散策", type: "必去景點", tagColor: "bg-wakatake", must: true, desc: "體驗海邊水上建築「舟屋」風情，搭乘觀光船餵海鷗", map: "Ine+Funaya" },
          { time: "18:30", title: "返回大阪市區", type: "交通", tagColor: "bg-mizuiro", desc: "專車返回日本橋 / 梅田解散" },
          { time: "19:30", title: "晚餐：炸牛排京都勝牛", type: "美食", tagColor: "bg-coral text-white", must: true, desc: "外酥內嫩金黃炸牛排，搭配多種沾醬 🥩", map: "Gyukatsu+Kyoto+Katsugyu+Osaka" }
        ]
      },
      4: {
        date: "2027.01.16 (六)",
        title: "Day 4 ‧ 淡路島 & 鳴門漩渦自然探索",
        badgeColor: "bg-coral",
        icon: "🌀",
        events: [
          { time: "08:00", title: "梅田集合出發", type: "集合", tagColor: "bg-sand", desc: "搭乘一日遊巴士跨越明石海峽大橋", map: "Osaka+Umeda+Station" },
          { time: "10:00 - 12:00", title: "淡路島景點體驗", type: "景點", tagColor: "bg-wakatake", desc: "漫步島上公園、品嚐美味洋蔥與神戶淡路海景", map: "Awaji+Island" },
          { time: "13:00 - 15:00", title: "鳴門漩渦觀光船", type: "必去景點", tagColor: "bg-coral text-white", must: true, desc: "近距離觀賞世界三大潮流之一的鳴門大漩渦 🌀", map: "Naruto+Whirlpools" },
          { time: "18:00", title: "返回梅田市區", type: "交通", tagColor: "bg-mizuiro", desc: "結束淡路島之旅返抵梅田" },
          { time: "19:00", title: "晚餐：炭燒富士鰻魚", type: "美食", tagColor: "bg-coral text-white", must: true, desc: "香氣四溢炭火蒲燒鰻魚飯 🍱", map: "Sumiyaki+Unagi+Fuji+Osaka" }
        ]
      },
      5: {
        date: "2027.01.17 (日)",
        title: "Day 5 ‧ 滿載而歸 關西機場返台",
        badgeColor: "bg-sand",
        icon: "🛫",
        events: [
          { time: "08:00", title: "辦理退房與整理最後行李", type: "住宿", tagColor: "bg-yamabuki", desc: "確認物品齊全，離開大阪龍仕柏飯店" },
          { time: "08:40 - 09:30", title: "前往關西國際機場 (KIX)", type: "交通", tagColor: "bg-mizuiro", desc: "搭乘 JR Haruka 或南海電鐵專車" },
          { time: "09:30 - 11:30", title: "機場 Check in & 免稅店採購", type: "購物", tagColor: "bg-wakatake", desc: "採買白色戀人、東京香蕉、Royce巧克力與最後免稅品", map: "Kansai+International+Airport" },
          { time: "11:30 - 13:50", title: "搭乘台灣虎航返抵台灣", type: "交通", tagColor: "bg-coral text-white", desc: "大阪關西 (KIX) ➔ 桃園機場 (TPE)" }
        ]
      }
    };

    // 切換日期 Tab
    function switchDay(dayNum) {
      document.querySelectorAll('.day-tab').forEach(tab => tab.classList.remove('active'));
      const activeTab = document.getElementById(`tab-d${dayNum}`);
      activeTab.classList.add('active');
      
      activeTab.classList.add('tab-bounce');
      setTimeout(() => activeTab.classList.remove('tab-bounce'), 300);

      const data = itineraryData[dayNum];

      document.getElementById('day-date-badge').innerText = data.date;
      document.getElementById('day-title').innerText = data.title;
      document.getElementById('day-svg').innerText = data.icon;
      document.getElementById('day-header').className = `${data.badgeColor} p-4 pb-border shadow-picture-book flex items-center justify-between transition-all`;

      const container = document.getElementById('timeline-container');
      container.innerHTML = '';

      data.events.forEach((item, index) => {
        const mustBadge = item.must ? `<span class="bg-coral text-white text-[10px] font-black px-1.5 py-0.5 rounded border border-ink ml-1 animate-pulse" contenteditable="true">必去</span>` : '';
        const navBtn = item.map ? `
          <a href="https://www.google.com/maps/search/?api=1&query=${item.map}" target="_blank" class="text-[10px] font-black bg-yamabuki px-2 py-0.5 rounded-md border border-ink shadow-picture-book-sm active:translate-y-0.5 flex items-center gap-1">
            <i class="fa-solid fa-location-dot text-coral"></i> 導航
          </a>
        ` : '';

        const html = `
          <div class="relative bg-paper p-4 pb-border-sm shadow-picture-book-sm space-y-1 transform transition-all hover:-translate-y-0.5">
            <div class="absolute -left-[27px] top-4 w-5 h-5 rounded-full bg-yamabuki border-2 border-ink flex items-center justify-center text-[10px] font-black">
              ${index + 1}
            </div>
            
            <div class="flex items-center justify-between gap-2">
              <span class="text-xs font-black text-ink/60" contenteditable="true"><i class="fa-regular fa-clock mr-1"></i>${item.time}</span>
              <div class="flex items-center gap-1.5">
                <span class="text-[10px] font-black ${item.tagColor} px-2 py-0.5 rounded-md border border-ink" contenteditable="true">${item.type}</span>
                ${navBtn}
              </div>
            </div>

            <h4 class="font-black text-base text-ink flex items-center" contenteditable="true">
              ${item.title} ${mustBadge}
            </h4>

            <p class="text-xs font-bold text-ink/70 leading-relaxed" contenteditable="true">${item.desc}</p>
          </div>
        `;
        container.insertAdjacentHTML('beforeend', html);
      });
    }

    // 3. 行李待辦清單 (LocalStorage 保存狀態)
    const carryOnItems = ["現金", "信用卡", "護照", "eSIM", "日幣", "頸枕", "行充", "耳機", "髮圈", "VSJ"];
    const checkedItems = [
      "衛生紙、卸妝巾/水、棉花棒",
      "搓澡巾、鯊魚夾、牙刷、毛巾",
      "隱眼用品、眼鏡、墨鏡",
      "保養品、化妝品、香水、防曬",
      "行李袋、購物袋、吹風機、圓梳",
      "衣服、睡衣、毛帽",
      "藥品、磨刀、充電線、手錶充電、飾品"
    ];

    let packingStatus = JSON.parse(localStorage.getItem('osaka_packing_status')) || {};

    function renderPackingList() {
      const carryContainer = document.getElementById('carryon-list');
      const checkedContainer = document.getElementById('checked-list');
      
      carryContainer.innerHTML = '';
      checkedContainer.innerHTML = '';

      let totalCount = carryOnItems.length + checkedItems.length;
      let checkedCount = 0;

      carryOnItems.forEach((item, idx) => {
        const key = `c_${idx}`;
        const isChecked = packingStatus[key] || false;
        if (isChecked) checkedCount++;

        carryContainer.insertAdjacentHTML('beforeend', `
          <label class="flex items-center gap-2 p-2 rounded-xl bg-sand/60 border border-ink/20 cursor-pointer">
            <input type="checkbox" class="custom-checkbox" onchange="togglePack('${key}')" ${isChecked ? 'checked' : ''}>
            <span class="${isChecked ? 'line-through opacity-50' : ''}" contenteditable="true">${item}</span>
          </label>
        `);
      });

      checkedItems.forEach((item, idx) => {
        const key = `k_${idx}`;
        const isChecked = packingStatus[key] || false;
        if (isChecked) checkedCount++;

        checkedContainer.insertAdjacentHTML('beforeend', `
          <label class="flex items-start gap-2 p-2 rounded-xl bg-sand/60 border border-ink/20 cursor-pointer">
            <input type="checkbox" class="custom-checkbox mt-0.5" onchange="togglePack('${key}')" ${isChecked ? 'checked' : ''}>
            <span class="${isChecked ? 'line-through opacity-50' : ''}" contenteditable="true">${item}</span>
          </label>
        `);
      });

      document.getElementById('packing-progress').innerText = `${checkedCount}/${totalCount} 完成`;
    }

    function togglePack(key) {
      packingStatus[key] = !packingStatus[key];
      localStorage.setItem('osaka_packing_status', JSON.stringify(packingStatus));
      renderPackingList();
    }

    // 4. 費用預算固定明細
    const budgetData = [
      { name: "機票 (台灣虎航)", cost: 13000, cat: "交通" },
      { name: "住宿 (大阪龍仕柏 4 晚)", cost: 8000, cat: "住宿" },
      { name: "預換日幣現金", cost: 5000, cat: "現金" },
      { name: "eSIM 上網卡", cost: 300, cat: "網卡" },
      { name: "機場接送 + 機捷", cost: 500, cat: "交通" },
      { name: "旅遊平安險", cost: 300, cat: "保險" },
      { name: "票券、行程套票", cost: 16184, cat: "票券" }
    ];

    function renderBudget() {
      const container = document.getElementById('budget-items');
      let total = 0;

      budgetData.forEach(item => {
        total += item.cost;
        container.insertAdjacentHTML('beforeend', `
          <div class="flex justify-between items-center p-2.5 rounded-xl bg-sand/40 border border-ink/20">
            <div class="flex items-center gap-2">
              <span class="text-[10px] bg-paper border border-ink px-1.5 py-0.5 rounded" contenteditable="true">${item.cat}</span>
              <span contenteditable="true">${item.name}</span>
            </div>
            <span class="font-black" contenteditable="true">NT$ ${item.cost.toLocaleString()}</span>
          </div>
        `);
      });

      document.getElementById('total-cost').innerText = `NT$ ${total.toLocaleString()}`;
    }

    // 5. 分帳記帳功能 (含每日總額與類別)
    let expenses = JSON.parse(localStorage.getItem('osaka_expenses')) || [
      { id: 1, date: "Day 1 (1/13)", cat: "🍜 餐飲美食", name: "鴨と葱拉麵", amount: 1200 },
      { id: 2, date: "Day 1 (1/13)", cat: "🍜 餐飲美食", name: "燒肉但馬屋", amount: 8500 },
      { id: 3, date: "Day 2 (1/14)", cat: "🎟️ 景點門票", name: "USJ 快速通關", amount: 15000 }
    ];

    function renderExpenses() {
      const listContainer = document.getElementById('expense-list');
      const dailyTotalsContainer = document.getElementById('daily-expense-totals');
      listContainer.innerHTML = '';
      dailyTotalsContainer.innerHTML = '';

      let dailySum = {
        "Day 1 (1/13)": 0,
        "Day 2 (1/14)": 0,
        "Day 3 (1/15)": 0,
        "Day 4 (1/16)": 0,
        "Day 5 (1/17)": 0
      };

      let grandTotal = 0;

      expenses.forEach((item) => {
        grandTotal += Number(item.amount);
        if (dailySum[item.date] !== undefined) {
          dailySum[item.date] += Number(item.amount);
        }

        listContainer.insertAdjacentHTML('beforeend', `
          <div class="flex items-center justify-between p-2.5 bg-sand/40 rounded-xl border border-ink/20">
            <div>
              <div class="flex items-center gap-1.5 text-[10px] text-ink/60 mb-0.5">
                <span class="bg-paper px-1.5 py-0.2 rounded border border-ink/30">${item.date}</span>
                <span>${item.cat}</span>
              </div>
              <p class="font-black text-sm text-ink">${item.name}</p>
            </div>
            <div class="flex items-center gap-2">
              <span class="font-black text-coral text-sm">$${Number(item.amount).toLocaleString()}</span>
              <button onclick="deleteExpense(${item.id})" class="text-ink/40 hover:text-coral p-1 cursor-pointer text-xs">
                <i class="fa-solid fa-trash-can"></i>
              </button>
            </div>
          </div>
        `);
      });

      // 渲染每日花費總額
      Object.keys(dailySum).forEach((dayKey) => {
        dailyTotalsContainer.insertAdjacentHTML('beforeend', `
          <div class="bg-paper p-2 rounded-xl border border-ink/30 flex justify-between items-center">
            <span class="text-ink/70">${dayKey}</span>
            <span class="text-coral">$${dailySum[dayKey].toLocaleString()}</span>
          </div>
        `);
      });

      document.getElementById('exp-grand-total').innerText = `總計: $${grandTotal.toLocaleString()}`;
    }

    function addExpense() {
      const date = document.getElementById('exp-date').value;
      const cat = document.getElementById('exp-cat').value;
      const name = document.getElementById('exp-name').value.trim();
      const amount = parseFloat(document.getElementById('exp-amount').value);

      if (!name || isNaN(amount) || amount <= 0) {
        alert('請輸入有效的消費名稱與金額！');
        return;
      }

      expenses.push({
        id: Date.now(),
        date,
        cat,
        name,
        amount
      });

      localStorage.setItem('osaka_expenses', JSON.stringify(expenses));
      document.getElementById('exp-name').value = '';
      document.getElementById('exp-amount').value = '';
      renderExpenses();
    }

    function deleteExpense(id) {
      expenses = expenses.filter(e => e.id !== id);
      localStorage.setItem('osaka_expenses', JSON.stringify(expenses));
      renderExpenses();
    }

    // 6. 採購清單功能
    let shoppingList = JSON.parse(localStorage.getItem('osaka_shopping')) || [
      { id: 1, name: "合利他命 EX Plus", checked: false },
      { id: 2, name: "SHISEIDO 護手霜", checked: true },
      { id: 3, name: "環球影城瑪利歐帽子", checked: false }
    ];

    function renderShopping() {
      const container = document.getElementById('shopping-list');
      container.innerHTML = '';

      let checkedCount = 0;

      shoppingList.forEach((item) => {
        if (item.checked) checkedCount++;

        container.insertAdjacentHTML('beforeend', `
          <div class="flex items-center justify-between p-2 rounded-xl bg-sand/60 border border-ink/20">
            <label class="flex items-center gap-2 flex-1 cursor-pointer">
              <input type="checkbox" class="custom-checkbox" onchange="toggleShopping(${item.id})" ${item.checked ? 'checked' : ''}>
              <span class="${item.checked ? 'line-through opacity-50' : ''}" contenteditable="true">${item.name}</span>
            </label>
            <button onclick="deleteShopping(${item.id})" class="text-ink/40 hover:text-coral p-1 cursor-pointer text-xs ml-2">
              <i class="fa-solid fa-xmark text-sm"></i>
            </button>
          </div>
        `);
      });

      document.getElementById('shop-progress').innerText = `${checkedCount}/${shoppingList.length} 完成`;
    }

    function addShoppingItem() {
      const input = document.getElementById('shop-input');
      const val = input.value.trim();
      if (!val) return;

      shoppingList.push({
        id: Date.now(),
        name: val,
        checked: false
      });

      localStorage.setItem('osaka_shopping', JSON.stringify(shoppingList));
      input.value = '';
      renderShopping();
    }

    function toggleShopping(id) {
      shoppingList = shoppingList.map(item => item.id === id ? { ...item, checked: !item.checked } : item);
      localStorage.setItem('osaka_shopping', JSON.stringify(shoppingList));
      renderShopping();
    }

    function deleteShopping(id) {
      shoppingList = shoppingList.filter(item => item.id !== id);
      localStorage.setItem('osaka_shopping', JSON.stringify(shoppingList));
      renderShopping();
    }

    // 初始化頁面
    window.onload = function() {
      switchDay(1);
      renderPackingList();
      renderBudget();
      renderExpenses();
      renderShopping();
    };
  </script>
</body>
</html>
