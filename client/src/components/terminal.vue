<template>
    <div class="container">
        <div class="head">
            <img class="window-button" src="../assets/singou.png">
        </div>
        <div class="terminal">
            <div class="wrapper">
                <div class="time">Last login:{{timeCommandLineFormat()}} on tty0731</div>
                <div v-for="command in commands">
                    <div ><span class='command'>yamawo@127.0.0.1 ~/develop $ </span>{{command[0]}}</div>
                    <div v-html="command[1]"/>
                </div>
                <span class='command'>yamawo@127.0.0.1 ~/develop $ </span>vim hello.go <span class="cursor"></span>
            </div>
        </div>
    </div>
</template>


<script>
    export default {
        name:"terminal",
    	data(){
    		return{
    			now : new Date(),
    			commands : [
	                ["whoami","Yamasaki Shota"],
	                ["birth","1995/07/31"],
	                ["hobby","Soccer,Playing FIFA,Programming"],
	                ["mail","y7a3m1asaki[at]gmail.com"]
	            ],
    		}
    	},
    	methods:{
	        timeCommandLineFormat(){
	            const months = ["Jan","Feb","Mar","Apr","May","Jun","Jul","Aug","Sep","Oct","Nov","Dec"];
	            const weeks = ["Sun","Mon","Tue","Wed","Thu","Fri","Sat"];
	            let year = this.now.getFullYear();
	            let month = months[this.now.getMonth()];
	            let week = weeks[this.now.getDay()];
	            let day = this.now.getDate();
	            let hour = this.now.getHours()+1;
	            let minutes = this.now.getMinutes()+1;
	            let seconds = this.now.getSeconds()+1;
	            return week+" "+month+" "+day+" "+year+" "+hour+":"+minutes+":"+seconds;
	        }
    	}

    };
</script>

<style scoped lang="scss">
    .container{
        color: white;
        .head{
            background: lightgrey;
            border-top-left-radius: 1em;
            border-top-right-radius: 1em;
            .window-button{
                width: 7vw;
                padding:0.5em;
                height:auto;
            }
        }
        .terminal{
            font-size: 1.5vw;
            background-color: black;
            top:0;
            border-bottom-left-radius: 1em;
            border-bottom-right-radius: 1em;
            .command{
                color:rgb(49,103,69);
            }
            .cursor::after {
                content: "";
                top: 0;
                right: -15px;
                display: inline-block;
                background-color: white;
                vertical-align: middle;
                width: 10px;
                height: 24px;
                -webkit-animation: blink 1s step-end infinite;
                animation: blink 1s step-end infinite;
            }
        }
    }

@media screen and (max-width : 600px) {
    .container{
        color: white;
        width:80vw;
        .head{
            background: lightgrey;
            border-top-left-radius: 1em;
            border-top-right-radius: 1em;
            .window-button{
                width: 20vw;
                height:auto;
            }
        }
        .terminal{
            font-size: 2.7vw;
            background-color: black;
            top:0;
            border-bottom-left-radius: 1em;
            border-bottom-right-radius: 1em;
            .command{
                color:rgb(49,103,69);
            }
            .cursor::after {
                content: "";
                top: 0;
                right: -15px;
                display: inline-block;
                background-color: white;
                vertical-align: middle;
                width: 8px;
                height: 15px;
                -webkit-animation: blink 1s step-end infinite;
                animation: blink 1s step-end infinite;
            }
        }
    }
}
.wrapper{
    padding: 15px;
}

@-webkit-keyframes blink {
    0% { opacity: 1.0; }
    50% { opacity: 0.0; }
    100% { opacity: 1.0; }
}

@keyframes blink {
    0% { opacity: 1.0; }
    50% { opacity: 0.0; }
    100% { opacity: 1.0; }
}


</style>
