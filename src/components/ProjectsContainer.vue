<template>
	<div id="projects-container">
    <div class="title">
			<span class="hashtag">#</span>my-projects
		</div>
		<div class="container">
			<b-row cols="2">
				<b-col style="padding: 0;">
					<project 
						image="video-request.png"
						name="video-request page"
						team="Ong Dev & Friends team"
						description="Props are custom attributes you can register on a component. When a value is passed to a prop attribute, it becomes a property on that component instance."
					/>
				</b-col>
				<b-col style="padding: 0;">
					<project 
						image="video-request.png"
						name="video-request page"
						team="Ong Dev & Friends team"
						description="Props are custom attributes you can register on a component. When a value is passed to a prop attribute, it becomes a property on that component instance."
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
	padding-left: 14.725em;
	padding-right: 14.725em;
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