<template>
  <div class="container main-view">
    <div class="row">
      <!--缩略图-->
      <div class="col-md-6" id="leftview">
        <div class="main-thumbnail"></div>
        <div class="row" style="margin-top: 12px">
          <div class="col-md-4" :class="'col-'+i" v-for="i in thumbnailCount">
            <div class="c-thumbnail" v-square v-if="i==1"></div>
            <div class="c-thumbnail" v-else></div>
          </div>
        </div>
      </div>
      <!--操作-->
      <div class="col-md-6" id="rightview">
        <h2>
          Winter Collection - Paris Jacket
        </h2>
        <div style="margin:30px 0;width: 150px;height: 2px;background-color: #d3995f"></div>
        <div class="commodity-price">
          $89.99
        </div>
        <!--options-->
        <options></options>
        <!--buy-->
        <div class="buy-btn" style="cursor: pointer">BUY THIS ITEM</div>
        <!--group-->
        <accordion-view></accordion-view>
      </div>
    </div>
    <!--Similiar Items-->
    <similiar-items></similiar-items>
  </div>
</template>

<script>
  import SimiliarItems from './SimiliarItems.vue'
  import AccordionView from './AccordionView.vue'
  import Options from './Options.vue'

  import Vue from 'vue'
  Vue.directive('square', {
    // 当绑定元素插入到 DOM 中。
    inserted: function (el) {
      // 聚焦元素
      let width = $(el).width()
      let thumbnails = $('.c-thumbnail')

      for (let item of thumbnails) {
        $(item).css('height', width)
      }
      $('#rightview').css('height', $('#leftview').height())
    }
  })
  export default {
    name: 'main_view',
    components: {SimiliarItems, AccordionView, Options},
    data () {
      return {
        thumbnailCount: 3,
      }
    },
    mounted(){
    }
  }
</script>

<style scoped>
  #rightview {
    position: relative;
    overflow: auto;
  }
  
  .col-1 {
    padding-right: 6px;
  }
  
  .col-2 {
    padding-left: 6px;
    padding-right: 6px;
  }
  
  .col-3 {
    padding-left: 6px;
  }
</style>
