<template>
  <div id="app" class="container-fluid">
    <main>
      <nav class="navbar navbar-expand-lg navbar-light bg-light" id="nav">
        <img alt="Vue logo" src="./assets/logo.png" width="50px">
        <span>Vuetishop</span>
        <button
          class="navbar-toggler"
          type="button"
          data-toggle="collapse"
          data-target="#navbarText"
          aria-controls="navbarText"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarText">
          <ul class="navbar-nav mr-auto">
            <li class="nav-item active ">
              <router-link to="/" class="nav-link float-right">Home</router-link>
            </li>
            <li class="nav-item">
              <router-link to="/products" class="nav-link float-right">All Products</router-link>
            </li>
            <li class="nav-item">
              <a class="nav-link float-right" href="#">Pricing</a>
            </li>
            <li class="nav-item">
              <router-link to="/about" class="nav-link float-right">About</router-link>
            </li>
          </ul>
          <ul class="navbar-nav ml-auto">
            <li class="nav-item">
              <router-link to="/cart" class="nav-link float-right">
                <i class="fa fa-shopping-cart mr-1">
                  <span class="ml-1"></span>
                </i>
              </router-link>
            </li>
            <li class="nav-item dropdown" >
              <a
                class="nav-link dropdown-toggle float-right"
                href="#"
                id="navbarDropdownMenuLink"
                role="button"
                data-toggle="dropdown"
                aria-haspopup="true"
                aria-expanded="false"
              ></a>
              <div class="dropdown-menu" aria-labelledby="navbarDropdownMenuLink">
                <router-link to="/" class="dropdown-item">Profile</router-link>
                <!-- <a class="dropdown-item" href="#">Another action</a>
                <a class="dropdown-item" href="#">Something else here</a>-->
                <router-link
                  to="/"
                  class="dropdown-item text-danger"
                  @click.native="loc_logout"
                >Logout</router-link>
              </div>
            </li>
            <li class="nav-item">
              <router-link to="/login" class="nav-link float-right">Login</router-link>
            </li>
          </ul>
        </div>
      </nav>
      <router-view/>
    </main>

    <footer class="container-fluid footer text-left mt-3">
      <p class="mr-auto">
        Developed by:
        <strong>Bhavesh Chari</strong>
      </p>
      <div style="float:right">
        <a href="mailto:bhaveshchari1997@gmail.com" style="margin-right:10px">
          <i class="fa fa-envelope-open" aria-hidden="true" style="font-size:20px"></i>
        </a>
        <a href="https://github.com/Chari16" target="_blank" style="margin-right:10px">
          <i class="fa fa-github" aria-hidden="true" style="font-size:20px"></i>
        </a>
        <a href="https://www.linkedin.com/in/bhavesh-chari-1703a1107/" target="_blank" style="margin-right:10px">
          <i class="fa fa-linkedin" aria-hidden="true" style="font-size:20px"></i>
        </a>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cartValue: 0
    };
  }

};
</script>


<style lang="scss">
@import "../node_modules/bootstrap/dist/css/bootstrap.min.css";

#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 15px;
  a {
    font-weight: bold;
    color: #2c3e50;
    &.router-link-exact-active {
      color: #42b983;
    }
  }
}

html {
  position: relative;
  min-height: 100%;
}
body {
  margin-bottom: 60px; /* Margin bottom by footer height */
}
.footer {
  position: relative;
  bottom: 0;
  width: 100%;
  height: 60px; /* Set the fixed height of the footer here */
  background-color: #f5f5f5;
}

footer {
  background-color: #f2f2f2;
  padding: 25px;
}

.footer p,
.footer div {
  display: inline;
  vertical-align: top;
  font-family: "Open Sans", sans-serif;
  font-size: 16px;
  line-height: 28px;
}
.footer p {
  font-weight: bold;
}

* a {
  color: #42b983;
}

* .fa {
  font-size: 18px;
}

.buttonGreen-outline {
  width: 100%;
  color: #41b883;
  background-color: transparent;
  border-color: #41b883;
}
.buttonGreen-outline:hover {
  color: #ffffff;
  background-color: #41b883;
  border-color: #41b883;
}

.buttonGreen {
  color: #fff;
  background-color: #41b883;
}

.buttonGreen:hover {
  background-color: #42a97b;
}

</style>
