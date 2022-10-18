<template>
    <div class="card_product" ref="box">
        <div id="rating_product">
            <p id="note">{{item.rate}} <img src="@/assets/icons_star.png" alt="star"></p>
        </div>
        <div >
            <img id="img_product" :src="require('@/assets/' + item.image + '')" alt="vanilla_latte_product">
        </div>
        <div id="body_card">
            <div id="cart_text">
                <h3 id="title_product">{{item.title}}</h3>
                <div id="product_caracteristic">
                    <button id="hot" @click="hot">Hot</button>
                    <button id="cold" @click="cold">Cold</button>
                </div>
            </div>
            <div id="product_right_column">
                <h3 id="price_product">21 K</h3>
                <button id="addToCart_button"><img src="@/assets/icons_AddToCartButton.png" alt="icons_addtocart"></button>
            </div>
        </div>

    </div>
</template>

<script>
export default {
  name: 'CardProduct',
  props: {
    product: Object
  },
  setup (props) {
    return {
      item: props.product
    }
  },
  methods: {
    cold () {
      this.$refs.box.style.backgroundColor = 'lightblue'
    },
    hot () {
      this.$refs.box.style.backgroundColor = 'orange'
    }
  }
}
</script>

<style>
.card_product{
    background-color: white;
    width: 355px;
    height: 385px;
    border-radius: 20px;
    border: solid 4px lightgray;
    filter: drop-shadow(10px 10px 32px rgba(0, 0, 0, 0.25));
    }

#rating_product{
    position: absolute;
    background-color: white;
    border: solid 4px lightgray;
    border-radius: 999px;
    width: 60px;
    height: 25px;
    left: 40px;
    top: 30px;
    font-size: 16px;
    line-height: 19px;
    display: flex;
    align-items: center;
    text-align: center;
    color: #000000;
}

#note{
    font-weight: bold;
    margin-left: 10px;

}

#img_product{
    border: solid 4px lightgray;
    width: auto;
    height: auto;
    left: 0px;
    margin-top: 15px;
    border-radius: 10%;
}

#body_card{
    display: flex;
    justify-content:space-around;
    align-items:center;

}

#cart_text {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: flex-start;
    margin-left: 20px;
}

#title_product{
    font-size: 20px;
    line-height: 23px;
    margin: 15px 0px;
    text-align: center;
    color: #000000;
    font-weight: bold;
}

#product_caracteristic{
    display: flex;
    justify-content: space-between;
    width: 150px;
}

#hot{
    border :solid 3px #FFD28F;
    background-color: white;
    border-radius: 10px;
    width: 60px;
    height: 25px;
    font-size: 20px;
    line-height: 20px;
    text-align: center;
    color: #FFD28F;
    font-style:'Poppins';
}

#hot:hover{
    border: solid #FF902B;
    color: #FF902B;
}

#cold{
    border :solid 3px #FFD28F;
    background-color: white;
    border-radius: 10px;
    width: 60px;
    height: 25px;
    font-size: 20px;
    line-height: 20px;
    text-align: center;
    color: #FFD28F;
    font-style:'Poppins';
}

#cold:hover{
    border: solid #FF902B;
    color: #FF902B;
}

#product_right_column{
    flex-direction: column;
    justify-content: space-around;
    align-items: center;
    margin-right: 20px;
    padding-top: 20px;
}

#addToCart_button{
    border: none;
    background-color: white;
    width: 50px;
    height: 50px;
    border-radius: 999px;
    margin-top: 20px;
}

#addToCart_button:hover{
    background-color: #FF902B;
}

#price_product{
    font-size: 20px;
    line-height: 23px;
    color: #000000;
    font-weight: bold;
}

</style>
