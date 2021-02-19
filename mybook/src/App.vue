<template>
  <div id="app">
    <Header v-bind:text="text"
    v-on:changeTextEvent="handleChangeText"
    />
    <Body v-bind:listbook="listbook" 
    v-on:deleteBookEvent="handleDeleteBookEvent"
    />
    <DemoRef />
    <Footer 
    v-bind:text="text"
    />
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Footer from "./components/Footer.vue";
import Body from "./components/ListBook.vue";
import DemoRef from "./components/DemoRef.vue";
export default {
  name: 'app',
  data () {
    return {
      text: 'Welcome to Your Vue.js App',
      listbook:[{
                id: 1,
                book: "sách văn học"
            },
            {
                id:2,
                book: "sách vật lý"
            },
            {   
                id:3,
                book: "truyện tranh"
            }]
    }
  },
  components: {
    Header,
    Footer,
    Body,
    DemoRef
  },
  methods:{
    handleChangeText(data){
      this.text = data.text,
      console.log("handleclick")
    },
    handleDeleteBookEvent(data){
      console.log("3",data)
      this.listbook.forEach((b, idx) =>{
        if(b.id === data.id){
          this.listbook.splice(idx,1)
        }
      })
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

</style>
