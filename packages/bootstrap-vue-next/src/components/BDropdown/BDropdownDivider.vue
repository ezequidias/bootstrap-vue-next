<template>
  <li role="presentation">
    <component
      :is="props.tag"
      class="dropdown-divider"
      role="separator"
      aria-orientation="horizontal"
    />
  </li>
</template>

<script setup lang="ts">
import {useDefaults} from '../../composables/useDefaults'
import type {BDropdownDividerProps} from '../../types/ComponentProps'

const _props = withDefaults(defineProps<BDropdownDividerProps>(), {
  tag: 'hr',
})
const props = useDefaults(_props, 'BDropdownDivider')
</script>
