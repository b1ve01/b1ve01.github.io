<style>
  /* 1. 修复导航栏：竖屏下自动换行或缩小间距 */
  @media (max-width: 480px) {
    header nav {
      display: flex !important;
      flex-wrap: wrap !important; /* 允许换行 */
      justify-content: center !important;
      gap: 10px !important; /* 缩小项目间距 */
    }
    header nav a {
      font-size: 0.8rem !important; /* 稍微缩小字体，确保一排能放下 */
      margin: 0 5px !important;
    }
  }

  /* 2. 之前的盒子适配代码 */
  .responsive-container {
    border: 2px solid #fff;
    padding: 20px;
    margin: -10px auto 20px auto;
    border-radius: 4px;
    text-align: center;
    width: 95%;
    max-width: 900px;
  }

  @media (max-width: 768px) {
    .responsive-container {
      margin-top: 10px; 
      padding: 10px;
    }
    .responsive-img {
      width: 100% !important;
    }
  }
</style>

<div class="responsive-container">
  <p style="margin-bottom: 15px; font-family: monospace;">hi, this is b1ve blog : )</p>
  <img src="her_0.png" alt="My Image" class="responsive-img"
       style="width: 70%; height: auto; display: block; margin: 0 auto; border-radius: 2px;">
</div>