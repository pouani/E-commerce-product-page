<template lang="">
    <div class="product flex items-center">
        <div class="flex gap-32 items-center">
            <Carousel />
            <div class="product_content flex flex-col gap-8">
                <div class="product_content-head">
                    <h3>sneaker company</h3>
                    <h2 class="mt-2">Fall Limited Edition Sneakers</h2>
                </div>
                <p class="product_content-text mt-2">
                    These low-profile sneakers are your perfect casual wear companion.
                    Featuring a durable rubber outer sole, they'll withstand everything the weather can offer
                </p>
                <div class="product_content-price">
                    <ul class="list-none flex items-center gap-4">
                        <li class="product_content-price-new">$125.00</li>
                        <li class="product_content-price-reduction">50%</li>
                    </ul>
                    <p>$250.00</p>
                </div>
                <div class="product_content-btn flex items-center gap-3">
                    <div class="product_content-btn-inc">
                        <button><img src="@/assets/images/icon-minus.svg" /></button>
                        <input type="text">
                        <button><img src="@/assets/images/icon-plus.svg" /></button>
                    </div>
                    <button class="btn-add flex items-center gap-4">
                        <img src="@/assets/images/icon-cart.svg" />
                        <span>Add to cart</span>
                    </button>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
import Carousel from './Carousel.vue'
export default {
    components: {
        Carousel
    }
}
</script>
<style scoped>

    

    @media only screen and (min-width: 768px){
        .product{
            height: 100vh;
            padding: 0 5rem;
        }
        .product_content{
            max-width: 28rem;
        }
    }

    @media only screen and (min-width: 1290px){
        .product{
            padding: 0 16rem;
        }
    }
</style>