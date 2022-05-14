<template>
  <div>
    <UserSection />
    <AboutSection />
    <Advantages />
  </div>
</template>

<script>
import UserSection from "~/components/Sections/UserSection.vue"
import AboutSection from "~/components/Sections/AboutSection.vue"
import Advantages from "~/components/Sections/Advantages.vue"
export default {
  name: 'ProfilePage',
  components: {
    UserSection,
    AboutSection,
    Advantages,
  }
}
</script>

<style module lang="scss">
 
</style>
