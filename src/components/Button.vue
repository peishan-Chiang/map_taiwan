<script>
export default {
  components: {
   
  },
  props:[
      "district"
  ],
  data() {
    return {
        
    }
  },
  methods: {
    
  },
  // 生命週期
  mounted() {
    // this.fn();


  }
}




</script>

<template>
  <button type="button" class="cityBtn">
   <p>{{ district }} </p> 
    </button>
</template>

<style scoped>
.cityBtn{
    margin: 10px;
    border: 2px solid #58645f;
    background: #aabcb5;
    color: rgb(67, 70, 64);
    width: 10vw;
    height: 2vw;
    display: flex;
    justify-content: center;
    border-radius: 5px;
    
    
    
}
p{
    flex-direction: column;
    display: flex;
    justify-content: center;
     align-items: center;
        text-align: center;
    }
.cityBtn:hover{
    background: #414845;
    color: rgb(243, 244, 241);
    transition: 1s;
}
.cityBtn:active{
    scale: 0.8;
}

</style>
