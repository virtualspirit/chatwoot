<script>
import FluentIcon from 'shared/components/FluentIcon/Index.vue';

export default {
  components: { FluentIcon },
  props: {
    link: {
      type: String,
      default: '',
    },
    title: {
      type: String,
      default: '',
    },
  },
  emits: ['selectArticle'],
  data() {
    return {};
  },
  methods: {
    onClick() {
      this.$emit('selectArticle', this.link);
    },
  },
};
</script>

<template>
  <li
    class="py-1 flex items-center justify-between -mx-1 px-1 rounded cursor-pointer text-slate-700 dark:text-slate-50"
    role="button"
    @click="onClick"
  >
    <button class="underline-offset-2 text-sm leading-6 text-left text-maroon">
      {{ title }}
    </button>
    <span class="pl-1 arrow">
      <FluentIcon icon="arrow-right" size="14" />
    </span>
  </li>
</template>

<style lang="scss" scoped>
.text-maroon {
  color: #4a0000;
}
</style>
