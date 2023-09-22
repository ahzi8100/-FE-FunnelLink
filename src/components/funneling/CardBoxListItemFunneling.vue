<script setup>
import UserAvatarCurrentUser from "@/components/UserAvatarCurrentUser.vue";

const props = defineProps({
  id_card_list: {
    type: [String, Number],
  },
});

const listFunnel = ([
  {
    id: 1,
    id_card_list: 1,
    name: 'Ahzi',
    date: 'Today at 13:32',
    text: 'Min, saya mau beli nasi goreng pake telor.',
  },
  {
    id: 2,
    id_card_list: 1,
    name: 'Ipul',
    date: 'Today at 13:12',
    text: 'Min, saya mau beli nasi goreng gk pake telor.',
  },
  {
    id: 3,
    id_card_list: 1,
    name: 'Cipul',
    date: 'Today at 13:42',
    text: 'Min, saya mau beli mie goreng pake telor.',
  },
  {
    id: 4,
    id_card_list: 1,
    name: 'Jipul',
    date: 'Today at 13:32',
    text: 'Min, saya mau beli nasi goreng pake telor.',
  },
  {
    id: 5,
    id_card_list: 1,
    name: 'Puput',
    date: 'Today at 13:12',
    text: 'Min, saya mau beli nasi goreng gk pake telor.',
  },
  {
    id: 6,
    id_card_list: 2,
    name: 'Ciprut',
    date: 'Today at 13:42',
    text: 'Min, saya mau beli mie goreng pake telor.',
  },
    {
    id: 7,
    id_card_list: 2,
    name: 'Cuprit',
    date: 'Today at 13:42',
    text: 'Min, saya mau beli mie goreng pake telor.',
  },
  {
    id: 8,
    id_card_list: 3,
    name: 'Hilu',
    date: 'Today at 13:32',
    text: 'Min, saya mau beli nasi goreng pake telor.',
  },
  {
    id: 9,
    id_card_list: 3,
    name: 'Hulu',
    date: 'Today at 13:12',
    text: 'Min, saya mau beli nasi goreng gk pake telor.',
  },
  {
    id: 10,
    id_card_list: 3,
    name: 'Hilir',
    date: 'Today at 13:42',
    text: 'Min, saya mau beli mie goreng pake telor.',
  },
])



</script>

<template>
  <li v-for="card in listFunnel" :key="card.id">
    <div v-if="card.id_card_list == props.id_card_list" class="flex flex-col p-3 bg-white rounded-xl shadow-sm">
      <div class="flex mb-2">
        <UserAvatarCurrentUser class="w-8" />
        <div class="flex flex-col ml-3">
          <p class="text-sm font-medium">{{ card.name }}</p>
          <p class="text-xs">{{ card.date }}</p>
        </div>
      </div>
      <p class="text-xs rounded-md border-2 p-1">{{ card.text }}</p>
    </div>
  </li>
</template>
