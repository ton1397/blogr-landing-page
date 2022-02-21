<template>
	<div id="blogr-middlebottom">
		<div class="middlebottom-container">
			<div class="middlebottom-content-left">
				<img src="../assets/illustration-laptop-desktop.svg" alt="">
			</div>
			<div class="middlebottom-content-right">
				<h1>Free, open, simple</h1>
				<p>
					Blogr is a free and open source application backed by a large community of helpful developers. It supports 
					features such as code syntax highlighting, RSS feeds, social media integration, third-party commenting tools, 
					and works seamlessly with Google Analytics. The architecture is clean and is relatively easy to learn.
				</p>

				<h1>Powerful tooling</h1>
				<p>
					Batteries included. We built a simple and straightforward CLI tool that makes customization and deployment a breeze, but
					capable of producing even the most complicated sites.
				</p>
			</div>
		</div>
	</div>
</template>

<style scoped>

#blogr-middlebottom{
	padding-bottom: 90px;
}

.middlebottom-container{
	padding-top: 50px;
	display: grid;
	grid-template-columns: 40% 60%;
}

.middlebottom-content-right{
    margin-left: auto;
    margin-right: 0;
    padding-top: 120px;
    color: #333;
	padding-right: 15vw;
    padding-left: 10vw;
}

.middlebottom-content-left{
    position: relative;
}

.middlebottom-content-left img{
    position: absolute;
    left: -217px;
    width: 770px;
}

@media screen and  (max-width: 991px) {
	.middlebottom-content-left img{
		left: -99%;
		top: 50%;
		transform: translate(30%,-50%);
		width: 175%;
	}
}

@media screen and (max-width: 800px) {
	.middlebottom-container{
		grid-template-columns: 100%;
	}

	.middlebottom-container .middlebottom-content-right{
		order: 2;
		padding-top: 60px;
	}

	.middlebottom-container .middlebottom-content-left{
		order: 1;
		padding: 25% 0;
	}

	.middlebottom-container .middlebottom-content-left img{
		width: 100%;
		top: 50%;
		left: 50%;
		transform: translate(-50%,-50%);
		content: url(../assets/illustration-laptop-mobile.svg)
	}
}

</style>