<template>
    <section class="py-10 bg-pink-50">
        <div class="max-w-6xl mx-auto px-4">
            <h2
                class="text-2xl md:text-3xl font-bold text-pink-600 text-center mb-8"
            >
                Bộ sưu tập bánh nổi bật 🎉
            </h2>

            <div class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 gap-6">
                <div
                    v-for="lipstick in lipsticks"
                    :key="lipstick.id"
                    class="bg-white rounded-lg shadow hover:shadow-lg transition overflow-hidden"
                >
                    <img
                        :src="lipstick.image"
                        :alt="lipstick.name"
                        class="w-full h-48 object-cover"
                    />
                    <div class="p-3 text-center">
                        <h3
                            class="text-sm font-semibold text-gray-800 line-clamp-2"
                        >
                            {{ lipstick.name }}
                        </h3>
                        <p class="text-pink-600 font-bold mt-2">
                            {{ lipstick.price }}
                        </p>
                        <button
                            class="mt-3 text-sm w-full border border-pink-500 text-pink-500 py-1 rounded hover:bg-pink-100 transition"
                        >
                            Mua ngay
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup>
const lipsticks = [
    {
        id: 1,
        name: "Bánh 3CE Mood Recipe – #114 Rows",
        price: "289.000₫",
        image: "images/banh_kem_1.png",
    },
    {
        id: 2,
        name: "Son Kem Black Rouge Air Fit",
        price: "199.000₫",
        image: "images/banh_kem_2.png",
    },
    {
        id: 3,
        name: "Bánh MAC Ruby Woo – Red Icon",
        price: "579.000₫",
        image: "images/banh_kem_3.png",
    },
    {
        id: 4,
        name: "Bánh Dior",
        price: "849.000₫",
        image: "images/banh_kem_4.png",
    },
];
</script>

<style scoped>
.line-clamp-2 {
    display: -webkit-box;
    -webkit-line-clamp: 2;
    -webkit-box-orient: vertical;
    overflow: hidden;
}
</style>
