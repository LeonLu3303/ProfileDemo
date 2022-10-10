<template>
  <div class="skill_container">
    <h2>技能 <span>Skill</span></h2>
    <div class="skill_content">
      <div class="skill_icon_container">
        <div class="icon_pic" v-for="item in skillIcon" :key="item">
          <img :src="require(`@/assets/img/skill_icon/${item}.png`)" alt="" />
        </div>
      </div>
      <div class="skill_detail_container">
        <div
          class="skill_detail_content"
          v-for="item in skillDetail"
          :key="item"
        >
          <div class="skill_title">{{ item.skillName }}</div>
          <hr />
          <ul>
            <li v-for="item in item.skill" :key="item">
              {{ item }}
            </li>
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
      skillIcon: [
        // 要存放.png檔案名稱
        'html5',
        'css3',
        'javascript',
        'jquery',
        'sass',
        'gsap',
        'mysql',
        'php',
        'git',
        'workbench',
        'figma',
        'vuejs',
        'bootstrap',
        'java',
        'autocad',
      ],
      skillDetail: [
        {
          skillName: '前端',
          skill: [
            'HTML5',
            'CSS3',
            'JavaScript',
            'JQuery',
            'SASS',
            'GSAP',
            'Vue.js',
            'Bootstrap',
            'RWD',
            'Web APIs',
            'gulp',
            'Webpack',
          ],
        },
        {
          skillName: '後端與資料庫',
          skill: [
            'PHP程式設計',
            'My SQL資料庫',
            'Git 版本控制',
            '系統分析(敏捷式開發)',
            'MongoDB',
            'RESTful API',
          ],
        },
        {
          skillName: '其他',
          skill: ['AutoCAD', 'ProE', 'Java'],
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
