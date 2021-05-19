<template>
	<div class="project-card">
		<img :src="require(`../assets/${image}`)" class="demo-image">
		<div class="project-name">
			{{ name }}
		</div>
		<div class="team-name">
			{{ team }}
		</div>
		<div class="project-description">
			{{ description }}
		</div>
  </div>
</template>

<script>
export default {
  name: 'Project',
	props: ['image', 'name', 'team', 'description'],
}
</script>

<style scoped>
.project-card {
	padding: 0;
	margin-right: 3em;
	margin-bottom: 3.75em;
}
.demo-image {
	width: 26em;
	height: auto;
	border-radius: 5px;
}
.project-name {
	font-weight: 500;
	font-size: 1.5em;
}
.team-name {
	font-size: 0.9em;
	margin-bottom: 1.15em;
}
</style>>