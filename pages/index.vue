<template>
	<div class="wrapper">
		<hero/>
	</div>
	
</template>

<script>
import Button from '@/components/Button.vue'

import hero from './hero.vue'
export default {
  components: { hero },
  name: 'IndexPage'
}

components: {
	Button
	hero
}
</script>
