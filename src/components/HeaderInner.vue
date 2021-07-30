<template>

    <header class="header">
        <div class="container">
            <div class="header__inner">
                <nav class="menu">
                    <ul class="menu__list">
                        <li class="menu__list-item">
                            <a class="menu__list-link" href="#">Про нас</a>
                        </li>
                        <li class="menu__list-item">
                            <a class="menu__list-link" href="#">Gallery</a>
                        </li>
                    </ul>
                </nav>
                <a href="#" class="logo">
                    <HeaderLogo />
                </a>
                <nav class="menu">
                    <ul class="menu__list">
                        <li class="menu__list-item">
                            <a class="menu__list-link" href="#">Blog</a>
                        </li>
                        <li class="menu__list-item">
                            <a class="menu__list-link" href="#">Contact</a>
                        </li>
                    </ul>
                </nav>
                <button class="header__btn">
                    <img src="src/assets/images/svg/icon_menu.svg" alt="icon menu">
                </button>

                <SideMenu />
            </div>
        </div>
    </header>
    
</template>

<script lang="ts">
    import HeaderLogo from "@/components/HeaderLogo";
    import SideMenu from "@/components/SideMenu";

export default{
    name: 'HeaderInner',
    components: {
        HeaderLogo,
        SideMenu
    }
}
</script>

<style scoped>

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
    font-size: 1.6rem;
}
.menu__list {
    display: flex;
    list-style: none;
}
.menu__list-item {
    padding-right: 4.5rem;
    padding-left: 3.5rem;
}
.menu__list-link {
    font-family: 'Montserrat', sans-serif;
    font-weight: 700;
    color: rgba(54, 56, 56, 0.9);
}
</style>