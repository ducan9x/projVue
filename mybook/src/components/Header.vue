<template>
  <header>
    {{ text }}
    <br>
    <button v-on:click="changeTextHeader">Thay đổi title</button>
  </header>
</template>

<script>
export default {
    name: 'comp-header',
    props:{
        text:String,
        default: "giá trị mặc định"
    },
    data(){
        return {
        }
    },
    methods:{
        changeTextHeader() {
            var data = {
                text: "chán lắm cơ !"
            }
            this.$emit('changeTextEvent',data)
        }
    }
}
</script>

<style>

</style>