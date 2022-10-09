<template>
  <div class="info_container">
    <div class="info_content">
      <div class="content_left">
        <div class="left_pic">
          <img src="@/assets/img/IMG_2727.jpg" alt="" />
        </div>
        <div class="ct_name">
          {{ ctName }}
        </div>
        <div class="en_name">
          {{ enName }}
        </div>
        <div class="looking_job">
          {{ lookingJob }}
        </div>
        <div class="en_looking_job">
          {{ enLookingJob }}
        </div>
      </div>
      <div class="content_right">
        <div class="introduction">
          {{ introduction }}
        </div>
        <div class="introduction_personality">
          {{ introductionPersonality }}
        </div>
        <div class="link_media">
          <div class="github_icon">
            <a href="https://github.com/LeonLu3303?tab=repositories"
              ><img src="../assets/img/icons8-github.svg" alt=""
            /></a>
          </div>
          <div>
            <div class="small">
              <span><img src="../assets/img/icons8-mail.svg" alt="" /></span>
              {{ email }}
            </div>
            <div class="small">
              <span><img src="../assets/img/icons8-phone.svg" alt="" /></span>
              {{ phone }}
            </div>
            <div class="small">
              <span
                ><img src="../assets/img/icons8-calendar-50.png" alt=""
              /></span>
              {{ birth }}
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      ctName: '呂柏霖',
      enName: 'Leon Lu',
      lookingJob: '前端工程師',
      enLookingJob: 'Front-End Develpor',
      introduction:
        '小弟我原先在傳統產業擔任開發工程師，待過汽車產業、塑膠產業，主要工作內容包羅萬象，對客戶的需求以及開發可行性討論，在內部安排會議挑論開發時程以及對各部門對專案展開開發，並將產線無法負荷之零件進行外包並與廠商溝同協調，也同時促使我培養大量的團隊經驗。',
      introductionPersonality:
        '我是一個慢熱的人準確來說是悶騷，但是在必要時可以切換社交模式，個性活潑帶點過動可能是因為我1992年屬猴，對於感興趣的事情會一股腦地去瞭解，以普羅大眾的眼光來看我應該算是幽默、反應快。',
      email: 'leon.lu1103@gmail.com',
      phone: '(+886)973380219',
      birth: '1992-11-03',
    };
  },
  methods: {},
  created() {},
  mounted() {},
};
</script>
<style lang="scss">
@import '@/assets/scss/basicInfo.scss';
</style>
