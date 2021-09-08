<template>

  <div class="alert alert-danger" style="text-align:center;width:400px;margin:10px auto">
    <h4 class="select" v-on:click="doAction" style="cursor: pointer">{{ number }}:{{ select }}</h4>
  </div>
</template>

<script>
export default {
  name:"sentaku",
  props:{
    title:String,
    select:String,
    answer:Boolean,
    number:String,
  },
  methods:{
      doAction(){
          console.log(this.answer)
          if(this.answer){
              document.getElementsByClassName("title")[0].innerText="┌∧∧∧∧┐\n＜　正解　＞\n└∨∨∨∨┘"
            // this.$refs.title.innerHTML="正解"
          }else{
              document.getElementsByClassName("title")[0].innerText="┌∧∧∧∧∧┐\n＜　不正解　＞\n└∨∨∨∨∨┘"
            //   this.$refs.title.innerHTML="不正解"
          }
      },
  }
}
</script>