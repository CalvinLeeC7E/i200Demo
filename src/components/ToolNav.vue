<template>
  <div id="tool_navbar" class="navbar navbar-inverse navbar-static-top">
    <div class="container">
      <form class="navbar-form navbar-right">
        <div class="input-group no-border-radius">
          <input type="text" class="form-control" placeholder="Search">
          <span class="input-group-addon input-group-addon-c">
        <i class="fa fa-search"></i>
        </span>
        </div>
        <div class="input-group no-border-radius">
        <span class="input-group-addon input-group-addon-c">
        <i class="fa fa-shopping-cart"></i>
        </span>
          <input type="button" class="form-control" value="$79.00">
        </div>
      </form>
      <ul class="nav navbar-nav navbar-right">
        <li>
          <a href="">Shopping Cart</a>
        </li>
        <li>
          <a href="">WishList (7)</a>
        </li>
        <li>
          <a href="">Checkout</a>
        </li>
        <li>
          <a href="">My Account</a>
        </li>
      </ul>
      
      <ul class="nav navbar-nav navbar-left">
        <li class="dropdown">
          <a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button">
            <img src="../assets/images/en.png"> EN <span class="caret"></span>
          </a>
          <ul class="dropdown-menu">
            <li><a href="#">ZH</a></li>
          </ul>
        </li>
        <li class="dropdown">
          <a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button">USD <span class="caret"></span></a>
          <ul class="dropdown-menu">
            <li><a href="#">CNY</a></li>
          </ul>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'tool_navbar',
    data () {
      return {}
    }
  }
</script>

<style>
</style>
