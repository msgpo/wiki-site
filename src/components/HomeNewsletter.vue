<template lang='pug'>
  .home-newsletter
    .home-newsletter-curve
    h3 Subscribe to our newsletter
    h4 Get notified of important announcements and new major releases.
    v-btn.mt-5(outline, dark, large, to='/newsletter') Subscribe
</template>

<script>

export default {
  name: 'HomeNewsletter',
  data () {
    return {}
  }
}
</script>

<style lang='scss'>
.home-newsletter {
  background: #6754e2 linear-gradient(45deg,#6754e2,#19cce6);
  text-align: center;
  padding: 0 0 100px 0;
  color: #FFF;
  border-bottom: 1px solid #FFF;

  @media screen and (max-width: 599px) {
    padding-bottom: 50px;
  }

  &-curve {
    background: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAB4AAAAA9CAYAAABMUXTjAAADamlUWHRYTUw6Y29tLmFkb2JlLnhtcAAAAAAAPD94cGFja2V0IGJlZ2luPSLvu78iIGlkPSJXNU0wTXBDZWhpSHpyZVN6TlRjemtjOWQiPz4KPHg6eG1wbWV0YSB4bWxuczp4PSJhZG9iZTpuczptZXRhLyIgeDp4bXB0az0iWE1QIENvcmUgNS41LjAiPgogPHJkZjpSREYgeG1sbnM6cmRmPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5LzAyLzIyLXJkZi1zeW50YXgtbnMjIj4KICA8cmRmOkRlc2NyaXB0aW9uIHJkZjphYm91dD0iIgogICAgeG1sbnM6eG1wTU09Imh0dHA6Ly9ucy5hZG9iZS5jb20veGFwLzEuMC9tbS8iCiAgICB4bWxuczpzdFJlZj0iaHR0cDovL25zLmFkb2JlLmNvbS94YXAvMS4wL3NUeXBlL1Jlc291cmNlUmVmIyIKICAgIHhtbG5zOnhtcD0iaHR0cDovL25zLmFkb2JlLmNvbS94YXAvMS4wLyIKICAgeG1wTU06T3JpZ2luYWxEb2N1bWVudElEPSJ4bXAuZGlkOmU3MjQ3YmIzLTg3NWMtZjM0ZS1iOTZhLTMwOTQyZTg3YTFiNiIKICAgeG1wTU06RG9jdW1lbnRJRD0ieG1wLmRpZDpDQUQwRkE3MTk0QTcxMUU4QjhDQUQ5MjgzN0NBQjc4OCIKICAgeG1wTU06SW5zdGFuY2VJRD0ieG1wLmlpZDpDQUQwRkE3MDk0QTcxMUU4QjhDQUQ5MjgzN0NBQjc4OCIKICAgeG1wOkNyZWF0b3JUb29sPSJBZG9iZSBQaG90b3Nob3AgQ0MgKFdpbmRvd3MpIj4KICAgPHhtcE1NOkRlcml2ZWRGcm9tCiAgICBzdFJlZjppbnN0YW5jZUlEPSJ4bXAuaWlkOjFiZTcyYzVmLTgzMTMtZWM0Mi04ZWU1LThmNDZkY2Q4YmZjYSIKICAgIHN0UmVmOmRvY3VtZW50SUQ9InhtcC5kaWQ6ZTcyNDdiYjMtODc1Yy1mMzRlLWI5NmEtMzA5NDJlODdhMWI2Ii8+CiAgPC9yZGY6RGVzY3JpcHRpb24+CiA8L3JkZjpSREY+CjwveDp4bXBtZXRhPgo8P3hw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) no-repeat scroll top;
    background-size: contain;
    width: 100%;
    height: 100px;
    margin-top: -1px;
  }

  h3 {
    font-size: 30px;
    font-weight: 600;
    margin-top: 50px;
    padding: 0 15px;
    line-height: 30px;

    @media screen and (max-width: 599px) {
      margin-top: 0;
    }
  }
  h4 {
    font-size: 16px;
    font-weight: 400;
    padding: 15px 15px 0;
  }
}
</style>
