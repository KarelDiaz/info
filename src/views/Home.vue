<template>
  <div class="flex flex-col h-screen overflow-auto space-y-7">
    <personal-component class="sticky top-0 z-10 sm:sticky" :info="info" />
    <div class="flex flex-col w-full p-3 m-auto space-y-10 sm:w-2/3">
      <history-component
        class="pl-3"
        v-for="history in info.histories"
        :key="history.name"
        :history="history"
      />
    </div>
  </div>
</template>

<script>
import data from '../../data';

import HistoryComponent from '../components/HistoryComponent.vue';
import PersonalComponent from '../components/PersonalComponent.vue';

export default {
  components: {
    HistoryComponent,
    PersonalComponent,
  },
  data() {
    return {
      info: data,
    };
  },
};
</script>
