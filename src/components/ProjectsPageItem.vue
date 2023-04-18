<template>
    <a target="_blank" :href="project.link" class="projects-item">   
        <div class="projects-item__image-wrap">        
            <img class="projects-item__image" :src="require('../assets/images/' + project.image)" alt="projects-photo">
        </div>
        <p class="projects-item__subtitle">{{ project.title }}</p>                
    </a>
</template>

<script>   
    export default {
        name: 'ProjectsPageItem',
        props: {
            project: {
                type: Object,
                default() {
                    return {}
                }
            }
        }
    }
</script>

<style lang="scss">
    .projects-item {
        display: flex;
        flex-direction: column;
        justify-content: stretch;
        flex-basis: 20%;
        box-shadow: 0 0 5px 5px rgba(247, 236, 222, 1);
        border-radius: 20px;
        overflow: hidden;
        cursor: pointer;
        min-width: 260px;
        position: relative;
        text-decoration: none;
        &:hover {
            box-shadow: 0 0 7px 10px rgba(255, 0, 0, 0.5);
        }
        &:hover &__subtitle {
            color: red;
        }
        &__image-wrap {
            position: relative;
            width: 100%;
            padding-top: 60%;
        }
        &__image {
            width: 100%;
            height: 100%;
            opacity: 0.9;
            position: absolute;
            top: 0;
            left: 0;
            object-fit: contain;
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
            min-height: 70px;
            @media (max-width: 425px) {
                font-size: 16px;
            }
        }
    }
</style>