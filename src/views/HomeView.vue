<script setup>
import { ref } from 'vue';
import axios from 'axios';
import { Icon } from '@iconify/vue';

const activity = ref('');


const fetchActivity = async () => {
    try {
    const response = await axios.get('https://www.boredapi.com/api/activity');
    activity.value = response.data.activity
    console.log(response);
  } catch (error) {
    console.error(error);
  }
}

</script>

<template>
    <div>
        <h1>Tired of feeling bored. </h1>
        <p>Click on the button below to get an activity you can do.</p>
        <button @click="fetchActivity"> Get Activity</button>
        <Icon icon="system-uicons:arrow-down" />
        <h2> {{ activity }}</h2>
    </div>
</template>



<style lang="scss" scoped>

  div{
    display: flex;
    flex-direction: column;
    margin-block-start: 6rem;
    align-items: center;
    gap: 2rem;

    h1{
      text-transform: uppercase;
      letter-spacing: 0.5rem;
    }
  }
</style>