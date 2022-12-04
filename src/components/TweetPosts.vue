<template>
    <div>
        <button>Tweet</button>
        <article v-for="tweet in tweets" :key="tweet[`post`]">
            <p>{{tweet[`posts`]}}</p>
            <p>{{tweet[`user`]}}</p>
            <p>{{tweet[`date`]}}</p>
        </article>
    </div>
</template>

<script>
    export default {
        name: "TweetPosts",
        data(){
            return{
                tweets :[
                    {
                    posts: "Did you mean Blake?",
                    user: "Blake",
                    date: "03/12/2022",
                    }
                ]
            }
        }
    }
</script>

<style scoped>

</style>