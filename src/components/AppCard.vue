<script>
export default {
    props: {
        card: Object
    }
}
</script>
<template lang="">
    <div class="card">
        <div class="card-img">
            <img :src="card.thumb" :alt="card.series">
        </div>
        <div class="card-title">
            <p>{{card.series}}</p>
        </div>
    </div>
</template>

<style lang="scss" >
.card {
    width: calc(100% / 6 - 10px);
    margin-top: 50px;


    .card-img {
        width: 100%;

        img {
            width: 100%;
            height: 200px;
            object-fit: cover;
            object-position: top;
        }
    }

}

.card-title {
    margin-top: 10px;

    p {
        font-size: 11px;
        text-transform: uppercase;
        color: white;
    }
}
</style>