<template>
   <div class="book">
       <p>{{ Book.book }}
           <button v-on:click="deleteBook">Xóa</button>
       </p>
       
    </div>
</template>

<script>
export default {
    name: 'book',
    props:{
        Book: {
            type: Object,
            default: null
        }
    },
    data(){
        return{
            
        }
    },
    methods:{
        deleteBook(){
            console.log("1")
            var data = {
                id: this.Book.id
            }
            this.$emit("deleteBook",data)
        }
    }
}
</script>

<style>

</style>