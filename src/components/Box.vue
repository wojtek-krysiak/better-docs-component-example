<template>
  <section class="wrapper">
    <header>
      {{title}}
      <div class="opts">
        <!-- @slot Options slot with some crazy description -->
        <slot name="options"></slot>
      </div>
    </header>
    <div class='inner-content'>
      <slot />
    </div>
  </section>
</template>

<script>
/**
 * @component
 * @example
 * <Box>
 *   I am inside a slot
 * </Box>
 * 
 * @example
 * <Box>
 *   <ProgressBar :spent="100" :remaining="50"></ProgressBar>
 *   <ProgressBar :spent="50" :remaining="50" style="margin-top: 20px"></ProgressBar>
 * </Box>
 */
export default {
  name: "Box",
  props: {
    title: {
      type: String,
      default: "My box"
    }
  }
}
</script>

<style scoped>
  section.wrapper {
    background: #fff;
    border: 1px solid #DADADA;
    border-radius: 4px;
    padding: 32px;
  }

  section.wrapper > header {
    font-size: 18px;
    color: #211D1A;
    font-weight: bold;
    margin-bottom: 20px;
  }
</style>