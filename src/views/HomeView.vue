<template>
  <div class="home">
    <div class="hero">
      <HeaderMenu/>
      <img src="@/assets/Hero.png" alt="hero">
    </div>
    <ul id="list_product">
      <li v-for="(coffee, idx) in coffees" :key="idx">
        <CardProduct :product="coffee"/>
      </li>
    </ul>
    <SlotedCard>
      <template #top>
        <div>
          <h2>Bienvenue, nous sommes nous</h2>
        </div>
      </template>
      <template #middle>
        <p>@Created by Valentin LABRUNE All rights reserved</p>
      </template>
      <template #bottom>
        <div>
          <img src="../assets/CafeStreet.png" alt="cafe_quiz1">
        </div>
      </template>
    </SlotedCard>

  </div>
</template>

<script>
import HeaderMenu from '@/components/HeaderMenu.vue'
import CardProduct from '@/components/CardProduct.vue'
import SlotedCard from '@/components/SlotedCard.vue'

export default {
  name: 'HomeView',
  components: {
    HeaderMenu,
    CardProduct,
    SlotedCard
  },
  setup () {
    const coffees = [
      {
        title: 'Vanilla Latte',
        price: '21K',
        rate: '4,8',
        image: 'VanillaLatte_img.png'
      },
      {
        title: 'Espresso',
        price: '12K',
        rate: '4,9',
        image: 'espresso_img.png'
      },
      {
        title: 'Hazelnut Latte',
        price: '23K',
        rate: '4,8',
        image: 'HazelnutLatte_img.png'
      }
    ]
    return {
      coffees
    }
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  font-family: 'Poppins', sans-serif;
}

.home{
  background-color: #F6EBDA;
}

.Hero{
  background-color: #F6EBDA;
  width: 100%;
  height: 100vh;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

#content_hero{
  width: 50%;
  height: 100%;
  justify-content: center;
  align-items: flex-start;
  padding-left: 10%;
}

#hero_details{
  display: flex;
  justify-content: space-around;
  align-items: center;
  width: 100%;
  height: 100%;
  padding: 0;
}

h1{
  font-style: normal;
  text-align: left;
  margin-left: 75px;
  font-size: 48px;
  font-weight: 600;
  line-height:70px;
  color: #000000;
}

strong{
  color: #FF902A
}

 #catch_description{
  font-style: normal;
  font-weight: normal;
  font-size: 18px;
  line-height: 36px;
  width: 350px;
  text-align: left;
  color: grey;
  margin-left: 75px;
}

#list_product{
  display: flex;
  justify-content: space-around;
  align-items: center;
  list-style: none;
}

</style>
