<script setup>
import {
  mdiStore,
} from "@mdi/js";
import LayoutAuthenticated from "@/layouts/LayoutAuthenticated.vue";
import SectionMain from "@/components/SectionMain.vue";
import SectionTitleLineWithButton from "@/components/SectionTitleLineWithButton.vue";
import CardBoxListFunneling from '@/components/funneling/CardBoxListFunneling.vue';
// import CardBoxListItemFunneling from "@/components/funneling/CardBoxListItemFunneling.vue";

const dataBoards =
{
  id: 1,
  title: "Let's Grow",
  numberInbox: 342,
  numberSales: 432,
}

</script>

<template>
  <LayoutAuthenticated>
    <SectionMain>
      <SectionTitleLineWithButton :icon="mdiStore" :title="dataBoards.title" main />
      <div class="flex flex-col h-screen">
        <main class="flex-1 overflow-hidden">
          <div class="flex flex-col h-full">
            <div class="flex-1 overflow-x-auto">
              <div class="inline-flex h-full items-start px-4 pb-4 space-x-4">
                  <CardBoxListFunneling />
              </div>
            </div>
          </div>
        </main>
      </div>
    </SectionMain>
  </LayoutAuthenticated>
</template>
