<template>
  <div class="home">
    <div class="aside_nav">
      <aside-nav />
    </div>
    <main>
        <section>
          <div>
            <picture>
              <source srcset="@/assets/banner/visual_02b.jpg" media="(max-width:800px)" />
              <img src="@/assets/banner/visual_02b.jpg" alt="" class="home-visual__image"/>
            </picture>
          </div>
        </section>
    </main>
    <footer class="c_footer">
      
    </footer>
  </div>
</template>

<script>
// @ is an alias to /src
import AsideNav from "@/components/AsideNav";

export default {
  name: "Home",
  components: {
    AsideNav,
  },
};
</script>
<style lang="less" scoped>
.home {
  min-width: 100vw;
  min-height: 100vh;
}
.aside_nav {
  width: 180px;
  position: fixed;
  z-index: 2;
  left: 0;
  top: 30px;
}
.home-visual__image {
  width: 100%;
}
.c_footer {
    position: relative;
    margin-top: 90px;
    padding-top: 120px;
    padding-bottom: 90px;
    background-color: #f78663;
    background-image: url('/static/footer/bg_dot.png');
    mask-image: url('/static/footer/footer_mask.svg'), url('/static/footer/box.png');
    mask-size: 800px auto,100% 100%;
    mask-repeat: repeat-x,no-repeat;
    mask-position: center top,left 100px;
    overflow: hidden;
    &::after {
      z-index: -1;
      position: absolute;
      display: block;
      width: 837px;
      height: 318px;
      left: calc(50% + 130px);
      bottom: -120px;
      background-image: url(/static/footer/footer_pad.png);
      content: "";
    }
}
</style>
