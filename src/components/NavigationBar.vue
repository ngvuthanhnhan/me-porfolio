<template>
	<div class="nav-bar" :class="{ 'nav-bar--hidden': !showNavbar }">
		<b-row class="h-100 text-left" align-v="center">
			<b-col cols="2" class="item">
				Projects
			</b-col>
			<b-col cols="2" class="item">
				My CV
			</b-col>
			<b-col class="item bold text-end">
				Hi!
			</b-col>
		</b-row>
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

<style>
.nav-bar {
	width: 100vw;
	height: 108px;
	position: fixed;
  transform: translate3d(0, 0, 0);
  transition: transform .525s cubic-bezier(0.55, 0.085, 0, 0.99);
	padding-left: 14.725em;
	padding-right: 14.725em;
}
.nav-bar.nav-bar--hidden {
  transform: translate3d(0, -100%, 0);
}
.item {
	color: #FFFFFE;
	font-size: 21px;
	font-weight: 500;
}
.bold {
	font-weight: 600;
}
</style>
