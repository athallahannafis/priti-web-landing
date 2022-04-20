<template>
    
    <div class="container">
        <priti-top-bar/>
        <div class="banner">
            <div class="upper-title-container px-4 lg:px-8">
                <p>
                    Nggak repot
                </p>
                <p>
                    Buat jadi keren
                </p>
            </div>
            
            <div class=" grid justify-content-center">
                <div class="about-container ">
                    <h1>Tentang kami</h1>
                    <p>
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit. 
                        Fusce dictum commodo massa sit amet bibendum. Curabitur molestie id eros quis interdum. 
                        Praesent eleifend pretium leo, eu faucibus leo porttitor ac. 
                        Duis dignissim, mauris et ornare cursus, dui quam consequat tortor, ut pulvinar leo ex nec orci.
                    </p>
                </div>
            </div>
        </div>


        <div class="statistic-container grid justify-content-center">
            <div class="stat-comp-container">
                <img src="@/assets/priti/download.png" />
                <p class="stat">1000+</p>
                <p class="stat-detail">App diunduh</p>
            </div>
            <div class="stat-comp-container">
                <img src="@/assets/priti/user.png" />
                <p class="stat">1000+</p>
                <p class="stat-detail">Pengguna aktif</p>
            </div>
            <div class="stat-comp-container">
                <img src="@/assets/priti/rating.png" />
                <p class="stat">4.8</p>
                <p class="stat-detail">Rating di playstore</p>
            </div>
        </div>

        <div class="fitur-container grid my-8 pt-2 md:pt-8">
            <h1>Fitur</h1>
            <div class="fitur-content ">
                <p>
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce dictum commodo massa sit amet bibendum. Curabitur molestie id eros quis interdum. Praesent eleifend pretium leo, eu faucibus leo porttitor ac. Duis dignissim, mauris et ornare cursus, dui quam consequat tortor, ut pulvinar leo ex nec orci. Suspendisse suscipit, mi nec suscipit rutrum, erat mi fringilla ex, ac suscipit dui lectus ac tortor. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce dictum commodo massa sit amet bibendum. Curabitur molestie id eros quis interdum. Praesent eleifend pretium leo, eu faucibus leo porttitor ac. Duis dignissim, mauris et ornare cursus, dui quam consequat tortor, ut pulvinar leo ex nec orci. Suspendisse suscipit, mi nec suscipit rutrum, erat mi fringilla ex, ac suscipit dui lectus ac tortor. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce dictum commodo massa sit amet bibendum. Curabitur molestie id eros quis interdum. Praesent eleifend pretium leo, eu faucibus leo porttitor ac. Duis dignissim, mauris et ornare cursus, dui quam consequat tortor, ut pulvinar leo ex nec orci. Suspendisse suscipit, mi nec suscipit rutrum, erat mi fringilla ex, ac suscipit dui lectus ac tortor.
                </p>
            </div>
        </div>

        <div class="mitra-container">
                <h1 class="mb-5">Mitra Kami</h1>
                <Carousel :value="salons" :numVisible="5" :numScroll="1" :circular="true" class="custom-carousel">
                    <template #item="salon">
                        <div class="salon-container">
                            <div class="salon-photo">
                                <img :src="salon.data.image" :alt="salon.data.name" class="product-image" />
                            </div>
                            <div>
                                <h4 class="mt-1">
                                    {{ salon.data.name }}
                                </h4>
                                <h6 class="mt-0 mb-3">Kota {{ salon.data.city }}</h6>
                                <div class="salon-footer mt-1">
                                    <img class="star mr-2" :src="'images/priti/star.png'"/>
                                    <p>{{ salon.data.rating }} | {{ salon.data.transactions }} transaksi</p>
                                </div>
                            </div>
                        </div>
                    </template>
                </Carousel>
            
        </div>
        <!-- <img src="../../assets/priti/header-bg.png"/> -->
    </div>
</template>

<script>
import PritiTopBar from './PritiTopBar.vue';
// import Paginator from 'primevue/paginator';
// import SalonCard from './SalonCard.vue'


export default {
    components: {
        'PritiTopBar': PritiTopBar,
        // 'Paginator': Paginator,
        // 'SalonCard': SalonCard,
    },
    data(){ 
        return {
            index: 0,
            images_path: [
                '@/assets/priti/download.png',
                '@/assets/priti/user.png',
                '@/assets/priti/rating.png'
            ],
            salons: [
                {
                    image: "images/priti/no-image.png",
                    name: "test1",
                    city: "Jakarta",
                    rating: 4.5,
                    transactions: 100,
                },
                {
                    image: "images/priti/no-image.png",
                    name: "test2",
                    city: "Jakarta",
                    rating: 4.5,
                    transactions: 100,
                },
                {
                    image: "images/priti/no-image.png",
                    name: "test3",
                    city: "Jakarta",
                    rating: 4.5,
                    transactions: 100,
                },
                {
                    image: "images/priti/no-image.png",
                    name: "test1",
                    city: "Jakarta",
                    rating: 4.5,
                    transactions: 100,
                },
                {
                    image: "images/priti/no-image.png",
                    name: "test2",
                    city: "Jakarta",
                    rating: 4.5,
                    transactions: 100,
                },
                {
                    image: "images/priti/no-image.png",
                    name: "test3",
                    city: "Jakarta",
                    rating: 4.5,
                    transactions: 100,
                },
                {
                    image: "images/priti/no-image.png",
                    name: "test1",
                    city: "Jakarta",
                    rating: 4.5,
                    transactions: 100,
                },
                {
                    image: "images/priti/no-image.png",
                    name: "test2",
                    city: "Jakarta",
                    rating: 4.5,
                    transactions: 100,
                },
                {
                    image: "images/priti/no-image.png",
                    name: "test3",
                    city: "Jakarta",
                    rating: 4.5,
                    transactions: 100,
                },
                {
                    image: "images/priti/no-image.png",
                    name: "test1",
                    city: "Jakarta",
                    rating: 4.5,
                    transactions: 100,
                },
                {
                    image: "images/priti/no-image.png",
                    name: "test2",
                    city: "Jakarta",
                    rating: 4.5,
                    transactions: 100,
                },
                {
                    image: "images/priti/no-image.png",
                    name: "test3",
                    city: "Jakarta",
                    rating: 4.5,
                    transactions: 100,
                },
                {
                    image: "images/priti/no-image.png",
                    name: "test1",
                    city: "Jakarta",
                    rating: 4.5,
                    transactions: 100,
                },
                {
                    image: "images/priti/no-image.png",
                    name: "test2",
                    city: "Jakarta",
                    rating: 4.5,
                    transactions: 100,
                },
                {
                    image: "images/priti/no-image.png",
                    name: "test3",
                    city: "Jakarta",
                    rating: 4.5,
                    transactions: 100,
                },
               
            ],
            carouselResponsiveOptions: [
                {
                    breakpoint: "1024px",
                    numVisible: 3,
                    numScroll: 3,
                },
                {
                    breakpoint: "768px",
                    numVisible: 2,
                    numScroll: 2,
                },
                {
                    breakpoint: "560px",
                    numVisible: 1,
                    numScroll: 1,
                },
            ],
        }
    }
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@200;300;800&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Open+Sans&family=Poppins:wght@200;300;800&display=swap');
:root {
    --margintop: 20em;
}
.container {
    background-color: #f9f9f9;
    padding-bottom: 10em;
    /* display: flex;
    flex-direction: column;
    align-items: center;
    align-content: center; */
}
.banner {
    background-image: url("../../assets/priti/header-bg.png");
    background-repeat: no-repeat;
    background-size: 100%;
    height: 70em;
    position: relative;
    /* z-index: -1; */
}
.upper-title-container{
    font-family: 'Poppins', sans-serif;
    font-weight:600;
    margin-top:20em;
    position:absolute;
    
    padding: 10em;
}
.upper-title-container p{
    font-size: 5em;
    color: white;
}
.about-container{
    font-family: 'Poppins', sans-serif;
    border-radius: 20px;
    background-color: white;
    margin: 10em;
    padding: 10em;
    display: flex;
    flex-direction: column;
    align-content: flex-start;
    position: absolute;
    margin-top: 60em
}
.about-container h1{
    font-weight: 600;
    color: #005faa;
}
.statistic-container {
    width: 100%;
    margin-top: 23em;
    display: flex;
    flex-direction: row;
    justify-content: center;
}
@media screen and (max-width: 1000px) {
    .statistic-container {
        margin-top: 50em;
    }
}
.statistic-container img {
    width: 9em;
    height: 8em;
}
.stat-comp-container {
    font-family: 'Open Sans', sans-serif;
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-left: 10em;
    margin-right: 10em;
}
.stat-comp-container p{
    text-align: center;
}
.stat {
    font-family: 'Poppins', sans-serif;
    font-weight: 600;
    color: #005faa;
    margin-top: 2em;
    font-size: 2em;
}
.stat-detail {
    font-family: 'Open Sans', sans-serif;
    font-size: 2em;

}
.fitur-container {
    margin-top: 10em;
    padding: 10em;
    background-image: url("../../assets/priti/fitur.png");
    background-repeat: no-repeat;
    background-size: 100%;
    height: 70em;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
}
.fitur-container h1 {
    font-family: 'Poppins', sans-serif;
    font-weight: 600;
    color: white;
}
.fitur-content {
    max-width: 55%;
}
.fitur-content p {
    font-family: 'Open Sans', sans-serif;
    color: white;
    font-size: 1.5em;
}
.mitra-container {
    margin-top: 10em;
    display: flex;
    flex-direction: column;
    align-items: center;
}
.mitra-container h1 {
    font-family: 'Poppins', sans-serif;
    font-weight: 600;
    color:#005faa;
}
.salon {
    margin-left: 2rem;
    margin-right: 2rem;
}
.custom-carousel {
    min-width: 100rem; 
    max-width:100rem;
}
.salon-container {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    background-color: white;
    margin-left: 2px;
    margin-right: 2px;
    width: fit-content;
    border-radius: 15px;
    padding: 1.5em;
    box-shadow: 0px 3px 5px rgba(0,0,0,.02), 0px 0px 2px rgba(0,0,0,.05), 0px 1px 4px rgba(0,0,0,.08);

}
.salon-container h4 {
    font-family: 'Open Sans', sans-serif;
    color: #747474;
    font-weight: 600;
}
.salon-footer {
    /* background: red; */
    display: flex;
    flex-direction: row;
    align-items: center;
}
.star {
    width: 1em;
    height: 1em;
}
</style>
