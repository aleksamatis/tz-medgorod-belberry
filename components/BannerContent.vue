<template>
  <div class="banner-content">
    <div class="action">Акция</div>
    <h2>
      {{title}}
      <slot name="title"></slot>
    </h2>
    <slot />
    <div class="baner-content-button-group">
      <el-button size="medium" type="primary" round>Записаться</el-button>
      <el-button size="medium" type="info" round>Подробнее</el-button>
    </div>
    <slot name="image" />
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: '',
    }
  }
}
</script>

<style scoped>
.banner-content {
  position: relative;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  height: 100%;
  width: 100%;
}

.banner-content .action {
  width: 81px;
  height: 29px;
  text-align: center;
  background: #035063;
  border-radius: 3.5px;
  color: #fff;
  font-style: normal;
  font-weight: 400;
  font-size: 16px;
  line-height: 29px;
}

.banner-content h2 {
  font-style: normal;
  font-weight: 700;
  font-size: 48px;
  color: #035063;
  max-width: 670px;
}

.banner-content >>> .el-button.el-button--primary.is-round {
  padding: 10px 32px;
  background: #FF7512;
  border: 1px solid #FF7512;
  border-radius: 40px;
  font-weight: 700;
  font-size: 18px;
  line-height: 156%;
}

.banner-content >>> .el-button.el-button--primary.is-round:active, .banner-content >>> .el-button.is-round:hover {
  background: #F78F45;
  border: 1px solid #F78F45;
  box-shadow: 0 4px 16px rgba(255 140 105 / 29%);
}

.banner-content >>> .el-button.el-button--info.is-round {
  padding: 10px 32px;
  background: rgba(3 80 99 / 70%);
  border: 1px solid transparent;
  border-radius: 40px;
  font-weight: 700;
  font-size: 18px;
  line-height: 156%;
}

.banner-content >>> .el-button.el-button--info.is-round:active, .banner-content >>> .el-button.el-button--info.is-round:hover {
  background: #33748E;
  border: 1px solid transparent;
  box-shadow: 0 4px 16px rgba(65 105 225 / 29%);
}

@media (max-width: 1360px){
 .banner-content h2 {
    font-size: 30px;
  }
}

@media (max-width: 1200px){
 .banner-content  {
    align-items: center;
  }

  .banner-content h2 {
    max-width: 100%;
  }
}

@media (max-width: 900px){
  .banner-content h2 {
    max-width: 100%;
    text-align: center;
  }

  .baner-content-button-group {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    padding-top: 16px;
  }

  .baner-content-button-group > * {
    margin: 0;
    width: 163px;
  }

  .baner-content-button-group > *:first-child {
    margin-bottom: 8px;
  }
}
</style>
