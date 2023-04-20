<script>
import { onMounted } from 'vue';


export default {
    props:{
        title: {
            type: String,
            required: true
        },
        imgName: {
            type: String,
            required: true
        }
    },
    data(){
        return{
            rootPath: 'src/img/'
        }
    },
    methods:{
       
    },
}


</script>

<template>
    <div class="card">
        <div>
            <img id="tournamentPicture" class="tournamentPicture" alt="Tournament Picture" :src="`${rootPath}${imgName}`" />
        </div>
        <div class="card-header">
            <h2>{{title}}</h2>
        </div>
        <div class="card-body">
            <ul>
              <li>Number of players registered : 5/8</li>
              <li>Statut : clotured</li>
              <li>Tournament date start : 20/05/2023</li>
              <li>Registration end date : 14/05/2023</li>
            </ul>
        </div>
    </div>
</template>

<style scoped>

    .card{
        display: flex;
        flex-direction: column;
        align-items: center;
        width: 320px;
        height: 370px;
        background-color: #393E46;
        border-radius: 0.5em;
        margin: 1em;
        border: solid #00ADB5 0.1em;
        box-shadow: 0 0 50px rgba(0, 0, 0, 0.5);
        transform: perspective(500px) rotateY(5deg);
        transition : all 0.3s ease-in-out;
    }

    .card:hover{
      transform: scale(1.05);
      transition: all 0.3s ease-in-out;
    }

    .card-header{
        color: #cfcdcd;
        width: 100%;
        height: 8%;
        display: flex;
        flex-direction: row;
        justify-content: start;
        margin-top: 0.5rem;
    }

    .card-header h2{
      text-shadow:
        -0.5px -0.5px 0 #000,  
        0.5px -0.5px 0 #000,
        -0.5px  0.5px 0 #000,
        0.5px  0.5px 0 #000;
        font-size: 1.5em;
        font-weight: bold;
        margin-left: 1rem;
    }

    .card-body{
      width: 100%;
      height: 40%;
      display: flex;
      flex-direction: column;
      justify-content: space-evenly;
      gap:0.1vh;
    }


    .tournamentPicture{
        width: 100%;
        border-radius: 0.5em 0.5em 0 0;
    }

</style>