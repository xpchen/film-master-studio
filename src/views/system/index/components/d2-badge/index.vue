<template>
  <div class="d2-badge">
    <p v-for="(group, groupIndex) of badges" :key="groupIndex" align="center">
      <a v-for="(badge, badgeIndex) of group" :key="badgeIndex" :href="badge.link" target="_blank">
        <img :src="badge.img"/>
      </a>
    </p>
  </div>
</template>

<script>
const linkD2Admin = 'https://github.com/d2-projects/d2-admin'
export default {
  data () {
    return {
      badges: [
        [
          { img: 'https://img.shields.io/github/stars/d2-projects/d2-admin.svg', link: `${linkD2Admin}/stargazers` },
          { img: 'https://img.shields.io/github/forks/d2-projects/d2-admin.svg', link: `${linkD2Admin}/network/members` },
          { img: 'https://img.shields.io/github/release/d2-projects/d2-admin.svg', link: `${linkD2Admin}/releases` },
          { img: 'https://img.shields.io/github/last-commit/d2-projects/d2-admin.svg', link: linkD2Admin },
          { img: 'https://api.netlify.com/api/v1/badges/a5dd4bbd-da3f-4145-98a9-8012577bdcf5/deploy-status', link: 'https://app.netlify.com/sites/d2-admin/deploys' },
          { img: 'https://visitor-badge.glitch.me/badge?page_id=d2-projects.d2-admin', link: linkD2Admin }
        ]
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.d2-badge {
  margin-bottom: 20px;
  p {
    margin: 0px;
    margin-bottom: 2px;
    &:last-child {
      margin-bottom: 0px;
    }
    img {
      display: inline-block;
      margin: 0px 2px;
    }
  }
}
</style>
