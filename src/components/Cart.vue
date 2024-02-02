<template>
    <div>
        <div v-if="props.cart.length>0" v-for="item in props.cart">
            <!-- CartItem --> 
            <CartItem :cartItem="item" @increaseCartItem = "Increase"/>
            

        </div>
        <div v-else>
            <div class="cart-empty" >
                <img src="../assets/empty.png" style="height: 130px;" alt="" srcset="">
            </div>
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue'
//import CartItem
import CartItem from './CartItem.vue'

// props, emit
const props = defineProps(['cart'])
const emit = defineEmits(['increaseCartItem','decreaseCartIiem'])


// Increase
function Increase(bookid){
    emit('increaseCart',bookid)
}


// Decrease




// Remove



</script>

<style  scoped>

</style>