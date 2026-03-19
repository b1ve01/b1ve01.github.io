<style>
  /* 这里的样式会自动根据屏幕宽度调整 */
  .responsive-container {
    border: 2px solid #fff;
    padding: 20px;
    margin: -10px auto 20px auto; /* 默认电脑端上移 */
    border-radius: 4px;
    text-align: center;
    width: 95%; /* 保证手机端不会贴边 */
    max-width: 900px; /* 保证电脑端不会太宽 */
  }

  /* 针对手机端的特殊调整 (屏幕小于 768px) */
  @media (max-width: 768px) {
    .responsive-container {
      margin-top: 10px; /* 手机端导航栏窄，不需要负边距，改回正值 */
      padding: 10px;    /* 缩小内边距省空间 */
    }
    .responsive-img {
      width: 100% !important; /* 手机端图片占满横向，才看得清 */
    }
  }
</style>

<div class="responsive-container">
  <p style="margin-bottom: 15px; font-family: monospace;">hi, this is b1ve blog : )</p>
  
  <img src="her_0.png" alt="My Image" class="responsive-img"
       style="width: 70%; height: auto; display: block; margin: 0 auto; border-radius: 2px;">
</div>