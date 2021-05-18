<template>
  <nav class="navbar navbar-expand-lg navbar-light bg-light">
    <div class="container-fluid">
      <div class="navbar-header">
        <router-link to="/" class="navbar-brand"> Stock Trader</router-link>
      </div>

      <div class="collapse navbar-collapse">
        <ul class="navbar-nav me-auto mb-2 mb-lg-0">
          <router-link to="/portfolio" active-class="active" tag="li">Portfolio</router-link>
          <router-link to="/stocks" active-class="active" tag="li">Stocks</router-link>
        </ul>
        <ul class="nav navbar-nav navbar-right">
          <li><a href="#">End Day</a></li>
          <li class="drop-down">
            <a href="#"
              class="dropdown-toggle"
              data-toggle="dropdown"
              role="button"
              aria-haspopup="true"
              aria-expanded="false">
              Save & Load <span class="caret"></span>
            </a>
            <ul class="dropdown-menu">
              <li> <a href="#">Save Data</a></li>
              <li> <a href="#">Load Data</a></li>
              
            </ul>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>