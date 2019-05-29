<template>
  <div class="full">
    <div class="row" v-for="(item,index) in list" :key="index">
      <div><span></span>{{item}}</div>
    </div>
  </div>
</template>


<script>
export default {
  name: 'Description',
  data() {
    return {
      list: ['Comfortable and Durable Canvas Sports Shoes', 'Attitude that makes you your own competition', 'Style that rises to make every eye fall', 'Adventure that makes you live life on the edge'],
    };
  },
};
</script>


<style scoped>
span{
  width: 9px;
  height: 9px;
  border-radius: 50%;
  border: 0;
  background-color: #d4d4d4;
  display: inline-block;
  margin-right: 5px;
}

.row{
  font-family: Helvetica;
  font-size: 13px;
  font-weight: 300;
  font-style: normal;
  font-stretch: normal;
  line-height: 1.85;
  letter-spacing: normal;
  text-align: justify;
  color: #111111;
}

.full{
  margin-bottom: 5vh;
}

@media only screen and (max-width: 1200px) {
    .full{
      margin-left: auto;
      margin-right: auto;
    }
  }


</style>
