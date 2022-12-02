<template lang="">
    <div>
        <div class="image-box">
            <img src="@/assets/images/icon-previous.svg" alt="prev" class="previous" @click="plusSlides(-1)">
            <img src="@/assets/images/image-product-1.jpg" alt="product-1" class="slides">
            <img src="@/assets/images/image-product-2.jpg" alt="product-2" class="slides">
            <img src="@/assets/images/image-product-3.jpg" alt="product-3" class="slides">
            <img src="@/assets/images/image-product-4.jpg" alt="product-4" class="slides">
             <img src="@/assets/images/icon-next.svg" alt="next" class="next" @click="plusSlides(1)">
            <div class="thumbnail-wrapper">
                <div class="thumbnails" @click="currentSlide(1)"><img src="@/assets/images/image-product-1-thumbnail.jpg" alt="thumbnail-1"></div>
                <div class="thumbnails" @click="currentSlide(2)"><img src="@/assets/images/image-product-2-thumbnail.jpg" alt="thumbnail-2"></div>
                <div class="thumbnails" @click="currentSlide(3)"><img src="@/assets/images/image-product-3-thumbnail.jpg" alt="thumbnail-3"></div>
                <div class="thumbnails" @click="currentSlide(4)"><img src="@/assets/images/image-product-4-thumbnail.jpg" alt="thumbnail-4"></div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    methods: {
        plusSlides(n){
            this.showSlides(this.slideIndex += n);
        },
        currentSlide(n){
            this.showSlides(this.slideIndex = n);
        },
        showSlides(n){
          let i;
          let slides = document.getElementsByClassName("slides");
          let dots = document.getElementsByClassName("thumbnails");
          if (n > slides.length) {this.slideIndex = 1}
          if (n < 1) {this.slideIndex = slides.length}
          console.log(this.slideIndex);

          for (i = 0; i < slides.length; i++) {
              slides[i].style.display = "none";
          }
          for (i = 0; i < dots.length; i++) {
              dots[i].className = dots[i].className.replace(" active", "");
          }
          slides[this.slideIndex-1].style.display = "block";
          dots[this.slideIndex-1].className += " active";
        }
    },
}
</script>
<style >
</style>