<template>
	<div id="projects-container">
    <div class="title">
			<span class="hashtag">#</span>my-projects
		</div>
		<div class="container">
			<b-row align-h="start">
				<b-col lg="6" style="padding: 0;">
					<project 
						image="video-request.png"
						name="video-request page"
						team="Ong Dev & Friends team"
						description="Props are custom attributes you can register on a component."
					/>
				</b-col>
				<b-col lg="6" style="padding: 0;">
					<project 
						image="video-request.png"
						name="video-request page"
						team="Ong Dev & Friends team"
						description="Props are custom attributes you can register on a component. It becomes a property on that component instance."
					/>
				</b-col>
			</b-row>
		</div>
  </div>
</template>

<script>
import Project from './Project.vue'
export default {
  components: { Project },
  name: 'ProjectContainer',
}
</script>

<style scoped>
#projects-container {
	margin-top: 25%;
}
.title {
	margin-bottom: 1.25em;
	font-size: 1.15em;
	font-weight: 500;
}
.hashtag {
	color: #BDBDBD;
}
</style>>