<template>
  <div class="form">
    <label :style="labelStyle">{{ label }}</label>
    <input 
      v-if="type != 'textarea'" 
      :type="type" 
      :value="value" 
      :placeholder="placeholder" 
      :style="inputStyle" 
      :disabled="disabled"/>
    <textarea 
      v-else 
      :style="inputStyle" 
      :rows="rows" 
      :cols="cols" 
      :placeholder="placeholder" 
      :disabled="disabled">{{ value }}</textarea>
    <small :style="descriptionStyle">{{ description }}</small>
  </div>
</template>

<script>

export default {
  name: 'forminput',
  props: [
    'label', 
    'type', 
    'description', 
    'value', 
    'placeholder',
    'disabled',

    'rows',
    'cols',

    'labelStyle',
    'descriptionStyle',
    'inputStyle',
    'textareaStyle'
  ]
}

</script>

<style scoped>
  .form {
    display: grid;
    grid-template-columns: 1fr;
  }
  .form label,
  .form small {
    justify-self: start;
    align-self: center;
  }
  .form small {
    padding-top: 3px;
  }
  .form input,
  .form textarea {
    border: 1px solid black;
    background-color: #ddd;
  }
</style>
