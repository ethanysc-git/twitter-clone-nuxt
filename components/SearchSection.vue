<template>
    <div class="border-x" :class="twitterBorderColor">
        <div class="sticky top-0 px-4 py-3 bg-white/80 backdrop-blur-md dark:bg-dim-900/80">
            <h2 class="text-xl font-bold text-gray-800 dark:text-gray-100">{{ props.title }}</h2>
        </div>
    </div>
</template>
<script setup>
const data = reactive({
    cities: [],
    searchQuery: "",
    filteredCities: [],
    noDataMessage: false,
});

function requestData() {
    fetch(
        "https://gist.githubusercontent.com/Miserlou/c5cd8364bf9b2420bb29/raw/2bf258763cdddd704f8ffd3ea9a3e81d25e2c6f6/cities.json"
    )
        .then((r) => r.json())
        .then((val) => data.cities.push(...val));
}

function checkQuery() {
    if (data.searchQuery.trim() === "") {
        data.filteredCities = [];
        var noDataMessage = false;
    } else {
    }
}

</script>