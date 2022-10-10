<template>
  <div class="experience_container">
    <h2>工作經歷 <span>Experience</span></h2>
    <div class="job_content">
      <div class="job_experience" v-for="item in job" :key="item">
        <div class="job_position">
          {{ item.position }}<span> • {{ item.company }}</span>
        </div>
        <div class="job_time">{{ item.workTime }}</div>
        <div class="main_work">
          <h3>主要工作內容</h3>
          <ul>
            <li v-for="index in item.mainWork" :key="index">{{ index }}</li>
          </ul>
        </div>
      </div>
    </div>
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
            '與客戶討論產品原料可行性及價格',
            '與國外廠商洽談、驗收原料資源',
            '協助客戶開發試作產品',
            '廠內原料開發試作',
          ],
        },
        {
          company: '江申工業股份有限公司',
          position: '開發工程師',
          workTime: '2016/08-2018/06',
          mainWork: [
            '納智捷Luxgen - 前保桿：協助公司前輩跟進零件開發及設計變更對應，並後期接手專案後期',
            '金龍汽車(中興巴士) - 通用公車車型車架：專案維護，跟進客戶設計變更',
            '國瑞汽車(豐田HINO) - 大車車型第六期環保專案：主導專案開發',
            '金龍汽車製造(中興巴士) - 新型電動公車車架：主導專案開發',
            '裕隆汽車NISSAN - 車體前輪轂鈑件：主導專案開發',
          ],
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
@import '../assets/scss/experience.scss';
</style>
