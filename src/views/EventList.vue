<template>
  <h1>Events For Good</h1>
  <div class="events">
    <EventCard
      v-for="event in events"
      :key="event.id"
      :event="event"
    ></EventCard>
  </div>
</template>

<script>
// @ is an alias to /src
import EventCard from "@/components/EventCard.vue";

export default {
  name: "EventList",
  components: {
    EventCard,
  },
  data() {
    return {
      events: [
        {
          id: 5928101,
          category: "animal welfare",
          title: "Cat Adoption Day",
          description: "Find your new feline friend at this event.",
          location: "Meow Town",
          date: "January 28,2022",
          time: "12:00",
          petsAllowed: true,
          organiser: "Kat Laydee",
        },
        {
          id: 4582797,
          category: "food",
          title: "Community Gardening",
          description: "Join us as we tend to community edible plants.",
          location: "Flora City",
          date: "March 14,2022",
          time: "10:00",
          petsAllowed: true,
          organiser: "Fern Pollin",
        },
        {
          id: 8419988,
          category: "sustainability",
          title: "Beach Cleanup",
          description: "Help pick up trash along the shore.",
          location: "Playa del Carmen",
          date: "July 22,2022",
          time: "11:00",
          petsAllowed: false,
          organiser: "Carey Wales",
        },
      ],
    };
  },
};
</script>
<style scoped>
.events {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
