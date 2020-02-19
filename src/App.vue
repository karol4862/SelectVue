<template>
  <div>
    <SelectVue v-model="results" :options="options" label="id" requiredForm
      searchable
    />
  </div>
</template>

<script>
import SelectVue from './components/SelectVue.vue';

export default {
  name: 'app',
  data() {
    return {
      results: '',
      options: [{
        id: 1,
        key: 'slideshow_homepage',
        name: 'Baner - Karuzela główna na stronie głównej',
        permissions: ['key', 'link', 'imagePath'],
        params: {
          imagePath: 'slideshow_homepage/',
          category: 'baner',
        },
      },
      {
        id: 3,
        key: 'staticPage_content',
        name: 'Zarządzanie treścią na statycznych stronach',
        permissions: ['pageSlug', 'content'],
        params: {
          category: 'strona',
        },
      },
      {
        id: 5,
        key: 'slideNews_homepage',
        name: 'Baner - Karuzela nowości na stronie głównej',
        permissions: ['key', 'link', 'imagePath'],
        params: {
          imagePath: 'slideNews_homepage/',
          category: 'baner',
        },
      },
      ],
    };
  },
  components: {
    SelectVue,
  },
};
</script>

<style lang="scss" scoped>

</style>
