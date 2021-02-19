<template>
    <div class="listbook">list book
    <Book 
    v-for="Book in listbook" 
    v-bind:key="Book.id"
    v-bind:Book="Book"
    v-on:deleteBook="deleteBook"
    />
    </div>
</template>

<script>
import Book from "./Book.vue";

export default {
    name: 'list-book',
    props:{
        listbook:{
            type: Array,
            default:[]
        }
    },
    data(){
        return{
            
        }
    },
    components: {
        Book
    },
    methods:{
        deleteBook(data){
            console.log("2",data)
            this.$emit("deleteBookEvent",data)
        }
    }
}
</script>

<style>

</style>