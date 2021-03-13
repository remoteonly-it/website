<template>
  <Header />
  <WhatIsIt />
  <WhoWeAre />
  <WhatWeDo />
</template>

<script>
import Header from './components/Header.vue';
import WhatIsIt from './components/WhatIsIt.vue';
import WhoWeAre from './components/WhoWeAre.vue';
import WhatWeDo from './components/WhatWeDo.vue';

export default {
  name: 'App',
  components: {
    Header,
    WhatIsIt,
    WhoWeAre,
    WhatWeDo,
  },
};
</script>
