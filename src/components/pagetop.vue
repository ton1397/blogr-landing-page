<template>
	<div id="blogr-pagetop">
		<navbar/>
		<div class="pagetop-content">
			<h1>A modern publishing platform</h1>
			<p>Grow your audience and build your online brand</p>
			<button class="btn-light">Start for Free</button>
			<button class="btn-outline-light">Learn More</button>
		</div>
	</div>
</template>

<script>
	import navbar from "./navbar.vue";
	export default {
		components:{
			navbar
		}
	};
</script>

<style>
#blogr-pagetop{
	background: url(/img/bg-pattern-intro-desktop.f48a1c78.png), linear-gradient(to right, hsl(13, 100%, 72%), hsl(353, 100%, 62%));
    background-repeat: no-repeat, no-repeat;
    background-position: calc(100% - -65vw), center;
    background-size: 195vw, 100%;
    padding-bottom: 80px;
    position: relative;
	border-radius: 0 0 0 85px;
}

.pagetop-content{
	text-align: center;
	background: url(../assets/bg-pattern-intro-desktop.png);
}

.pagetop-content button{
	margin: 5px;
}



.pagetop-content h1{
	color: #fff;
    margin: 30px 0 15px 0;
	font-size: 3em;
}

.pagetop-content p{
	color: #f5d7d7;
	margin: 15px 0 30px 0;
}

.pagetop-img{
	width: 500px;
    height: 400px;
}
@media screen and (max-width: 699px) {
	.pagetop-content h1 {
		font-size: 2.5em;
		padding: 0 5%;
	}
}
</style>