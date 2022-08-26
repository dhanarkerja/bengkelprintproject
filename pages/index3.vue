<template>
<div class="container">
    <div class="row d-flex justify-content-center">
        <div class="col-12 text-center">Bengkel Print Indonesia</div>
        <div class="col-12">
            <b-carousel
                id="carousel-fade"
                style="text-shadow: 0px 0px 2px #000"
                fade
                indicators
                img-width="1024"
                img-height="480"
            >
                <b-carousel-slide
                caption="First Slide"
                img-src="../assets/images/carousel-3.png"
                ></b-carousel-slide>
                <b-carousel-slide
                caption="Second Slide"
                img-src="../assets/images/carousel-2.png"
                ></b-carousel-slide>
            </b-carousel>
        </div>
</div>
</div>
</template>
<script>
export default {
    data(){
        return {

        }
    },
}
</script>
