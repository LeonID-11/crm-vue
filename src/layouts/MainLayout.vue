<template>
    <div class="app-main-layout">
        <Navbar @navbar="openNavbar = !openNavbar"/>
        <Sitebar v-model="openNavbar"/>

        <main class="app-content" :class="{'full': !openNavbar}">
            <div class="app-page">
                <router-view />
            </div>
        </main>

        <div class="fixed-action-btn">
            <a class="btn-floating btn-large blue" href="#">
                <i class="large material-icons">add</i>
            </a>
        </div>
    </div>
</template>

<script>
import Navbar from '@/components/main/Navbar'
import Sitebar from '@/components/main/Sitebar'
export default {
    data: ()=>({
        openNavbar: true,
    }),
    components:{
        Navbar, Sitebar
    },
    
}
</script>
