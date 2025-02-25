<script>
export default {
  data() {
    return {
		text: 'xxx',
	}
  },
  methods:{
    change(){
        this.text = "ууу"
    },
    update_1: function(){
        this.text = "ppp"
    },
    update_2(){
        this.text = "eee"
    }
  }
};
</script>


<template>
  {{ text }}
  <br>
  <button @click="change">Поменять на ууу</button>
  <br>
  <button @click="update_1" style="margin-top: 10px;">Поменять на ррр</button>
  <br>
  <button @click="update_2" style="margin-top: 10px;">Поменять на еее</button>

</template>
