<template>
  <div @click='focusInput'>
    <v-select :options="options" :label="label" v-model="inputVal">
      <template #search="{attributes, events}">
        <input
          class="vs__search"
          v-bind="attributes"
          :required="requiredForm && !results"
          v-on="events"
        />
      </template>
    </v-select>
  </div>
</template>

<script>
import vSelect from 'vue-select';

export default {
  name: 'SelectVue',
  data() {
    return {
      results: '',
    };
  },
  props: {
    options: Array,
    requiredForm: Boolean,
    label: String,
  },
  components: {
    vSelect,
  },
  computed: {
    inputVal: {
      get() {
        return this.value;
      },
      set(val) {
        this.$emit('input', val);
        this.results = val;
      },
    },
  },
  methods: {
    focusInput() {
      const ul = document.querySelector('ul');
      if (ul) {
        const ulCords = ul.getBoundingClientRect();
        // eslint-disable-next-line no-unused-expressions
        ulCords.top + ulCords.height > window.innerHeight && ul.classList.add('menu-top');
      }
    },
  },
};
</script>

<style lang="scss">
.menu-top{
  top: 0 !important;
  transform: translateY(-100%) !important;
}
</style>
