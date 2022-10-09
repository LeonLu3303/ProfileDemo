<template>
  <section class="resume">
    <BasicInfo />
    <Skill />
  </section>
</template>
<script>
import BasicInfo from '@/components/BasicInfo.vue';
import Skill from '@/components/Skill.vue';

export default {
  data() {
    return {};
  },
  components: { BasicInfo, Skill },
  methods: {},
  created() {},
  mounted() {},
};
</script>
<style lang="scss">
@import '../assets/scss/style.scss';
</style>
