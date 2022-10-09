<template>
  <div class="skill_container">
    <h2>工作經歷</h2>
    <h3>{{}}</h3>
  </div>
</template>
<script>
export default {
  data() {
    return {
      job: [
        {
          company: '京元塑膠有限公司',
          position: '開發工程師',
          workTime: '2018/07-2021/02',
          mainWork: [
            '與國外廠商洽談、驗收原料資源',
            '與客戶討論產品原料可行性及價格',
            '協助客戶開發試作產品',
            '廠內原料開發試作',
          ],
        },
        {
          company: '江申工業股份有限公司',
          position: '開發工程師',
          workTime: '2016/08-2018/06',
          mainWork: ['', '', '', '', '', ''],
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
@import '../assets/scss/skill.scss';
</style>
