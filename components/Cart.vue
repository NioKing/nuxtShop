<template>
    <div class="container">
        <div class="cart-card">
            <div class="item-card">
                    <div class="cart-img">
                        <img style="width: 80px;" src="" alt="Product image">
                    </div>
                <div class="cart-product-title">
                    <span>Product title</span>
                </div>
                <div class="cart-quantity">
                    <span class="cart-icon">+</span>
                    <span>2</span>
                    <span class="cart-icon">-</span>
                </div>
                <div class="cart-price">
                    <span>
                        Product price
                    </span>
                </div>
            </div>
            <div class="cart-value-card">
                <div class="cart-value">
                    <span>Total value: </span>
                    <span>$5.19</span>
                </div>
                <div class="btn">
                    <button>Checkout</button>
                </div>
            </div>
            </div>
        </div>
        
</template>

<style>
.cart-card {
    margin-top: 200px;
    border-bottom: 1px solid grey;
    width: 600px;
    padding: 20px;
    box-shadow: 0px 2px 1px -1px rgb(0 0 0 / 20%),
        0px 1px 1px 0px rgb(0 0 0 / 14%),
        0px 1px 3px 0px rgb(0 0 0 / 12%);
    display: flex;
    flex-direction: column;
    gap: 2rem;
}

.item-card {
    display: flex;
    padding: 20px;
    justify-content: space-between;
    box-shadow: 0px 3px 3px -1px rgb(0 0 0 / 20%),
            0px 2px 2px 0px rgb(0 0 0 / 14%),
            0px 1px 3px 0px rgb(0 0 0 / 12%);
    align-items: center;
}

.cart-img {
    display: flex;
}
.cart-product-title {
display: flex;
}
.cart-quantity {
display: flex;
gap: 10px;
align-items: center;
}

.cart-price {
display: flex;
}
.cart-icon {
    background: #F7F5F5;
    border-radius: 15px;
    width: 20px;
    display: flex;
    justify-content: center;
    box-shadow: 0px 2px 1px -1px rgb(0 0 0 / 20%),
            0px 1px 1px 0px rgb(0 0 0 / 14%),
            0px 1px 3px 0px rgb(0 0 0 / 12%);
    cursor: pointer;
}
.cart-value-card {
    display: flex;
    flex-direction: column;
    width: 45%;
    gap: 10px;
    align-self: flex-end;
    text-align: center;
    padding: 10px;
    font-size: 1.25rem;
    border-bottom: 1px solid grey;
}
</style>

<script setup>

</script>