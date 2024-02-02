<template>
    <div>
        
        <div v-for="book in books">
            <!-- BookItem -->
            <BookItem v-bind:book="book" v-on:addBookItem="AddToCart" />
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue'
//import BookItem
import BookItem from './BookItem.vue'


// props, emit
const props = defineProps(['books'])
const books =ref(props.books)
const emit = defineEmits(['addBook'])

// AddToCart
function AddToCart(book){
      emit( 'addBook'  , book )
}


</script>

<style  scoped>

</style>