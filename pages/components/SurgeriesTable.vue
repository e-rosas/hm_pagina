<template>
  <div>
    <b-table responsive head-variant="light" hover :items="services"></b-table>
  </div>
</template>

<script>
export default {
  name: 'SurgeriesTable',
  data() {
    return {
      services: [
        {
          procedure: 'Tonsil Surgery',
          hospital_méxico: '$1,700 dlls.',
          USA: '$5,500 dlls.'
        },
        {
          procedure: 'Appendix Surgery',
          hospital_méxico: '$2,300 dlls.',
          USA: '$10,000 dlls.'
        },
        {
          procedure: 'Gallbladder Surgery',
          hospital_méxico: '$4,300 dlls.',
          USA: '$16,000 dlls.'
        },
        {
          procedure: 'Kidney Stone Surgery',
          hospital_méxico: '$3,100 dlls.',
          USA: '$12,000 dlls.'
        }
      ]
    }
  }
}
</script>
