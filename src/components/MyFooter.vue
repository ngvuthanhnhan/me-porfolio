<template>
  <div id="footer">
    <div class="contact">
      <div class="at">
        Contact me at:
      </div>
      <div class="email">
        ngvuthanhnhan@gmail.com
      </div>
    </div>
    <div class="github">
      <a href="https://github.com/ngvuthanhnhan" target="_blank">Github</a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MyFooter',
  
}
</script>

<style>
#footer {
  margin-top: 5rem;
  margin-bottom: 1.5rem;
}
.contact {
  margin: 0;
}
.at {
  font-size: 1.25rem;
  font-weight: 500;
  margin-bottom: -0.75rem;
}
.email {
  font-size: 2rem;
  font-weight: 500;
  margin-bottom: 1.25rem;
}
.email:hover {
  text-decoration: underline;
}
.github {
  font-size: 1.15rem;
  font-weight: 500;
  margin: auto 0 0 auto;
}
</style>
