<template>
<div class="recommend">
  <div class="recommend-contend">
    <div class="slider-wrapper">
      <Slider>
        <div v-for="item in recommends" :key="item.id">
          <a :href="item.linkUrl">
            <img :src="item.picUrl" alt="">
          </a>
        </div>
      </Slider>
    </div>
    <div class="recommend-list">
      <h1 class="list-title">热门歌单推荐</h1>
      <ul>
      </ul>
    </div>
  </div>
</div>
</template>

<script>
import Slider from '@/base/slider/slider'
import {getRecommend} from '@/api/recommend'
import {ERR_OK} from '@/api/config'

export default {
  data() {
    return {
      recommends: [
        {
          id: 1,
          linkUrl: 'https://y.qq.com/n/m/detail/taoge/index.html?ADTAG=myqq&from=myqq&channel=10007100&id=6227751694',
          picUrl: 'https://p.qpic.cn/music_cover/ltomernzQVcJmroHNJ99oFJ3ozuoYeszeOXPSEdjV6ZfqGjLktfMJg/600'
        },
        {
          id: 2,
          linkUrl: 'https://y.qq.com/n/m/detail/taoge/index.html?ADTAG=myqq&from=myqq&channel=10007100&id=6474117513',
          picUrl: 'https://p.qpic.cn/music_cover/7vlTTvwBiaibKJpyXffTHicMjPm0HbKPEiaw1XSXemlqhDRp0iaAGIibrUNw/600'
        },
        {
          id: 3,
          linkUrl: 'https://y.qq.com/n/m/detail/taoge/index.html?ADTAG=myqq&from=myqq&channel=10007100&id=6966426033',
          picUrl: 'https://p.qpic.cn/music_cover/4pmnRu5sL5QbtO8OS8NKJSMjvbG2LduzCtOVqic5SIzIaEGedOV0Biag/600'
        },
        {
          id: 4,
          linkUrl: 'https://y.qq.com/n/m/detail/taoge/index.html?ADTAG=myqq&from=myqq&channel=10007100&id=6229206509',
          picUrl: 'https://p.qpic.cn/music_cover/4pmnRu5sL5QbtO8OS8NKJatYBQN0DrKNsH3BicZgGacjmgKicXotm25Q/600'
        }
      ]
    }
  },
  components: {
    Slider
  },
  created() {
    this._getRecommend()
  },
  methods: {
    _getRecommend() {
      getRecommend().then((res) => {
        if (res.code === ERR_OK) {
          console.log(res.data.slider)
        }
      })
    }
  }
}
</script>

<style scoped>

</style>
