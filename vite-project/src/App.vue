<template>
  <!-- 网站主容器 - 柔和的渐变背景 -->
  <div class="min-h-screen bg-gradient-to-br from-slate-50 via-white to-blue-50/20">
    
    <!-- ===== 1. 专业导航栏 ===== -->
    <nav class="fixed top-0 w-full z-50 bg-white/90 backdrop-blur-md border-b border-slate-200/80 shadow-sm animate-fadeInDown">
      <div class="container mx-auto px-6">
        <div class="flex items-center justify-between h-20">
          <!-- Logo区域 - 品牌标识 -->
          <div class="flex items-center space-x-4 group cursor-pointer hover:scale-105 transition-transform duration-300">
            <div class="relative">
              <div class="w-12 h-12 rounded-xl bg-gradient-to-br from-blue-600 to-cyan-500 flex items-center justify-center shadow-lg overflow-hidden">
                <!-- 替换为图片图标 -->
                <img 
                  src="/logo.png" 
                  alt="镌纹留痕" 
                  class="w-8 h-8 object-contain"
                  onerror="this.style.display='none'; console.log('图标加载失败，请检查logo.png路径')"
                >
              </div>
              <div class="absolute inset-0 bg-gradient-to-br from-blue-600 to-cyan-500 rounded-xl blur-md opacity-0 group-hover:opacity-30 transition-opacity duration-300 -z-10"></div>
            </div>
            <div>
              <h1 class="text-2xl font-black text-slate-800 tracking-tight">镌纹留痕</h1>
              <p class="text-xs font-semibold text-cyan-600 mt-1">中国国际大学生创新大赛参赛项目</p>
            </div>
          </div>

          <!-- 桌面导航菜单 -->
          <div class="hidden lg:flex items-center space-x-8">
            <a v-for="item in navItems" 
               :key="item.id" 
               :href="item.link"
               class="nav-link text-sm font-semibold text-slate-700 hover:text-cyan-600 transition-all duration-300 relative group">
              <span class="relative z-10">{{ item.text }}</span>
              <span class="absolute bottom-0 left-0 w-0 h-0.5 bg-gradient-to-r from-blue-500 to-cyan-500 group-hover:w-full transition-all duration-300"></span>
            </a>
          </div>

          <!-- 主CTA按钮 -->
          <a href="#contact" class="hidden lg:inline-flex items-center px-6 py-3 bg-gradient-to-r from-blue-600 to-cyan-500 text-white font-semibold rounded-xl shadow-lg hover:shadow-xl transition-all duration-300 hover:-translate-y-0.5 hover:scale-105 transform-gpu animate-pulse-subtle">
            获取方案
            <svg class="w-4 h-4 ml-2 animate-bounce-x" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 7l5 5m0 0l-5 5m5-5H6"/>
            </svg>
          </a>

          <!-- 移动端菜单按钮 -->
          <button class="lg:hidden p-2 text-slate-700 hover:text-cyan-600 transition-colors duration-300">
            <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"/>
            </svg>
          </button>
        </div>
      </div>
    </nav>

    <!-- 主内容区域 -->
    <main class="pt-20">
      <!-- ===== 2. 主视觉区 ===== -->
      <section class="relative min-h-screen flex items-center justify-center py-20 md:py-32 overflow-hidden">
        <!-- 背景装饰 -->
        <div class="absolute inset-0 z-0">
          <div class="absolute top-0 right-0 w-96 h-96 bg-gradient-to-br from-cyan-500/10 to-blue-500/5 rounded-full blur-3xl"></div>
          <div class="absolute bottom-0 left-0 w-96 h-96 bg-gradient-to-br from-blue-900/5 to-cyan-500/5 rounded-full blur-3xl"></div>
        </div>

        <div class="container mx-auto px-6 relative z-10">
          <!-- 整体居中容器 -->
          <div class="flex flex-col items-center justify-center w-full">
            
            <!-- 大赛标识徽章 -->
            <div class="inline-flex items-center px-4 py-2 bg-cyan-100 text-cyan-800 rounded-full text-sm font-semibold mb-8 border border-cyan-200/50">
              <span class="w-2 h-2 bg-cyan-500 rounded-full mr-2 animate-pulse"></span>
              中国国际大学生创新大赛（2026）· 高教主赛道
            </div>
            
            <!-- 主标题 - 居中对齐 -->
            <div class="text-center max-w-5xl mx-auto">
              <h1 class="text-4xl md:text-6xl font-black text-slate-900 mb-6 leading-tight">
                镌纹留痕：
                <span class="block mt-4 text-transparent bg-clip-text bg-gradient-to-r from-blue-600 via-cyan-500 to-emerald-500">
                  陶瓷器立体纹饰三维数字化修复
                </span>
                <span class="block text-2xl md:text-3xl font-semibold text-slate-700 mt-4">
                  与再生应用
                </span>
              </h1>
            </div>
            
            <!-- 项目描述 - 居中对齐，限制宽度 -->
            <div class="max-w-3xl mx-auto text-center mt-8">
              <p class="text-lg md:text-xl text-slate-600 leading-relaxed">
                面向
                <span class="font-semibold text-amber-600 bg-amber-50 px-2 py-1 rounded-lg">基层文保单位</span>
                ，自主研发基于
                <span class="font-medium text-slate-800">"高精度逆向工程+特征映射算法+精密增材制造"</span>
                的标准化解决方案，将修复成本降低
                <span class="font-bold text-emerald-600">80%</span>
                ，周期缩短
                <span class="font-bold text-cyan-600">70%</span>
                ，让每一道历史刻痕在数字中获得新生。
              </p>
            </div>

            <!-- 行动按钮组 - 居中对齐 -->
            <div class="flex flex-col sm:flex-row gap-4 justify-center mt-12">
              <a href="#solution" class="inline-flex items-center justify-center px-8 py-4 bg-gradient-to-r from-blue-600 to-cyan-500 text-white font-semibold rounded-xl shadow-lg hover:shadow-xl transition-all duration-300 hover:-translate-y-1">
                <svg class="w-5 h-5 mr-3" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9.663 17h4.673M12 3v1m6.364 1.636l-.707.707M21 12h-1M4 12H3m3.343-5.657l-.707-.707m2.828 9.9a5 5 0 117.072 0l-.548.547A3.374 3.374 0 0014 18.469V19a2 2 0 11-4 0v-.531c0-.895-.356-1.754-.988-2.386l-.548-.547z"/>
                </svg>
                查看技术方案
              </a>
              <a href="#contact" class="inline-flex items-center justify-center px-8 py-4 bg-white text-slate-800 font-semibold rounded-xl border-2 border-slate-300 hover:border-cyan-500 transition-all duration-300">
                获取完整计划书
              </a>
            </div>

            <!-- 核心数据展示 - 四等分，居中对齐 -->
            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6 max-w-6xl mx-auto mt-20">
              <!-- 数据卡片1 -->
              <div class="bg-white rounded-2xl p-8 shadow-xl border border-slate-100 text-center">
                <div class="text-5xl font-black text-emerald-500 mb-4">93%</div>
                <h3 class="text-xl font-bold text-slate-900 mb-3">基层单位急需</h3>
                <p class="text-slate-600 mb-4">山西省30家县级博物馆调研数据</p>
                <div class="text-sm text-slate-500">支付意愿 2,000-4,500元/件</div>
              </div>
              
              <!-- 数据卡片2 -->
              <div class="bg-white rounded-2xl p-8 shadow-xl border border-slate-100 text-center">
                <div class="text-5xl font-black text-cyan-500 mb-4">&gt; 80%</div>
                <h3 class="text-xl font-bold text-slate-900 mb-3">成本降低</h3>
                <p class="text-slate-600 mb-4">相比传统修复工艺</p>
                <div class="text-sm text-slate-500">单件直接材料成本 &lt; 500元</div>
              </div>
              
              <!-- 数据卡片3 -->
              <div class="bg-white rounded-2xl p-8 shadow-xl border border-slate-100 text-center">
                <div class="text-5xl font-black text-blue-500 mb-4">&gt; 70%</div>
                <h3 class="text-xl font-bold text-slate-900 mb-3">周期缩短</h3>
                <p class="text-slate-600 mb-4">复杂纹饰修复效率</p>
                <div class="text-sm text-slate-500">从15-30天缩短至5-10天</div>
              </div>
              
              <!-- 数据卡片4 -->
              <div class="bg-white rounded-2xl p-8 shadow-xl border border-slate-100 text-center">
                <div class="text-5xl font-black text-amber-500 mb-4">150万元</div>
                <h3 class="text-xl font-bold text-slate-900 mb-3">年市场规模</h3>
                <p class="text-slate-600 mb-4">仅山西省基层文保市场</p>
                <div class="text-sm text-slate-500">年度潜在服务量 500+件</div>
              </div>
            </div>
          </div>
        </div>
      </section>
      <!-- ===== 3. 项目概述 ===== -->
      <section id="project" class="py-20 bg-white animate-fadeIn">
        <div class="container mx-auto px-6">
          <div class="text-center mb-16">
            <h2 class="text-4xl md:text-5xl font-black text-slate-900 mb-6 animate-slideInUp">项目概述</h2>
            <p class="text-lg text-slate-600 max-w-2xl mx-auto animate-slideInUp delay-200">用数字科技解决文保修复"卡脖子"难题，让文化遗产在新时代焕发新生</p>
          </div>

          <div class="grid lg:grid-cols-2 gap-12">
            <!-- 左侧：核心信息 -->
            <div class="space-y-8">
              <!-- 参赛信息卡片 -->
              <div class="bg-gradient-to-br from-slate-50 to-white rounded-2xl p-8 shadow-lg border border-slate-200 hover:shadow-xl transition-all duration-500 animate-slideInLeft">
                <h3 class="text-2xl font-bold text-slate-900 mb-6 flex items-center">
                  <svg class="w-6 h-6 text-cyan-600 mr-3 animate-pulse" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z"/>
                  </svg>
                  参赛信息
                </h3>
                <div class="grid grid-cols-2 gap-6">
                  <div class="hover:scale-105 transition-transform duration-300">
                    <p class="text-sm text-slate-600 mb-2">参赛赛道</p>
                    <p class="font-semibold text-slate-900 text-lg">高教主赛道</p>
                  </div>
                  <div class="hover:scale-105 transition-transform duration-300">
                    <p class="text-sm text-slate-600 mb-2">参赛组别</p>
                    <p class="font-semibold text-slate-900 text-lg">本科生创意组</p>
                  </div>
                  <div class="hover:scale-105 transition-transform duration-300">
                    <p class="text-sm text-slate-600 mb-2">项目负责人</p>
                    <p class="font-semibold text-slate-900 text-lg">杨天宇</p>
                  </div>
                  <div class="hover:scale-105 transition-transform duration-300">
                    <p class="text-sm text-slate-600 mb-2">指导教师</p>
                    <p class="font-semibold text-slate-900 text-lg">常小燕 韩姣姣</p>
                  </div>
                </div>
              </div>

              <!-- 痛点分析 -->
              <div class="animate-slideInLeft delay-300">
                <h3 class="text-2xl font-bold text-slate-900 mb-6 flex items-center">
                  <svg class="w-6 h-6 text-amber-600 mr-3 animate-bounce" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 9v2m0 4h.01m-6.938 4h13.856c1.54 0 2.502-1.667 1.732-2.5L13.732 4c-.77-.833-1.998-.833-2.732 0L4.232 16.5c-.77.833.192 2.5 1.732 2.5z"/>
                  </svg>
                  行业痛点
                </h3>
                <div class="bg-amber-50 border-l-4 border-amber-500 pl-6 py-4 rounded-r-lg hover:shadow-md transition-all duration-300">
                  <p class="text-slate-700 leading-relaxed">
                    山西省晋南地区宋金元陶瓷文物存量丰富，立体纹饰极具价值。然而，传统"石膏补配+手工仿刻"方法周期长达15-30天，成本高昂（3000-8000元/件），导致42.1%的馆藏文物"沉睡"。
                  </p>
                </div>
              </div>

              <!-- 时代机遇 -->
              <div class="animate-slideInLeft delay-400">
                <h3 class="text-2xl font-bold text-slate-900 mb-6 flex items-center">
                  <svg class="w-6 h-6 text-emerald-600 mr-3 animate-spin-slow" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"/>
                  </svg>
                  时代机遇
                </h3>
                <div class="bg-emerald-50 border-l-4 border-emerald-500 pl-6 py-4 rounded-r-lg hover:shadow-md transition-all duration-300">
                  <p class="text-slate-700 leading-relaxed">
                    桌面级高精度3D打印技术成熟，成本大幅降低。国家"新文科"建设战略鼓励科技与人文深度融合，本项目恰逢其时，旨在用数字技术解决文保修复"卡脖子"难题。
                  </p>
                </div>
              </div>
            </div>

            <!-- 右侧：项目意义 -->
            <div class="animate-slideInRight">
              <div class="bg-gradient-to-br from-cyan-50 to-blue-50 rounded-2xl p-8 shadow-lg border border-cyan-200 hover:shadow-xl transition-all duration-500">
                <h3 class="text-2xl font-bold text-slate-900 mb-8 text-center animate-pulse">项目意义</h3>
                
                <div class="space-y-8">
                  <!-- 价值1 -->
                  <div class="flex items-start group hover:bg-white/50 p-4 rounded-xl transition-all duration-300 hover:scale-105 transform-gpu">
                    <div class="w-12 h-12 rounded-xl bg-blue-100 flex items-center justify-center mr-5 flex-shrink-0 group-hover:scale-110 transition-transform duration-300 animate-bounce-subtle">
                      <svg class="w-6 h-6 text-blue-600" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"/>
                      </svg>
                    </div>
                    <div>
                      <h4 class="text-xl font-semibold text-slate-900 mb-2 group-hover:text-blue-600 transition-colors duration-300">行业革新价值</h4>
                      <p class="text-slate-600 group-hover:text-slate-800 transition-colors duration-300">提供低成本、标准化方案，推动行业从"经验驱动"向"数据与工艺驱动"转型</p>
                    </div>
                  </div>
                  
                  <!-- 价值2 -->
                  <div class="flex items-start group hover:bg-white/50 p-4 rounded-xl transition-all duration-300 hover:scale-105 transform-gpu delay-100">
                    <div class="w-12 h-12 rounded-xl bg-emerald-100 flex items-center justify-center mr-5 flex-shrink-0 group-hover:scale-110 transition-transform duration-300 animate-bounce-subtle" style="animation-delay: 0.1s;">
                      <svg class="w-6 h-6 text-emerald-600" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 11H5m14 0a2 2 0 012 2v6a2 2 0 01-2 2H5a2 2 0 01-2-2v-6a2 2 0 012-2m14 0V9a2 2 0 00-2-2M5 11V9a2 2 0 012-2m0 0V5a2 2 0 012-2h6a2 2 0 012 2v2M7 7h10"/>
                      </svg>
                    </div>
                    <div>
                      <h4 class="text-xl font-semibold text-slate-900 mb-2 group-hover:text-emerald-600 transition-colors duration-300">社会文化价值</h4>
                      <p class="text-slate-600 group-hover:text-slate-800 transition-colors duration-300">让残损文物科学"再生"，助力历史研究与公共教育，传承三晋文明，坚定文化自信</p>
                    </div>
                  </div>
                  
                  <!-- 价值3 -->
                  <div class="flex items-start group hover:bg-white/50 p-4 rounded-xl transition-all duration-300 hover:scale-105 transform-gpu delay-200">
                    <div class="w-12 h-12 rounded-xl bg-cyan-100 flex items-center justify-center mr-5 flex-shrink-0 group-hover:scale-110 transition-transform duration-300 animate-bounce-subtle" style="animation-delay: 0.2s;">
                      <svg class="w-6 h-6 text-cyan-600" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 14l9-5-9-5-9 5 9 5z"/>
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 14l6.16-3.422a12.083 12.083 0 01.665 6.479A11.952 11.952 0 0012 20.055a11.952 11.952 0 00-6.824-2.998 12.078 12.078 0 01.665-6.479L12 14z"/>
                      </svg>
                    </div>
                    <div>
                      <h4 class="text-xl font-semibold text-slate-900 mb-2 group-hover:text-cyan-600 transition-colors duration-300">教育教学价值</h4>
                      <p class="text-slate-600 group-hover:text-slate-800 transition-colors duration-300">深度践行"新工科"与"新文科"交叉融合，培养学生解决复杂社会问题的创新与实践能力</p>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- ===== 4. 市场分析 ===== -->
      <section id="market" class="py-20 bg-gradient-to-br from-slate-50 to-blue-50/30 animate-fadeIn">
        <div class="container mx-auto px-6">
          <!-- 模块标题 -->
          <div class="text-center mb-16">
            <h2 class="text-4xl md:text-5xl font-black text-slate-900 mb-6 animate-slideInUp">市场分析</h2>
            <p class="text-lg text-slate-600 max-w-2xl mx-auto animate-slideInUp delay-200">深入调研山西省基层文保市场，发现数字化修复的巨大潜力与空白</p>
          </div>

          <div class="grid lg:grid-cols-2 gap-12">
            <!-- 左侧：市场需求分析 -->
            <div>
              <div class="bg-white rounded-2xl p-8 shadow-lg border border-slate-200 mb-8 hover:shadow-xl transition-all duration-500 animate-slideInLeft">
                <h3 class="text-2xl font-bold text-slate-900 mb-6 flex items-center">
                  <svg class="w-6 h-6 text-blue-600 mr-3 animate-pulse" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 19v-6a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2a2 2 0 002-2zm0 0V9a2 2 0 012-2h2a2 2 0 012 2v10m-6 0a2 2 0 002 2h2a2 2 0 002-2m0 0V5a2 2 0 012-2h2a2 2 0 012 2v14a2 2 0 01-2 2h-2a2 2 0 01-2-2z"/>
                  </svg>
                  市场需求与规模
                </h3>
                
                <div class="space-y-6">
                  <div>
                    <h4 class="text-lg font-semibold text-slate-900 mb-3">调研方法与样本</h4>
                    <p class="text-slate-600 mb-4">
                      采用"线上问卷+深度访谈"对山西省内30家县级博物馆定向调研，依据《山西省博物馆名录》选择不同地市、不同藏品规模的单位。
                    </p>
                  </div>
                  
                  <!-- 核心数据网格 -->
                  <div class="grid grid-cols-2 gap-4">
                    <div class="bg-blue-50 rounded-xl p-4 text-center hover:scale-105 transition-transform duration-300 animate-slideInUp delay-100">
                      <div class="text-2xl font-black text-blue-600 mb-1 animate-count" data-target="93">93%</div>
                      <p class="text-sm text-slate-700">单位亟需但难以承担</p>
                    </div>
                    <div class="bg-cyan-50 rounded-xl p-4 text-center hover:scale-105 transition-transform duration-300 animate-slideInUp delay-200">
                      <div class="text-2xl font-black text-cyan-600 mb-1 animate-count" data-target="5">5</div>
                      <p class="text-sm text-slate-700">年均需修复数量</p>
                    </div>
                    <div class="bg-emerald-50 rounded-xl p-4 text-center hover:scale-105 transition-transform duration-300 animate-slideInUp delay-300">
                      <div class="text-2xl font-black text-emerald-600 mb-1 animate-count" data-target="3">3</div>
                      <p class="text-sm text-slate-700">年度修复预算中位数</p>
                    </div>
                    <div class="bg-amber-50 rounded-xl p-4 text-center hover:scale-105 transition-transform duration-300 animate-slideInUp delay-400">
                      <div class="text-2xl font-black text-amber-600 mb-1 animate-count" data-target="150">150</div>
                      <p class="text-sm text-slate-700">年直接服务市场规模</p>
                    </div>
                  </div>
                  
                  <div>
                    <h4 class="text-lg font-semibold text-slate-900 mb-3">市场测算</h4>
                    <p class="text-slate-600">
                      山西省内市、县级文保单位超100家，每家年均需修复5件，年潜在服务量超500件。以市场可接受的3000元/件单价估算，年度直接服务市场规模约150万元。
                    </p>
                  </div>
                </div>
              </div>
              
              <!-- 需求金字塔 -->
              <div class="bg-white rounded-2xl p-8 shadow-lg border border-slate-200 hover:shadow-xl transition-all duration-500 animate-slideInLeft delay-300">
                <h4 class="text-lg font-semibold text-slate-900 mb-4">基层单位核心需求</h4>
                <div class="space-y-3">
                  <div class="flex items-center hover:translate-x-2 transition-transform duration-300">
                    <div class="w-3 h-3 bg-blue-500 rounded-full mr-3 animate-pulse"></div>
                    <span class="text-slate-700">低成本（单件预算 ≤ 5000元）</span>
                  </div>
                  <div class="flex items-center hover:translate-x-2 transition-transform duration-300 delay-100">
                    <div class="w-3 h-3 bg-cyan-500 rounded-full mr-3 animate-pulse" style="animation-delay: 0.1s;"></div>
                    <span class="text-slate-700">短周期（15天内完成）</span>
                  </div>
                  <div class="flex items-center hover:translate-x-2 transition-transform duration-300 delay-200">
                    <div class="w-3 h-3 bg-emerald-500 rounded-full mr-3 animate-pulse" style="animation-delay: 0.2s;"></div>
                    <span class="text-slate-700">可追溯（修复过程透明）</span>
                  </div>
                  <div class="flex items-center hover:translate-x-2 transition-transform duration-300 delay-300">
                    <div class="w-3 h-3 bg-amber-500 rounded-full mr-3 animate-pulse" style="animation-delay: 0.3s;"></div>
                    <span class="text-slate-700">易操作（培训后即可上手）</span>
                  </div>
                </div>
              </div>
            </div>

            <!-- 右侧：竞争分析 -->
            <div>
              <div class="bg-white rounded-2xl p-8 shadow-lg border border-slate-200 mb-8 hover:shadow-xl transition-all duration-500 animate-slideInRight">
                <h3 class="text-2xl font-bold text-slate-900 mb-6 flex items-center">
                  <svg class="w-6 h-6 text-amber-600 mr-3 animate-bounce" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"/>
                  </svg>
                  竞争格局分析
                </h3>
                
                <!-- 传统修复 -->
                <div class="mb-6 pb-6 border-b border-slate-200">
                  <h4 class="text-lg font-semibold text-slate-900 mb-3">传统手工修复</h4>
                  <div class="flex items-start text-slate-600 mb-2 hover:text-red-500 transition-colors duration-300">
                    <svg class="w-5 h-5 text-red-500 mr-2 mt-0.5 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20">
                      <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zM8.707 7.293a1 1 0 00-1.414 1.414L8.586 10l-1.293 1.293a1 1 0 101.414 1.414L10 11.414l1.293 1.293a1 1 0 001.414-1.414L11.414 10l1.293-1.293a1 1 0 00-1.414-1.414L10 8.586 8.707 7.293z" clip-rule="evenodd"/>
                    </svg>
                    <span>质量高但产能有限，依赖资深技师</span>
                  </div>
                  <div class="flex items-start text-slate-600 mb-2 hover:text-red-500 transition-colors duration-300">
                    <svg class="w-5 h-5 text-red-500 mr-2 mt-0.5 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20">
                      <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zM8.707 7.293a1 1 0 00-1.414 1.414L8.586 10l-1.293 1.293a1 1 0 101.414 1.414L10 11.414l1.293 1.293a1 1 0 001.414-1.414L11.414 10l1.293-1.293a1 1 0 00-1.414-1.414L10 8.586 8.707 7.293z" clip-rule="evenodd"/>
                    </svg>
                    <span>成本高昂（3000-8000元/件）</span>
                  </div>
                  <div class="flex items-start text-slate-600 hover:text-red-500 transition-colors duration-300">
                    <svg class="w-5 h-5 text-red-500 mr-2 mt-0.5 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20">
                      <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zM8.707 7.293a1 1 0 00-1.414 1.414L8.586 10l-1.293 1.293a1 1 0 101.414 1.414L10 11.414l1.293 1.293a1 1 0 001.414-1.414L11.414 10l1.293-1.293a1 1 0 00-1.414-1.414L10 8.586 8.707 7.293z" clip-rule="evenodd"/>
                    </svg>
                    <span>周期长（15-30天），人才断代严重</span>
                  </div>
                </div>
                
                <!-- 高端数字化修复 -->
                <div class="mb-6">
                  <h4 class="text-lg font-semibold text-slate-900 mb-3">高端商业数字化修复</h4>
                  <div class="flex items-start text-slate-600 mb-2 hover:text-yellow-500 transition-colors duration-300">
                    <svg class="w-5 h-5 text-yellow-500 mr-2 mt-0.5 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20">
                      <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zM7 9a1 1 0 000 2h6a1 1 0 100-2H7z" clip-rule="evenodd"/>
                    </svg>
                    <span>技术先进但价格昂贵（数万元/件）</span>
                  </div>
                  <div class="flex items-start text-slate-600 hover:text-yellow-500 transition-colors duration-300">
                    <svg class="w-5 h-5 text-yellow-500 mr-2 mt-0.5 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20">
                      <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zM7 9a1 1 0 000 2h6a1 1 0 100-2H7z" clip-rule="evenodd"/>
                    </svg>
                    <span>不服务基层文保单位单件需求</span>
                  </div>
                </div>
                
                <!-- 我们的定位 -->
                <div class="bg-gradient-to-r from-blue-50 to-cyan-50 rounded-xl p-6 border border-blue-200 hover:shadow-lg transition-all duration-300 animate-pulse-subtle">
                  <h4 class="text-lg font-semibold text-slate-900 mb-3">我们的定位</h4>
                  <p class="text-slate-700 leading-relaxed">
                    专注"基层赋能"，提供介于两者之间的高性价比整体解决方案（技术+工具+培训），填补市场空白，解决基层文保单位"修不起、等不及"的痛点。
                  </p>
                </div>
              </div>
              
              <!-- 市场趋势 -->
              <div class="bg-gradient-to-br from-blue-900/5 to-cyan-900/5 rounded-2xl p-8 border border-blue-200/50 hover:shadow-lg transition-all duration-500 animate-slideInRight delay-300">
                <h4 class="text-lg font-semibold text-slate-900 mb-4">政策与市场趋势</h4>
                <div class="space-y-3">
                  <div class="flex items-start hover:translate-x-2 transition-transform duration-300">
                    <svg class="w-5 h-5 text-emerald-500 mr-3 mt-0.5 flex-shrink-0 animate-pulse" fill="currentColor" viewBox="0 0 20 20">
                      <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"/>
                    </svg>
                    <span class="text-slate-700">国家"新文科"建设推动科技与人文融合</span>
                  </div>
                  <div class="flex items-start hover:translate-x-2 transition-transform duration-300 delay-100">
                    <svg class="w-5 h-5 text-emerald-500 mr-3 mt-0.5 flex-shrink-0 animate-pulse" style="animation-delay: 0.1s;" fill="currentColor" viewBox="0 0 20 20">
                      <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"/>
                    </svg>
                    <span class="text-slate-700">3D打印等数字化技术成本大幅降低</span>
                  </div>
                  <div class="flex items-start hover:translate-x-2 transition-transform duration-300 delay-200">
                    <svg class="w-5 h-5 text-emerald-500 mr-3 mt-0.5 flex-shrink-0 animate-pulse" style="animation-delay: 0.2s;" fill="currentColor" viewBox="0 0 20 20">
                      <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"/>
                    </svg>
                    <span class="text-slate-700">基层文保数字化需求进入爆发前夜</span>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- ===== 5. 解决方案 ===== -->
      <section id="solution" class="py-20 bg-white animate-fadeIn">
        <div class="container mx-auto px-6">
          <div class="text-center mb-16">
            <h2 class="text-4xl md:text-5xl font-black text-slate-900 mb-6 animate-slideInUp">解决方案</h2>
            <p class="text-lg text-slate-600 max-w-2xl mx-auto animate-slideInUp delay-200">"高精度逆向工程+特征映射算法+精密增材制造"三位一体的标准化修复方案</p>
          </div>

          <!-- 三步骤流程 -->
          <div class="grid lg:grid-cols-3 gap-8 mb-16">
            <!-- 步骤1 -->
            <div class="relative group animate-slideInLeft delay-100">
              <div class="bg-gradient-to-br from-blue-50 to-white rounded-2xl p-8 shadow-lg border border-slate-200 h-full hover:shadow-xl transition-all duration-500 group-hover:-translate-y-2">
                <div class="absolute -top-4 -left-4 w-12 h-12 rounded-xl bg-gradient-to-br from-blue-600 to-cyan-500 flex items-center justify-center text-white font-black text-xl shadow-lg animate-bounce-subtle">
                  1
                </div>
                <h3 class="text-2xl font-bold text-slate-900 mb-4 mt-4 group-hover:text-blue-600 transition-colors duration-300">三维数字特征库</h3>
                <p class="text-slate-600 mb-6 group-hover:text-slate-800 transition-colors duration-300">系统化提取并参数化建模晋南地区典型陶瓷纹饰单元，建立标准化数字特征库</p>
                <ul class="space-y-2 text-slate-600 text-sm">
                  <li class="flex items-start hover:translate-x-2 transition-transform duration-300">
                    <svg class="w-4 h-4 text-blue-500 mr-2 mt-0.5 flex-shrink-0 animate-pulse" fill="currentColor" viewBox="0 0 20 20">
                      <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"/>
                    </svg>
                    <span>宋金元时期典型纹饰收录</span>
                  </li>
                  <li class="flex items-start hover:translate-x-2 transition-transform duration-300 delay-100">
                    <svg class="w-4 h-4 text-blue-500 mr-2 mt-0.5 flex-shrink-0 animate-pulse" style="animation-delay: 0.1s;" fill="currentColor" viewBox="0 0 20 20">
                      <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"/>
                    </svg>
                    <span>参数化建模，支持灵活调整</span>
                  </li>
                  <li class="flex items-start hover:translate-x-2 transition-transform duration-300 delay-200">
                    <svg class="w-4 h-4 text-blue-500 mr-2 mt-0.5 flex-shrink-0 animate-pulse" style="animation-delay: 0.2s;" fill="currentColor" viewBox="0 0 20 20">
                      <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"/>
                    </svg>
                    <span>为AI辅助修复提供数据基础</span>
                  </li>
                </ul>
              </div>
            </div>
            
            <!-- 步骤2 -->
            <div class="relative group animate-slideInUp delay-200">
              <div class="bg-gradient-to-br from-cyan-50 to-white rounded-2xl p-8 shadow-lg border border-slate-200 h-full hover:shadow-xl transition-all duration-500 group-hover:-translate-y-2">
                <div class="absolute -top-4 -left-4 w-12 h-12 rounded-xl bg-gradient-to-br from-cyan-500 to-emerald-500 flex items-center justify-center text-white font-black text-xl shadow-lg animate-bounce-subtle" style="animation-delay: 0.1s;">
                  2
                </div>
                <h3 class="text-2xl font-bold text-slate-900 mb-4 mt-4 group-hover:text-cyan-600 transition-colors duration-300">标准化修复指南</h3>
                <p class="text-slate-600 mb-6 group-hover:text-slate-800 transition-colors duration-300">涵盖扫描、建模、打印、做旧的全流程操作规范(SOP V1.0)，确保修复质量一致性</p>
                <ul class="space-y-2 text-slate-600 text-sm">
                  <li class="flex items-start hover:translate-x-2 transition-transform duration-300">
                    <svg class="w-4 h-4 text-cyan-500 mr-2 mt-0.5 flex-shrink-0 animate-pulse" fill="currentColor" viewBox="0 0 20 20">
                      <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"/>
                    </svg>
                    <span>9大步骤，38个操作节点</span>
                  </li>
                  <li class="flex items-start hover:translate-x-2 transition-transform duration-300 delay-100">
                    <svg class="w-4 h-4 text-cyan-500 mr-2 mt-0.5 flex-shrink-0 animate-pulse" style="animation-delay: 0.1s;" fill="currentColor" viewBox="0 0 20 20">
                      <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"/>
                    </svg>
                    <span>详细的质量控制标准</span>
                  </li>
                  <li class="flex items-start hover:translate-x-2 transition-transform duration-300 delay-200">
                    <svg class="w-4 h-4 text-cyan-500 mr-2 mt-0.5 flex-shrink-0 animate-pulse" style="animation-delay: 0.2s;" fill="currentColor" viewBox="0 0 20 20">
                      <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"/>
                    </svg>
                    <span>培训后普通技术人员可操作</span>
                  </li>
                </ul>
              </div>
            </div>
            
            <!-- 步骤3 -->
            <div class="relative group animate-slideInRight delay-300">
              <div class="bg-gradient-to-br from-emerald-50 to-white rounded-2xl p-8 shadow-lg border border-slate-200 h-full hover:shadow-xl transition-all duration-500 group-hover:-translate-y-2">
                <div class="absolute -top-4 -left-4 w-12 h-12 rounded-xl bg-gradient-to-br from-emerald-500 to-amber-500 flex items-center justify-center text-white font-black text-xl shadow-lg animate-bounce-subtle" style="animation-delay: 0.2s;">
                  3
                </div>
                <h3 class="text-2xl font-bold text-slate-900 mb-4 mt-4 group-hover:text-emerald-600 transition-colors duration-300">专用耗材参数包</h3>
                <p class="text-slate-600 mb-6 group-hover:text-slate-800 transition-colors duration-300">优化的3D打印与后处理工艺方案，确保修复部件与原文物完美匹配</p>
                <ul class="space-y-2 text-slate-600 text-sm">
                  <li class="flex items-start hover:translate-x-2 transition-transform duration-300">
                    <svg class="w-4 h-4 text-emerald-500 mr-2 mt-0.5 flex-shrink-0 animate-pulse" fill="currentColor" viewBox="0 0 20 20">
                      <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"/>
                    </svg>
                    <span>文保专用树脂材料配方</span>
                  </li>
                  <li class="flex items-start hover:translate-x-2 transition-transform duration-300 delay-100">
                    <svg class="w-4 h-4 text-emerald-500 mr-2 mt-0.5 flex-shrink-0 animate-pulse" style="animation-delay: 0.1s;" fill="currentColor" viewBox="0 0 20 20">
                      <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"/>
                    </svg>
                    <span>色彩、质感、重量匹配方案</span>
                  </li>
                  <li class="flex items-start hover:translate-x-2 transition-transform duration-300 delay-200">
                    <svg class="w-4 h-4 text-emerald-500 mr-2 mt-0.5 flex-shrink-0 animate-pulse" style="animation-delay: 0.2s;" fill="currentColor" viewBox="0 0 20 20">
                      <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"/>
                    </svg>
                    <span>耐候性、稳定性测试数据</span>
                  </li>
                </ul>
              </div>
            </div>
          </div>

          <!-- 核心技术路径 -->
          <div class="bg-gradient-to-r from-slate-50 to-blue-50 rounded-2xl p-8 border border-slate-200 hover:shadow-lg transition-all duration-500 animate-slideInUp delay-400">
            <h3 class="text-2xl font-bold text-slate-900 mb-6 text-center">核心技术路径</h3>
            <div class="max-w-3xl mx-auto">
              <p class="text-slate-700 leading-relaxed text-center">
                采用"逆向工程+特征映射"的稳健科学策略，包括轴对称镜像复制、连续纹样特征阵列、复杂破损曲面融合，杜绝"AI黑箱"，确保复原过程可追溯、可调整，数字模型精度偏差 &lt; 0.2mm。
              </p>
            </div>
          </div>
        </div>
      </section>

      <!-- ===== 6. 商业模式 ===== -->
      <section id="business" class="py-20 bg-gradient-to-br from-blue-50/30 to-slate-50 animate-fadeIn">
        <div class="container mx-auto px-6">
          <div class="text-center mb-16">
            <h2 class="text-4xl md:text-5xl font-black text-slate-900 mb-6 animate-slideInUp">商业模式</h2>
            <p class="text-lg text-slate-600 max-w-2xl mx-auto animate-slideInUp delay-200">构建"技术服务+产品销售+培训授权"三位一体的多元化收入模式</p>
          </div>

          <!-- 三种收入模式 -->
          <div class="grid lg:grid-cols-3 gap-8 mb-16">
            <!-- 模式1 -->
            <div class="bg-white rounded-2xl p-8 shadow-lg border border-slate-200 text-center hover:shadow-xl transition-all duration-500 hover:-translate-y-2 animate-slideInLeft delay-100">
              <div class="w-16 h-16 rounded-2xl bg-gradient-to-br from-blue-600 to-cyan-500 flex items-center justify-center mx-auto mb-6 animate-rotate-in">
                <svg class="w-8 h-8 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z"/>
                </svg>
              </div>
              <h3 class="text-2xl font-bold text-slate-900 mb-4 group-hover:text-blue-600 transition-colors duration-300">技术服务</h3>
              <p class="text-slate-600 mb-6 group-hover:text-slate-800 transition-colors duration-300">提供"交钥匙"数字化修复整体解决方案</p>
              <div class="bg-blue-50 rounded-xl p-4 hover:scale-105 transition-transform duration-300">
                <div class="text-3xl font-black text-blue-600 animate-count" data-target="3000">3000</div>
                <p class="text-sm text-slate-600">标准服务价格</p>
              </div>
            </div>
            
            <!-- 模式2 -->
            <div class="bg-white rounded-2xl p-8 shadow-lg border border-slate-200 text-center hover:shadow-xl transition-all duration-500 hover:-translate-y-2 animate-slideInUp delay-200">
              <div class="w-16 h-16 rounded-2xl bg-gradient-to-br from-cyan-500 to-emerald-500 flex items-center justify-center mx-auto mb-6 animate-rotate-in" style="animation-delay: 0.1s;">
                <svg class="w-8 h-8 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M20 7l-8-4-8 4m16 0l-8 4m8-4v10l-8 4m0-10L4 7m8 4v10M4 7v10l8 4"/>
                </svg>
              </div>
              <h3 class="text-2xl font-bold text-slate-900 mb-4 group-hover:text-cyan-600 transition-colors duration-300">产品销售</h3>
              <p class="text-slate-600 mb-6 group-hover:text-slate-800 transition-colors duration-300">销售定制化的"高精度树脂修复部件"</p>
              <div class="bg-cyan-50 rounded-xl p-4 hover:scale-105 transition-transform duration-300">
                <div class="text-3xl font-black text-cyan-600 animate-count" data-target="800">800</div>
                <p class="text-sm text-slate-600">标准部件价格</p>
              </div>
            </div>
            
            <!-- 模式3 -->
            <div class="bg-white rounded-2xl p-8 shadow-lg border border-slate-200 text-center hover:shadow-xl transition-all duration-500 hover:-translate-y-2 animate-slideInRight delay-300">
              <div class="w-16 h-16 rounded-2xl bg-gradient-to-br from-emerald-500 to-amber-500 flex items-center justify-center mx-auto mb-6 animate-rotate-in" style="animation-delay: 0.2s;">
                <svg class="w-8 h-8 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 6.253v13m0-13C10.832 5.477 9.246 5 7.5 5S4.168 5.477 3 6.253v13C4.168 18.477 5.754 18 7.5 18s3.332.477 4.5 1.253m0-13C13.168 5.477 14.754 5 16.5 5c1.747 0 3.332.477 4.5 1.253v13C19.832 18.477 18.247 18 16.5 18c-1.746 0-3.332.477-4.5 1.253"/>
                </svg>
              </div>
              <h3 class="text-2xl font-bold text-slate-900 mb-4 group-hover:text-emerald-600 transition-colors duration-300">培训授权</h3>
              <p class="text-slate-600 mb-6 group-hover:text-slate-800 transition-colors duration-300">提供标准化流程技术培训与授权</p>
              <div class="bg-emerald-50 rounded-xl p-4 hover:scale-105 transition-transform duration-300">
                <div class="text-3xl font-black text-emerald-600 animate-count" data-target="10000">10000</div>
                <p class="text-sm text-slate-600">标准培训价格</p>
              </div>
            </div>
          </div>

          <!-- 价值对比表 -->
          <div class="bg-white rounded-2xl shadow-lg overflow-hidden hover:shadow-2xl transition-all duration-500 animate-slideInUp delay-400">
            <h3 class="text-2xl font-bold text-slate-900 mb-8 p-8 pb-0 text-center">价值主张对比</h3>
            <div class="overflow-x-auto">
              <table class="w-full">
                <thead>
                  <tr class="bg-slate-50">
                    <th class="text-left p-6 font-semibold text-slate-700">对比项</th>
                    <th class="text-left p-6 font-semibold text-slate-700">传统手工修复</th>
                    <th class="text-left p-6 font-semibold text-slate-700 text-blue-600">本项目数字化方案</th>
                  </tr>
                </thead>
                <tbody>
                  <tr class="border-b border-slate-200 hover:bg-slate-50/50 hover:scale-105 transition-all duration-300">
                    <td class="p-6 font-medium text-slate-800">单件综合周期</td>
                    <td class="p-6 text-red-600 font-medium animate-pulse">15-30 天/件</td>
                    <td class="p-6 text-emerald-600 font-semibold animate-pulse">5-10 天/件</td>
                  </tr>
                  <tr class="border-b border-slate-200 hover:bg-slate-50/50 hover:scale-105 transition-all duration-300 delay-100">
                    <td class="p-6 font-medium text-slate-800">修复成本</td>
                    <td class="p-6 text-red-600 font-medium animate-pulse" style="animation-delay: 0.1s;">3000-8000 元/件</td>
                    <td class="p-6 text-emerald-600 font-semibold animate-pulse" style="animation-delay: 0.1s;">&lt; 500元（材料成本）</td>
                  </tr>
                  <tr class="border-b border-slate-200 hover:bg-slate-50/50 hover:scale-105 transition-all duration-300 delay-200">
                    <td class="p-6 font-medium text-slate-800">人员技能要求</td>
                    <td class="p-6 text-red-600 font-medium animate-pulse" style="animation-delay: 0.2s;">依赖资深技师</td>
                    <td class="p-6 text-emerald-600 font-semibold animate-pulse" style="animation-delay: 0.2s;">培训后普通技术人员可操作</td>
                  </tr>
                  <tr class="hover:bg-slate-50/50 hover:scale-105 transition-all duration-300 delay-300">
                    <td class="p-6 font-medium text-slate-800">修复过程可追溯性</td>
                    <td class="p-6 text-red-600 font-medium animate-pulse" style="animation-delay: 0.3s;">依赖个人经验，难追溯</td>
                    <td class="p-6 text-emerald-600 font-semibold animate-pulse" style="animation-delay: 0.3s;">全流程数字化记录，可追溯可复现</td>
                  </tr>
                </tbody>
              </table>
            </div>
          </div>
        </div>
      </section>

      <!-- ===== 7. 核心团队 ===== -->
      <section id="team" class="py-20 bg-white animate-fadeIn">
        <div class="container mx-auto px-6">
          <div class="text-center mb-16">
            <h2 class="text-4xl md:text-5xl font-black text-slate-900 mb-6 animate-slideInUp">核心团队</h2>
            <p class="text-lg text-slate-600 max-w-2xl mx-auto animate-slideInUp delay-200">"文理工信"深度融合的跨学科团队，在双导师指导下开展创新实践</p>
          </div>

          <!-- 指导老师 -->
          <div class="grid lg:grid-cols-2 gap-8 mb-16">
            <!-- 常小燕老师 -->
            <div class="bg-gradient-to-br from-blue-50/60 to-cyan-50/40 rounded-2xl p-8 border border-blue-100 hover:shadow-xl transition-all duration-500 animate-slideInLeft">
              <div class="flex items-center mb-6">
                <div class="w-16 h-16 rounded-2xl bg-gradient-to-br from-blue-600 to-cyan-500 p-1.5 shadow-lg mr-6 animate-rotate-in">
                  <div class="w-full h-full bg-white rounded-2xl flex items-center justify-center">
                    <span class="text-2xl font-bold text-blue-700">常</span>
                  </div>
                </div>
                <div>
                  <h3 class="text-2xl font-bold text-slate-900 mb-1">常小燕 老师</h3>
                  <p class="text-blue-600 font-semibold">产业实践指导教师</p>
                </div>
              </div>
              
              <div class="space-y-4 text-slate-700 mb-6">
                <div class="flex items-start hover:translate-x-2 transition-transform duration-300">
                  <svg class="w-5 h-5 text-blue-500 mr-3 mt-0.5 flex-shrink-0 animate-pulse" fill="currentColor" viewBox="0 0 20 20">
                    <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"/>
                  </svg>
                  <div>
                    <p class="font-medium text-slate-900">研究方向</p>
                    <p class="text-sm text-slate-600">文化遗产保护、数字人文、博物馆学</p>
                  </div>
                </div>
                
                <div class="flex items-start hover:translate-x-2 transition-transform duration-300 delay-100">
                  <svg class="w-5 h-5 text-blue-500 mr-3 mt-0.5 flex-shrink-0 animate-pulse" style="animation-delay: 0.1s;" fill="currentColor" viewBox="0 0 20 20">
                    <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"/>
                  </svg>
                  <div>
                    <p class="font-medium text-slate-900">指导方向</p>
                    <p class="text-sm text-slate-600">项目学术规划、文保专业把关、研究范式指导</p>
                  </div>
                </div>
              </div>
              
              <div class="pt-6 border-t border-slate-200">
                <p class="text-slate-600 italic text-sm leading-relaxed">
                  "常老师深厚的学术功底确保项目在文化遗产保护领域的专业性与创新性，为技术研发提供坚实的理论支撑。"
                </p>
              </div>
            </div>

            <!-- 韩姣姣老师 -->
            <div class="bg-gradient-to-br from-emerald-50/60 to-teal-50/40 rounded-2xl p-8 border border-emerald-100 hover:shadow-xl transition-all duration-500 animate-slideInRight">
              <div class="flex items-center mb-6">
                <div class="w-16 h-16 rounded-2xl bg-gradient-to-br from-emerald-600 to-teal-500 p-1.5 shadow-lg mr-6 animate-rotate-in" style="animation-delay: 0.1s;">
                  <div class="w-full h-full bg-white rounded-2xl flex items-center justify-center">
                    <span class="text-2xl font-bold text-emerald-700">韩</span>
                  </div>
                </div>
                <div>
                  <h3 class="text-2xl font-bold text-slate-900 mb-1">韩姣姣 讲师</h3>
                  <p class="text-emerald-600 font-semibold">学术指导教师</p>
                  <p class="text-sm text-slate-500">文化遗产与艺术学院党总支副书记</p>
                </div>
              </div>
              
              <div class="space-y-4 text-slate-700 mb-6">
                <div class="flex items-start hover:translate-x-2 transition-transform duration-300">
                  <svg class="w-5 h-5 text-emerald-500 mr-3 mt-0.5 flex-shrink-0 animate-pulse" fill="currentColor" viewBox="0 0 20 20">
                    <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"/>
                  </svg>
                  <div>
                    <p class="font-medium text-slate-900">专业领域</p>
                    <p class="text-sm text-slate-600">博物馆学、田野考古、文化遗产保护</p>
                  </div>
                </div>
                
                <div class="flex items-start hover:translate-x-2 transition-transform duration-300 delay-100">
                  <svg class="w-5 h-5 text-emerald-500 mr-3 mt-0.5 flex-shrink-0 animate-pulse" style="animation-delay: 0.1s;" fill="currentColor" viewBox="0 0 20 20">
                    <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"/>
                  </svg>
                  <div>
                    <p class="font-medium text-slate-900">产业经验</p>
                    <p class="text-sm text-slate-600">吉县"十五五"文旅融合专项规划（19.4万元）</p>
                  </div>
                </div>
                
                <div class="flex items-start hover:translate-x-2 transition-transform duration-300 delay-200">
                  <svg class="w-5 h-5 text-emerald-500 mr-3 mt-0.5 flex-shrink-0 animate-pulse" style="animation-delay: 0.2s;" fill="currentColor" viewBox="0 0 20 20">
                    <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"/>
                  </svg>
                  <div>
                    <p class="font-medium text-slate-900">课程教学</p>
                    <p class="text-sm text-slate-600">《博物馆学基础》《田野考古学》《中国考古学通论》</p>
                  </div>
                </div>
              </div>
              
              <div class="pt-6 border-t border-slate-200">
                <p class="text-slate-600 italic text-sm leading-relaxed">
                  "韩老师丰富的产业经验与教学改革实践，确保项目技术方案落地可行，为基层文保单位提供切实可用的解决方案。"
                </p>
              </div>
            </div>
          </div>

          <!-- 学生团队 -->
          <div>
            <h3 class="text-3xl font-bold text-center mb-8 text-slate-900 animate-slideInUp">核心学生团队</h3>
            
            <div class="grid sm:grid-cols-2 lg:grid-cols-5 gap-6">
              <!-- 成员1: 杨天宇 (负责人) -->
              <div class="team-member-card border-t-4 border-blue-500 animate-slideInLeft delay-100">
                <div class="w-20 h-20 mx-auto rounded-full bg-gradient-to-br from-blue-100 to-blue-50 flex items-center justify-center mb-4 border-4 border-white shadow mt-2 animate-rotate-in">
                  <span class="text-2xl font-bold text-blue-700">杨</span>
                </div>
                <h4 class="text-lg font-bold text-slate-900 mb-1 hover:text-blue-600 transition-colors duration-300">杨天宇</h4>
                <p class="text-blue-600 font-semibold text-sm mb-2">项目负责人</p>
                <p class="text-slate-700 text-sm mb-1">文化遗产与艺术学院</p>
                <p class="text-slate-500 text-xs">文物保护技术2502班</p>
              </div>
              
              <!-- 成员2: 雷凤龙 -->
              <div class="team-member-card border-t-4 border-cyan-500 animate-slideInLeft delay-200">
                <div class="w-20 h-20 mx-auto rounded-full bg-gradient-to-br from-cyan-100 to-cyan-50 flex items-center justify-center mb-4 border-4 border-white shadow animate-rotate-in" style="animation-delay: 0.1s;">
                  <span class="text-2xl font-bold text-cyan-700">雷</span>
                </div>
                <h4 class="text-lg font-bold text-slate-900 mb-1 hover:text-cyan-600 transition-colors duration-300">雷凤龙</h4>
                <p class="text-blue-600 font-semibold text-sm mb-2">智能制造专家</p>
                <p class="text-slate-700 text-sm mb-1">智能制造工程学院</p>
                <p class="text-slate-500 text-xs">机械电子工程2402班</p>
              </div>
              
              <!-- 成员3: 贾易翰 -->
              <div class="team-member-card border-t-4 border-emerald-500 animate-slideInUp delay-300">
                <div class="w-20 h-20 mx-auto rounded-full bg-gradient-to-br from-emerald-100 to-emerald-50 flex items-center justify-center mb-4 border-4 border-white shadow animate-rotate-in" style="animation-delay: 0.2s;">
                  <span class="text-2xl font-bold text-emerald-700">贾</span>
                </div>
                <h4 class="text-lg font-bold text-slate-900 mb-1 hover:text-emerald-600 transition-colors duration-300">贾易翰</h4>
                <p class="text-blue-600 font-semibold text-sm mb-2">机械工程专家</p>
                <p class="text-slate-700 text-sm mb-1">智能制造工程学院</p>
                <p class="text-slate-500 text-xs">机械电子工程2403班</p>
              </div>
              
              <!-- 成员4: 成果 -->
              <div class="team-member-card border-t-4 border-purple-500 animate-slideInRight delay-400">
                <div class="w-20 h-20 mx-auto rounded-full bg-gradient-to-br from-purple-100 to-purple-50 flex items-center justify-center mb-4 border-4 border-white shadow animate-rotate-in" style="animation-delay: 0.3s;">
                  <span class="text-2xl font-bold text-purple-700">成</span>
                </div>
                <h4 class="text-lg font-bold text-slate-900 mb-1 hover:text-purple-600 transition-colors duration-300">成果</h4>
                <p class="text-blue-600 font-semibold text-sm mb-2">人工智能专家</p>
                <p class="text-slate-700 text-sm mb-1">信息与通信工程学院</p>
                <p class="text-slate-500 text-xs">人工智能2401班</p>
              </div>
              
              <!-- 成员5: 吴婧瑄 -->
              <div class="team-member-card border-t-4 border-amber-500 animate-slideInRight delay-500">
                <div class="w-20 h-20 mx-auto rounded-full bg-gradient-to-br from-amber-100 to-amber-50 flex items-center justify-center mb-4 border-4 border-white shadow animate-rotate-in" style="animation-delay: 0.4s;">
                  <span class="text-2xl font-bold text-amber-700">吴</span>
                </div>
                <h4 class="text-lg font-bold text-slate-900 mb-1 hover:text-amber-600 transition-colors duration-300">吴婧瑄</h4>
                <p class="text-blue-600 font-semibold text-sm mb-2">环境科学专家</p>
                <p class="text-slate-700 text-sm mb-1">环境与生命科学学院</p>
                <p class="text-slate-500 text-xs">环境工程2402班</p>
              </div>
            </div>
          </div>

          <!-- 团队优势总结 -->
          <div class="mt-12 bg-gradient-to-r from-slate-50 to-blue-50/30 rounded-2xl p-8 border border-slate-200 hover:shadow-xl transition-all duration-500 animate-fadeInUp delay-600">
            <h4 class="text-xl font-bold text-slate-900 mb-6 text-center">团队核心优势</h4>
            <div class="grid md:grid-cols-3 gap-8 text-center">
              <div>
                <div class="w-12 h-12 rounded-xl bg-blue-100 flex items-center justify-center mx-auto mb-4 hover:scale-110 transition-transform duration-300 animate-bounce-subtle">
                  <svg class="w-6 h-6 text-blue-600" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 21V5a2 2 0 00-2-2H7a2 2 0 00-2 2v16m14 0h2m-2 0h-5m-9 0H3m2 0h5M9 7h1m-1 4h1m4-4h1m-1 4h1m-5 10v-5a1 1 0 011-1h2a1 1 0 011 1v5m-4 0h4"/>
                  </svg>
                </div>
                <p class="font-semibold text-slate-900 mb-2 hover:text-blue-600 transition-colors duration-300">学科交叉融合</p>
                <p class="text-sm text-slate-600">"文理工信"深度融合，覆盖修复全链条</p>
              </div>
              
              <div>
                <div class="w-12 h-12 rounded-xl bg-cyan-100 flex items-center justify-center mx-auto mb-4 hover:scale-110 transition-transform duration-300 animate-bounce-subtle" style="animation-delay: 0.1s;">
                  <svg class="w-6 h-6 text-cyan-600" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z"/>
                  </svg>
                </div>
                <p class="font-semibold text-slate-900 mb-2 hover:text-cyan-600 transition-colors duration-300">双导师制指导</p>
                <p class="text-sm text-slate-600">学术+产业双指导，确保专业与落地并重</p>
              </div>
              
              <div>
                <div class="w-12 h-12 rounded-xl bg-emerald-100 flex items-center justify-center mx-auto mb-4 hover:scale-110 transition-transform duration-300 animate-bounce-subtle" style="animation-delay: 0.2s;">
                  <svg class="w-6 h-6 text-emerald-600" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"/>
                  </svg>
                </div>
                <p class="font-semibold text-slate-900 mb-2 hover:text-emerald-600 transition-colors duration-300">完全学生主导</p>
                <p class="text-sm text-slate-600">本科生完全主导，展现青年创新力量</p>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- ===== 8. 联系我们（高级优化版） ===== -->
      <section id="contact" class="relative py-20 md:py-32 overflow-hidden bg-gradient-to-br from-slate-900 via-blue-900/90 to-cyan-900/90 text-white animate-fadeIn">
        <!-- 背景动态元素 -->
        <div class="absolute inset-0 z-0">
          <div class="absolute top-1/4 left-1/4 w-64 h-64 bg-gradient-to-br from-cyan-500/10 to-blue-500/5 rounded-full blur-3xl animate-float-slow"></div>
          <div class="absolute bottom-1/4 right-1/4 w-80 h-80 bg-gradient-to-br from-blue-500/10 to-cyan-500/5 rounded-full blur-3xl animate-float-slow" style="animation-delay: 2s;"></div>
          
          <!-- 扫描线效果 -->
          <div class="absolute inset-0 bg-[linear-gradient(transparent_1px,transparent_1px)] bg-[size:100px_100px] [mask-image:linear-gradient(to_bottom,transparent_0%,white_20%,white_80%,transparent_100%)]"></div>
          
          <!-- 浮动光点 -->
          <div class="floating-dots">
            <div v-for="i in 20" :key="i" :class="`floating-dot dot-${i}`"></div>
          </div>
        </div>

        <div class="container mx-auto px-6 relative z-10">
          <div class="max-w-6xl mx-auto animate-slideInUp">
            <!-- 标题区域 -->
            <div class="text-center mb-16">
              <div class="inline-flex items-center px-4 py-2 bg-white/10 backdrop-blur-sm text-cyan-300 rounded-full text-sm font-semibold mb-6 border border-cyan-500/30 animate-pulse-subtle">
                <svg class="w-4 h-4 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"/>
                </svg>
                开启数字化修复新篇章
              </div>
              
              <h2 class="text-4xl md:text-6xl font-black mb-6 bg-gradient-to-r from-white via-cyan-200 to-emerald-200 text-transparent bg-clip-text">
                携手共创
                <span class="block text-3xl md:text-5xl mt-4 font-semibold text-cyan-300">文物修复的数字化未来</span>
              </h2>
              
              <p class="text-xl text-slate-300 max-w-3xl mx-auto leading-relaxed animate-typing">
                我们正与临汾市博物馆等机构推进应用试点。诚邀更多文保单位、投资机构、行业专家加入，让每一道历史刻痕在数字中获得新生。
              </p>
            </div>

            <div class="grid lg:grid-cols-2 gap-12">
              <!-- 左侧：联系表单 -->
              <div class="bg-gradient-to-br from-white/5 to-white/10 backdrop-blur-xl rounded-3xl p-8 md:p-10 border border-white/20 shadow-2xl hover:shadow-3xl transition-all duration-500 group">
                <div class="flex items-center mb-8">
                  <div class="w-12 h-12 rounded-2xl bg-gradient-to-br from-cyan-500 to-blue-600 flex items-center justify-center mr-4 animate-pulse">
                    <svg class="w-6 h-6 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"/>
                    </svg>
                  </div>
                  <div>
                    <h3 class="text-2xl font-bold text-white">提交合作意向</h3>
                    <p class="text-cyan-200 text-sm">24小时内回复，专业团队对接</p>
                  </div>
                </div>
                
                <form class="space-y-6">
                  <!-- 姓名/单位 -->
                  <div class="group">
                    <label class="block mb-3 text-cyan-200 font-medium text-sm uppercase tracking-wider">单位 / 姓名</label>
                    <div class="relative">
                      <input type="text" 
                             class="w-full p-4 rounded-xl bg-white/5 border border-white/10 text-white placeholder-slate-400 focus:outline-none focus:ring-2 focus:ring-cyan-500 focus:border-transparent transition-all duration-300 backdrop-blur-sm"
                             placeholder="请输入您的单位或姓名"
                             required>
                      <div class="absolute bottom-0 left-0 w-0 h-0.5 bg-gradient-to-r from-cyan-500 to-blue-500 group-focus-within:w-full transition-all duration-500"></div>
                    </div>
                  </div>
                  
                  <!-- 联系方式 -->
                  <div class="group">
                    <label class="block mb-3 text-cyan-200 font-medium text-sm uppercase tracking-wider">联系方式</label>
                    <div class="relative">
                      <input type="text" 
                             class="w-full p-4 rounded-xl bg-white/5 border border-white/10 text-white placeholder-slate-400 focus:outline-none focus:ring-2 focus:ring-cyan-500 focus:border-transparent transition-all duration-300 backdrop-blur-sm"
                             placeholder="邮箱、电话或微信"
                             required>
                      <div class="absolute bottom-0 left-0 w-0 h-0.5 bg-gradient-to-r from-blue-500 to-cyan-500 group-focus-within:w-full transition-all duration-500"></div>
                    </div>
                  </div>
                  
                  <!-- 合作意向 -->
                  <div class="group">
                    <label class="block mb-3 text-cyan-200 font-medium text-sm uppercase tracking-wider">合作意向</label>
                    <div class="relative">
                      <select class="w-full p-4 rounded-xl bg-white/5 border border-white/10 text-white focus:outline-none focus:ring-2 focus:ring-cyan-500 focus:border-transparent transition-all duration-300 backdrop-blur-sm appearance-none">
                        <option value="" class="bg-slate-800">请选择合作类型</option>
                        <option value="technical" class="bg-slate-800">技术服务合作</option>
                        <option value="investment" class="bg-slate-800">投资洽谈</option>
                        <option value="academic" class="bg-slate-800">学术交流</option>
                        <option value="other" class="bg-slate-800">其他合作</option>
                      </select>
                      <div class="absolute inset-y-0 right-4 flex items-center pointer-events-none">
                        <svg class="w-5 h-5 text-cyan-300" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"/>
                        </svg>
                      </div>
                      <div class="absolute bottom-0 left-0 w-0 h-0.5 bg-gradient-to-r from-emerald-500 to-cyan-500 group-focus-within:w-full transition-all duration-500"></div>
                    </div>
                  </div>
                  
                  <!-- 备注信息 -->
                  <div class="group">
                    <label class="block mb-3 text-cyan-200 font-medium text-sm uppercase tracking-wider">备注信息</label>
                    <div class="relative">
                      <textarea rows="4" 
                                class="w-full p-4 rounded-xl bg-white/5 border border-white/10 text-white placeholder-slate-400 focus:outline-none focus:ring-2 focus:ring-cyan-500 focus:border-transparent transition-all duration-300 backdrop-blur-sm resize-none"
                                placeholder="请简要描述您的具体需求..."
                                ></textarea>
                      <div class="absolute bottom-0 left-0 w-0 h-0.5 bg-gradient-to-r from-cyan-500 to-emerald-500 group-focus-within:w-full transition-all duration-500"></div>
                    </div>
                  </div>
                  
                  <!-- 提交按钮 -->
                  <button type="submit" 
                          class="w-full bg-gradient-to-r from-cyan-500 to-blue-600 text-white font-semibold py-4 rounded-xl hover:opacity-90 transition-all duration-300 text-lg shadow-lg hover:shadow-xl hover:-translate-y-1 hover:scale-[1.02] transform-gpu group/btn relative overflow-hidden">
                    <span class="relative z-10 flex items-center justify-center">
                      <svg class="w-5 h-5 mr-3 group-hover/btn:rotate-12 transition-transform duration-300" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"/>
                      </svg>
                      立即提交合作意向
                    </span>
                    <div class="absolute inset-0 bg-gradient-to-r from-blue-600 to-cyan-500 opacity-0 group-hover/btn:opacity-100 transition-opacity duration-300"></div>
                  </button>
                </form>
              </div>

              <!-- 右侧：联系信息 -->
              <div class="space-y-8">
                <!-- 项目联系 -->
                <div class="bg-gradient-to-br from-white/5 to-white/10 backdrop-blur-xl rounded-3xl p-8 border border-white/20 shadow-2xl hover:shadow-3xl transition-all duration-500 group">
                  <div class="flex items-center mb-6">
                    <div class="w-10 h-10 rounded-xl bg-gradient-to-br from-cyan-500 to-blue-600 flex items-center justify-center mr-4 animate-bounce-subtle">
                      <svg class="w-5 h-5 text-white" fill="currentColor" viewBox="0 0 20 20">
                        <path fill-rule="evenodd" d="M5.05 4.05a7 7 0 119.9 9.9L10 18.9l-4.95-4.95a7 7 0 010-9.9zM10 11a2 2 0 100-4 2 2 0 000 4z" clip-rule="evenodd"/>
                      </svg>
                    </div>
                    <h3 class="text-2xl font-bold text-white">项目联系</h3>
                  </div>
                  
                  <div class="space-y-6">
                    <div class="flex items-start group hover:bg-white/5 p-4 rounded-xl transition-all duration-300 hover:translate-x-2">
                      <div class="w-10 h-10 rounded-xl bg-cyan-500/20 flex items-center justify-center mr-4 flex-shrink-0 group-hover:scale-110 transition-transform duration-300">
                        <svg class="w-5 h-5 text-cyan-300" fill="currentColor" viewBox="0 0 20 20">
                          <path d="M2.003 5.884L10 9.882l7.997-3.998A2 2 0 0016 4H4a2 2 0 00-1.997 1.884z"/>
                          <path d="M18 8.118l-8 4-8-4V14a2 2 0 002 2h12a2 2 0 002-2V8.118z"/>
                        </svg>
                      </div>
                      <div>
                        <p class="font-medium text-cyan-200 mb-1">项目负责人邮箱</p>
                        <p class="text-lg font-semibold text-white group-hover:text-cyan-300 transition-colors duration-300">yangtianyu27@outlook.com</p>
                      </div>
                    </div>
                    
                    <div class="flex items-start group hover:bg-white/5 p-4 rounded-xl transition-all duration-300 hover:translate-x-2">
                      <div class="w-10 h-10 rounded-xl bg-blue-500/20 flex items-center justify-center mr-4 flex-shrink-0 group-hover:scale-110 transition-transform duration-300">
                        <svg class="w-5 h-5 text-blue-300" fill="currentColor" viewBox="0 0 20 20">
                          <path fill-rule="evenodd" d="M5.05 4.05a7 7 0 119.9 9.9L10 18.9l-4.95-4.95a7 7 0 010-9.9zM10 11a2 2 0 100-4 2 2 0 000 4z" clip-rule="evenodd"/>
                        </svg>
                      </div>
                      <div>
                        <p class="font-medium text-cyan-200 mb-1">项目所在地</p>
                        <p class="text-lg font-semibold text-white group-hover:text-blue-300 transition-colors duration-300">山西电子科技学院</p>
                      </div>
                    </div>
                  </div>
                </div>

                <!-- 产业合作 -->
                <div class="bg-gradient-to-br from-white/5 to-white/10 backdrop-blur-xl rounded-3xl p-8 border border-white/20 shadow-2xl hover:shadow-3xl transition-all duration-500 group">
                  <div class="flex items-center mb-6">
                    <div class="w-10 h-10 rounded-xl bg-gradient-to-br from-emerald-500 to-teal-600 flex items-center justify-center mr-4 animate-bounce-subtle" style="animation-delay: 0.2s;">
                      <svg class="w-5 h-5 text-white" fill="currentColor" viewBox="0 0 20 20">
                        <path fill-rule="evenodd" d="M12.395 2.553a1 1 0 00-1.45-.385c-.345.23-.614.558-.822.88-.214.33-.403.713-.57 1.116-.334.804-.614 1.768-.84 2.734a31.365 31.365 0 00-.613 3.58 2.64 2.64 0 01-.945-1.067c-.328-.68-.398-1.534-.398-2.654A1 1 0 005.05 6.05 6.981 6.981 0 003 11a7 7 0 1011.95-4.95c-.592-.591-.98-.985-1.348-1.467-.363-.476-.724-1.063-1.207-2.03zM12.12 15.12A3 3 0 017 13s.879.5 2.5.5c0-1 .5-4 1.25-4.5.5 1 .786 1.293 1.371 1.879A2.99 2.99 0 0113 13a2.99 2.99 0 01-.879 2.121z" clip-rule="evenodd"/>
                      </svg>
                    </div>
                    <h3 class="text-2xl font-bold text-white">产业合作</h3>
                  </div>
                  
                  <div class="space-y-4">
                    <p class="text-slate-300 leading-relaxed">
                      已与
                      <span class="text-emerald-300 font-semibold animate-pulse">"醒狮数字缮物"</span>
                      公司达成合作意向，正在推进《技术咨询支持备忘录》签署流程。
                    </p>
                    
                    <div class="bg-gradient-to-r from-emerald-500/20 to-teal-600/20 rounded-xl p-4 border border-emerald-500/30 hover:border-emerald-400 transition-all duration-300">
                      <div class="flex items-center">
                        <div class="w-8 h-8 rounded-full bg-gradient-to-br from-emerald-500 to-teal-600 flex items-center justify-center mr-3 animate-spin-slow">
                          <svg class="w-4 h-4 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"/>
                          </svg>
                        </div>
                        <div>
                          <p class="text-sm font-medium text-emerald-200">战略合作状态</p>
                          <p class="text-lg font-semibold text-white">意向合作进行中</p>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>

                <!-- 商务合作 -->
                <div class="bg-gradient-to-br from-white/5 to-white/10 backdrop-blur-xl rounded-3xl p-8 border border-white/20 shadow-2xl hover:shadow-3xl transition-all duration-500 group">
                  <div class="flex items-center mb-6">
                    <div class="w-10 h-10 rounded-xl bg-gradient-to-br from-amber-500 to-orange-600 flex items-center justify-center mr-4 animate-bounce-subtle" style="animation-delay: 0.4s;">
                      <svg class="w-5 h-5 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 13.255A23.931 23.931 0 0112 15c-3.183 0-6.22-.62-9-1.745M16 6V4a2 2 0 00-2-2h-4a2 2 0 00-2 2v2m4 6h.01M5 20h14a2 2 0 002-2V8a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"/>
                      </svg>
                    </div>
                    <h3 class="text-2xl font-bold text-white">商务合作</h3>
                  </div>
                  
                  <div class="space-y-4">
                    <p class="text-slate-300 leading-relaxed">
                      欢迎文保单位、投资机构、技术伙伴联系我们，共同探索文物数字化修复的商业化路径。
                    </p>
                    
                    <div class="grid grid-cols-2 gap-3">
                      <div class="text-center p-3 rounded-xl bg-white/5 hover:bg-amber-500/20 transition-all duration-300 group hover:scale-105">
                        <div class="text-amber-300 font-black text-xl mb-1 group-hover:text-amber-200">B2B</div>
                        <div class="text-xs text-slate-300">机构合作</div>
                      </div>
                      <div class="text-center p-3 rounded-xl bg-white/5 hover:bg-blue-500/20 transition-all duration-300 group hover:scale-105">
                        <div class="text-blue-300 font-black text-xl mb-1 group-hover:text-blue-200">B2G</div>
                        <div class="text-xs text-slate-300">政府合作</div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- ===== 9. 页脚 ===== -->
      <footer class="bg-gradient-to-br from-slate-900 to-blue-900/90 text-white py-12 md:py-16 animate-fadeIn">
        <div class="container mx-auto px-6">
          <div class="flex flex-col lg:flex-row justify-between items-center mb-8">
            <!-- Logo和品牌 -->
            <div class="flex items-center mb-8 lg:mb-0 animate-slideInLeft">
              <div class="relative group">
                <div class="w-16 h-16 rounded-2xl bg-gradient-to-br from-cyan-500 to-blue-600 flex items-center justify-center shadow-xl mr-6 animate-rotate-in">
                  <!-- 页脚图标（与导航栏一致） -->
                  <img 
                    src="/logo.png" 
                    alt="镌纹留痕" 
                    class="w-10 h-10 object-contain"
                    onerror="this.style.display='none'; console.log('图标加载失败，请检查logo.png路径')"
                  >
                </div>
                <div class="absolute inset-0 bg-gradient-to-br from-cyan-500 to-blue-600 rounded-2xl blur-md opacity-0 group-hover:opacity-30 transition-opacity duration-300 -z-10"></div>
              </div>
              <div>
                <h3 class="text-3xl font-bold mb-2 hover:text-cyan-300 transition-colors duration-300">镌纹留痕</h3>
                <p class="text-slate-400 text-sm">让历史在数字中重获新生</p>
              </div>
            </div>
            
            <!-- 快速链接 -->
            <div class="flex flex-wrap justify-center gap-6 mb-8 lg:mb-0 animate-slideInUp">
              <a v-for="item in navItems" 
                 :key="item.id" 
                 :href="item.link"
                 class="text-slate-400 hover:text-cyan-300 transition-colors duration-300 hover:underline underline-offset-4">
                {{ item.text }}
              </a>
            </div>
            
            <!-- 社交媒体 -->
<div class="flex space-x-4 animate-slideInRight">
  <!-- 微信 -->
  <a href="javascript:void(0)" class="w-10 h-10 rounded-xl bg-white/10 hover:bg-green-500 flex items-center justify-center transition-all duration-300 hover:scale-110 hover:rotate-12 group" title="微信">
    <svg class="w-5 h-5 text-white group-hover:text-white" viewBox="0 0 24 24" fill="currentColor">
      <path d="M20.344,3.656C18.422,1.734,15.797,0.75,12.5,0.75c-3.297,0-5.922,0.984-7.844,2.906C2.734,5.578,1.75,8.203,1.75,11.5c0,1.781,0.422,3.477,1.266,5.086L1.047,22.455c-0.062,0.203-0.016,0.422,0.125,0.578C1.313,23.188,1.5,23.25,1.688,23.25c0.078,0,0.156-0.016,0.234-0.047l5.5-2.219c1.625,0.797,3.406,1.203,5.344,1.203c3.297,0,5.922-0.984,7.844-2.906c1.922-1.922,2.906-4.547,2.906-7.844C23.25,8.203,22.266,5.578,20.344,3.656z M12.5,21.5c-1.641,0-3.188-0.375-4.641-1.125c-0.141-0.078-0.297-0.109-0.453-0.094l-4.266,1.719l1.375-4.516c0.047-0.141,0.031-0.297-0.047-0.438c-0.812-1.438-1.219-3-1.219-4.688c0-2.844,0.906-5.25,2.719-7.062C8.25,2.906,10.656,2,12.5,2c2.844,0,5.25,0.906,7.062,2.719c1.813,1.813,2.719,4.219,2.719,7.062C22.281,17.281,17.719,21.5,12.5,21.5z"/>
    </svg>
  </a>
  
  <!-- QQ -->
  <a href="javascript:void(0)" class="w-10 h-10 rounded-xl bg-white/10 hover:bg-blue-500 flex items-center justify-center transition-all duration-300 hover:scale-110 hover:-rotate-12 group" title="QQ">
    <svg class="w-5 h-5 text-white group-hover:text-white" viewBox="0 0 24 24" fill="currentColor">
      <path d="M12,2C6.48,2,2,6.48,2,12s4.48,10,10,10s10-4.48,10-10S17.52,2,12,2z M12,3.77c4.41,0,8,3.59,8,8s-3.59,8-8,8s-8-3.59-8-8S7.59,3.77,12,3.77z M12,5.54c-3.73,0-6.77,3.04-6.77,6.77c0,1.52,0.5,2.92,1.35,4.05c0.18,0.23,0.48,0.29,0.73,0.11c0.25-0.18,0.31-0.5,0.12-0.75C6.58,14.73,6.23,13.5,6.23,12.31c0-3.19,2.6-5.77,5.77-5.77c3.19,0,5.77,2.6,5.77,5.77c0,1.19-0.35,2.42-1.2,3.31c-0.19,0.25-0.13,0.57,0.12,0.75c0.25,0.18,0.57,0.12,0.75-0.12c0.85-1.13,1.35-2.53,1.35-4.05C18.77,8.58,15.73,5.54,12,5.54z"/>
    </svg>
  </a>
  
  <!-- 邮箱 -->
  <a href="mailto:yangtianyu27@outlook.com" class="w-10 h-10 rounded-xl bg-white/10 hover:bg-red-500 flex items-center justify-center transition-all duration-300 hover:scale-110 hover:rotate-12 group" title="邮箱">
    <svg class="w-5 h-5 text-white group-hover:text-white" viewBox="0 0 24 24" fill="currentColor">
      <path d="M20,4H4C2.9,4,2.01,4.9,2.01,6L2,18c0,1.1,0.9,2,2,2h16c1.1,0,2-0.9,2-2V6C22,4.9,21.1,4,20,4z M20,8l-8,5L4,8V6l8,5l8-5V8z"/>
    </svg>
  </a>
</div>
          </div>
          
          <!-- 版权信息 -->
          <div class="pt-8 border-t border-white/20 text-center animate-fadeInUp">
            <p class="text-slate-400 text-lg mb-4 leading-relaxed">
              山西电子科技学院大学生创新训练计划项目（2026-2028）
              <span class="block text-slate-500 text-sm mt-2">
                陶瓷器立体纹饰三维数字化修复与再生应用官方展示平台
              </span>
            </p>
            
            <div class="text-slate-500 text-sm">
              <p>© 2023-2026 镌纹留痕项目团队. 本页面为项目研究成果展示。</p>
              <p class="mt-2 text-slate-600">数据来源于实地调研与专家访谈，最终解释权归项目团队所有。</p>
            </div>
          </div>
        </div>
      </footer>
    </main>
  </div>
</template>