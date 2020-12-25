<template>
  <div class="navigationColor">
    <nav class="navbar" role="navigation" aria-label="main navigation">
      <div class="navbar-brand">
        <a class="navbar-item" href="/">
          <img src="https://chouftv.ma/content/themes/chouftv/dist/images/brand.svg" 
          height="87" width="150"
          style="height:87px !important;min-height:87px;"
          >
        </a>
    
        <a role="button" class="navbar-burger" aria-label="menu" aria-expanded="false" data-target="navbarBasicExample">
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
        </a>
      </div>
    
      <div id="navbarBasicExample" class="navbar-menu">
        <div class="navbar-start">
          <a  href="/" class="navbar-item">
            الصفحة الرئيسية
          </a>
    
          <a href="/posts" class="navbar-item">
            مقالات
          </a>
  
         
    
          
        </div>
    
       
      </div>
    </nav>
  </div>
 
</template>

<style scoped>
  .navigationColor .navbar{
    background-color: #6459a6;
    color:white !important;
  }
  .navigationColor .navbar .navbar-item {
    color:white !important
  }
  .navigationColor .navbar .navbar-item:hover {
    color:black !important
  }
  .navbar-start{
    margin-left: 10px !important;
  }
</style>