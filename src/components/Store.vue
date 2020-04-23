<template>
    <div class="container-fluid">
        <div class="row">
            <div class="col bg-dark text-white">
                <a class="navbar-brand">SKLEP SPORTOWY</a>
                <cart-summary />
            </div>
        </div>
        <div class="row">
            <div class="col-3 bg-info p-2">
                <category-controls class="mb-5" />
                <button class="btn btn-block btn-warning mt-5" v-on:click="setShowSearch(true)">Szukaj</button>
            </div>
            <div class="col-9 bg-success p-2">
                <search />
                <product-list />
            </div>
        </div>
    </div>
</template>
<script>
import ProductList from "./ProductList";
import CategoryControls from "./CategoryControls";
import CartSummary from "./CartSummary";
import Search from "./Search";
import { mapMutations } from "vuex";

export default {
    components: { ProductList, CategoryControls, CartSummary, Search },
    methods: {
        ...mapMutations(["setShowSearch"])
    }
}
</script>
