<script setup lang="ts">
import { ref, reactive } from "vue";
// defineProps<{
//   msg: string;
// }>();
interface Faqs {
  id: number;
  question: string;
  answer: string;
  show: boolean;
}
let faqs: Faqs[] = reactive([
  {
    id: 1,
    question: "What is frontend mentor, and how will it help you",
    answer:
      "Frontend mentors offers realistic coding challenges to help developers to improve their frontend coding skills with projects in HTML, CSS and Javascript. It's suitable for all levels and ideal for portfolio building",
    show: false,
  },
  {
    id: 2,
    question: "Can i use frontend mentor's project in my portfolio",
    answer:
      "Frontend mentors offers realistic coding challenges to help developers to improve their frontend coding skills with projects in HTML, CSS and Javascript. It's suitable for all levels and ideal for portfolio building",
    show: false,
  },
  {
    id: 3,
    question: "How can i get help if i am stucked in a challenge",
    answer:
      " Frontend mentors offers realistic coding challenges to help developers to improve their frontend coding skills with projects in HTML, CSS and Javascript. It's suitable for all levels and ideal for portfolio building",

    show: false,
  },
  // { id: 4, question: "", answer: "" },
]);
</script>

<template>
  <div class="bg-white rounded-lg h-full md:w-[500px]">
    <div class="py-7 px-6">
      <div class="flex space-x-4">
        <div>
          <img src="/icon-star.svg" alt="star-icon" />
        </div>
        <h1 class="text-4xl text-dark-purple font-bold">FAQs</h1>
      </div>
      <div class="border-b" v-for="faq in faqs" :key="faq.id">
        <div class="pt-5 pb-4">
          <div class="pt-2 flex justify-between items-center space-x-10">
            <h2
              class="text-lg md:text-sm text-dark-purple pb-4 hover:text-purple-500 hover:font-bold"
            >
              {{ faq.question }} ?
            </h2>
            <button
              @click="faq.show = !faq.show"
              class="focus:outline-none hover:opacity-50"
            >
              <img src="/icon-plus.svg" alt="plus icon" v-if="!faq.show" />
              <img src="/icon-minus.svg" alt="minus icon" v-else />
            </button>
          </div>
          <div v-if="faq.show == true" class="pb-4">
            <p class="text-lg md:text-xs text-grayish-purple">
              {{ faq.answer }}
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped></style>
