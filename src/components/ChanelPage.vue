<template>
    <div class="chanel-page"> 
        <h2 class="chanel-page__title">My Youtube chanel</h2>
        <h3 class="chanel-page__subtitle">I created a Ukrainian-language Frontend development course for both beginners and more experienced developers. In my videos, I pay special attention to the Vue.js framework.</h3>
        <p class="chanel-page__text">Here you can see the most popular of them</p>
        <div class="chanel-page__content">
            <chanel-items
                v-for="chanel in chanels"
                :key="chanel.id"
                :chanel="chanel"
            />
        </div> 
    </div>
</template>

<script>  
    import ChanelItems from './ChanelItems.vue';
    export default {
        name: 'ChanelPage',
        components: {
            ChanelItems
        },
        data: () => {
            return { 
                chanels: [
                {   title: 'Creating a project on Vue.js using Vue CLI 3',
                    image: 'lesson1.png',
                    id: 1,
                    link: 'https://www.youtube.com/watch?v=YtVO2ILezgo&t=2s'
                },
                {
                    title: 'Passing data between Vue.js components. Props, v-bind, $emit',
                    image: 'lesson3.png',
                    id: 2,
                    link:'https://www.youtube.com/watch?v=grneI5Vyv98&t=1s'
                },
                {
                    title: 'Getting data from API and working with central data store Vuex',
                    image: 'lesson4.png',
                    id: 3,
                    link:'https://www.youtube.com/watch?v=pJOqLmXMZxo'
                },
                {
                    title: 'VueRouter. Navigation in the project on Vue.js',
                    image: 'lesson6.png',
                    id: 4,
                    link:'https://www.youtube.com/watch?v=V7Eh4cCXoDY'
                }
            ]
            }
        }
    }
</script>
<style lang="scss">
    .chanel-page {
        display: flex;
        flex-direction: column;      
        border-bottom: 1px solid #F6F6F6;
        padding-bottom: 50px;
        gap: 50px;            
        @media (max-width: 425px) {            
            background-color: #F6F6F6;
            gap: 20px;  
        }
        &__title {
            font-family: 'Libre Baskerville';
            font-size: 36px;                
            padding-top: 50px;
            text-transform: uppercase;
            margin: 0 auto;
            @media (max-width: 1440px) {
                font-size: 30px;
            }
            @media (max-width: 768px) {
                font-size: 20px;
            }
            @media (max-width: 425px) {
                padding-top: 20px;
            }
        }
        &__subtitle {
            font-size: 18px;
            margin: 0 auto;
            text-align: center;            
            max-width: 500px; 
            padding: 0 10px;              
            @media (max-width: 425px) {
                font-size: 16px;
            }
        }
        &__text {
            font-style: normal;
            font-size: 16px;
            margin: 0 auto;
            text-align: center;
        }
        &__content {
            max-width: 100%;
            display: flex;
            align-items: center;
            justify-content: space-around;
            gap: 50px;
            flex-wrap: wrap; 
        }
    }
</style>