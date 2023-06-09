<script>
  export let size = 'small';
  export let shadow = false;
</script>

<button class={size === 'large' ? "size-lg" : "size-sm"}><slot>Default Text</slot></button>

<style lang="scss">
  button {
    border: none;
    background-color: #ff3e00;
    color: #ffffff;
    font-weight: bold;
    border-radius: 5px;
    cursor: pointer;
    &.size-sm {
      padding: 15px 20px;
    }
    &.size-lg {
      padding: 20px 30px;
      font-size: 20px;
    }
  }
</style>