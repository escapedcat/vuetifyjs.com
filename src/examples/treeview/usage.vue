<template>
  <v-treeview
    :items="items"
    :open="open"
  ></v-treeview>
</template>

<script>
  export default {
    data: () => ({
      items: [
        {
          id: 1,
          name: 'Parent 1',
          children: [
            {
              id: 2,
              name: 'Child 1',
              children: [
                {
                  id: 3,
                  name: 'Grandchild 1'
                },
                {
                  id: 4,
                  name: 'Grandchild 2'
                }
              ]
            },
            {
              id: 5,
              name: 'Child 2'
            }
          ]
        },
        {
          id: 6,
          name: 'Parent 2',
          children: [
            {
              id: 7,
              name: 'Child 3'
            }
          ]
        }
      ],
      open: [1, 2]
    })
  }
</script>
