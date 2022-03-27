<template>
  <div class="banner-item">
    <div class="banner-item-inner">
      <slot></slot>
    </div>
  </div>
</template>

<style scoped>
.banner-item {
  padding: 50px 0;
  height: 100%;
  display: flex;
}

.banner-item-inner {
  border-radius: 20px;
  background: url('/healthcare-roche 1.png');
  padding: 67px;
  flex: 1 1;
}

@media (max-width: 540px) {
  .banner-item-inner {
    padding-top: 15px;
    padding-bottom: 15px;
  }
}
</style>
