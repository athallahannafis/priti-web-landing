<template>
    <div class="topbar-priti">
        <router-link to="/" class="layout-topbar-logo">
            <img alt="Logo" :src="topbarImage()" />
            <span>LOGO_PRITI</span>
        </router-link>

        

        <ul class="layout-topbar-menu hidden lg:flex origin-top">
            <li>
                <Button label="Tentang kami" @click="smoothScroll('.about-container')" class="p-button-link mr-2 mb-2 font-button-color" />
            </li>
            <li>
                <Button label="Mitra" @click="test()" class="p-button-link mr-2 mb-2 font-button-color" />
            </li>
            <li>
                <Button label="Fitur" @click="smoothScroll('.fitur-container')" class="p-button-link mr-2 mb-2 font-button-color" />
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    methods: {
        onMenuToggle(event) {
            this.$emit('menu-toggle', event);
        },
        onTopbarMenuToggle(event) {
            this.$emit('topbar-menu-toggle', event);
        },
        topbarImage() {
            return this.$appState.darkTheme ? 'images/logo-white.svg' : 'images/logo-dark.svg';
        },
        test() {
            console.log("Pressed");
        },
        smoothScroll(id){
            document.querySelector(id).scrollIntoView({
                behavior: 'smooth'
            });
        }
    },
    computed: {
        darkTheme() {
            return this.$appState.darkTheme;
        }
    }
}
</script>
<style scoped>
.font-button-color{ 
    color:white;
}
</style>