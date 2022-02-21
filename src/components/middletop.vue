<template>
	<div id="middletop">
		<div class="middletop-container">
			<div class="middletop-content-right">
				<h2>Introducing an extensible editor</h2>
				<p>
					Blogr features an exceedingly intuitive interface which lets you focus on one thing: creating content. 
					The editor supports management of multiple blogs and allows easy manipulation of embeds such as images, 
					videos, and Markdown. Extensibility with plugins and themes provide easy ways to add functionality or 
					change the looks of a blog.
				</p>
				<br>
				<h2>Robust content management</h2>
				<p>
					Flexible content management enables users to easily move through posts. Increase the usability of your blog 
					by adding customized categories, sections, format, or flow. With this functionality, you’re in full control.
				</p>
			</div>
			<div class="middletop-content-left">
				<img src="../assets/illustration-editor-desktop.svg" alt="">
			</div>
		</div>
	</div>
</template>

<style scoped>
#middletop{
	padding: 20px 0;
	color: hsl(237, 23%, 32%);
	overflow: hidden;
}

.middletop-container{
	padding-top: 50px;
	display: grid;
	grid-template-columns: 60% 40%;
	min-height: 690px;
}

.middletop-content-right{
    margin-left: auto;
    margin-right: 0;
    padding-top: 120px;
    color: #333;
	padding-right: 15vw;
    padding-left: 10vw;
}

.middletop-content-left{
    position: relative;
}

.middletop-content-left img{
    position: absolute;
    right: -230px;
	top: 50%;
    transform: translate(0,-50%);
    width: 770px;
}

@media screen and  (max-width: 991px) {
	.middletop-content-left img{
		right: 0;
		top: 50%;
		transform: translate(30%,-50%);
		width: 175%;
	}
}

@media screen and (max-width: 800px) {
	.middletop-container{
		grid-template-columns: 100%;
	}

	.middletop-container .middletop-content-right{
		order: 2;
		padding-top: 60px;
	}

	.middletop-container .middletop-content-left{
		order: 1;
		padding: 25% 0;
	}

	.middletop-container .middletop-content-left img{
		width: 75%;
		top: 50%;
		left: 50%;
		transform: translate(-50%,-50%);
		content: url(../assets/illustration-editor-mobile.svg)
	}
}


</style>