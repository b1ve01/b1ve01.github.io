<style>
  /* 强制重置导航栏，解决手机竖屏显示不全 */
  @media (max-width: 600px) {
    /* 1. 强制容器宽度并允许换行 */
    .menu, .menu__inner, header nav {
      display: block !important;
      width: 100% !important;
      text-align: center !important;
    }
    
    /* 2. 让每个导航项（About, Showcase, Network）变成块级元素，垂直排列 */
    .menu__inner li, header nav a {
      display: inline-block !important;
      margin: 5px 10px !important;
      padding: 5px 10px !important;
      border: 1px solid #333 !important; /* 增加点击感 */
      font-size: 14px !important;
    }

    /* 3. 缩短 Logo 间距，防止占位太多 */
    .logo { margin-bottom: 10px !important; }
  }

  /* 盒子和图片的响应式保持不变 */
  .responsive-container {
    border: 2px solid #fff;
    padding: 15px;
    margin: 10px auto; /* 手机端用正边距，防止重叠 */
    width: 95%;
    max-width: 800px;
  }
</style>

<div class="responsive-container" style="text-align: center;">
  <p style="margin-bottom: 10px; font-family: monospace;">hi, this is b1ve blog : )</p>
  <img src="her_0.png" alt="My Image" style="width: 100%; height: auto; display: block; margin: 0 auto;">
</div>