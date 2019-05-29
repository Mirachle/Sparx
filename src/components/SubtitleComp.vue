<template>
  <div class="card">
    <h1>Sparx</h1>
    <h2>{{shoeType}}</h2>
    <h3>{{shoePrice}}</h3>
    <rating-comp/>
    <h4>Colour: {{shoeColor}} <span :class="background"></span> </h4>
    <description-comp/>
    <size-input/>
    <input type="button" value="Add to Kart">
  </div>
</template>

<script>
import Rating from '@/components/Rating';
import Description from '@/components/Description';
import SizeInput from '@/components/SizeInput';

export default {
  name: 'SubtitleComp',
  props: ['shoeType', 'shoePrice', 'shoeColor'],
  components: {
    'rating-comp': Rating,
    'description-comp': Description,
    'size-input': SizeInput,
  },
  computed: {
    background() {
      if (this.shoeColor === 'Blue') {
        return 'blue';
      } else if (this.shoeColor === 'Green') {
        return 'green';
      }
      return 'black';
    },
  },
};
</script>

<style>
h1{
  font-family: Helvetica;
  font-size: 48px;
  font-weight: bold;
  font-style: normal;
  font-stretch: normal;
  line-height: 0.5;
  letter-spacing: normal;
  color: #3c3c3c;
  margin-bottom: 5vh;
  text-align: center;
}

h2{
  font-family: Helvetica;
  font-size: 24px;
  font-weight: 300;
  font-style: normal;
  font-stretch: normal;
  line-height: 1;
  letter-spacing: normal;
  color: #3c3c3c;
  margin-bottom: 3vh;
  padding-left: 10%;
}

h3{
  font-family: Helvetica;
  font-size: 24px;
  font-weight: normal;
  font-style: normal;
  font-stretch: normal;
  line-height: normal;
  letter-spacing: normal;
  color: #3c3c3c;
  text-align: center;
  margin-bottom: 3vh;
}

h4{
  font-family: Helvetica;
  font-size: 20px;
  font-weight: 300;
  font-style: normal;
  font-stretch: normal;
  line-height: 0.95;
  letter-spacing: normal;
  color: #111111;
  text-align: center;
  margin-bottom: 3vh;
  display: flex;
  align-items: center;
  margin-left: 30%;
}

.card{
  border: 0ch;
  margin-right: 12vw;
  background-color: transparent;
}

input[type="button"]{
  border-radius: 5px;
  background-color: #1ea62d;
  font-family: Helvetica;
  font-size: 18px;
  font-weight: 300;
  font-style: normal;
  font-stretch: normal;
  line-height: 1.06;
  letter-spacing: normal;
  color: #f0f0f0;
  margin: auto;
  padding-top:1vh;
  padding-bottom:2vh;
  padding-left:2vw;
  padding-right:4vw;
  border: 0px;
}

span{
  width: 23px;
  height: 23px;
  border-radius: 50%;
  border: 0;
  margin-left: 2vw;
  display: inline-block;
  align-items: center;
}

.blue{
  background-color: #4f5487;
}
.green{
  background-color: #417a48;
}
.black{
  background-color: #000000;
}

@media only screen and (max-width: 1200px) {
    h2{
      text-align: center;
      padding-left: 0%;
    }
    h4{
      margin-left: auto;
      margin-right: auto;
    }
  }

@media only screen and (max-width: 434px) {
    h2{
      font-size: 5vw;
    }
  }

</style>
