<template>
    <div class="experience-page">         
        <div class="experience-page__content">
            <h2 class="experience-page__subtitle">Background</h2>            
            <h3 class="experience-page__company">Freelance</h3>
            <p class="experience-page__text">Front-end developer, 2022-2023</p>
            <h3 class="experience-page__company">Moma Gifts</h3>
            <p class="experience-page__text">Front-end developer, 2021-2022</p>
        </div>
        <div class="experience-page__content">
            <h2 class="experience-page__subtitle">Professional Skills</h2>
            <ul class="experience-page__list" type="disc">
                <li class="experience-page__text">HTML&CSS</li>
                <li class="experience-page__text">Javascript</li>
                <li class="experience-page__text">Experience with Vue.js Framework</li>
                <li class="experience-page__text">Experience with CSS preprocessors</li>
                <li class="experience-page__text">Experience with Bootstrap Framework</li>
                <li class="experience-page__text">Knowledge of Git</li>
                <li class="experience-page__text">Experience with Webpack, Gulp</li>
                <li class="experience-page__text">Knowledge of Photoshop Adobe, Figma</li>
                <li class="experience-page__text">Node.js</li>
            </ul>
        </div>
        <div class="experience-page__image-wrap">
            <img class="experience-page__image" src="../assets/images/experience.jpg" alt="about-photo">
        </div> 
    </div>
</template>

<script> 
    export default {
        name: 'AboutMePage'
    }
</script>

<style lang="scss">
        .experience-page {
            display: flex;
            justify-content: space-around; 
            @media (max-width: 1024px) {
                position: relative;
            }
            @media (max-width: 425px) {
                flex-direction: column-reverse;
                padding: 20px 0;
                background-color: #F6F6F6;
            }
            &__content {
                width: 25%;
                display: flex;
                flex-direction: column;
                align-items: flex-start; 
                gap: 20px;
                @media (max-width: 1024px) {
                    width: 30%;
                }
                @media (max-width: 600px) {
                    width: 45%;
                }
                @media (max-width: 425px) {
                    width: 100%;
                    align-items: center;
                }
            }
            &__subtitle {
                font-family: 'Libre Baskerville';
                font-size: 36px;
                padding: 50px 0 20px;
                text-transform: uppercase;
                @media (max-width: 1440px) {
                    font-size: 30px;
                }
                @media (max-width: 768px) {
                    font-size: 20px;
                }
                @media (max-width: 425px) {
                    padding-top: 0;
                }
            }
            &__list {
                padding-bottom: 20px;
            }
            &__text {
                font-size: 16px;
                padding-bottom: 20px;
                @media (max-width: 1960px) {
                    padding-bottom: 10px;
                }
                @media (max-width: 768px) {
                    padding-bottom: 5px;
                }
                @media (max-width: 500px) {
                    font-size: 14px;
                }
            }
            &__image-wrap {
                position: relative;
                width: 30%;
                overflow: hidden;
                padding-top: 20px;
                @media (max-width: 1024px) {
                    position: absolute;
                    bottom: 0;
                    z-index: -1;
                    left: 25%;
                }
                @media (max-width: 600px) {
                    display: none;
                }
            }
            &__image {
                width: 100%;
                height: 100%;
                object-fit: contain;
                object-position: bottom left;
            }
        }
</style>
