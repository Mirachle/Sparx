<template>
  <div>
    <p>{{listTitle}}</p>
    <div class="row">
      <div class="col-lg-3 col-sm-6 col-12" v-for="(item,index) in listShoe" :key="index">
        <list-item @clicked="changeItem" :item="item" :index="index"/>
      </div>
    </div>
  </div>
</template>

<script>
import ListItem from '@/components/ListItem';

export default {
  name: 'ListComp',
  props: ['listShoe'],
  components: {
    'list-item': ListItem,
  },
  data() {
    return {
      listTitle: 'Customers Who Bought This Item Also Bought',
    };
  },
  methods: {
    changeItem(index) {
      this.$emit('change', index);
    },
  },
};
</script>

<style>

p{
  font-family: Helvetica;
  font-size: 18px;
  font-weight: normal;
  font-style: normal;
  font-stretch: normal;
  line-height: 1.52;
  letter-spacing: normal;
  color: #111111;
  margin-left: 3vw;
  margin-top:5vh;
}

@media only screen and (max-width: 1200px) {
    p{
      text-align: center;
      margin-left: 0%;
    }
  }

</style>
