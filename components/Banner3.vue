<template>
<BannerItem>
  <BannerContent title="ЭКГ + ЭХО-КГ">
    <div>
      <BannerDiscount old-price="4150 руб." new-price="2900 руб." :discount="30"></BannerDiscount>
      <div class="promotion-action">Акция действует до 30.09.2021 г.</div>
    </div>
    <img class="banner-image" src="/image 38 1.png" />
  </BannerContent>
</BannerItem>
</template>

<style scoped>
.banner-image {
  position: absolute;
  right: 0;
  z-index: 200;
  bottom: -68px;
}

.promotion-action {
  font-style: normal;
  font-weight: 400;
  font-size: 14px;
  line-height: 143%;
  color: #333;
  opacity: 0.75;
}

@media (max-width: 1200px){
  .banner-image {
    display: none;
  }
}
</style>
