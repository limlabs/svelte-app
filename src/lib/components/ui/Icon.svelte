<!-- Icon.svelte -->
<script lang="ts">
  let className = '';
  export { className as class };
  export let size: 'sm' | 'md' | 'lg' = 'md';

  const sizes = {
    sm: 'h-4 w-4',
    md: 'h-5 w-5',
    lg: 'h-6 w-6'
  };

  $: classes = `${sizes[size]} ${className}`;
</script>

<div class={classes}>
  <slot />
</div>

<style>
  /* Add any additional icon styles here */
</style>
