<template>
  <base-card>
    <base-button
      :mode="activeTab ? '' : 'nav'"
      @click="setSelectedTab('add-weight')"
      >Add Weight</base-button
    >
    <base-button
      :mode="activeTab ? 'nav' : ''"
      @click="setSelectedTab('weight-records')"
      >Weight Record</base-button
    >
    <component :is="selectedTab"></component>
  </base-card>
</template>

<script>
import WeightRecords from "./WeightRecords";
import AddWeight from "./AddWeight";
export default {
  computed: {
    activeTab() {
      if (this.selectedTab === "add-weight") {
        return true;
      } else {
        return false;
      }
    },
  },
  components: {
    WeightRecords,
    AddWeight,
  },
  provide() {
    return {
      weightData: this.weightData,
      addWeight: this.addWeight,
    };
  },
  data() {
    return {
      selectedTab: "add-weight",
      weightData: [],
    };
  },
  methods: {
    setSelectedTab(tab) {
      this.selectedTab = tab;
    },

    addWeight(record) {
      this.weightData.push(record);
      this.selectedTab = "weight-records";
    },
  },
};
</script>
