<template>
    <div class="contact-page"> 
        <div class="contact-page__image-wrap">
            <img src="../assets/images/contact.jpg" alt="contact" class="contact-page__image">
        </div>
        <div class="contact-page__content">
            <h2 class="contact-page__title">Зв'яжись зі мною</h2>
            <div class="contact-page__btns">
                <a href="https://t.me/Alina_Psychologist" target="_blank" class="contact-page__link">
                    <span class="icon-telegram"></span>
                    <p class="contact-page__text">Telegram</p>  
                </a>
                <a href="https://msng.link/o/?380935767257=vi" target="_blank" class="contact-page__link">
                    <span class="icon-viber"></span>
                    <p class="contact-page__text">Viber</p>  
                </a>
                <a href="https://instagram.com/alinagaidash?igshid=YmMyMTA2M2Y=" target="_blank" class="contact-page__link">
                    <span class="icon-instagram"></span>
                    <p class="contact-page__text">Instagram</p>  
                </a>
            </div>
        </div>
    </div>
</template>

<script>    
    export default {
        name: 'ContactPage'
    }
</script>
<style lang="scss">
    .contact-page {
        display: flex;
        align-items: center;
        justify-content: space-between;
        flex-direction: row-reverse;
        @media (max-width: 500px) {
            flex-direction: column-reverse;
        }
        &__image-wrap {
            width: 50%;
            overflow: hidden;
            position: relative;
            height: 600px;
            @media (max-width: 935px) {
                height: 450px;
            }
            @media (max-width: 500px) {
                height: 300px;
                width: 100%;
            }
        }
        &__image {
            width: 100%;
            height: 80%;
            object-fit: contain;
            object-position: center;
            position: absolute;
            top: 40px;
        }
        &__content {
            width: 50%;
            display: flex;
            align-items: center;
            flex-direction: column;
            gap: 50px;
            padding: 50px 0 20px;
            @media (max-width: 935px) {
                gap: 20px;
            }
            @media (max-width: 425px) {
                padding-top: 20px;
                width: 100%;
            }
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
        &__btns {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 20px;
        }
        &__link {
            text-decoration: none;
            display: flex;
            align-items: center;
            justify-content: center;
            border: 1px solid #ddd;
            box-sizing: border-box;
            border-radius: 5px;
            gap: 10px;
            width: 150px;
            height: 50px;
            color: #000;
            cursor: pointer;
            font-size: 18px;
            &:hover {
                opacity: 0.5;
            }
            @media (max-width: 768px) {
                font-size: 14px;
            }
        }
        &__resume {
            background-color: #d14836;
            color: #fff;
            cursor: pointer;
            font-size: 18px;
            text-decoration: none;
            width: 250px;
            height: 50px;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 5px;
            &:hover {
                opacity: 0.7;
            }
            @media (max-width: 768px) {
                font-size: 14px;
                width: 200px;
            }
        }
    }
</style>