<template>
	<div id="blogr-middle">
		<div class="middle-container">
			<div class="middle-content-left">
				<img src="../assets/illustration-phones.svg" alt="">
			</div>
			<div class="middle-content-right">
				<h1>State of the Art Infrastructure</h1>
				<p>
					With reliability and speed in mind, worldwide data centers provide the backbone for ultra-fast connectivity. 
  					This ensures your site will load instantly, no matter where your readers are, keeping your site competitive.
				</p>
			</div>
		</div>
	</div>
</template>

<style scoped>

#blogr-middle{
	background: url(../assets/bg-pattern-circles.svg), linear-gradient(to right, hsl(237, 17%, 21%), hsl(237, 23%, 32%));
    background-repeat: no-repeat, no-repeat;
    background-position: calc(100% - 45vw) calc(100% - -5vw), center;
    background-size: 70vw, 100%;
    position: relative;
    border-radius: 0 85px 0 85px;
    width: 100%;
}

.middle-container{
	display: grid;
	grid-template-columns: 50% 50%;
	min-height: 410px;
}

.middle-content-right{
    margin-left: auto;
    margin-right: 0;
    padding-top: 80px;
    color: #fff;
    padding-right: 15vw;
}

.middle-content-left{
    position: relative;
}

.middle-content-left img{
    position: absolute;
    top: -70px;
    left: 40%;
    transform: translate(-40%);
}

@media screen and (max-width: 991px) {
	.middle-content-left img{
		top: 53%;
		transform: translate(-40%, -50%);
		width: 55vw;
	}
}

@media screen and (max-width: 800px) {

	#blogr-middle{
		background-position: calc(100% - -30vw) calc(20% - 80vw), center;
    	background-size: 165vw, 100%;
	}

	.middle-container{
		grid-template-columns: 100%;
		margin-top: 40%;
	}

	.middle-container .middle-content-right{
		order: 2;
		padding: 60px 10vw 35px 10vw;
	}

	.middle-container .middle-content-left{
		order: 1;
		padding: 20% 0;
	}

	.middle-container .middle-content-left img{
		width: 85%;
		top: 10%;
		left: 50%;
		transform: translate(-50%,-50%);
	}
}

</style>