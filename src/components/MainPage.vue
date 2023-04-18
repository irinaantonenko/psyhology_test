<template>
    <div class="main-page">  
        <div class="main-page__content">
            <h1 class="main-page__title">Аліна Гайдаш</h1>            
            <h2 class="main-page__subtitle">Психолог</h2>
            <p class="main-page__text">Мене звати Аліна Гайдаш.
                Я практичний психолог, спеціаліст з психосоматики. В мене на сторінці Ви зможете знайти багато цікавої та корисної інформації про психіку та тіло. В сторіз можна задавати питання МАКартам. Хочу бачити навколо щасливих і здорових людей, тому  подарую консультацію щодо психосоматики або будь-якого іншого запиту (тривожність, страхи, самоцінність, реалізація, відносини, гроші тощо).
            </p>
        </div>
        <div class="main-page__image-wrap">
            <img src="../assets/images/11.jpg" alt="main" class="main-page__image">
        </div>
    </div>
</template>

<script>  
    export default {
        name: 'MainPage'
    }
</script>

<style lang="scss">
    .main-page {
        display: flex;
        align-items: center;
        justify-content: space-between; 
        flex-direction: row-reverse;      
        background-color: #Fffff5;
        @media (max-width: 935px) {
            flex-direction: column;
        }
        &__content {
            width: 50%;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            gap: 50px;
            min-height: 600px;
            @media (max-width: 935px) {
                width: 100%;
                min-height: 450px;
            }
            @media (max-width: 768px) {
                gap: 30px;
            }
        }
        &__subtitle {
            font-size: 16px;
            text-transform: uppercase;
            @media (max-width: 425px) {
                font-size: 14px;
            }
        }
        &__title {
            font-family: 'Poppins', sans-serif;
            font-size: 60px;
            text-align: center;
            @media (max-width: 935px) {
                font-size: 50px;
            }
            @media (max-width: 425px) {
                font-size: 40px;
                margin-bottom: 0;
            }
        }
        &__text {
            width: 400px;
            font-size: 16px;
            @media (max-width: 935px) {
                width: 500px;
            } 
            @media (max-width: 590px) {
                width: 80%;
            }
            @media (max-width: 500px) {
                font-size: 14px;
            }
        }
        &__mail {
            text-transform: uppercase;
            text-decoration: none;
            padding-bottom: 10px;
            border-bottom: 1px solid #000;
            color: #000;
            &:hover {
                color: red;
                border-bottom: 1px solid red;
            }
        }
        &__image-wrap {
            position: relative;
            width: 50%;
            height: 600px;
            overflow: hidden;
            @media (max-width: 935px) {
                width: 100%;
                height: 450px;
            }
            @media (max-width: 425px) {
                height: 400px;
            }
        }
        &__image {
            width: 100%;
            height: 90%;
            object-fit: contain;
            object-position:center;
            position: absolute;
            top: 20px;
        }
    }
</style>
