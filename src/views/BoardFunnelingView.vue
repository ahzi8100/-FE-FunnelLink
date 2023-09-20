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

</script>

<template>
  <LayoutAuthenticated>
    <SectionMain>
      <SectionTitleLineWithButton :icon="mdiDeveloperBoard" title="Board Funneling" main>
        <BaseButton href="#" :icon="mdiPlus" label="Create Funneling" color="info" rounded-full small />
      </SectionTitleLineWithButton>
      <div class="grid grid-cols-1 gap-6 lg:grid-cols-3 mb-6">
        <CardBoxBoards title="Madu Alami" color="text-emerald-500" :icon="mdiStore" :numberInbox="512" :numberSales="223"
          labelInbox="Inbox" labelSales="Sales" />
        <CardBoxBoards title="Baju Muslim" color="text-emerald-500" :icon="mdiStore" :numberInbox="534" :numberSales="123"
            labelInbox="Inbox" labelSales="Sales" />
        <CardBoxBoards title="Let's Grow" color="text-emerald-500" :icon="mdiStore" :numberInbox="534" :numberSales="123"
            labelInbox="Inbox" labelSales="Sales" />
      </div>
    </SectionMain>
  </LayoutAuthenticated>
</template>
