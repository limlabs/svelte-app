<!-- Card.svelte -->
<script lang="ts">
  let className = '';
  export { className as class };
  export let hoverable = false;
  export let variant: 'default' | 'outline' = 'default';

  const variants = {
    default: 'bg-white',
    outline: 'border border-gray-200'
  };

  $: classes = `rounded-lg shadow-sm ${hoverable ? 'transition-shadow hover:shadow-md' : ''} ${variants[variant]} ${className}`;
</script>

<div class={classes} {...$$restProps}>
  <slot />
</div>

<style>
  /* Add any additional card styles here */
</style>
