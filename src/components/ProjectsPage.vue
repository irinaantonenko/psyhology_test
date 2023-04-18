<template>
    <div class="projects-page"> 
        <h2 class="projects-page__title">Теми, з якими я працюю</h2>
        <div class="projects-page__content">
            <projects-page-item
                v-for="project in projects"
                :key="project.id"
                :project="project"
            />
        </div>               
    </div>
</template>

<script>   
    import ProjectsPageItem from "./ProjectsPageItem.vue";
    export default {
        name: 'ProjectsPage',
        data: () => {
            return { 
                projects: [
                {   title: 'Психосоматика',
                    image: 'psychosomatics.jpg',
                    id: 1
                },
                {
                    title: 'Стосунки',
                    image: 'relationships.jpg',
                    id: 2
                },
                {
                    title: 'Страхи',
                    image: 'fears.jpg',
                    id: 3
                },
                {
                    title: 'Тривожність',
                    image: 'anxiety.jpg',
                    id: 4
                },
                {
                    title: 'Самоцінність',
                    image: 'selfworth.jpg',
                    id: 5
                },
                {
                    title: 'Цілі, мрії, плани',
                    image: 'goals.jpg',
                    id: 6
                },
                {
                    title: 'Робота з майбутнім',
                    image: 'future.jpg',
                    id: 7
                },
                {
                    title: 'Фінанси',
                    image: 'finances.jpg',
                    id: 8
                }
            ]
            }
        },
        components: {
            ProjectsPageItem
        }
    }
</script>

<style lang="scss">
        .projects-page {
            display: flex;
            flex-direction: column;      
            background-color: #ffffff;
            padding-bottom: 50px;
            gap: 50px;            
            @media (max-width: 425px) {            
                background-color: #fff;
                gap: 20px;  
            }
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
            &__subtitle {
                font-size: 18px;
                margin: 0 auto;
                text-align: center;                 
                padding: 0 10px;            
                @media (max-width: 425px) {
                    font-size: 16px;
                }
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
