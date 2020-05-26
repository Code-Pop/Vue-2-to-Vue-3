<template>
  <select name="salutation" @change="$emit('update:salutation', $event.target.value)">
    <option value="">-</option>
    <option
      v-for="slt of salutations"
      :value="slt"
      :key="slt"
      :selected="salutation === slt"
    >
      {{ slt }}
    </option>
  </select>

  <input
    :value="name"
    @input="$emit('update:name', $event.target.value)"
    type="text"
    name="name"
  />
</template>

<script>
const salutations = [
  'Ms.',
  'Mrs.',
  'Miss',
  'Mx.',
  'Dr.'
]

export default {
  emits: ['update:salutation', 'update:name'],
  props: {
    salutation: {
      type: String,
      default: ''
    },
    name: {
      type: String,
      default: ''
    }
  },
  setup () {
    return {
      salutations
    }
  }
}
</script>

<style lang="scss" scoped>
select {
  margin-right: 0.5rem;
}

input {
  width: 50%;
}
</style>
