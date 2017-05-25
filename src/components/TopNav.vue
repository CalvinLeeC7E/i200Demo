<template>
  <div id="top_navbar" class="navbar navbar-inverse navbar-static-top new-height">
    <div class="container">
      <div class="navbar-header">
        <button class="navbar-toggle collapsed" type="button" data-toggle="collapse" data-target="#first_nav_bar">
          <span class="sr-only">Toggle navigation</span>
          <span class="icon-bar"></span>
          <span class="icon-bar"></span>
          <span class="icon-bar"></span>
        </button>
      </div>
      <div class="navbar-collapse collapse" id="first_nav_bar" role="navigation">
        <ul class="nav navbar-nav">
          <li>
            <a href="#">gabooo@mail.com</a>
          </li>
          <li>
            <a href="#">+12 345-678-90</a>
          </li>
        </ul>
        <ul class="nav navbar-nav navbar-right hidden-sm">
          <li>
            <a href="#"><i class="fa fa-facebook"></i></a>
          </li>
          <li>
            <a href="#"><i class="fa fa-twitter"></i></a>
          </li>
          <li>
            <a href="#"><img class="icon-image" src="../assets/images/g+.png"></a>
          </li>
          <li>
            <a href="#">Login</a>
          </li>
          <li>
            <a href="#">Register</a>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'top_navbar',
    data () {
      return {}
    }
  }
</script>

<style scoped>
  .new-height li>a {
    padding-top: 10px;
    padding-bottom: 10px;
  }
</style>
