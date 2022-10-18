<template>
    <div class="header-menu">
          <div class="header-menu__logo">
              <img src="@/assets/LogoImage.png" alt="logo">
              <img src="@/assets/CafeStreet.png" alt="logo_text">
          </div>
          <div class="header-menu__menu">
            <nav>
              <router-link to="/">Home</router-link>
              <router-link to="/about">About</router-link>
              <router-link to="/contact">Contact</router-link>
            </nav>
          </div>
          <div class="search_bar_shoppping_cart">
              <input id="search_bar" type="text" v-model="input" placeholder="Cappuccino"/>
              <button class="header-menu__button"><img src="@/assets/icons_cart.png" alt="Shopping_cart"></button>
          </div>
      </div>
    <router-view/>
  </template>

<script>
export default {

  name: 'HeaderMenu'
}
</script>

<style lang="scss">
* {
  font-family: 'Poppins', sans-serif;
}

.header-menu{
    display: flex;
    justify-content: space-around;
    align-items: center;
    position: auto;
    height: auto;
    background-color: #F6EBDA;
    padding-top: 1%;
}

.header-menu__logo{
    box-sizing: border-box;
    border:  #000000;
}

.header-menu__menu {
    display: flex;
    width: 322px;
    height: 27px;
    left: 554px;
    top: 42px;
}

.search_bar_shopping_cart{
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 100%;
    height: 100%;
    padding: 0;
    margin: 0;
}

#search_bar{
    border: solid black;
    border-radius: 40px;
    margin-right :40px;
    zoom:200%;
    height: 20px;
    //margin-bottom: 2px;
}

.header-menu__button{
    border: none;
    background-color: #F6EBDA;
}

#app {
font-family: Avenir, Helvetica, Arial, sans-serif;
-webkit-font-smoothing: antialiased;
-moz-osx-font-smoothing: grayscale;
text-align: center;
color: #2c3e50;
}

nav {
padding: 30px;
display: flex;
justify-content: space-around;
align-items: center;
list-style: none;
width: 100%;
height: 100%;
padding: 0;
margin: 0;

a {
    font-weight: bold;
    color: black;

    &.router-link-exact-active {
    font-family: 'Poppins';
    font-style: normal;
    color: #FF902A;
    text-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
    }
}
}

</style>
