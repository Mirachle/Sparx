<template>
  <div :class="imageChanged" @click="clickItem" style="text-align: center;">
    <img class="picture-border" :src="picture.img" alt="Shoe">
    <div class="shoe-type">Sparx Men's Canvas Sneakers</div>
    <div class="id-style">{{this.item.shoeId}}</div>
    <rating-comp/>
    <div class="price-style">{{this.item.shoePrice}}</div>
  </div>
</template>

<script>
import Rating from '@/components/Rating';

export default {
  name: 'ListItem',
  components: {
    'rating-comp': Rating,
  },
  props: ['item', 'index'],
  data() {
    return {
      picture: this.item.shoePicture,
    };
  },
  computed: {
    imageChanged() {
      this.picture = this.item.shoePicture;
      return null;
    },
  },
  methods: {
    clickItem() {
      this.$emit('clicked', this.index);
    },
  },
};
</script>

<style>

img{
  height: 230px;
  width: 230px;
}

.picture-border{
  border-radius: 16px;
  border: solid 1px #979797;
  background-color: #ffffff;
}

.shoe-type{
  font-family: Helvetica;
  font-size: 12px;
  font-weight: normal;
  font-style: normal;
  font-stretch: normal;
  line-height: 1.58;
  letter-spacing: normal;
  text-align: center;
  color: #3c3c3c;
  }

.id-style{
  font-family: Helvetica;
  font-size: 14px;
  font-weight: normal;
  font-style: normal;
  font-stretch: normal;
  line-height: 1.36;
  letter-spacing: normal;
  text-align: center;
  color: #3978ac;
  }

.price-style{
  font-family: Helvetica;
  font-size: 18px;
  font-weight: normal;
  font-style: normal;
  font-stretch: normal;
  line-height: normal;
  letter-spacing: normal;
  color: #3c3c3c;
}

</style>
