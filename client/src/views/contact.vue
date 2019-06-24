<template>
  <div class="contact">
    <h1>This is a {{pageName}} page</h1>
    {{getNow()}}
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
				pageName:"contact",
				list:["y","m","w"]
			}
		},
		methods:{
			getNow(){
				return Date.now().toString();
			}
		}
	}
</script>
<style>
	
</style>
