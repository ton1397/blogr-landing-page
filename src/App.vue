<template>
	<div id="app">
		<page/>
	</div>
</template>

<script>
	import page from './components/blogr-landing-page.vue';
	export default {
		name: "App",
		components:{
			page
		}
	};
</script>

<style>
	@import url(./styles/css/fonts.css);
	body{
		margin: 0;
		padding: 0;
		font-family: 'Overpass';
		background-color: #fafafa;
	}
	*{
		box-sizing: border-box;
	}
	ul,li,a{
		margin: 0;
		padding: 0;
		list-style: none;
	}
	a{
		text-decoration: none;
	}

	.btn-light {
		background-color: #fff;
		border-radius: 50px;
		padding: 10px 25px !important;
		margin: 0 15px;
		color: red;
		border: #fff;
		font-size: .9em;
		cursor: pointer;
	}

	.btn-light:hover {
		background: rgba(255,255,255,.5);
		color: #fff;
	}

	.btn-outline-light {
		background-color: transparent;
		border-radius: 50px;
		    padding: 10px 25px !important;
		margin: 0 15px;
		color: #fff;
		border: 1px solid #fff;
		font-weight: 600;
		font-size: .9em;
		cursor: pointer;
	}

	.btn-outline-light:hover {
		background-color: #fff;
		color: red;
	}
</style>
