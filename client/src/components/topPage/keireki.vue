<template>
	<div>
		<ul>
			<li>{{getName("yamao")}}</li>
			<li>{{getNow()}}</li>
		</ul>
		<div v-if="show">
			detaaa
		</div>
		<button @click="toggle()">toggle</button>
	</div>
</template>
<script>
	export default{
		name:"keireki",
		data(){
			return{
				numbers:[3,4,5,6,3],
				show:false
			}
		},
		methods:{
			getName(name){
				return name+"様";
			},
			getNow(){
				console.log(new Date())
				return new Date();
			},
			toggle(){
				this.show = !this.show;
			}
		}
	}
</script>
<style lang="scss" scoped>

</style>