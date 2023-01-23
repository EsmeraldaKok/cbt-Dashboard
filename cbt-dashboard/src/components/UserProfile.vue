<template>
    <div>
      {{ user.username }} - {{ fullName }}
      <strong>followers</strong> {{ followers }}
      <button @click="followUser">
        Follow
      </button>
    </div>
  </template>

<script>
  
  export default {
    name: 'UserProfile',
    data() {
      return {
        followers:0,
        user: {
          id: 1,
          username: '@_booboo',
          firstName: 'mikey',
          lastName: 'kok',
          isAdmin: true
        }
      }
    },
    watch: {
      followers(newFollowerCount, oldFollowerCount) {
        if (oldFollowerCount < newFollowerCount) {
          console.log(`${this.user.userName} has gained a follower!`)
        }
      }
    },
  
    computed: {
      fullName() {
        return`${this.user.firstName} ${this.user.lastName}`;
      }
    },
  
    methods: {
      followUser() {
        this.followers++
      }
    },
  
    //mounted: when component first load
    mounted() {
      this.followUser();
    }
  }
  </script>
  


