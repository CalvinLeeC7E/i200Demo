<template>
  <div class="panel-group details" id="accordion" role="tablist">
    <!--DETAIL-->
    <div class="panel panel-default" v-for="i in 5">
      <div class="panel-heading" role="tab" id="headingOne">
        <h4 class="panel-title">
          <a role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseOne">
            DETAIL
          </a>
        </h4>
      </div>
      <div id="collapseOne" class="panel-collapse collapse in" role="tabpanel">
        <div class="panel-body">
          Curabitur arcu erat, accumsan id imperdiet et, porttitor at sem. Vestibulum ac diam sit amet quam vehicula
          elementum sed sit amet dui. Vivamus suscipit tortor eget felis porttitor volutpat.
        </div>
      </div>
    </div>
    <!--DELIVERY-->
    <div class="panel panel-default">
      <div class="panel-heading" role="tab" id="headingTwo">
        <h4 class="panel-title">
          <a class="collapsed" role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseTwo">
            DELIVERY
          </a>
        </h4>
      </div>
      <div id="collapseTwo" class="panel-collapse collapse" role="tabpanel">
        <div class="panel-body">
          Curabitur arcu erat, accumsan id imperdiet et, porttitor at sem. Vestibulum ac diam sit amet quam vehicula
          elementum sed sit amet dui. Vivamus suscipit tortor eget felis porttitor volutpat.
        </div>
      </div>
    </div>
    <!--STYLE-->
    <div class="panel panel-default">
      <div class="panel-heading" role="tab" id="headingThree">
        <h4 class="panel-title">
          <a class="collapsed" role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseThree">
            STYLE
          </a>
        </h4>
      </div>
      <div id="collapseThree" class="panel-collapse collapse" role="tabpanel">
        <div class="panel-body">
          Curabitur arcu erat, accumsan id imperdiet et, porttitor at sem. Vestibulum ac diam sit amet quam vehicula
          elementum sed sit amet dui. Vivamus suscipit tortor eget felis porttitor volutpat.
        
        </div>
      </div>
    </div>
    <!--STYLE-->
    <div class="panel panel-default">
      <div class="panel-heading" role="tab" id="headingFour">
        <h4 class="panel-title">
          <a class="collapsed" role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseFour">
            STYLE
          </a>
        </h4>
      </div>
      <div id="collapseFour" class="panel-collapse collapse" role="tabpanel">
        <div class="panel-body">
          Curabitur arcu erat, accumsan id imperdiet et, porttitor at sem. Vestibulum ac diam sit amet quam vehicula
          elementum sed sit amet dui. Vivamus suscipit tortor eget felis porttitor volutpat.
        
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'accordion_view',
    data () {
      return {}
    }
  }
</script>

<style>
</style>
