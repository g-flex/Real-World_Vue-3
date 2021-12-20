<template>
  <h1>Events for Good</h1>
  <div class="events">
    <img alt="Vue logo" src="../assets/logo.png" />
    <event-card v-for="event in events" :key="event.id" :event="event" />
  </div>
</template>

<script>
// @ is an alias to /src
import EventCard from "@/components/EventCard.vue";

export default {
  name: "Home",
  components: {
    EventCard
  },
  data() {
    return {
      events: [
        {
          id: 5928101,
          category: 'Dating',
          title: 'Lets do it together',
          description: 'Bring here your tinder date',
          location: 'Milano San Siro',
          date: 'Jan 28, 2022',
          time: '12:00',
          petsAllowed: true,
          organizer: "Tony P",
        },
        {
          id: 5928104,
          category: 'Smoking',
          title: 'Puff puff together',
          description: 'Only hashish allowed',
          location: 'Terps Army BCN',
          date: 'Jan 31, 2022',
          time: '18:00',
          petsAllowed: false,
          organizer: "Arjan S H",
        },
        {
          id: 5928115,
          category: 'Swimming',
          title: 'Pool lesson',
          description: 'Learn how to swim',
          location: 'Milano piscina cozzi',
          date: 'Feb 6, 2022',
          time: '15:00',
          petsAllowed: false,
          organizer: "Federica Pellegrini",
        },
        {
          id: 5928120,
          category: 'Cinema',
          title: 'Matrix new film',
          description: 'Just released in every iMax theatre',
          location: 'UCI Milano Bicocca',
          date: '31 Dec, 2022',
          time: '21:00',
          petsAllowed: false,
          organizer: "Keanu Reeves",
        },
      ]
    }
  }
};
</script>

<style scoped>

  .events {
    display: flex;
    flex-direction: column;
    align-items: center;
  }

</style>