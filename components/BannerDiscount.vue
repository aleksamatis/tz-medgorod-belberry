<template>
  <div class="discount">
    <div class="discount-discount">
      <div class="discount-old-price">{{oldPrice}}</div>
      <div  v-if="oldPrice" class="discount-percent">
        <div class="triangle" />
        <div class="discount-value">-{{discount}} %</div>
      </div>
    </div>
    <div v-if="message" class="discount-message-description">{{message}}</div>
    <div class="discount-new-price">{{newPrice}}</div>
  </div>
</template>

<script>
export default {
  props: {
    oldPrice: {
      type: String,
      default: ''
    },
    newPrice: {
      type: String,
      default: ''
    },
    discount: {
      type: Number,
      default: 0,
    },
    message: {
      type: String,
      default: '',
    },
  }
}
</script>

<style scoped>
.discount-discount {
  display: flex;
}

.discount-percent {
  display: flex;
  align-items: center;
}

.discount-value {
  background-color: #FF7512;
  border-radius: 5px;
  display: flex;
  height: 30px;
  align-items: center;
  padding: 0 10px;
  color: #fff;
}

.discount-old-price {
  text-decoration:line-through;
  font-style: normal;
  font-weight: 600;
  font-size: 20px;
  color: #333;
  margin-right: 40px;
}

.discount-new-price {
  font-style: normal;
  font-weight: 800;
  font-size: 46px;
  color: #035063;
}

.discount-message-description {
  font-style: normal;
  font-weight: 700;
  font-size: 36px;
  line-height: 156%;
  color: #035063;
}

.triangle {
  width: 0;
  height: 15px;
  border-top: 7.5px solid transparent;
  border-bottom: 7.5px solid transparent;
  border-right: 10px solid #FF7512;
}

@media (max-width: 1360px){
  .discount-new-price {
    font-size: 20px;
  }
}

@media (max-width: 540px){
  .discount-old-price {
    margin-right: 10px;
  }

  .discount-message-description {
    font-size: 26px;
    line-height: 1.2;
  }
}
</style>
