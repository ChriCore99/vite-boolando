<script>

    export default {
        props: {
            item: {
                type: Object
            }
        }
    }

</script>

<template>

    <div class="col-3">
        <div class="top-card">
            <img :src="`/img/${item.frontImage}`" alt="" class="principale">
            <div class="badge-container">
                <span class="badge-rosso">-50%</span>
                <span class="badge-verde">Sostenibilità</span>
            </div>
            <span class="badge-cuore"> &hearts; </span>
            <!-- seconda foto -->
            <div class="over">
                <img :src="`/img/${item.backImage}`" alt="" class="secondaria">
            </div>
        </div>
        <div class="bottom-card">
            <p> {{ item.brand }} </p>
            <p>
            <h4> {{ item.name }} </h4>
            </p>
            <p><span>14,98€</span><del>29,99€</del></p>
        </div>
    </div>

</template>

<style lang="scss" scoped>

@use './styleNew/general'

</style>