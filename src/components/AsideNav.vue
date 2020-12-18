<template>
  <div class="nav">
    <div class="logo"></div>
    <ul class="list">
      <li>STORY</li>
      <li>CHARACTER</li>
      <li>ONAIR</li>
      <li>STAFF&CAST</li>
      <li>MOVIE</li>
    </ul>
    <ul class="share">
      <li class="text"></li>
      <li class="icon"></li>
    </ul>
    <div class="c-language"></div>
  </div>
</template>

<script>
export default {
  name: "AsideNav",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
.nav {
  width: 100%;
  height: 100%;
  display: flex;
  cursor: pointer;
  flex-direction: column;
  align-items: center;
  background-color: rgba(248, 245, 239, 0.95);
  border-radius: 0 15px 15px 0;
  box-shadow: 0 0 10px 0 rgba(0, 0, 0, 0.25);
  .logo {
    width: 120px;
    height: 65px;
    margin: 10px 0px;
    background-image: url("/static/img/logo.png");
    background-size: 100% 100%;
    background-repeat: no-repeat;
    &:hover {
      opacity: 0.6;
    }
  }
  .list {
    width: 100%;
    margin-top: 10px;
  }
  .list>li {
    width: 100%;
    color: #4b0100;
    font-size: 1rem;
    padding: .9em 0em;
    font-weight: 800;
    font-family: Nunito, sans-serif;
    margin-bottom: 1px;
    line-height: 1;
    letter-spacing: 0.05em;
    font-feature-settings: "palt";
    position: relative;
    z-index: 1;
    &::before,
    &::after {
      position: absolute;
      left: 0;
      top: 0;
      display: block;
      height: 100%;
      -webkit-transition: 0.2s;
      transition: 0.2s;
      content: "";
    }
    &::before {
      z-index: -1;
      width: 10px;
      background-color: #f8bc33;
    }
    &::after {
      width: 100%;
      background-image: url("/static/img/menu_item_bg.png");
      background-position: center center;
      opacity: 0;
    }
    &:hover {
      &::before {
        width: 100%;
      }
      &::after {
        opacity: 1;
      }
    }
  }
}
</style>
