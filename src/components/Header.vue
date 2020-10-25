<template>
    <header>
        <div class="logo_holder">
            <a href="index.php" class="logo"><img src="../assets/images/Logo@2x.png" /></a>
        </div>

        <!-- navigation -->
        <nav>
            <div class="menu" v-on:click="showMenu">
                <span class="menu_bar top_menu"></span>
                <span class="menu_bar mid_menu"></span>
                <span class="menu_bar btm_menu"></span>
                <span class="menu_block"></span>
            </div>
        </nav>

        <div class="main_nav">
            <a id="btnServices" alt="Services" href="#">Services</a>
            <a id="btnPrices" alt="Prices" href="#">Prices</a>
            <a id="btnContact" alt="Contact" href="#">Contact</a>
        </div>
    </header>
</template>

<script>
import $ from 'jquery'

export default{
    methods:{
        showMenu(){
            $('.menu_bar').toggleClass('animate');
            $('.main_nav').toggleClass('active');
        }
    }
}
</script>