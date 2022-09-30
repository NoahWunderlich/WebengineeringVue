
<template>
      <div>
        <h1>TEST</h1>
        <TimeTable/>
      </div>
</template>
    
    <script>
        import TimeTable from '@/components/TimeTable.vue'

    // @ is an alias to /src    
    export default {
      name: 'TimeTableView',
      components: {
        TimeTable
      }
    }
    </script>
    