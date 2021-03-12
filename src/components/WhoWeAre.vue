<template>
  <section class="section">
    <div class="container content is-small">
      <h1 class="title">
        <span class="ourcolor">-</span> Who we are<span class="ourcolor"
          >?</span
        >
      </h1>
    </div>
    <div class="block columns is-mobile is-multiline">
      <GithubBadge
        username="ilonadynska"
        class="column is-narrow"
        :width="120"
        :height="120"
        shape="round"
      />
      <GithubBadge
        username="matteocrippa"
        class="column is-narrow"
        :width="120"
        :height="120"
        shape="round"
      />
    </div>
  </section>
</template>

<script>
import GithubBadge from './GithubBadge.vue';

export default {
  name: 'WhoWeAre',
  components: {
    GithubBadge,
  },
};
</script>
