<template lang="pug">
  #app.app
    form.grid
      note(v-for="(item, index) in calendar", :index="index", :key="item.id", :id="item.id", :title="item.title")
</template>

<script>
import Note from '@/components/Note'
export default {
  name: 'app',
  components: {
    Note
  },
  data () {
    return {
      calendar: [
        {
          id: 'monday',
          title: 'Monday'
        },
        {
          id: 'tuesday',
          title: 'Tuesday'
        },
        {
          id: 'wednesday',
          title: 'Wednesday'
        },
        {
          id: 'thursday',
          title: 'Thursday'
        },
        {
          id: 'friday',
          title: 'Friday'
        },
        {
          id: 'weekend',
          title: 'Weekend'
        },
        {
          id: 'this_month',
          title: 'This Month'
        },
        {
          id: 'next_month',
          title: 'Next Month'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.app {
  display: flex;
  width: 100%;
  height: 100%;
}

.grid {
  padding: 1rem;
  display: grid;
  grid-template-columns: repeat(6, minmax(300px, 1fr));
  grid-template-rows: 66% auto;
  grid-gap: 0.75rem;
  flex-basis: 100%;
}
</style>
