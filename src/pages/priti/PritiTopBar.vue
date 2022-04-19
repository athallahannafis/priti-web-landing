<template>
    <div class="topbar-priti">
        <router-link to="/" class="layout-topbar-logo">
            <img alt="Logo" :src="topbarImage()" />
            <span>LOGO_PRITI</span>
        </router-link>

        

        <ul class="layout-topbar-menu hidden lg:flex origin-top">
            <li>
                <Button label="Tentang kami" @click="test()" class="p-button-link mr-2 mb-2 font-button-color" />
            </li>
            <li>
                <Button label="Mitra" @click="test()" class="p-button-link mr-2 mb-2 font-button-color" />
            </li>
            <li>
                <Button label="Fitur" @click="test()" class="p-button-link mr-2 mb-2 font-button-color" />
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
.topbar-bg {
    background-image: url("../../assets/priti/header-bg.png");
    background-repeat: no-repeat;
    background-size: 100%;
    height: 70em;
    position: absolute;
    z-index: -1;
}
.font-button-color{ 
    color:white;
}
</style>