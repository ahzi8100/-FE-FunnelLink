<script setup>
import {
  mdiDeveloperBoard,
  mdiPlus,
  mdiStore,
} from "@mdi/js";
// import { Popover, PopoverButton, PopoverPanel, PopoverOverlay } from '@headlessui/vue'
import SectionMain from "@/components/SectionMain.vue";
import CardBoxBoards from "@/components/CardBoxBoards.vue";
import LayoutAuthenticated from "@/layouts/LayoutAuthenticated.vue";
import SectionTitleLineWithButton from "@/components/SectionTitleLineWithButton.vue";
import BaseButton from "@/components/BaseButton.vue";

const dataBoards = [
  {
    id: 1,
    title: "Let's Grow",
    numberInbox: 342,
    numberSales: 432,
  },
    {
    id: 2,
    title: "Toko Baju Muslim",
    numberInbox: 122,
    numberSales: 1232,
  },
    {
    id: 3,
    title: "Toko Makmur",
    numberInbox: 3542,
    numberSales: 1232,
  },
    {
    id: 4,
    title: "Jual Laptop",
    numberInbox: 242,
    numberSales: 132,
  },
    {
    id: 5,
    title: "Naswa Store",
    numberInbox: 522,
    numberSales: 432,
  },
    {
    id: 6,
    title: "Mie Ayam Enak",
    numberInbox: 222,
    numberSales: 1242,
  },
]

</script>

<template>
  <LayoutAuthenticated>
    <SectionMain>
      <SectionTitleLineWithButton :icon="mdiDeveloperBoard" title="Board Funneling" main>
        <BaseButton href="#" @click="$router.push({ name: 'Create Funneling'})" :icon="mdiPlus" label="Create Funneling" color="info" rounded-full small />
      </SectionTitleLineWithButton>
      <div class="grid grid-cols-1 gap-6 lg:grid-cols-3 sm:grid-cols-2 mb-6">
          <CardBoxBoards v-for="data in dataBoards" :key="data.id"  :title=data.title color="text-emerald-500" :icon="mdiStore" :numberInbox="data.numberInbox" :numberSales="data.numberSales"
            labelInbox="Inbox" labelSales="Sales" class="cursor-pointer" @click="$router.push({ name: 'Show Funneling', params: { id: data.id } })" />
      </div>
    </SectionMain>
  </LayoutAuthenticated>
</template>
