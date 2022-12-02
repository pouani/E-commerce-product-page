<template lang="">
    <div>
        <div class="caroussel">
            <img src="@/assets/images/icon-previous.svg" alt="prev" class="caroussel-btn previous md:hidden" @click="plusSlides(-1)">
            <div class="rounded-xl overflow-hidden mb-3">
                <img src="@/assets/images/image-product-1.jpg" alt="product-1" class="slides">
                <img src="@/assets/images/image-product-2.jpg" alt="product-2" class="slides">
                <img src="@/assets/images/image-product-3.jpg" alt="product-3" class="slides">
                <img src="@/assets/images/image-product-4.jpg" alt="product-4" class="slides">
            </div>
             <img src="@/assets/images/icon-next.svg" alt="next" class="caroussel-btn next md:hidden" @click="plusSlides(1)">
            <ul class="thumbnail-wrapper flex gap-6 list-none">
                <li class="thumbnails" @click="currentSlide(1)"><img src="@/assets/images/image-product-1-thumbnail.jpg" alt="thumbnail-1"></li>
                <li class="thumbnails" @click="currentSlide(2)"><img src="@/assets/images/image-product-2-thumbnail.jpg" alt="thumbnail-2"></li>
                <li class="thumbnails" @click="currentSlide(3)"><img src="@/assets/images/image-product-3-thumbnail.jpg" alt="thumbnail-3"></li>
                <li class="thumbnails" @click="currentSlide(4)"><img src="@/assets/images/image-product-4-thumbnail.jpg" alt="thumbnail-4"></li>
            </ul>
        </div>
    </div>
</template>
<script>
export default {
    data (){
        return {
            slideIndex: 1,
        }
    },
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
    mounted() {
         this.showSlides(this.slideIndex);
    },
}
</script>
<style >
.thumbnails{
    border-radius: .6rem;
    overflow: hidden;
}
.thumbnails:hover{
  cursor: pointer;
  opacity: 0.5;
}
.active.thumbnails{
    opacity: 0.3;
}
.slides {
  display: none;
}

.slides img {
    height: auto;
    border-radius: 5px;
}

.caroussel{
    max-width: 35rem;
    min-width: 25rem;
}

/* .caroussel-btn{
    position: absolute;
    top: 30%;
}
.next{
    left: 40rem;
} */
</style>