<template>
  <div id="game-container">
    <div id="gamesPannel">
      <div class="gamesPannel_left">
        <div class="resources eggs">
          <img src="./assets/egg.png" alt="">
        </div>
        <div class="resources chicken">
          <img src="./assets/chicken.png" alt="">
        </div>
        <div class="resources chicken-mom">
          <img src="./assets/chicken_mom.png" alt="">
        </div>
        <div class="resources roosters">
          <img src="./assets/rooster.png" alt="">
        </div>
        <div class="resources fox">
          <img src="./assets/fox.png" alt="">
        </div>
      </div>
      <div class="gamesPannel_center">
        <div class="dices">
          <div class="dice">
            <img src="./assets/dice_images/dice-1.png" alt="">
          </div>
          <div class="dice">
            <img src="./assets/dice_images/dice-6.png" alt="">
          </div>
        </div>
        <div class="actions">
          <button class="btn btn-throw">Throw dices</button>
        </div>
      </div>
      <div class="gamesPannel_right">
        <img src="./assets/players/player_1.png" alt="">
        <img src="./assets/players/player_2.png" alt="">
      </div>
    </div>
  </div>
</template>

<script>

export default {
  data() {
    return {
      numberOfPlayers: 0,
      playersData: [],
      gameSettings: {
        gameStarted: false,
        playerTurn: 0,
        resourcesAvailable: {
          eggs: 56,
          chickens: 48,
          chicks: 36,
          roosters: 4
        }
      }
    }
  },
  name: 'App',
  components: {}
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 0;
  padding: 0;
}

#game-container {
  width: 100vw;
  height: 100vh;
  background-image: url("./assets/farm.jpg");

  display: flex;
  flex-direction: column;
  align-items: center;
  z-index: 0;
}

#gamesPannel {
  width: 80vw;
  height: 20vh;
  background-color: #2c3e50;
  opacity: 0.85;
  border-radius: 5px;
  margin-top: 5vh;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  justify-items: center;
  z-index: 5;
}

.gamesPannel_left{
  width: 30%;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-around;
  justify-self: flex-start;
  margin: 0 100px;
}
.gamesPannel_center{
  width: 30%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.gamesPannel_center .dices{
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-around;
  height: 50%;
}
.dice {
  width: 45%;
  margin: 20px;
}
.dice img {
  width: 80px;
}

.gamesPannel_center .actions{
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  height: 50%;
}

.btn{
  padding: 15px;
  border-radius: 3px;
  margin-bottom: 10px;
  background-color: chocolate;
  border: none;
  color: #ffffff;
  font-weight: bold;
  font-size: 18px;
}




.gamesPannel_right{
  width: 30%;
  display: inherit;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-around;
}
.resources {
  z-index: 10;
}
</style>
