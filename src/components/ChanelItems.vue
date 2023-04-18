<template>
    <a target="_blank" :href="chanel.link" class="chanel-items">   
        <div class="chanel-items__image-wrap">        
            <img class="chanel-items__image" :src="require('../assets/images/' + chanel.image)" alt="chanel-photo">
        </div>
        <p class="chanel-items__subtitle">{{ chanel.title }}</p>                
    </a>
</template>

<script>   
    export default {
        name: 'ChanelItems',
        props: {
            chanel: {
                type: Object,
                default() {
                    return {}
                }
            }
        }
    }
</script>

<style lang="scss">
    .chanel-items {
        display: flex;
        flex-direction: column;
        justify-content: stretch;
        flex-basis: 20%;
        box-shadow: 0 0 5px 5px rgba(0, 0, 0, 0.2);
        border-radius: 20px;
        overflow: hidden;
        cursor: pointer;
        min-width: 260px;
        position: relative;
        text-decoration: none;
        &:hover {
            box-shadow: 0 0 7px 10px rgba(255,255,0, 0.5);
        }
        &__image-wrap {
            position: relative;
            width: 100%;
            padding-top: 60%;
        }
        &__image {
            width: 100%;
            height: 100%;
            opacity: 0.8;
            position: absolute;
            top: 0;
            left: 0;
            object-fit: cover;
            object-position: center;
            &:hover {
                opacity: 1;
            }
        }
        &__subtitle {
            padding: 10px;
            font-size: 18px;
            margin: 0 auto;
            color: #000;
            min-height: 100px;
            @media (max-width: 425px) {
                font-size: 16px;
            }
        }
    }
</style>