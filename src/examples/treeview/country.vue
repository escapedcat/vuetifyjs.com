<template>
  <v-card>
    <v-layout
      align-center
      pa-3
    >
      <v-treeview
        v-model="tree"
        :items="items"
        class="grow"
        item-key="name"
        expand-icon="mdi-chevron-down"
        open-on-click
        selectable
        transition
      ></v-treeview>
      <v-divider vertical class="mx-5"></v-divider>
      <v-flex xs6 ml-auto>
        <v-combobox
          :value="tree"
          box
          chips
          hide-details
          label="Places you want to go"
          multiple
          readonly
        ></v-combobox>
      </v-flex>
    </v-layout>
  </v-card>
</template>

<script>
  export default {
    data: () => ({
      items: [
        {
          name: 'Asia',
          children: [
            { name: 'China' },
            { name: 'Japan' },
            { name: 'Mongolia' }
          ]
        },
        {
          name: 'North America',
          children: [
            {
              name: 'USA',
              children: [
                { name: 'California' },
                { name: 'Florida' }
              ]
            },
            { name: 'Canada' },
            { name: 'Mexico' }
          ]
        },
        {
          name: 'South America',
          children: [
            { name: 'Brazil' },
            { name: 'Argentina' },
            { name: 'Colombia' }
          ]
        },
        {
          name: 'Europe',
          children: [
            { name: 'England' },
            { name: 'Germany' },
            { name: 'Bulgaria' },
            { name: 'Poland' }
          ]
        }
      ],
      tree: []
    })
  }
</script>
