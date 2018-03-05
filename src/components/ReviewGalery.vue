<template>
  <div class="hello">
    <ul id="reviews-list">
      <li
        v-for="review in reviews"
        :key="review.reviewer.id"
      >
        {{ review.reviewer.name }}
        {{ review.review_text }}
      </li>
    </ul>

  </div>
</template>

<script>
import Reviews from '../../reviews.json'

export default {
  name: 'ReviewGalery',
  data () {
    return {
      reviews: Reviews.reviews
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
