<template>
    <div class="about-page"> 
        <h2 class="about-page__title">Відгуки</h2>
        <carousel :items-to-show="1">
            <slide 
                v-for="slide in sliders" 
                :key="slide.id"
                >
                    <span class="about-page__slide">{{ slide.text }}</span>
            </slide>
            <template #addons>
                <navigation />
                <pagination />
            </template>
        </carousel>        
    </div>
</template>

<script>   
    import 'vue3-carousel/dist/carousel.css'
    import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel'
    export default {
        name: 'AboutMePage',
        components: {
            Carousel,
            Slide,
            Pagination,
            Navigation,
        },
        data: () => {
            return { 
                sliders: [
                    {
                        text: 'Задоволена сесією з Аліною, вона чуйний, професійний та підтримуючий терапевт. Однозначно забронюю більше сесій з нею.',
                        id: 1
                    },
                    {
                        text: 'Задоволена сесією з Аліною, вона чуйний, професійний та підтримуючий терапевт. Однозначно забронюю більше сесій з нею.',
                        id: 2
                    },
                    {
                        text: 'Задоволена сесією з Аліною, вона чуйний, професійний та підтримуючий терапевт. Однозначно забронюю більше сесій з нею.',
                        id: 3
                    },
                    {
                        text: 'Задоволена сесією з Аліною, вона чуйний, професійний та підтримуючий терапевт. Однозначно забронюю більше сесій з нею.',
                        id: 4
                    },
                    {
                        text: 'Задоволена сесією з Аліною, вона чуйний, професійний та підтримуючий терапевт. Однозначно забронюю більше сесій з нею.',
                        id: 5
                    },
                    {
                        text: 'Задоволена сесією з Аліною, вона чуйний, професійний та підтримуючий терапевт. Однозначно забронюю більше сесій з нею.',
                        id: 6
                    }
                ]
            }
        }
    }
</script>

<style lang="scss">
    .about-page {
        display: flex;
        flex-direction: column;
        align-items: center;
        background-color: #fffff5;
        height: 600px;
        &__title {
            font-family: 'Poppins', sans-serif;
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
        &__slide {
            width: 70%;
        }
    }
    .carousel {
        width: 100%;
        height: 400px;
        &__viewport {
            width: 100%;
            height: 100%;
            margin: 0 auto;
        }
        &__track {
            width: 100%;
            height: 100%;
        }
        &__pagination-button::after {
            background-color: rgba(247, 236, 222, 1);
        }
        &__pagination-button--active::after {
            background-color: rgba(255, 0, 0, 0.5);
        }
        &__pagination-button:hover::after {
            background-color: rgba(255, 0, 0, 0.5);
        }
        &__icon {
            color: rgba(255, 0, 0, 0.5);
        }
    }
</style>
