
## Intro



- The [VueJS](https://vuejs.org/) wrapper for [Owl Carousel](https://owlcarousel2.github.io/OwlCarousel2/).



- [Owl Carousel](https://owlcarousel2.github.io/OwlCarousel2/) is touch enabled jQuery plugin that lets you create a beautiful responsive carousel slider.

- Extended from [vue-owl-carousel](https://github.com/s950329/vue-owl-carousel)


## Installation



`npm i -s vue-owl-carousel` or `yarn add vue-owl-carousel`

## Usage

```
<script>

import carousel from 'vue-owl-carousel'

export default {
    components: { carousel },
}

</script>
```

Basic Usage

```
<carousel>

    <img src="https://placeimg.com/200/200/any?1">

    <img src="https://placeimg.com/200/200/any?2">

    <img src="https://placeimg.com/200/200/any?3">

    <img src="https://placeimg.com/200/200/any?4">

</carousel>
