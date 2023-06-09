<script>
  export let size = 'small';
  export let shadow = false;

  export let bgColor = 'inherit';
  export let textColor = 'inherit';
</script>

  <!-- style:background-color={bgColor}
  style:color={textColor} -->
<button 
  style:--buttonBgColor={bgColor}
  style:--buttonTextColor={textColor}
  class:size-lg={size === 'large'}
  class:size-sm={size === 'small'}
  class:shadow={shadow}
><slot>Default Text</slot></button>

<style lang="scss">
  button {
    border: none;
    background-color: var(--buttonBgColor);
    color: var(--buttonTextColor);
    font-weight: bold;
    border-radius: 5px;
    cursor: pointer;
    &:hover {
      background-image: linear-gradient(rgba(0,0,0,0.4) 0 0);
    }
    &:active {
      background-image: linear-gradient(rgba(255, 255, 255, 0.2) 0 0);
    }
    &.size-sm {
      padding: 15px 20px;
    }
    &.size-lg {
      padding: 20px 30px;
      font-size: 20px;
    }
    &.shadow {
      box-shadow: 0 0 10px rgba(1,1,1,0.6);
    }
  }
</style>