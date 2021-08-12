<template>
    <div class="side-menu side-menu--close">
        <button class="side-menu__close">
            <img src="../assets/images/svg/close.svg" alt="Close button">
        </button>
        <div class="side-menu__content">
            <a class="side-menu__logo" href="#">
                <img src="../assets/images/svg/logo-big.svg" alt="big logo">
            </a>
        <h4 class="side-menu__title">Furniture for life</h4>
            <p class="side-menu__text">Sustainable hot chicken skateboard, dreamcatcher meggings actually squid.
                Slow-carb everyday carry +1 art party microdosing, put a bird on it brooklyn</p>
            <img src="../assets/images/side-menu__img.jpg" alt="Side Menu Image" class="side-menu__img">
        </div>
    </div>
</template>

<script>
export default {
    data () {
        return {
            // closeIcon: require('../assets/images/svg/close.svg'),
            // logoBig: require('../assets/images/svg/logo-big.svg'),
            // sideMenuImg: require('../assets/images/side-menu__img.jpg')

        }
    }
}

// $(function () {
//     $('header__btn').on('click', function () {
//         $('.rightside-menu').removeClass('rightside-menu--close')
//     })
// })
</script>

<style lang="scss" scoped>

/* Side-menu */

.side-menu {
    position: absolute;
    right: 0;
    top: 0;
    max-width: 69.4rem;
    width: 100%;
    height: 100%;
    background-color: #fff;
    padding: 4rem 4rem 0;
    box-shadow: -3px 0px 4px 1px #3638380f;
    transition: all 0.6s;
    z-index: 100;
    &--close {
        transform: translateX(500%);
    }
    &__content {
        text-align: center;
        display: flex;
        flex-direction: column;
        align-items: center;
    }
    &__title {
        font-family: 'Montserrat', sans-serif;
        font-size: 3.6rem;
        line-height: 5.1rem;
        color: #363838;
        font-weight: 700;
        &::after {
            content: '';
            background-color: #6d7278;
            height: 1px;
            width: 25.2rem;
            display: block;
            margin: 1.8rem auto 2.2rem;
        }
    }
    &__logo {
        margin-bottom: 3rem;        
    }
    &__text {
        font-size: 1.6rem;
        line-height: 2.7rem;
        margin-bottom: 4rem;
        max-width: 48.3rem;
    }
    &__img {
        width: 100%;
        max-width: 48.5rem;
        height: auto;
    }
}
</style>