<script setup>
import memoji from "@/assets/image/memoji.png";
import DownloadBtn from "@/components/DownloadBtn.vue";
</script>

<template>
    <div class="home-cointainer">
        <div class="welcome-txt">
            <div class="hi-txt">
                <p>Hello, I'm</p>
            </div>
            <div class="name">
                <p>Mujib Nizar</p>
            </div>
            <div class="intro-txt">
                <p>A Python developer currently working in financial sector, 
                    experienced in API development using Django and Flask</p>
            </div>
            <DownloadBtn/>
        </div>
        <div class="profile-pic">
            <div class="pic">
                <img :src="memoji" alt="Profile picture" />
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "HomePage",
    components: {
        DownloadBtn
    },
    data(){
        return {
            memoji:memoji,
        }
    }
}
</script>

<style scoped>
.home-cointainer {
    left:15rem; top: 5rem;
    width: 100vh;
    display: grid;
    font-family: 'Roboto',sans-serif;
    font-size: 3.5rem;
}

.welcome-txt {
    width: 70vh;
}

.hi-txt{
    color: #2983be;
    font-size:2rem;
    font-weight:700;
    
}
.name{
    color:#303841;
    font-style: bold;
    font-weight: 900;
    font-size: 7rem
}

.intro-txt {
    font-size:2rem;
    font-weight: 10;
}

.profile-pic{
    margin-left: 15.5rem;
    grid-row-start:1;
    grid-column-start:2;
}

.pic img{
    width: 25rem;
    height: 25rem;
}

</style>

