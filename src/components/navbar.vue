<template>
	<div id="blogr-navbar">
		<div class="navbar-header-container">
			<div class="navbar-header navbar-logo">
				<a class="nav-logo" href="#"><img src="../assets/logo.svg" alt=""></a>
			</div>
			<div class="nav-header navbar-btn-menu">
				<button class="btn btn-menu" @click="showMenu">
				</button>
			</div>
			<div class="navbar-header-content">
				<div class="navbar-header navbar-left">
					<ul>
						<li class="nav-item dropdown" @click="changeDropdown" v-click-outside="changeDropdown">
							<a href="#">Product</a>
							<span class="dropdown-icon"><img src="../assets/icon-arrow-light.svg" alt=""></span>
							<div class="dropdown-content">
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
						</li>
						<li class="nav-item dropdown" @click="changeDropdown" v-click-outside="changeDropdown">
							<a href="#">Company</a>
							<span class="dropdown-icon"><img src="../assets/icon-arrow-light.svg" alt=""></span>
							<div class="dropdown-content">
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
						</li>
						<li class="nav-item dropdown" @click="changeDropdown" v-click-outside="changeDropdown">
							<a href="#">Connect</a>
							<span class="dropdown-icon"><img src="../assets/icon-arrow-light.svg" alt=""></span>
							<div class="dropdown-content">
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
						</li>
					</ul>
				</div>
				<div class="navbar-header navbar-right">
					<ul>
						<li class="nav-item">
							<a href="#">Login</a>
						</li>
						<li class="nav-item">
							<a class="btn-light" href="#">Sign Up</a>
						</li>
					</ul>
				</div>
			</div>
			
		</div>
	</div>
</template>

<script>
import '../clickoutside'
export default {
	methods:{
		showMenu(){
			if(window.screen.availWidth <= 800){
				let nav_left = document.querySelector(".navbar-left");
				let nav_right = document.querySelector(".navbar-right");
				let btn_menu = document.querySelector(".navbar-btn-menu .btn-menu");
				let nav_content = document.querySelector(".navbar-header-content")
				if (nav_left.className.indexOf('mobile-active') > -1 && nav_right.className.indexOf('mobile-active') > -1) {
					nav_content.classList.remove("mobile-menu");
					nav_left.classList.remove('mobile-active');
					nav_right.classList.remove('mobile-active');
					btn_menu.style.backgroundImage = `url(${require('../assets/icon-hamburger.svg')})`;
				}else{
					nav_content.classList.add("mobile-menu");
					nav_left.classList.add('mobile-active');
					nav_right.classList.add('mobile-active');
					btn_menu.style.backgroundImage = `url(${require('../assets/icon-close.svg')})`;
				}
			}
			
		},
		changeDropdown(ev){
			if(window.screen.availWidth <= 800){
				let el_base = ev.target;
				let el_name = ev.target.localName;
				let dropdowns = document.querySelectorAll(".nav-item.dropdown");
				if(el_name == "a"){
					el_base = el_base.parentNode;
				}
				if(el_base.className.indexOf('active') == -1){
					dropdowns.forEach(el=>{
						el.classList.remove('active');
					})
					el_base.classList.add('active');
				}else{
					dropdowns.forEach(el=>{
						el.classList.remove('active');
					})
				}
			}
		}
	}
}
</script>

<style>

#blogr-navbar{
    padding: 25px 60px;
}

.navbar-header-container{
	padding: 25px;
    display: grid;
    grid-template-columns: 117PX 90%;
	align-items: center;
}

.navbar-header-content{
	padding: 25px;
    display: grid;
    grid-template-columns: 59.4% 40.6%;
    align-items: center;
}

.navbar-header-content.mobile-menu{
    display: block;
    position: absolute;
    width: 90vw;
    top: 70px;
    transform: translate(-50%);
    left: 50%;
    background-color: #fff;
    border-radius: 5px;
    z-index: 1;
}

.mobile-active{
	text-align: center !important;
}

.navbar-header-content.mobile-menu li{
    display: block;
}

.navbar-header-content.mobile-menu li a{
    color: hsl(237, 23%, 32%);
    font-weight: 600;
    font-size: 1.1em;
}

.navbar-header-content.mobile-menu .navbar-left{
	padding-bottom: 10px;
}

.navbar-header-content.mobile-menu .navbar-right{
    border-top: 1px solid #ccc;
	padding-top: 10px;
}

.navbar-header-content.mobile-menu li span img{
    content: url(../assets/icon-arrow-dark.svg);
}

.navbar-header-content.mobile-menu .btn-light{
    background: linear-gradient(to right, hsl(13, 100%, 72%), hsl(353, 100%, 62%));
    border-radius: 50px;
    padding: 12px 30px !important;
    margin: 0 15px;
    color: #fff;
    border: #fff;
    font-size: .9em;
    cursor: pointer;
}

.navbar-right{
	text-align: right;
}

.navbar-btn-menu{
	display: none;
	text-align: end;
}

.btn-menu{
	background-image: url(../assets/icon-hamburger.svg);
    background-repeat: no-repeat;
    background-color: transparent;
    background-position: center;
    border: none;
    padding: 20px;
}

.navbar-header .nav-item {
    display: inline;
    padding: 10px;
	position: relative;
}

.nav-item > a:not(.btn-light), .nav-item span{
	color: #fff;
}

.dropdown-icon{
	padding: 5px;
}

.dropdown.active .dropdown-content {
    display: block;
}

.mobile-active .dropdown.active .dropdown-content {
    background-color: #ccc;
	position: relative;
	left: 0;
    top: 0;
}

.mobile-active .dropdown.active .dropdown-icon img{
    transform: rotate(180deg);
}

img{
	vertical-align: middle;
}

.navbar-header.mobile-active, .navbar-header.mobile-active ul{
	display: block;
}

.dropdown-content{
	display: none;
    position: absolute;
    top: 40px;
    left: 5px;
    border-radius: 5px;
    padding: 20px;
    background: #fff;
}

.dropdown-content li > a{
	padding: 5px 0;
    display: inline-block;
	color: #000;
}

.dropdown-content li > a:hover{
	font-weight: bold;
}

@media screen and (max-width: 800px) {
	#blogr-navbar {
		padding: 0;
	}
	.navbar-btn-menu{
		display: block;
	}
	.navbar-header ul{
		display: none;
	}
	.navbar-header-container {
		display: grid;
		grid-template-columns: 50% 50%;
		align-items: center;
	}
}
</style>