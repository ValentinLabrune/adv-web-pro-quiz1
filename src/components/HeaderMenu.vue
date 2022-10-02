<template>
    <div class="header-menu">
        <div class="header-menu__logo">
            <img src="../assets/LogoImage.png" alt="logo">
            <img src="../assets/CafeStreet.png" alt="logo_text">
        </div>
        <div class="header-menu__menu">
            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="#">About</a></li>
                <li><a href="#">Contact</a></li>
            </ul>
        </div>
        <div class="search_bar">
            <input type="text" v-model="input" placeholder="Search..."/>
        </div>
        <div class="Shopping_cart">
            <button class="header-menu__button"><img src="../assets/icons_cart.png" alt="Shopping_cart"></button>
        </div>
    </div>
</template>

<script>
export default {
  name: 'HeaderMenu'
}
</script>

<style scoped lang="scss">
.header-menu{
    display: flex;
    position: absolute;
    width: 1161px;
    height: 40px;
    left: 135px;
    top: 36px;
}

.search_bar{
    position: absolute;
    width: 222px;
    height: 40px;
    left: 1018px;
    top: 36px;
    filter: drop-shadow(6px 2px 24px rgba(0, 0, 0, 0.13));
}

.shopping_cart{
    box-sizing: border-box;

    position: absolute;
    width: 32px;
    height: 32px;
    left: 1264px;
    top: 40px;

    border: 1px solid #000000;
}

.header-menu__menu {
    position: absolute;
    width: 322px;
    height: 27px;
    left: 554px;
    top: 42px;
}

.header-menu__logo{
    box-sizing: border-box;

    position: absolute;
    width: 150px;
    height: 30px;
    left: 135px;
    top: 41px;

    border: 1px solid #000000;
}
</style>
