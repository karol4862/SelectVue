<template>
  <div>
    <SelectVue v-model="results" :options="options" label="value" requiredForm/>
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
        value: 'option 1',
      },
      {
        id: 2,
        value: 'option 2',
      },
      {
        id: 3,
        value: 'option 3',
      },
      {
        id: 4,
        value: 'option 4',
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
