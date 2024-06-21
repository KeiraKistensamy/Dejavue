
<template>
  <div class="container">
    <div class="row" v-if="friends.length">
        <Card v-for="friend in friends" :key="friend.id" >
          <template #cardHeader>
              <img class="img-fluid" :src="friend.profile" :alt="friend.firstName" loading="lazy"/>
              
          </template>
          <template #cardBody>

                    <p>{{friend.id}}</p>
                    <p>{{friend.firstName }}</p>
                    <p>{{friend.lastName }}</p>
                    <p :class="{male: friend.gender.toLowerCase() == 'male', female: friend.gender.toLowerCase() == 'female'}">{{ friend.gender }}</p>
                    <p>{{friend.contact }}</p>

          </template>

        </Card>
    </div>
  </div>
    
</template>

<script>
import Card from "./Card.vue"

export default {
  name: "FriendsComp",
  components: {
    Card,
  },
  computed: {
  },

data() {
  return {
    friends: [
      {
            id: 1,
            firstName:"Chelsea",
            lastName:"Julies",
            gender:"female",
            contact:"096 897 5647",
            profile:"https://keirakistensamy.github.io/allimages/images/KeiraKistensamy.png",
      },
        {
              id: 2,
              firstName:"Daniel",
              lastName:"Nguma",
              gender:"male",
              contact:"096 578 1369",
              profile:"https://keirakistensamy.github.io/allimages/images/KeiraKistensamy.png",
        },
      {
            id: 3,
            firstName:"Erin",
            lastName:"Williams",
            gender:"female",
            contact:"098 764 7223",
            profile:"https://keirakistensamy.github.io/allimages/images/KeiraKistensamy.png",
      },
      {
            id: 4,
            firstName:"Awodwa",
            lastName:"Hendriks",
            gender:"male",
            contact:"028 658 9654",
            profile:"https://keirakistensamy.github.io/allimages/images/KeiraKistensamy.png",
      },
    ]
  }
}
}
</script>


<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.male{
  border: 2px solid gold;
}
.female{
  border: 2px solid pink;
}

</style>
