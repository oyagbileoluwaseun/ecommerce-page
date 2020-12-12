<template>
  <div class="mypics">
    <b-carousel
      id="carousel-1"
      v-model="slide"
      :interval="4000"
      controls
      background="#ababab"
      img-width=""
      img-height=""
      style="text-shadow: 1px 1px 2px #333;"
      @sliding-start="onSlideStart"
      @sliding-end="onSlideEnd"
    >
      <!-- Text slides with image -->
      <b-carousel-slide
        img-src="https://cdn.nohat.cc/thumb/f/720/d4fdb86eca3c48a5a41d.jpg"
      ></b-carousel-slide>

      <!-- Slides with custom text -->
      <b-carousel-slide img-src="https://www.alpineages.com/public/uploads/sliders/ABg2GMn3e0rCdpdItH3AUM4iyUsfv28DeFhqG3wk.jpeg">
      </b-carousel-slide>

      <!-- Slides with image only -->
      <b-carousel-slide img-src="https://i.pinimg.com/originals/03/11/62/0311622466bc4c9406c411cc8417888d.jpg"></b-carousel-slide>

      <!-- Slides with img slot -->
      <!-- Note the classes .d-block and .img-fluid to prevent browser default image alignment -->
      <b-carousel-slide>
        <template #img>
          <img
            class="d-block img-fluid w-100"
            width=""
            height=""
            src="https://image.freepik.com/free-vector/abstract-colorful-sale-theme-wallpaper_23-2148417226.jpg"
            alt="image slot"
          >
        </template>
      </b-carousel-slide>
    </b-carousel>

  </div>
</template>

<script>
  export default {
    data() {
      return {
        slide: 0,
        sliding: null
      }
    },
    methods: {
      
    }
  }
</script>

<style>
#carousel-1 img {
  
  height:320px;
}

.mypics{
width:1000px;
margin-left: 133px;
margin-top: 25px;
}

#carousel-1 > controls{
    color: red;
}

</style>