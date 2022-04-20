<template>
    <div class="salon-container">
        <div class="salon-photo">
            <img :src="image" :alt="name" class="product-image" />
        </div>
        <div>
            <h4 class="mt-1">
                {{ name }}
            </h4>
            <h6 class="mt-0 mb-3">Kota {{ city }}</h6>
            <div class="salon-footer mt-1">
                <img class="star mr-2" :src="'images/priti/star.png'"/>
                <p>{{ rating }} | {{ transactions }} transaksi</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        propTest: String,
        name: String,
        image: String,
        rating: Number,
        city: String,
        transactions: Number,
    }
}
</script>

<style scoped>
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