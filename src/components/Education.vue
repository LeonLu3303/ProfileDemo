<template>
  <div class="education_container">
    <h2>學歷 <span>Education</span></h2>
    <div class="ed_content">
      <div class="content_detail" v-for="item in education" :key="item">
        <div class="content_card">
          <div class="ed_name">{{ item.name }}</div>
          <div class="ed_time">{{ item.time }}</div>
          <div class="ed_maior">{{ item.major }}</div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      education: [
        {
          name: '緯育 TibaMe',
          major: '前端工程專業養成班',
          time: '2022/06-2022/10',
        },
        {
          name: '私立大同大學',
          major: '機械工程學系',
          time: '2011/09-2016/6',
        },
      ],
    };
  },
  methods: {},
  created() {},
  mounted() {},
};
</script>
<style lang="scss">
@import '../assets/scss/education.scss';
</style>
