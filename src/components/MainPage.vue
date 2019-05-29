<template>
  <div>
    <div class="row line-maker">
      <div class="col-12 col-xl-6">
        <picture-comp :picture="shoePicture"/>
      </div>
      <div class="col-12 col-xl-6">
        <subtitle-comp :shoeType="shoeType" :shoeColor="shoeColor" :shoePrice="shoePrice"/>
      </div>
    </div>
    <div class="row">
      <div class="col-12">
        <list-comp :listShoe="listShoe" @change="itemChange"/>
      </div>
    </div>
  </div>
</template>


<script>
import PictureComp from '@/components/PictureComp';
import SubtitleComp from '@/components/SubtitleComp';
import ListComp from '@/components/ListComp';

export default {
  name: 'MainPage',
  components: {
    'picture-comp': PictureComp,
    'subtitle-comp': SubtitleComp,
    'list-comp': ListComp,
  },
  methods: {
    itemChange(index) {
      // alert(tempImage);
      this.tempImage = this.listShoe[index].shoePicture;
      this.tempId = this.listShoe[index].shoeId;
      this.tempPrice = this.listShoe[index].shoePrice;
      this.tempColor = this.listShoe[index].shoeColor;
      this.listShoe[index].shoePicture = this.shoePicture;
      this.listShoe[index].shoeId = this.shoeId;
      this.listShoe[index].shoePrice = this.shoePrice;
      this.listShoe[index].shoeColor = this.shoeColor;
      this.shoePicture = this.tempImage;
      this.shoeId = this.tempId;
      this.shoePrice = this.tempPrice;
      this.shoeColor = this.tempColor;
    },
  },
  data() {
    return {
      tempImage: '',
      tempId: '',
      tempPrice: '',
      tempColor: '',
      /* eslint-disable global-require */
      shoeType: "Men's Canvas Sneaker",
      shoePicture: { img: require('@/assets/cipo1.png') },
      shoeId: 'AHU6799',
      shoePrice: '20$',
      shoeColor: 'Blue',
      listShoe: [
        {
          shoePicture: { img: require('@/assets/cipo2.png') },
          shoeId: 'AHU6798',
          shoePrice: '20$',
          shoeColor: 'Blue',
        },
        {
          shoePicture: { img: require('@/assets/cipo3.png') },
          shoeId: 'AHU6798',
          shoePrice: '23$',
          shoeColor: 'Black',
        },
        {
          shoePicture: { img: require('@/assets/cipo4.png') },
          shoeId: 'AHIRE6678',
          shoePrice: '25$',
          shoeColor: 'Green',
        },
        {
          shoePicture: { img: require('@/assets/cipo5.png') },
          shoeId: 'AHU68928',
          shoePrice: '16$',
          shoeColor: 'Green',
          /* eslint-enable global-require */
        },
      ],
    };
  },
};
</script>


<style scoped>
.line-maker{
  margin-left: 10vw;
}
</style>
