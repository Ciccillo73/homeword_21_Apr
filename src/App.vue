<template>
  <div>
    <h1>Tweets</h1>
    <list-of-tweets-item v-for="(tweet, index) in tweets" :key="index":tweet="tweet" ></list-of-tweets-item>
    <h2>Total Number of Tweets:{{totalTweets}}</h2>
  </div>

</template>

<script>
import ListOfTweets from './components/ListOfTweets.vue'

export default {
  name: 'App',
  data() {
  return {
    tweets:[
      {
        id: 1,
        name: 'James',
        handle: '@jokerjames',
        img: 'https://semantic-ui.com/images/avatar2/large/matthew.png',
        tweet: "If you don't succeed, dust yourself off and try again.",
        likes: 10,
      },
      {
        id: 2,
        name: 'Fatima',
        handle: '@fantasticfatima',
        img: 'https://semantic-ui.com/images/avatar2/large/molly.png',
        tweet: 'Better late than never but never late is better.',
        likes: 12,
      },
      {
        id: 3,
        name: 'Xin',
        handle: '@xeroxin',
        img: 'https://semantic-ui.com/images/avatar2/large/elyse.png',
        tweet: 'Beauty in the struggle, ugliness in the success.',
        likes: 18,
      }
    ]
  }
},
  components: {
    'list-of-tweets-item': ListOfTweets

  },
  computed: {
    totalTweets: function() {
      return this.tweets.reduce((total, tweet) => {
        return total + tweet.likes;
      }, 0);
    }
  }
}
</script>

<style>

</style>
