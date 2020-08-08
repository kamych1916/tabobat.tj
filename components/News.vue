<template>
  <div class="search-board">
    <div class="inner">
      <div>
        <h1>Новости</h1>
        <vueper-slides
          class="no-shadow"
          :visible-slides="3"
          :slide-ratio="1 / 4"
          :dragging-distance="50"
          :gap="5"
          :arrows="false"
        >
          <vueper-slide
            v-for="(slide, i) in slides"
            :key="i"
            :image="slide.image"
            :title="slide.title"
            :content="slide.content"
          />
        </vueper-slides>
      </div>
    </div>
  </div>
</template>

<script>
import { VueperSlides, VueperSlide } from 'vueperslides'
import 'vueperslides/dist/vueperslides.css'

export default {
  components: { VueperSlides, VueperSlide },
  data: () => ({
    slides: [
      {
        title: 'El Teide Volcano, Spain',
        content: 'Photo by Max Rive',
        // You can also provide a URL for the image.
        image: require('@/static/images/pediatr.png'),
      },
      {
        title: 'El Teide Volcano, Spain',
        content: 'Photo by Max Rive',
        // You can also provide a URL for the image.
        image: require('@/static/images/terapevt.png'),
      },
      {
        title: 'El Teide Volcano, Spain',
        content: 'Photo by Max Rive',
        // You can also provide a URL for the image.
        image: require('@/static/images/pediatr.png'),
      },
      {
        title: 'El Teide Volcano, Spain',
        content: 'Photo by Max Rive',
        // You can also provide a URL for the image.
        image: require('@/static/images/terapevt.png'),
      },
            {
        title: 'El Teide Volcano, Spain',
        content: 'Photo by Max Rive',
        // You can also provide a URL for the image.
        image: require('@/static/images/pediatr.png'),
      },
      {
        title: 'El Teide Volcano, Spain',
        content: 'Photo by Max Rive',
        // You can also provide a URL for the image.
        image: require('@/static/images/terapevt.png'),
      },
    ],
  }),
}
</script>  

<style>
.search-board .inner {
  padding-top: 30px;
}
.vueperslide__content-wrapper.parallax-fixed-content, .vueperslide__content-wrapper:not(.vueperslide__content-wrapper--outside-top):not(.vueperslide__content-wrapper--outside-bottom) {
    display: flex;
    -webkit-box-orient: vertical;
    align-items: center;
    justify-content: flex-end;
}
</style>
