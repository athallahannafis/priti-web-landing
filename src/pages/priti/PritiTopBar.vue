<template>
    <div class="layout-topbar">
        <router-link to="/" class="layout-topbar-logo">
            <img alt="Logo" :src="topbarImage()" />
            <span>SAKAI</span>
        </router-link>

        <button class="p-link layout-topbar-menu-button layout-topbar-button"
            v-styleclass="{ selector: '@next', enterClass: 'hidden', enterActiveClass: 'scalein', 
            leaveToClass: 'hidden', leaveActiveClass: 'fadeout', hideOnOutsideClick: true}">
            <i class="pi pi-ellipsis-v"></i>
        </button>
        

        <ul class="layout-topbar-menu hidden lg:flex origin-top">
            <li>
                <Button label="Tentang kami" @click="test()" class="p-button-link mr-2 mb-2" />
            </li>
            <li>
                <Button label="Mitra" @click="test()" class="p-button-link mr-2 mb-2" />
            </li>
            <li>
                <Button label="Fitur" @click="test()" class="p-button-link mr-2 mb-2" />
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