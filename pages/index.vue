<template>
  <div>
    <UserSection />
    <AboutSection />
    <Advantages />
    <Experience />
    <Projects />
  </div>
</template>

<script>
import UserSection from "~/components/Sections/UserSection.vue"
import AboutSection from "~/components/Sections/AboutSection.vue"
import Advantages from "~/components/Sections/Advantages.vue"
import Experience from "~/components/Sections/Experience.vue"
import Projects from "~/components/Sections/Projects.vue"

export default {
  name: 'ProfilePage',
  components: {
    UserSection,
    AboutSection,
    Advantages,
    Experience,
    Projects,
  }
}
</script>

<style module lang="scss">
 
</style>
