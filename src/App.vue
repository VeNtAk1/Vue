<script>
export default {
  data() {
    return {
		cost: 100,
        amount: 2,
	}
  },
  methods:{
    update_cost(){
        this.cost = 150
    },
    price: function(){
            return this.amount * this.cost
        }
    }   
}
</script>


<template>
    <button @click="update_cost">Поменять</button>
    <p> {{ price() }}</p>
</template>
