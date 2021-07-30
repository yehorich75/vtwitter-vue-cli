<template>
    <div class="wrapper">
        <!-- header -->
        <HeaderInner />
        <MainContent />
        <!-- <div class="wrapper-content">
            <div class="view">
                <div class="container">
                    <Form @onSubmit="handleSubmit" />
                    <List :items="items" />
                </div>
            </div>
        </div> -->
        <!-- footer -->
    </div>
</template>

<script>
import HeaderInner from "@/components/HeaderInner";
import MainContent from "@/components/MainContent";
import Form from "@/components/Form";
import List from "@/components/List";

export default {
    components: { Form, List, HeaderInner, MainContent },
    data() {
        return {
            items: [
                {
                    id: 1,
                    body: 'hello vue 3',
                    likes: 12,
                    avatar: `https://avatars.dicebear.com/api/male/1.svg`,
                    date: new Date(Date.now()).toLocaleString(),
                },
                {
                    id: 2,
                    body: 'hello world',
                    likes: 6,
                    avatar: `https://avatars.dicebear.com/api/male/2.svg`,
                    date: new Date(Date.now()).toLocaleString(),
                }
            ],
        }
    },
    methods: {
        handleSubmit (item) {
            this.items.push(item)
        }
    }
};
</script>

<style lang="scss">

@import url(https://necolas.github.io/normalize.css/8.0.1/normalize.css);

/* Global */

* {
    padding: 0;
    margin: 0;
    box-sizing: border-box;
}

html,
body {
    height: 100%;
}

html {
    font-size: 10px;
}

body {
    font-family: "Open Sans", sans-serif;
    font-size: 1.6rem;
    line-height: 2.7rem;
    font-weight: 400;
    color: #5a5a5a;
    overflow-x: hidden;
    min-width: 32rem;
}

.wrapper {
    display: flex;
    flex-direction: column;
    min-height: 100%;
}

.main {
    flex: 1 0 auto;
}
.footer {
    flex: 0 0 auto;
}

.container {
    max-width: 1140px;
    margin: 0 auto;
    padding: 0 15px;
}

.container-fluid {
    max-width: 192rem;
    margin: 0 auto;
    padding: 0 1rem;
}

.slick-dots {
    display: flex;
    justify-content: center;
    align-items: center;
    button {
        width: 8px;
        height: 8px;
        background-color: #363838;
        border: none;
        border-radius: 4px;
        margin: 0 15px;
        font-size: 0;
    }
    li.slick-active
        button {
            background-color: #f1d152;
        }
}

</style>

