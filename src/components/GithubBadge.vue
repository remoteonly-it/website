<template>
  <div>
    <a v-if="linkable === true" :href="getUrl" target="_blank">
      <img :src="getAvatarUrl" :alt="username" :class="getClass" :width="width" :height="height" />
    </a>
    <img v-else :src="getAvatarUrl" :alt="username" :class="getClass" :width="width" :height="height" />
  </div>
</template>

<style scoped>
  .round {
    border-radius: 50%;
  }
</style>

<script lang="ts">
export default {
  name: 'GithubBadge',
  props: {
    username: {
      required: true,
      type: String,
    },
    shape: {
      type: String,
      default: 'square',
      validator: function(value: string) {
        return ['square','round'].indexOf(value) !== -1
      }
    },
    linkable: {
      default: true,
      type: Boolean,
    },
    width: {
      default: 512,
      type: Number
    },
    height: {
      default: 512,
      type: Number
    }
  },
  computed: {
    getClass: function () {
      return this.shape;
    },
    getUrl: function() {
      return `https://github.com/${this.username}`;
    },
    getAvatarUrl: function() {
      return `https://avatars.githubusercontent.com/${this.username}`;
    }
  }
}
</script>