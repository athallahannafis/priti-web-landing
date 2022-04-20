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

        <div class="fitur-container">
            <div class="flex flex-column align-items-start grid my-8 pt-90">
                <h1>Fitur</h1>
                <div class="fitur-content ">
                    <p>
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce dictum commodo massa sit amet bibendum. Curabitur molestie id eros quis interdum. Praesent eleifend pretium leo, eu faucibus leo porttitor ac. Duis dignissim, mauris et ornare cursus, dui quam consequat tortor, ut pulvinar leo ex nec orci. Suspendisse suscipit, mi nec suscipit rutrum, erat mi fringilla ex, ac suscipit dui lectus ac tortor. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce dictum commodo massa sit amet bibendum. Curabitur molestie id eros quis interdum. Praesent eleifend pretium leo, eu faucibus leo porttitor ac. Duis dignissim, mauris et ornare cursus, dui quam consequat tortor, ut pulvinar leo ex nec orci. Suspendisse suscipit, mi nec suscipit rutrum, erat mi fringilla ex, ac suscipit dui lectus ac tortor. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce dictum commodo massa sit amet bibendum. Curabitur molestie id eros quis interdum. Praesent eleifend pretium leo, eu faucibus leo porttitor ac. Duis dignissim, mauris et ornare cursus, dui quam consequat tortor, ut pulvinar leo ex nec orci. Suspendisse suscipit, mi nec suscipit rutrum, erat mi fringilla ex, ac suscipit dui lectus ac tortor.
                    </p>
                </div>
            </div>
            <!-- <div class="flex justify-content-center col-12 lg:col-6 p-0 flex-order-1 lg:flex-order-0" style="border-radius:8px;">
                <img class="w-9" :src="'images/priti/fitur-phone.png'"/>
            </div> -->
        </div>

        <div class="mitra-container">
                <h1 class="mb-5">Mitra Kami</h1>
                <Carousel :value="salons" :numVisible="5" :numScroll="1" :circular="true" class="custom-carousel">
                    <template #item="salon">
                        <salon-card 
                        :name="salon.data.name"
                        :image="salon.data.image"
                        :city="salon.data.city" 
                        :rating="salon.data.rating"
                        :transactions="salon.data.transactions"
                        />
                    </template>
                </Carousel>
        </div>

        <div class="daftar-container mt-8 mb-8 ">
            <div class="daftar-content flex flex-column justify-content-center align-items-center text-center">
                <h1 class="mb-5">Ingin salonmu ada di Priti.id?</h1>
                <span class="daftar-desc text-2xl">Kembangkan bisnismu bersama kami, perbanyak income salonmu bersama Priti!</span>
                <Button  class="p-button-info mt-7" >
                    <span class="gabung-sekarang">
                        Gabung sekarang
                    </span>
                </Button>
            </div>
        </div>
        <!-- <img src="../../assets/priti/header-bg.png"/> -->
       
    </div>
     <div class="footer-landing flex flex-row align-items-center justify-content-between px-7 py-7">
        <div class="footer-container flex flex-column align-items-start w-3 ml-2 mr-2">
            <img style="width:120px" :src="'images/priti/logo.png'" />
            <div class="mt-3">
                <p class="footer-text">
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
                </p>
            </div>

            <div class="flex flex-row mt-8">
                <img :src="'images/priti/twitter.png'" class="ml-2 mr-2" />
                <img :src="'images/priti/instagram.png'" class="ml-2 mr-2" />
                <img :src="'images/priti/facebook.png'" class="ml-2 mr-2" />
            </div>

            <div class="footer-text mt-8">
                <p>© Priti 2022, All Rights Reserved</p>
            </div>
        </div>

        <div class="footer-container flex flex-row align-items-start justify-content-start w-3 ml-2 mr-8">
            <div class="flex flex-column align-items-start ml-6 mr-6">
                <p class="footer-text footer-title mt-2 mb-4">Tentang kami</p>
                <p class="footer-text mt-2 mb-2">Aplikasi</p>
                <p class="footer-text mt-2 mb-2">Solutions</p>
                <p class="footer-text mt-2 mb-2">Blog</p>
                <p class="footer-text mt-2 mb-2">Company</p>
            </div>
            <div class="flex flex-column align-items-start ml-6 mr-6">
                <p class="footer-text footer-title mt-2 mb-4">Mitra</p>
                <p class="footer-text mt-2 mb-2">Mitra</p>
                <p class="footer-text mt-2 mb-2">Gabung</p>
            </div>
            <div class="flex flex-column align-items-start ml-6 mr-6">
                <p class="footer-text footer-title mt-2 mb-4">Fitur</p>
                <p class="footer-text mt-2 mb-2">Fitur</p>
                <p class="footer-text mt-2 mb-2">Unduh</p>
            </div>
        </div>
    </div>
</template>

<script>
import PritiTopBar from './PritiTopBar.vue';
// import Paginator from 'primevue/paginator';
import SalonCard from './SalonCard.vue'


export default {
    components: {
        'PritiTopBar': PritiTopBar,
        // 'Paginator': Paginator,
        'SalonCard': SalonCard,
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
    margin-top:22em;
    margin-left: 6em;
    margin-right: 10em;
    position:absolute;    
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
    padding-left: 10em;
    padding-right: 10em;
    background-image: url("../../../public/images/priti/fitur.png");
    background-repeat: no-repeat;
    background-size: 100%;
    height: 70em;
    display: flex;
    flex-direction: row;
    align-items: center;
}
.fitur-container h1 {
    font-family: 'Poppins', sans-serif;
    font-weight: 600;
    color: white;
}
.fitur-container img {
    
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
.custom-carousel {
    min-width: 100rem; 
    max-width:100rem;
}
.daftar-container {
    display: flex;
    flex-direction: column;
    align-items: center;
}
.daftar-content {
    border-radius: 10px;
    background: white;
    padding: 10em;
    padding-top:4em;
    padding-bottom:4em;
    border-width: 1px;
    border-style: solid;
    border-color: #d0d0d0;
}
.daftar-content h1 {
    font-family: 'Poppins', sans-serif;
    font-weight: 600;
    color:#005faa;
}
.daftar-desc {
    font-family: 'Open Sans', sans-serif;
    color: #6f809a
}
.gabung-sekarang {
    font-family: 'Open Sans', sans-serif;
    color: white;
    font-weight: bolder;
}
.footer-landing {
    background: white;

}
.footer-text {
    font-family: 'Open Sans', sans-serif;
    color: #454545;
    font-size:24px;
}
.footer-title {
    color:#005faa;
    font-weight: bold;
}
</style>
