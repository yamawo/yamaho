<template>
  <div class="contact">
    <h1>{{pageName}}</h1>
   
    <div v-for="item in list" :key=item>
    	{{item}}
    </div>
  </div>
</template>
<script>
	export default{
		name:"contact",
		data(){
			return {
				pageName:"Contact",
				list:["e-mail : y7a3m1asaki@gmail.com","Twitter : @tamachan_zzz","Instagram : yamao_123","GitHub : yamawo"]
			}
		},
		methods:{
			
		}
	}
</script>
<style scoped>
	
	
</style>
