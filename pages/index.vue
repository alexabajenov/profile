<template>
  <div>
    <UserSection />
    <AboutSection />
    <Advantages />
    <Experience />
    <Projects />
    <Footer />
  </div>
</template>

<script>
import UserSection from "~/components/Sections/UserSection.vue"
import AboutSection from "~/components/Sections/AboutSection.vue"
import Advantages from "~/components/Sections/Advantages.vue"
import Experience from "~/components/Sections/Experience.vue"
import Projects from "~/components/Sections/Projects.vue"
import Footer from "~/components/Sections/Footer.vue"

export default {
  name: 'ProfilePage',
  components: {
    UserSection,
    AboutSection,
    Advantages,
    Experience,
    Projects,
    Footer,
  }
}
</script>

<style module lang="scss">
 
</style>
