<template>
  <div>
    <UserSection />
    <AboutSection />
    <Advantages />
    <Experience />
  </div>
</template>

<script>
import UserSection from "~/components/Sections/UserSection.vue"
import AboutSection from "~/components/Sections/AboutSection.vue"
import Advantages from "~/components/Sections/Advantages.vue"
import Experience from "~/components/Sections/Experience.vue"
export default {
  name: 'ProfilePage',
  components: {
    UserSection,
    AboutSection,
    Advantages,
    Experience,
  }
}
</script>

<style module lang="scss">
 
</style>
