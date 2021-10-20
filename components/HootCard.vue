<template>
    <div class="card" :class="rarity">
        <img class="owl" :src="imgURL" />
    </div>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
    props: {
        card: {
            type: Object,
            default () {
                return {
                    rarity: 'none',
                    imgURL: ''
                }
            }
        }
    },
    data() {
        return {
            rarity: this.card.rarity,
            imgURL: this.card.imgURL
        }
    }
})
</script>

