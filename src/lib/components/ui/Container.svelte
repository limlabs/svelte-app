<!-- Container.svelte -->
<script lang="ts">
  let className = '';
  export { className as class };
  export let size: 'sm' | 'md' | 'lg' | 'xl' = 'lg';

  const sizes = {
    sm: 'max-w-3xl',
    md: 'max-w-4xl',
    lg: 'max-w-6xl',
    xl: 'max-w-7xl'
  };

  $: classes = `mx-auto px-4 sm:px-6 lg:px-8 ${sizes[size]} ${className}`;
</script>

<div class={classes} {...$$restProps}>
  <slot />
</div>
