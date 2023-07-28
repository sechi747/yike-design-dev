<template>
  <div :class="bem()">
    <textarea ref="textareaRef" :class="bem('inner')"></textarea>
  </div>
</template>
<script setup lang="ts">
import { ref } from 'vue'
import { TextareaProps } from './textarea'
import { createCssScope } from '../../../utils/bem'
import '../style'

const bem = createCssScope('textarea')

defineOptions({
  name: 'YkTextarea',
})
const props = withDefaults(defineProps<TextareaProps>(), {
  id: '',
})

const textareaRef = ref<HTMLTextAreaElement>()
</script>
