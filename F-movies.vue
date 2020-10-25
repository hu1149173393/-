<template>
  <div class="F_movies">
        <Carousel autoplay v-model="value2" loop>
        <CarouselItem>
            <div class="demo-carousel"><img :src="image1" alt="" class="homepage_background_img"></div>
        </CarouselItem>
        <CarouselItem>
            <div class="demo-carousel"><img :src="image2" alt="" class="homepage_background_img"></div>
        </CarouselItem>
        <CarouselItem>
            <div class="demo-carousel"><img :src="image3" alt="" class="homepage_background_img"></div>
        </CarouselItem>
        <CarouselItem>
            <div class="demo-carousel"><img :src="image4" alt="" class="homepage_background_img"></div>
        </CarouselItem>
    </Carousel>
  </div>
</template>

<script>
export default {
    name:'F_movies',
    data(){
      return {
        movie:'',
        value2: 0,
        image1: require('../../assets/04.jpg'),
        image2: require('../../assets/05.jpg'),
        image3: require('../../assets/07.jpg'),
        image4: require('../../assets/08.jpg'),
      }
    },
    created(){

    },
    methods:{

    },
    computed:{
      
    },
}
</script>

<style>

</style>