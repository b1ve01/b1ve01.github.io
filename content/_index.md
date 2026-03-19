<style>
  /* 强制修复手机竖屏导航栏 */
  @media (max-width: 600px) {
    /* 强行拆掉主题的导航栏横向锁定 */
    header nav, .menu__inner {
      display: flex !important;
      flex-wrap: wrap !important;
      justify-content: center !important;
      width: 100% !important;
      gap: 10px !important;
    }
    header nav a {
      font-size: 14px !important;
      margin: 5px !important;
      display: inline-block !important;
    }
    /* 盒子向上挪一点，贴近一点 */
    .responsive-box { margin-top: 5px !important; }
  }

  /* 基础盒子样式 */
  .responsive-box {
    border: 2px solid #fff;
    padding: 15px;
    margin: -15px auto 20px auto;
    border-radius: 4px;
    width: 95%;
    max-width: 850px;
    text-align: center;
  }
</style>

<div class="responsive-box">
  <p style="margin-bottom: 15px; font-family: monospace;">hi, this is b1ve blog : )</p>
  <img src="her_0.png" style="width: 100%; height: auto; display: block; margin: 0 auto;">
</div>