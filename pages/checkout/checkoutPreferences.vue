<!-- <template>
  <teleport to="body">
    <div
      v-if="isVisible"
      class="fixed inset-0 bg-black bg-opacity-70 flex items-center justify-center z-50"
    >
      <div class="w-[816px] h-[684px] border rounded-lg bg-white"></div>
    </div>
  </teleport>
</template>

<script></script>

<style lang="scss" scoped></style> -->
<template>
  <div
    class="w-[816px] h-[684px] bg-white p-6 rounded-lg shadow-lg max-w-md mx-auto"
  >
    <div class="flex justify-between items-center mb-4">
      <img
        src="/assets/images/Foods/food3.png"
        alt="Poke Bowl"
        class="w-16 h-16 rounded-lg"
      />
      <div class="flex flex-col">
        <h2 class="text-2xl font-bold">Build Your Own Poke Bowl</h2>
        <p class="text-sm text-gray-600 mb-4">
          Extra proteins for an additional charge.
        </p>
      </div>
    </div>

    <form>
      <fieldset class="mb-4">
        <legend class="font-semibold mb-2">Choose a Base</legend>
        <label class="block mb-2">
          <input type="radio" name="base" value="white_rice" class="mr-2" />
          White Rice
        </label>
        <label class="block mb-2">
          <input type="radio" name="base" value="brown_rice" class="mr-2" />
          Brown Rice
        </label>
        <label class="block mb-2">
          <input type="radio" name="base" value="salad" class="mr-2" />
          Salad
        </label>
        <label class="block mb-2">
          <input
            type="radio"
            name="base"
            value="half_white_brown"
            class="mr-2"
          />
          Half and Half (White Rice and Brown Rice)
        </label>
        <label class="block mb-2">
          <input
            type="radio"
            name="base"
            value="half_white_salad"
            class="mr-2"
          />
          Half and Half (White Rice and Salad)
        </label>
        <label class="block mb-2">
          <input
            type="radio"
            name="base"
            value="half_noodles_salad"
            class="mr-2"
          />
          Half and Half (Noodles and Salad)
        </label>
      </fieldset>

      <div class="flex items-center mb-4">
        <button
          type="button"
          class="bg-gray-200 text-gray-700 px-2 py-1 rounded-l"
        >
          -
        </button>
        <input
          type="number"
          value="1"
          class="w-12 text-center border-t border-b border-gray-200"
        />
        <button
          type="button"
          class="bg-gray-200 text-gray-700 px-2 py-1 rounded-r"
        >
          +
        </button>
      </div>

      <button
        type="submit"
        class="w-full bg-green-500 hover:bg-green-700 text-white font-bold py-2 px-4 rounded"
      >
        Add to cart $20
      </button>
    </form>
  </div>
</template>

<script setup>
// Define your component logic here
</script>

<style scoped>
/* Add custom styles or override Tailwind styles here */
</style>
