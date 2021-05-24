<template>
	<div class="project-card">
		<div class="card-content">
			<div class="img-container">
				<img :src="require(`../assets/${image}`)" class="demo-image">
				<div class="overlay">
					<div class="text">
						<a :href="figmaurl" target="_blank">Figma</a>
						<a :href="siteurl" target="_blank">Visit site ;)</a>
					</div>
				</div>
			</div>
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
  </div>
</template>

<script>
export default {
  name: 'Project',
	props: ['image', 'name', 'figmaurl', 'siteurl', 'team', 'description'],
}
</script>

<style scoped>
.project-card {
	padding: 0;
	margin-right: 3.75em;
	margin-bottom: 5em;
}
.img-container {
	position: relative;
	width: 100%;
}
.overlay {
	position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  height: 100%;
  width: 100%;
  opacity: 0;
  transition: .15s ease;
  background-color: rgba(255, 255, 254, 0.85);
	border-radius: 3px;
}
.text {
	color: #262626;
	background-color: transparent;
  font-size: 20px;
  position: absolute;
  top: 50%;
  left: 50%;
  -webkit-transform: translate(-50%, -50%);
  -ms-transform: translate(-50%, -50%);
  transform: translate(-50%, -50%);
  text-align: center;
	display: flex;
	flex-direction: column;
	width: 100%;
}
.demo-image {
	width: 100%;
	height: auto;
	display: block;
	border-radius: 3px;
}
a {
	text-decoration: none;
	background-color: transparent;
	font-size: 1.25em;
	font-weight: 400;
	color: #262626 !important;
	margin-bottom: 0.5rem;
}
a:hover {
	text-decoration: underline !important;
	color: #262626;
}
.card-content:hover .overlay {
	opacity: 1;
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