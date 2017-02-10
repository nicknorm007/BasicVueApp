<template>
  <div id="app">
    <div class="content" align="center">
      <h1>{{msg}}</h1>
    </div>
    </br>
    <simple-env></simple-env>
  </div>
</template>

<script>

import SimpleEnv from './simple-env.vue';

export default {
  name: 'app',
  components: {
    SimpleEnv
  },
  data () {
    return {
      msg: 'Authoring Environment Information'
    }
  }
}
</script>

<style lang="scss">
@import "styles/index.scss";

body {
  font-family: -apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,Helvetica,Arial,sans-serif,"Apple Color Emoji","Segoe UI Emoji","Segoe UI Symbol";
  height: 100%;
}

aside {
  width:180px;
}

/*2e70b2*/
.button.is-success {
  background-color: #2e70b2;
}
.nav-left .searchbox {
  margin-top: 10px;
}
.nav.is-default {
  background-color:#f5f5f5;
}
.icon-chevron {
  font-size: 12px;
}
.icon-item-type i {
  font-size:12px;
  padding:6px 15px 6px 6px;
  color:#bbbbbb;
}
.aside {
  background-color: #232B2D;
}
.aside .uploader {
  background-color: #3273dc;
  height: 95px;
  margin:0 -10px;
  padding: 25px 30px;
}
.aside .uploader .button {
  background-color: transparent;
  border: 3px dashed #F6F7F7;
  padding: 20px 70px;
  color: #F6F7F7;
}
.aside .main {
  padding: 40px;
  color: #6F7B7E;
}
.aside .title {
  color: #6F7B7E;
  font-size: 12px;
  font-weight: bold;
  text-transform: uppercase;
}
.aside .main .item {
  display: block;
  padding: 10px 0;
  /*color: #6F7B7E;*/
  color: #FFFFFF;
}
.aside .menu-list a {
    border-radius: 2px;
    color: #3273dc;
    display: block;
    padding: 0.5em 0.75em;
}
.aside .menu-list a:hover {
  color: #0069D1;
}
.aside .main .item.active {
  color: #F6F7F7;
}
.aside .main .icon {
  font-size: 19px;
  padding-right: 30px;
}
.aside .main .name {
  font-size: 16px;
  font-weight: bold;
}
.content {
  display: block;
  background-color: #fff;
  padding: 40px 20px;
}
.nav.menu {
  background-color: #fff;
  border-bottom: 1px solid #e1e1e1;
  z-index: 1;
}
.nav.menu .nav-item .icon-btn {
  border: 3px solid #B7C6C9;
  border-radius: 90px;
  padding: 5px 7px;
  color: #B7C6C9;
}
.nav.menu .nav-item .icon-btn.thin {
  padding: 5px 8px;
}
.nav.menu .nav-item.is-active .icon-btn {
  color: #3273dc;
  border: 3px solid #3273dc;
}
.nav.menu .nav-item .icon-btn .fa {
  font-size: 20px;
  color: #B7C6C9;
}
.nav.menu .nav-item.is-active .icon-btn .fa {
  color: #3273dc;
}
.item.is-treeitem-active {
  background-color: #666666;
}
.nav-item a.is-tab.is-active, a.nav-item.is-tab.is-active {
  color: #3273dc;
  border-bottom: 3px solid #3273dc;
}
.nav-item a.is-tabm, a.nav-item.is-tab:hover {
  color: #3273dc;
  border-bottom: 1px solid #3273dc;
}
.nav-item a.is-tab a.is-tab.is-active, a.nav-item.is-tab.is-active {
  color: #3273dc;
  border-bottom: 3px solid #3273dc;
}
.padtop {
  padding-top:10px;
}
.padleft {
  padding-left:5px;
}
.fa-4x {
  font-size: 4em !important;
}
.fa-5x {
  font-size: 5em !important;
}
.fa-6x {
  font-size: 6em !important;
}
</style>
