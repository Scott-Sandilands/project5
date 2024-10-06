<script setup>
import { faker } from '@faker-js/faker'
const adjective = faker.word.adjective();
const flowerType = faker.helpers.arrayElement(['lily', 'rose', 'tulip', 'daisy', 'violet', 'orchid']);
const flowerName = `${adjective} ${flowerType}`;
const bio = faker.lorem.lines(2);
const color = faker.color.human();
const imageUrl = faker.image.urlLoremFlickr({ category: 'flowers' });
const height = faker.number.float({ min: 10, max: 100, precision: 0.1 });
const habitat = faker.address.country();
</script>

<template>
    <!-- {{ fullname }} <br /> -->
    <div class="border border-gray-400 rounded-lg shadow bg-gray-200 h-full">
        <img :src="imageUrl" class="rounded-t-xl w-full h-auto aspect-[3/4] object-cover" />
        <div class="p-4 bg-yellow-200 rounded-lg">
            <p class="mb-2 text-2xl font-bold">Flower Name: {{ flowerName }}</p>
            <p class="mb-3 font-normal text-gray-700">Color: {{ color }}</p>
            <p class="mb-3 font-normal text-gray-700">Desc: {{ bio }}</p>
            <p class="mb-3 font-normal text-gray-700">Size: {{ height }}</p>
            <p class="mb-3 font-normal text-gray-700">Region: {{ habitat }}</p>
        </div>
    </div>
</template>