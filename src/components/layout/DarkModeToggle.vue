<template>
  <div class="toggle-wrapper">
    <label class="toggle">
      <input
        type="checkbox"
        :checked="mode === 'night' ? 'checked' : false"
        @change="$emit('toggle')"
      />
      <v-img
        id="icon-dark"
        :src="require('/src/assets/circle-dark.svg')"
      ></v-img>
    </label>
  </div>
</template>

<script>
export default {
  props: ["mode"],
};
</script>

<style>
.toggle-wrapper {
  height: 100%;
  width: 5vw;
  display: flex;
  justify-content: center;
  cursor: pointer;
}
.toggle {
  display: flex;
  justify-content: center;
  align-items: center;
}
.toggle input {
  opacity: 0;
  width: 0;
  height: 0;
}
@media screen and (max-width: 600px) {
  .toggle {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 8vw;
  }
  .toggle-wrapper {
    width: 8vw;
  }
}</style
>r
