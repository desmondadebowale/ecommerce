<template>
<div>
    <carousel  :perpage= "1" :mousedrag= "true" :autoplay= "true">
    <slide v-for="slide in images" :key="slide.id">
    <img :src="slide.path" height="300px">
    </slide>
  </carousel>
</div>
</template>

<script>

import { Carousel, Slide } from 'vue-carousel';

export default {
    name: "productslide",
    data(){
        return{
            images: [
                {
                    path:require('../assets/sliderimage/office-chairs.png'),
                    id: 1
                },
                {
                    path:require('../assets/sliderimage/office-chairs.png'),
                    id: 2
                },
                {
                    path:require('../assets/sliderimage/office-chairs.png'),
                    id: 3
                }
            ]
        }
    },
    components: {
    Carousel,
    Slide
  }
}
</script>