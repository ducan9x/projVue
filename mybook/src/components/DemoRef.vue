<template>
  <div class="demo-ref">
      <button class="btn-avata"
      v-on:click="handleChangeImage"
      >Thay đổi ảnh đại diện</button>
      <input ref="updateImage" type="file" style="display: none"/>
  </div>
</template>

<script>
export default {
    name: 'demoref',
    data(){
        return{
            
        }
    },
    methods:{
        handleChangeImage(){
            this.$refs.updateImage.click()
        }
    }
}
</script>

<style>
    .demo-ref{
        width: 600px;
        height: 200px;
        margin: 20px;
        border:1px solid black;
        margin: auto;
        padding-top: 80px;
        box-sizing: border-box;
    }
    .btn-avata{
        cursor: pointer;
        width: 90px;
        height: 40px;
        background-color: black;
        border: 1px solid #333;
        color: white;
    }
</style>