<template>
  <div class="about">
    <h3>COPYWRITER. CREATIVE DIRECTOR. PRODUCER.</h3>
    <p>
      Lorem ipsum dolor amet keffiyeh hella skateboard jean shorts, shoreditch blue bottle tacos poutine pop-up chia thundercats vaporware hashtag stumptown. Humblebrag activated charcoal ramps irony, hella quinoa scenester. Post-ironic fashion axe VHS, XOXO mustache 90's normcore gentrify pok pok narwhal schlitz lumbersexual jianbing. Raclette echo park copper mug try-hard.

      Roof party beard tumeric bushwick la croix portland.
    </p>
    <button class="button contact">Contact</button>
  </div>
</template>

<script>

export default {
  name: 'About',

  props: {
    show: Boolean
  },

  computed: {
    showWork() {
      return this.$store.state.viewWork
    }
  },

  methods: {
    viewWork() {
      this.$store.commit('toggleWork')
    }
  }
}

</script>

<style lang="scss">

@import '@/assets/scss/app.scss';

.about {
  position: fixed;
  top: 0;
  left: 0;
  height: calc(100% - 50px);
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  transform: translateX(100%);
  text-align: center;

  h3 {
    color: $red;
  }

  p {
    padding: 0 3rem;
  }

  .contact {
    margin-top: 2rem;
    background: $red;
    color: $yellow;
  }
}

</style>
