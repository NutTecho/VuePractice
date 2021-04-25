<template>
  <b-carousel id="slider" 
        controls
        indicators
         >
    <div v-for="item in items" :key="item.caption">
      <b-carousel-slide 
          :caption=item.caption
          :text=item.text
          :img-src=item.image
          >
      </b-carousel-slide>
    </div>
    </b-carousel>
</template>
<script>
export default ({
  data()
  {
    return{
      items : [
        {caption:"first page",text:"this is first page",image:require("@/assets/image/sea1.JPG")},
        {caption:"second page",text:"this is second page",image:require("@/assets/image/sea2.JPG")},
        {caption:"third page",text:"this is third page",image:require("@/assets/image/sea3.JPG")},
        {caption:"fourth page",text:"this is fourrth page",image:require("@/assets/image/sea4.JPG")}
      ]
    }
  }
})
</script>
<style>
.carousel-item {
    width: 100%;
}
.carousel-caption {
        color: gold;
        text-align: right;
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        font-size:50%;
        }
</style>
