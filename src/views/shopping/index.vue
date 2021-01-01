<template>
    <div class="card-group">
        <cart v-bind:cartdata="items"/>
        <div class="card">
            <img src="@/assets/product1.jpg" class="card-img-top" alt="image">
            <div class="card-body">
                <h5 class="card-title" v-bind="name">Brite Tailore</h5>
                <p class="card-text">Women Jeans Light Blue Dress</p>
                <p class="card-text" v-bind:price="price">580</p>
            </div>
            <div class="card-footer">
                <div>
                    Quantity : <input class="quantity" type="number" v-model="quantity">
                </div>
                <div>
                    <button class="btn" @click="increment">Add To Cart</button>
                </div>
            </div>
        </div>
        <div class="card">
            <img src="@/assets/product2.jpg" class="card-img-top" alt="image">
            <div class="card-body">
                <h5 class="card-title" v-bind="name">TOKYO TALKS</h5>
                <p class="card-text">Women A-line Black Dress</p>
                <p class="card-text" v-bind="price">850</p>
            </div>
            <div class="card-footer">
                <div>
                    Quantity : <input class="quantity" type="number" v-model="quantity">
                </div>
                <div>
                    <button class="btn"  @click="increment">Add To Cart</button>
                </div>
            </div>
        </div>
        <div class="card">
            <img src="@/assets/product3.jpg" class="card-img-top" alt="image">
            <div class="card-body">
                <h5 class="card-title" v-bind="name">Maze</h5>
                <p class="card-text">Women Blue Shirt & Jeans Dress</p>
                <p class="card-text" v-bind="price">1500</p>
            </div>
            <div class="card-footer">
                <div>
                    Quantity : <input class="quantity" type="number" v-model="quantity">
                </div>
                <div>
                    <button class="btn"  @click="increment">Add To Cart</button>count:{{cout}}name:{{name}}Quantity:{{quantity}}Price:{{price}}
                </div>
            </div>
        </div>
    </div>
</template>

<script>
// import myNavBar form '../src/layouts/myNavBar.vue';
 import cart from '@/views/cart';
export default {
    data () {
        return {
            // quantity:'',
            // name: true,
            name:'',
            cout:0,
                // items:["Brite Tailore",'1', "580"]
                items:[
            {'name':"Brite Tailore", 'quantity':"1",'price':"580"},
            {'name':"TOKYO TALKS", 'quantity':"1",'price':"850"},
            {'name':"Maze",'quantity':"1", 'price':"1500"}
        ],

        }
    },
    methods:{
        addTocart(){
            this.$emit('increment');
            // this.quantity;
        },
         increment() {
            this.cout +=1;
            this.name;
            this.quantity;
            this.price;
        }
    },
     components:{
        // myNavBar,
        cart,
    }
    
}
</script>

<style scoped>
.card-group{
    max-width:1200px;
    margin:20px auto;
}
.card-footer{
    display:flex;
    justify-content:space-around;
}
.quantity{
    width:50px;
    border:1px solid lightgray;
}
.btn{
    background-color:#337ab7;
    border:1px solid #337ab7;
    color:white;
}
</style>