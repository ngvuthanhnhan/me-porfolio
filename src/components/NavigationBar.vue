<template>
	<div class="nav-bar" :class="{ 'nav-bar--hidden': !showNavbar }">
		<div class="item">
			<a href="#">Projects</a>
		</div>
		<div class="item">
			<a href="#">My-CV</a>
		</div>
		<div style="width: inherit"></div>
		<div class="item hi" v-b-tooltip.hover.bottom title="Have a nice day! ;)">
			<a href="#" class="bold">Hi!</a>
		</div>
	</div>
</template>

<script>
export default {
  name: 'NavigationBar',
  data () {
		return {
			showNavbar: true,
			lastScrollPosition: 0
		}
	},
	mounted () {
		window.addEventListener('scroll', this.onScroll)
	},
	beforeDestroy () {
		window.removeEventListener('scroll', this.onScroll)
	},
	methods: {
		onScroll () {
			const currentScrollPosition = window.pageYOffset || document.documentElement.scrollTop
			if (currentScrollPosition < 0) {
				return
			}
			if (Math.abs(currentScrollPosition - this.lastScrollPosition) < 80) {
				return
			}
			this.showNavbar = currentScrollPosition < this.lastScrollPosition
			this.lastScrollPosition = currentScrollPosition
		}
	}
}
</script>

<style scope>
.nav-bar {
	position: fixed;
	z-index: 2;
	top: 0;
	right: 0;
	left: 0;
	transform: translateY(0);
	height: 108px;
	display: block;
	width: 100%;
	background-color: #222222;
  transform: translate3d(0, 0, 0);
  transition: transform .525s cubic-bezier(0.55, 0.085, 0, 0.99);
	padding-left: 4.75rem !important;
	padding-right: 4.75rem !important;
	display: flex;
}
.nav-bar.nav-bar--hidden {
  transform: translate3d(0, -100%, 0);
}
.item {
	width: 33.3333%;
	margin: auto;
}
.hi {
	text-align: end;
  width: 20%;
}
a {
	color: #FFFFFE !important;
	text-decoration: none !important;
	font-size: 21px;
	font-weight: 500;
}
a:hover {
	text-decoration: underline !important;
}
.bold {
	font-weight: 600;
}
</style>
