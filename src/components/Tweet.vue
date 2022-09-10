<template>
  <div className="tweet">
    <ProfileImage :src="imageAvatar" />

    <div className="body">
      <div className="top">
        <User :name="twitterName" :handle="twitterHandle" />

        <Timestamp :timestamp="twitterTimestamp" />
      </div>

      <Message :message="twitterMessage" />

      <Actions />
    </div>

    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>

<script>
import ProfileImage from './ProfileImage.vue';
import User from "./User.vue";
import Timestamp from "./Timestamp.vue";
import Message from "./Message.vue"
import Actions from "./Actions.vue"

  export default {
    components: { ProfileImage, User, Timestamp, Message, Actions },
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
      required: true,
    },
    twitterTimestamp: {
      type: String,
      required: true,
    },
    twitterMessage: {
      type: String,
      required: true,
      default: "Yep. I'm coding.",
    },
  },
  };
  </script>

<style scoped>
a {
  color: #42b983;
}
</style>
