<template>
    <div>
        <div class="flex-header">

            <div class="images">
                <img class="back-mobile" src="@/assets/bg-intro-mobile.svg"/>
     <img class="back-desk" src="@/assets/bg-intro-desktop.svg"/>
         <img class="image-mobile" src="@/assets/image-mockups.png" />
            </div>

            <div class="text-header">
                <h2>Next generation<br> digital banking</h2>
                <p>Take your financial life online. Your Easybank account will be a one-stop-shop for spending, saving, budgeting, investing, and much more.</p>
                <button class="request-button">Request Invite</button>
            </div>
    </div>

<div class="header-two">
<div class="header-two-header">
    <h2>Why choose Easybank?</h2>
    <p>We leverage Open Banking to turn your bank account into your financial hub. Control your finances like never before.</p>
</div>

<div class="flex-cards">
<ul  v-for="card in cards" :key="card.index">
    
    <li>
    <div class="flex-card-items">
 <img class="icon-green" :src="card.image" /><br>
 
 <h3>{{card.title}}</h3>
 <p>{{card.subtitle}} </p>
</div>
    </li>
 
</ul>
   </div>

</div>

    </div>
</template>

<script>
import online from "@/assets/icon-online.svg"; 
import budgeting from "@/assets/icon-budgeting.svg"; 
import onboarding from "@/assets/icon-onboarding.svg"; 
import apis from "@/assets/icon-api.svg"; 

export default {
    name:"Header", 
    data(){
        return{
            cards:[
                {
                    title: "Online banking", 
                    subtitle: "Our modern web and mobile applications allow you to keep track of your finances wherever you are in the world.", 
                    image: online,
                },
                   {
                    title: "Simple Budgeting", 
                    subtitle: "See exactly where your money goes each month. Receive notifications when you’re close to hitting your limits.", 
                    image: budgeting,
                },
                     {
                    title: "Fast Onboarding", 
                    subtitle: "We don’t do branches. Open your account in minutes online and start taking control of your finances right away.", 
                    image: onboarding,
                },
                     {
                    title: "Open API", 
                    subtitle: "Manage your savings, investments, pension, and much more from one account. Tracking your money has never been easier.", 
                    image: apis,
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import "@/assets/styles/header.scss";

</style>