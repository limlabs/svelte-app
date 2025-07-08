<!-- Button.svelte -->
<script lang="ts">
  let className = '';
  export let variant: 'default' | 'outline' | 'ghost' = 'default';
  export let size: 'sm' | 'md' | 'lg' = 'md';
  export { className as class };

  const variants = {
    'default': 'bg-blue-600 text-white hover:bg-blue-700 focus:ring-blue-500',
    'outline': 'border border-blue-600 text-blue-600 hover:bg-blue-50 focus:ring-blue-500',
    'ghost': 'text-gray-600 hover:text-blue-600 hover:bg-blue-50 focus:ring-blue-500'
  } as const;

  const sizes = {
    'sm': 'px-3 py-1.5 text-sm',
    'md': 'px-4 py-2 text-base',
    'lg': 'px-6 py-3 text-lg'
  } as const;

  $: classes = `inline-flex items-center justify-center rounded-md font-medium transition-colors focus:outline-none focus:ring-2 focus:ring-offset-2 disabled:opacity-50 disabled:pointer-events-none ${variants[variant]} ${sizes[size]} ${className}`;
</script>

<button 
  class={classes} 
  on:click
>
  <slot />
</button>
