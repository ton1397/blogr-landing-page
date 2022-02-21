<template>
	<div id="blogr-template">
		<pagetop/>
		<middletop/>
		<middle/>
		<middlebottom/>
		<footerbar/>
	</div>
</template>

<script>
	import navbar from "./navbar.vue";
	import pagetop from "./pagetop.vue";
	import middletop from "./middletop.vue";
	import middle from "./middle.vue";
	import middlebottom from "./middlebottom.vue";
	import footerbar from "./footer.vue";
	export default {
		components:{
			navbar,
			pagetop,
			middletop,
			middle,
			middlebottom,
			footerbar
		}
	};
</script>

<style>
</style>