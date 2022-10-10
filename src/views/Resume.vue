<template>
  <section class="resume">
    <BasicInfo />
    <Skill />
    <Experience />
    <Education />
  </section>
</template>
<script>
import BasicInfo from '@/components/BasicInfo.vue';
import Experience from '@/components/Experience.vue';
import Skill from '@/components/Skill.vue';
import Education from '@/components/Education.vue';

export default {
  data() {
    return {};
  },
  components: { BasicInfo, Experience, Skill, Education },
  methods: {},
  created() {},
  mounted() {},
};
</script>
<style lang="scss">
@import '../assets/scss/style.scss';
</style>
