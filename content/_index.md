<style>
  /* 基础容器 */
  .dashboard-box {
    border: 2px solid #fff;
    padding: 20px;
    margin: 10px auto;
    border-radius: 4px;
    text-align: center;
    width: 95%;
    max-width: 800px;
  }

  /* ============================================== */
  /* 核心修复：彻底解决奇怪横线问题 */
  /* ============================================== */
  hr.solid-white-line {
    /* 1. 清除主题自带的所有边框和纹理 */
    border: none !important;
    
    /* 2. 用高度和背景色定义完美的 1像素 实心白线 */
    height: 1px !important;
    background-color: #fff !important; /* 纯白色 */
    opacity: 0.9 !important; /* 稍微降低一点点透明度，防止在大屏幕下刺眼，可选 */
    
    /* 3. 精确控制间距 */
    width: 70%; /* 让线不要占满整个盒子，看起来更高级 */
    margin: 25px auto !important; /* 上下预留呼吸空间 */
  }

  /* 模拟导航链接（按钮）样式保持不变 */
  .nav-links {
    margin-top: 15px; 
    display: flex;
    justify-content: center;
    gap: 15px;
    flex-wrap: wrap;
  }
  /* ...nav-item 樣式不變... */

  /* 针对 nav-item 及其容器强制隐藏所有可能的修饰点 */
  .nav-links, .nav-item {
      text-decoration: none !important;
      list-style: none !important;
  }

  /* 强力清除可能存在的伪元素（很多主题的小点是这么来的） */
  .nav-item::before, .nav-item::after {
      content: "" !important;
      display: none !important;
  }
</style>

<div class="dashboard-box">
  <p style="margin-bottom: 15px; font-family: monospace;">hi, this is b1ve blog : )</p>
  
  <img src="her_0.png" style="width: 80%; height: auto; display: block; margin: 0 auto 15px auto;">

  <hr class="solid-white-line">

  <div class="nav-links">
    <a href="/about" class="nav-item">[ ABOUT ]</a>
    <a href="/showcase" class="nav-item">[ SHOWCASE ]</a>
  </div>

</div>