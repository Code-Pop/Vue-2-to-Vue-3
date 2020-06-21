<template>
  <div>
    <label>{{ label }}</label>
    <input
      v-bind="{
        ...$attrs,
        onInput: (event) => $emit('update:modelValue', event.target.value)
      }"
      :value="modelValue"
    />
  </div>
</template>

<script>
export default {
  inheritAttrs: false,
  props: {
    modelValue: {
      type: [String, Number],
      default: ''
    },
    label: {
      type: String,
      default: null
    }
  },
  setup (props, context) {
    console.log(context.attrs)
  }
}
</script>
