<template>
  <section class='highlight content-section'>
  <div class="container">
    <div class="highlight-left">
      <prismic-rich-text class="text" :field="slice.primary.text"/>
      <prismic-rich-text class="testing" :field="slice.primary.testing"/>
      <prismic-rich-text class="title" :field="slice.primary.title"/>
      <prismic-rich-text class="headline" :field="slice.primary.headline"/>
      
    </div>
    <div class="highlight-right">
      <prismic-image :field="slice.primary.featured_image"/>
    </div>
  </div>
  </section>
</template>

<script>
export default {
  props: ['slice'],
  name: 'work-slice'
}
</script>

<style scoped>

.container {
        display: flex;
        align-items: center;
        justify-content: center;
        padding-top:0px;
        text-align:justify;
      }
.highlight {
  position: relative;
  overflow: auto;
}
.highlight-left {
  width: 43%;
  float: left;
}
.highlight-right {
  padding-left:40px;
  width: 48%;
  float: right;
}
.text{
  font-weight: bolder;
  color:#ff009c;
  font-size:12pt;
}
.testing{
 color:purple;
 font-weight: bolder;
 font-size: 40pt;
}
.work_button {
  background:white;
  border-radius: 50px;
  border:2px solid purple;
  color: purple;
  font-size: 12px;
  font-weight: 700;
  padding: 15px 40px;
}
.work_button:hover {
  background: #c8c9cb;
}




</style>
