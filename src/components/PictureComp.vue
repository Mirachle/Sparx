<template>
  <div>
    <img class="image" :src="picture.img" alt="shoe">
  </div>
</template>

<script>
export default {
  name: 'PictureComp',
  props: ['picture'],
};
</script>

<style>
.image{
  width: 500px;
  height: 500px;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}

@media only screen and (max-width: 1200px) {
    .image{
      margin-left: 10vw;
      margin-right: auto;
      width: 50vw;
      height: 50vw;
    }
  }
</style>
