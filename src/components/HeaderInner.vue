<template>

    <header class="header">
        <div class="container">
            <div class="header__inner">
                <nav class="menu">
                    <ul class="menu__list">
                        <li class="menu__list-item">
                            <a class="menu__list-link" href="#">Світильники</a>
                        </li>
                        <li class="menu__list-item">
                            <a class="menu__list-link" href="#">Кришталеві підвіски</a>
                        </li>
                                                <li class="menu__list-item">
                            <a class="menu__list-link" href="#">Кришталева плитка</a>
                        </li>
                    </ul>
                </nav>
                <a href="#" class="logo">
                    <HeaderLogo />
                </a>
                <nav class="menu">
                    <ul class="menu__list">
                        <li class="menu__list-item">
                            <a class="menu__list-link" href="#">3D сувеніри</a>
                        </li>
                        <li class="menu__list-item">
                            <a class="menu__list-link" href="#">Фігурки</a>
                        </li>
                        <li class="menu__list-item">
                            <a class="menu__list-link" href="#">Стрази</a>
                        </li>
                    </ul>
                </nav>
                <button class="header__btn">
                    <img src="../assets/images/svg/icon_menu.svg" alt="icon menu">
                </button>

                <SideMenu />
            </div>
        </div>
    </header>
    
</template>

<script>
    import HeaderLogo from "../components/HeaderLogo.vue";
    import SideMenu from "../components/SideMenu.vue";

export default{
    name: 'HeaderInner',
    components: {
        HeaderLogo,
        SideMenu
    },
    // data () {
    //     return {
    //         iconMenu: require('../assets/images/svg/icon_menu.svg')
    //     }
    // }
}
</script>

<style lang="scss" scoped>

.header__inner {
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 12rem;
}
.header__btn {
    border: none;
    background: transparent;
    cursor: pointer;
}

.logo {
    margin: 0 auto;
}

.menu {
    padding-right: 1.5rem;
    font-size: 1.4rem;
    line-height: 1.5;
    &__list {
        display: flex;
        list-style: none;
        &-item {
            padding-right: 4.5rem;
            padding-left: 3.5rem;
        }
        &-link {
            font-family: 'Montserrat', sans-serif;
            font-weight: 700;
            color: rgba(54, 56, 56, 0.9);
            text-decoration: none;
        }
    }
}

</style>