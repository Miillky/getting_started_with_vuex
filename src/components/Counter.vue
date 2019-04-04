<template>
  <div>
    <p>Clicked {{ count }} times! Count is {{ parity }}.</p>
    <button @click="increment" variant="success" >Increment</button>
    <button @click="decrement" variant="danger">Decrement</button>
    <button @click="incrementIfOdd" variant="info">Increment if Odd</button>
    <button @click="incrementAsync" variant="warning">Increment Async</button>
  </div>
</template>

<script>

import { mapState, mapGetters, mapMutations, mapActions } from 'vuex';

export default {
  name: 'Counter',
  computed: {
    ...mapState([
      'count'
    ]),
    ...mapGetters([
      'parity'
    ])
  },
  methods: mapActions([
    'increment',
    'decrement',
    'incrementIfOdd',
    'incrementAsync'
  ])
}
</script>
