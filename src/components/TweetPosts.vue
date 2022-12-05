
<template>
    <div>
        <button>Switch</button>
        <article v-for="(tweet, index) in tweets" :key="index">
            <p>{{tweets[`posts`]}}</p>
            <p>{{tweets[`users`]}}</p>
            <p>{{tweets[`dates`]}}</p>
        </article>
    </div>
</template>

<script>
    export default {
        name: "TweetPosts",
        data(){
            return{
                isList: true,
                tweets:{
                    posts: ["Did you mean Blake?", "It's Jacqueline"],
                    users: ["Blake", "Jacqueline"],
                    dates: ["03/12/2022", "05/09/2021"],
                    }
                
            }
        },
        methods: {
                gridList(){
                    if (this.isList){
                        document.body.style.backgroundColor = `white`;
                    }else{
                        document.body.style.backgroundColor = `blue`;
                    }
                    this.isList = !this.isList
                    console.log(`it worked`);
                },
                // showPost() {
                //     let myDiv = document.querySelector(`article`);
                //     for (let tweet of this.tweets.posts){
                //     myDiv.insertAdjacentHTML(`beforeend`, `<p>${tweet}</p>`)
                //     }
                //     for (let user of this.tweets.users){
                //     myDiv.insertAdjacentHTML(`beforeend`, `<p>${user}</p>`)
                //     }
                //     for (let date of this.tweets.dates){
                //     myDiv.insertAdjacentHTML(`beforeend`, `<p>${date}</p>`)
                //     }
                // }
            },
            mounted () {
                document.querySelector(`button`).addEventListener(`click`, this.gridList);
                // this.showPost();
            },
    }
</script>

<style scoped>
    article{
        display: grid;
        grid-template-columns: 1fr 1fr;
        border: navy 2px solid;
    }
</style>