<template>
  <div className="tweet">
    <ProfileImage :src="imageAvatar" />

    <div className="body">
      <div className="top">
        <User :name="twitterName" :handle="twitterHandle" />

        <Timestamp :timestamp="twitterTimestamp" />
      </div>

      <p className="message">
        {{ message }}
      </p>

      <div className="actions">
        <!-- Font Awesome icons -->
        <i class="far fa-comment"></i>
        <i class="fas fa-retweet"></i>
        <i class="far fa-heart"></i>
        <i class="fas fa-share"></i>
      </div>
    </div>

    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>

<script>
import ProfileImage from './ProfileImage.vue';
import User from "./User.vue";
import Timestamp from "./Timestamp.vue";

  export default {
    components: { ProfileImage, User, Timestamp },
    props: {
      twitterName: {
      type: String,
      default: "Ironhack",
    },
    imageAvatar: {
      type: String,
      required: true,
    },
    twitterHandle: {
      type: String,
    },
    twitterTimestamp: {
      type: String,
      required: true,
    },
    message: {
      type: String,
      required: true,
    },
  },
  };
  </script>

<style scoped>
a {
  color: #42b983;
}
</style>
