<script setup lang="ts">

//import { computed } from 'vue';
//import { useStore } from '../store';
import FilterProduct from './filterProduct.vue';
import { defineProps } from 'vue';

interface Card {
    id: number;
    ide: number | string;
    name: string;
    image: string;
    price: number;
    quantity: number;
    trending: boolean;
    color: string;
    size: string;
}
const props = defineProps<{ card: Card }>()


//const store = useStore();
//const grandTotal:number = computed<number>(() => store.sum);
//const cardCurrent = computed<Card | null>(() => store.getCardCurrent);
</script>

<template>
    <div>
        <div class="about wrap">
            <div class="center wrap center-about">
                <h1 class="center-about-h1">WOMEN COLLECTION</h1>
            </div>
            <div class="center-line">
                <img src="../../public/img/linepink.svg" alt="linepink">
            </div>
            <div>
                <h2 class="center-about-h2">MOSCHINO CHEAP AND CHIC</h2>
            </div>
            <div>
                <p class="center-about-p">Compellingly actualize fully researched processes before proactive
                    outsourcing.
                    Progressively syndicate
                    collaborative architectures before cutting-edge services. Completely visualize parallel core
                    competencies rather than exceptional portals. </p>
            </div>
            <div>
                <p class="sale561">$ {{ props.card?.price }}</p>
            </div>
            <hr class="hr">

            <filter-product></filter-product>
        </div>
    </div>
</template>
