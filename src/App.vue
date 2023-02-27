<template>
  <br><br>
  <div class="inputs">
    <input type="text" placeholder="Enter Your Data" v-model="data">

    <button @click="addinput">
      Create
    </button>

  </div>
  <br>

<item_box v-for="input in inputs" :key="input.content"
:content="input.data"/>

</template>




<script>
import item_box from './components/inputs.vue';


export default{
    name: 'main_word',
    data(){
      return {
        data: '',
        inputs: [
          //here pushing process
        ]
      }
    },


    components : {
      item_box
    },


    methods:{
      addinput: function(){
        this.inputs.push({
          data: this.data
        });
        this.data = ''
      }
      }
    }
</script>





<style>
  .inputs{
    width: 30%;
    height: 30%;
    margin: auto;
  }

  input{
    text-align: center;
    width: 100%;
    padding: 10px;
  }

  button{
    margin-top: 10px;
    padding: 5px 20px;
    background-color: crimson;
    color: white;
    border: none;
  }

</style>
