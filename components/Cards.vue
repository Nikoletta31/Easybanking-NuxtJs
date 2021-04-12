<template>
<div>
    <h2>Latest Articles</h2>
<div class="cards-blog">

    <div class="card-blog">
<ul v-for="card in cards" :key="card.index">
    <li>
        <div class="card-blog-white">
            <img :src="card.image"/>
            <div class="card-content">
            <p class="author">{{card.author}}</p>
            <h4>{{card.title}}</h4>
            <p class="text-parag">{{card.text}}</p>
            </div>
        </div>
    </li>
</ul>
    </div>

</div>
    </div>
</template>

<script>
import money from "@/assets/image-currency.jpg";
import plane from "@/assets/image-plane.jpg";
import confetti from "@/assets/image-confetti.jpg";
import restaurant from "@/assets/image-restaurant.jpg";

export default {
    name:"Cards", 
    data(){
        return{
            cards:[
                {
                    image: money, 
                    author: "By Claire Robinson", 
                    title:"Receive money in any currency with no fees", 
                    text: "The world is getting smaller and we’re becoming more mobile. So why should you be forced to only receive money in a single …",
                },
                   {
                    image: restaurant, 
                    author: "By Wilson Hutton", 
                    title:"Treat yourself without worrying about money", 
                    text: "Our simple budgeting feature allows you to separate out your spending and set realistic limits each month. That means you …",
                },
                   {
                    image: plane, 
                    author: "By Wilson Hutton", 
                    title:"Take your Easybank card wherever you go", 
                    text: "We want you to enjoy your travels. This is why we don’t charge any fees on purchases while you’re abroad. We’ll even show you …",
                },
                   {
                    image: confetti, 
                    author: "By Claire Robinson", 
                    title:"Our invite-only Beta accounts are now live!", 
                    text: "After a lot of hard work by the whole team, we’re excited to launch our closed beta. It’s easy to request an invite through the site ...",
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import "@/assets/styles/cards.scss";
</style>