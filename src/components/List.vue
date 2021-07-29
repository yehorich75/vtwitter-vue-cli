<template>
    <ul>
        <li
            v-for="(tweet, index) in items"
            :key="tweet.id">
            <img :src="tweet.avatar" width="100" height="100">
            <span>{{tweet.date}}</span>
            <div>{{tweet.body}}</div>
        </li>
    </ul>
</template>

<script>


export default {
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
}
</script>
