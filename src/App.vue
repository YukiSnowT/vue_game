<template>
  <div id="app">
    <mondai title="なぞなぞ" v-bind:message="que"/>
    <div class="alert">
    <h3 ref="title" class="title" style="text-align:center;width:400px;margin:30px auto 0 auto">選択肢</h3>
    </div>
    <sentaku v-bind:select="ans.A" v-bind:answer='false' number="A" />
    <sentaku v-bind:select="ans.B" v-bind:answer='false' number="B" />
    <sentaku v-bind:select="ans.C" v-bind:answer='false' number="C" />
    <sentaku v-bind:select="ans.D" v-bind:answer='true' number="D" />
  </div>
</template>

<script>
import mondai from './components/mondai.vue';
import sentaku from './components/sentaku.vue';

export default {
  name:"App",
  components:{
    mondai,
    sentaku,
  },
  data(){
    return {
      que:"根は植物。本は楽器。炭は回転。では盆は？",
      ans:{
        A:"三国志",
        B:"太陽系",
        C:"化学式",
        D:"体組織"
      }
    }
  }
}

</script>
