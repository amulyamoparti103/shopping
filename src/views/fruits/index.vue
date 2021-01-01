<template>
   <div>
      <b-container>
         <b-row>
            <b-col>
               <h2>Products</h2>
            </b-col>
         </b-row>
         <b-row>
            <b-col v-for="product in products" :key="product.id">
               <b-card
                  :title="product.name"
                  :img-src="require('@/assets/product${product.id}.jpg')"
                  img-alt="image"
                  img-top
                  tag="article"
                  style="max-width:20rem;"
                  class="mb-2"
               >
               <b-card-text>
                  price: {{ product.price }}
               </b-card-text>
               <b-button v-if="!product.cart" @click="add(product)" href="#" variant="primary">Add To Shipping Cart</b-button>
               <b-button v-if="!product.cart" @click="add(product)" :disabled="product.cart" href="#" variant="warning">product Added To Shipping Cart</b-button>
               </b-card>
            </b-col>
         </b-row>
         <b-row>
            <b-col>
               <b-table bordered hover:items="cart" :fields="fields">
                  <template slot="#" slot-scope="data">
                     {{data.index+1}}
                  <template>
                  <template> slot="price" slot-slope="data">
                  <template>
                  <template> slot="remove" slot-slope="data"
                     {{data.item.price*data.item}}
</template>

<script>
export default {

}
</script>

<style>

</style>