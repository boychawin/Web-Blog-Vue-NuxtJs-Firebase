<template>
  <div>
    <b-carousel
      id="carousel-1"
      v-model="slide"
      :interval="4000"
      controls
      indicators
      background="#ababab"
      img-width="1024"
      img-height="480"
      style="text-shadow: 1px 1px 2px #333"
      @sliding-start="onSlideStart"
      @sliding-end="onSlideEnd"
    >
      <!-- Text slides with image -->

      <!-- Slides with img slot -->
      <!-- Note the classes .d-block and .img-fluid to prevent browser default image alignment -->
      <!-- <div v-for="item in items" :key="item"> -->
        <b-carousel-slide>
          <template #img>
            <img
              class="d-block img-fluid w-100"
              width="1024"
              height="480"
              src="https://picsum.photos/1024/480/?image=55"
              alt="image slot"
            />
          </template>
        </b-carousel-slide>
      <!-- </div> -->
    </b-carousel>

    <p class="mt-4">
      Slide #: {{ slide }}<br />
      Sliding: {{ sliding }}
    </p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      slide: 0,
      sliding: null,
      item: [
        {
          caption: 'A',
          image: 'https://picsum.photos/1024/480/?image=55',
          text: 'Nulla vita',
        },
        {
          caption: 'B',
          image: 'https://picsum.photos/1024/480/?image=55',
          text: 'Nulla vita',
        },
        {
          caption: 'C',
          image: 'https://picsum.photos/1024/480/?image=55',
          text: 'Nulla vita',
        },
      ],
    }
  },
  methods: {
    onSlideStart(slide) {
      this.sliding = true
    },
    onSlideEnd(slide) {
      this.sliding = false
    },
  },
}
</script>