<template>
    
    <div class="container">
        <priti-top-bar/>
        <div class="banner">
            <div class="upper-title-container">
                <p>
                    Nggak repot
                </p>
                <p>
                    Buat jadi keren
                </p>
            </div>
        </div>

        <div class="about-container">
            <h1>Tentang kami</h1>
            <p>
                Lorem ipsum dolor sit amet, consectetur adipiscing elit. 
                Fusce dictum commodo massa sit amet bibendum. Curabitur molestie id eros quis interdum. 
                Praesent eleifend pretium leo, eu faucibus leo porttitor ac. 
                Duis dignissim, mauris et ornare cursus, dui quam consequat tortor, ut pulvinar leo ex nec orci.
            </p>
        </div>

        <div class="statistic-container">
            <div class="stat-comp-container">
                <img src="../../assets/priti/download.png" />
                <p class="stat">1000+</p>
                <p class="stat-detail">App diunduh</p>
            </div>
            <div class="stat-comp-container">
                <img src="../../assets/priti/user.png" />
                <p class="stat">1000+</p>
                <p class="stat-detail">Pengguna aktif</p>
            </div>
            <div class="stat-comp-container">
                <img src="../../assets/priti/rating.png" />
                <p class="stat">4.8</p>
                <p class="stat-detail">Rating di playstore</p>
            </div>
        </div>
        <!-- <img src="../../assets/priti/header-bg.png"/> -->
    </div>
</template>

<script>
import PritiTopBar from './PritiTopBar.vue';

export default {
    components: {
        'PritiTopBar': PritiTopBar,
    }
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@200;300;800&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Open+Sans&family=Poppins:wght@200;300;800&display=swap');
.container {
    background-color: #f9f9f9;
    padding-bottom: 10em;
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
}
.about-container h1{
    font-weight: 600;
    color: #005faa;
}
.statistic-container {
    width: 100%;
    margin-top: 3em;
    
    display: flex;
    flex-direction: row;
    justify-content: center;
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
</style>
