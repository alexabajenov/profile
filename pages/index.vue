<template>
  <div>
    <UserSection />
    <AboutSection />
  </div>
</template>

<script>
import UserSection from "~/components/Sections/UserSection.vue"
import AboutSection from "~/components/Sections/AboutSection.vue"
export default {
  name: 'ProfilePage',
  components: {
    UserSection,
    AboutSection,
  }
}
</script>

<style module lang="scss">
 
</style>
