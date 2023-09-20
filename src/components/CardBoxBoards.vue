<script setup>
import { mdiCog } from "@mdi/js";
import CardBox from "@/components/CardBox.vue";
import NumberDynamic from "@/components/NumberDynamic.vue";
import BaseIcon from "@/components/BaseIcon.vue";
import BaseLevel from "@/components/BaseLevel.vue";
import BaseButton from "@/components/BaseButton.vue";
import { stringify } from "postcss";

defineProps({
  title: {
    type: stringify,
    default: null,
  },
  numberInbox: {
    type: Number,
    default: 0,
  },
  numberSales: {
    type: Number,
    default: 0,
  },
  icon: {
    type: String,
    default: null,
  },
  prefix: {
    type: String,
    default: null,
  },
  suffix: {
    type: String,
    default: null,
  },
  labelInbox: {
    type: String,
    default: null,
  },
    labelSales: {
    type: String,
    default: null,
  },
  color: {
    type: String,
    default: null,
  },
  trend: {
    type: String,
    default: null,
  },
  trendType: {
    type: String,
    default: null,
  },
});
</script>

<template>
  <CardBox>
    <BaseLevel class="mb-3" mobile>
      <p class="text-2xl">{{ title }}</p>
      <BaseButton :icon="mdiCog" icon-w="w-4" icon-h="h-4" color="lightDark" small />
    </BaseLevel>
    <BaseLevel mobile>
      <div class="inline-flex gap-x-8">
        <div>
          <h3 class="text-lg leading-tight text-gray-500 dark:text-slate-400">
            {{ labelInbox }}
          </h3>
          <h1 class="text-xl leading-tight font-semibold">
            <NumberDynamic :value="numberInbox" :prefix="prefix" :suffix="suffix" />
          </h1>
        </div>
          <div>
            <h3 class="text-lg leading-tight text-gray-500 dark:text-slate-400">
              {{ labelSales }}
            </h3>
            <h1 class="text-xl leading-tight font-semibold">
              <NumberDynamic :value="numberSales" :prefix="prefix" :suffix="suffix" />
            </h1>
          </div>
      </div>
      <BaseIcon v-if="icon" :path="icon" size="48" w="" h="h-16" :class="color" />
    </BaseLevel>
  </CardBox>
</template>
