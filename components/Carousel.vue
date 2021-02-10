<template>
  <carousel-3d :width="200" :height="400">
    <slide class="slide"
      v-for="(slide, i) in slides"
      :index="i"
      :key="slide.id">
      <span class="title">{{slide.title}}</span>
    </slide>
  </carousel-3d>
</template>

<script>
export default {
  name: 'Carousel',
  components: {
  },
  data() {
    return {
      slides: [
          {
            "id":1,
            "title": "Первый слайд"
          },
          {
            "id":2,
            "title": "Второй слайд"
          },
          {
            "id":3,
            "title": "Третий слайд"
          },
          {
            "id":4,
            "title": "Четвертый слайд"
          },
          {
            "id":5,
            "title": "Пятый слайд"
          },
          {
            "id":6,
            "title": "Шестой слайд"
          },
      ],
    }
  },
}
</script>