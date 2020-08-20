<template>
    <div>
      <p> HP Player {{randomNumber(1,3)}}
          {{ player[randomNumber(1,3)-1].name }}
      </p> 
      +รูป
      <hr />
        name = {{ aPlayer.name }}
        hp = {{ aPlayer.hp }}
        image = {{ aPlayer.image }}
      <hr />
      <p> HP Monster {{randomNumber(4,6)}}
          {{ player[randomNumber(4,6)-1].name }}
      </p> 
      +รูป
      <button @click="start()">Start</button>
      <button @click="attack()">Attack</button>
    </div>
</template>

<script>
export default {
    data:function(){
        return{ 
            aPlayer: { name: '', HP: 0, image: '' },
            // ชื่อ player[random].name
            player: [ { name: 'Knight', HP: 75, image: '1' },
                      { name: 'Swordsman', HP: 100, image: '2' },
                      { name: 'Archer', HP: 125, image: '3' } ],
            Monster: [ { name: 'Bird', HP: 100, image: '4' },
                       { name: 'Golem', HP: 150, image: '5' },
                       { name: 'Panda', HP: 200, image: '6' } ],
        }
    }
    methods:{
        randomDamage: function(min, max) {             
            return Math.max(Math.floor(Math.random() * 
            max) + 1, min);    
        },

        start:function(){
            // 1. random Player 1-3 --> ชื่อ hp รูป 
            this.player = this.player[this.randomNumber(1,3)-1]
            //{...}

            // 2. random Monster 1-3  
            this.Monster = this.Monster[this.randomNumber(4,6)-1]
        },

        attack:function(){
            // 1. player --> monster
            // 2. player <-- monster
            // 3. player.hp? <==0 ===> ?
            // 4. monster.hp? <==0 ===> ?
            // 5. END GAME
        }
    }
}
</script>

<style></style>