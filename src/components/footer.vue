<template>
	<div id="blogr-footerbar">
		<div class="footerbar-container">
			<div>
				<img src="../assets/logo.svg" alt="">
			</div>
			<div class="footerbar-list">
				<p>Product</p>
				<ul>
					<li>
						<a href="#">Overview</a>
					</li>
					<li>
						<a href="#">Pricing</a>
					</li>
					<li>
						<a href="#">Marketplace</a>
					</li>
					<li>
						<a href="#">Features</a>
					</li>
					<li>
						<a href="#">Integrations</a>
					</li>
				</ul>
			</div>
			<div class="footerbar-list">
				<p>Company</p>
				<ul>
					<li>
						<a href="#">About</a>
					</li>
					<li>
						<a href="#">Team</a>
					</li>
					<li>
						<a href="#">Blog</a>
					</li>
					<li>
						<a href="#">Careers</a>
					</li>
				</ul>
			</div>
			<div class="footerbar-list">
				<p>Connect</p>
				<ul>
					<li>
						<a href="#">Contact</a>
					</li>
					<li>
						<a href="#">Newsletter</a>
					</li>
					<li>
						<a href="#">LinkedIn</a>
					</li>
				</ul>
			</div>
		</div>
	</div>
</template>

<style scoped>
#blogr-footerbar{
	background-color: hsl(240, 10%, 16%);
}
.footerbar-container{
	display: grid;
	grid-template-columns: 25% 25% 25% 25%;
	color: #fff;
	padding: 40px 10vw;
}

.footerbar-list p{
	font-size: 1.2em;
	padding-bottom: 15px;
}

.footerbar-list li{
	margin: 15px 0;
}

.footerbar-list li a{
	color: hsl(240, 2%, 79%);
}

@media screen and (max-width: 800px) {
	.footerbar-container{
		grid-template-columns: 100%;
		text-align: center;
	}
}
</style>