<template>
	<div id="projects-container">
    <div class="title">
			<span class="hashtag">#</span>my-projects
		</div>
		<div class="container">
			<b-row align-h="start">
				<b-col lg="6" class="project-card">
					<project 
						image="video-request.png"
						name="video-request page"
						figmaurl="#"
						siteurl="https://request.ongdev.com/"
						team="Working in Ong Dev & Friends team"
						description="Design and development of a requests site for videos, Q&A and Udemy course for Ong Dev followers with a-bunch-of love."
					/>
				</b-col>
				<b-col lg="6" class="project-card">
					<project 
						image="team-note.png"
						name="team-note"
						figmaurl="https://www.figma.com/file/XCwMoCo1XmHSpEkVudEuYe/Team-Notes?node-id=0%3A1"
						siteurl="#"
						team="Solo Project"
						description="(On-going) Design and development a zone where you and your teammates get to brainstorm together for an idea, with or without a time limit."
					/>
				</b-col>
				<b-col lg="6" class="project-card">
					<project 
						image="smart-food-court.png"
						name="Smart Food Court"
						figmaurl="#"
						siteurl="#"
						team="Working in Me and the boys team"
						description="A Software Engineering project for building a Smart Food Court System for our University. This system allow customer to order foods at the food courts, or pre-order through the web-app."
					/>
				</b-col>
				<b-col lg="6" class="project-card">
					<project 
						image="my-porfolio.png"
						name="my-porfolio"
						figmaurl="https://www.figma.com/file/4j59No264IZG70QxxZZpza/Porfolio?node-id=0%3A1"
						siteurl="https://ngvuthanhnhan.github.io/me-porfolio/"
						team="Solo Project"
						description="Hello, world! 🌏"
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
	margin-top: 37.5555%;
}
.title {
	margin-bottom: 2.75em;
	font-size: 1.5em;
	font-weight: 500;
}
.hashtag {
	color: #BDBDBD;
}
.project-card {
	padding: 0;
	margin-left: 0;
}
</style>>