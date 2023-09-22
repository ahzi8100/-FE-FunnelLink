<script setup>
import {
  mdiCog,
} from "@mdi/js";
import PillTag from '@/components/PillTag.vue'
import BaseButton from '@/components/BaseButton.vue'
import CardBoxListItemFunneling from '@/components/funneling/CardBoxListItemFunneling.vue';
// import Draggable from 'vuedraggable'

const listFunnel = [
  {
    id: '1',
    board_id: '1',
    label: '5',
    title: 'Inbox',
    color: 'info'
  },
  {
    id: '2',
    board_id: '1',
    label: '2',
    title: 'Cold',
    color: 'contras'
  },
  {
    id: '3',
    board_id: '1',
    label: '3',
    title: 'Warm',
    color: 'warning'
  },
  {
    id: '4',
    board_id: '1',
    label: '',
    title: 'Hot',
    color: 'danger'
  },
  {
    id: '5',
    board_id: '1',
    label: '',
    title: 'Sales',
    color: 'success'
  }
]


</script>

<template>
  <div v-for="list in listFunnel" :key="list.id">
    <div class="bg-gray-100 p-4 my-3 rounded-xl w-72">
      <div class="flex items-center justify-between p-3 bg-white rounded-xl shadow-md mb-3">
        <div class="flex items-center">
          <PillTag :color="list.color" :label="list.label" small />
          <h3 class="text-lg font-medium ml-2">{{ list.title }}</h3>
        </div>
        <BaseButton :icon="mdiCog" icon-w="w-4" icon-h="h-4" color="lightDark" small />
      </div>
      <ul class="space-y-2">
        <CardBoxListItemFunneling :id_card_list="list.id" />
      </ul>

      <!-- <Draggable v-model="listFunnel" group="card" item-key="id" class="space-y-2" tag="">
        <template #item="{ element }">
          <CardBoxListItemFunneling :id_card_list="list.id" :card="element"/>
        </template>
      </Draggable> -->
    </div>
  </div>
</template>
