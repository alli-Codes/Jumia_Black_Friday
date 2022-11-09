<template>
    <div
        class="bg-white w-full h-full flex flex-col items-stretch cursor-pointer rounded hover:shadow-lg hover:scale-105">
        <div class="product-container h-72 w-full rounded">
            <img :src="image" alt="" class=" w-full object-cover rounded-t">
        </div>

        <div class="description  p-2 text-sm flex flex-col items-start rounded">
            <p class="w-full truncate">{{description}}</p>
            <p class="font-bold">{{ price }}</p>
            <p class="text-gray-400 text-xs line-through">{{ formerPrice }}</p>
            <div class="progressBar w-full mt-2 flex flex-col items-start text-xs" v-show="progressVisibility">
                <p>14 items left</p>
                <progress value="3" max="10" class="h-2 w-full"></progress>
            </div>
        </div>
    </div>
</template>

<script>

export default {
    props: {
        description: String,
        price: String,
        formerPrice: String,
        progressVisibility: Boolean,
        image: String
    }
}
</script>

<style scoped>
progress {
    border: 0;
    /* height: 40px; */
    border-radius: 20px;
}

progress::-webkit-progress-bar {
    background-color: #c7c7cd;
    border: 0;
    /* height: 40px; */
    border-radius: 20px;
}

progress::-webkit-progress-value {
    background-color: #f6b01e;
    border: 0;
    /* height: 40px; */
    border-radius: 20px;
}

progress::-moz-progress-bar {
    background-color: #c7c7cd;
    border: 0;
    /* height: 40px; */
    border-radius: 20px;
}
</style>