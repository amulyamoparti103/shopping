<template>
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
        <a class="navbar-brand" href="#">SHOPPING PRODUCTS</a>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
            <div class="navbar-nav">
                <router-link to="/"> <a class="nav-item nav-link" href="#">Home</a></router-link>
                <router-link to="/shopping"> <a class="nav-item nav-link" href="#">Shopping Products </a></router-link>                
                <!-- <router-link to="/cart"><button class="btn"><a class="nav-iem nav-link" href="#">Cart</a></button></router-link> -->
                <!-- <router-link to="/fruits"> <a class="nav-item nav-link" href="#">Fruits</a></router-link> -->
                <!-- <a class="nav-item nav-link disabled" href="#">Disabled</a> -->
            </div>
        </div>
        <div class="btn">
            <router-link to="/cart"><button class="cart">Cart ({{ cout }})</button></router-link>
            <!-- <shopping/> -->
        </div>
    </nav>
</template>

<script>
// import shopping from "../views/shopping";
export default {
    components:{
        // shopping
    }
}
</script>

<style>
    .btn{
        float:right;
        /* background-color:#337ab7 ; */
    }
    .cart{
        background-color:#337ab7 ;
        border:1px solid #337ab7;
        color:white;
        padding:2px 10px; 
        /* letter-spacing: 1px; */

    }
</style>