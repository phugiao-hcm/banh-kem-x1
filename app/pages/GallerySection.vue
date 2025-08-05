<template>
    <section class="py-16 bg-white">
        <div class="max-w-7xl mx-auto px-4">
            <!-- Tiêu đề -->
            <div class="text-center mb-12">
                <h2 class="text-3xl md:text-4xl font-bold text-red-500">
                    Kem Bánh
                </h2>
                <div class="mt-2 w-16 h-1 bg-red-500 mx-auto"></div>
            </div>

            <!-- Danh sách sản phẩm -->
            <div
                class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-8"
            >
                <div
                    v-for="(item, index) in products"
                    :key="index"
                    class="text-center space-y-2"
                >
                    <!-- Ảnh sản phẩm -->
                    <img
                        :src="item.image"
                        :alt="item.title"
                        class="w-full rounded-md shadow-md"
                    />

                    <!-- Thể loại -->
                    <p class="text-sm text-gray-500">Kem Bánh</p>

                    <!-- Tiêu đề -->
                    <h3 class="text-base font-semibold text-pink-600">
                        {{ item.title }}
                    </h3>

                    <!-- Tags -->
                    <div class="flex justify-center flex-wrap gap-2">
                        <span
                            v-for="(tag, tagIndex) in item.tags"
                            :key="tagIndex"
                            class="bg-blue-500 text-white text-xs font-semibold px-3 py-1 rounded-full flex items-center gap-1"
                        >
                            <svg
                                class="w-3 h-3"
                                fill="currentColor"
                                viewBox="0 0 20 20"
                            >
                                <path
                                    fill-rule="evenodd"
                                    d="M10 18a8 8 0 100-16 8 8 0 000 16zm-.75-9.25a.75.75 0 011.5 0v2.5a.75.75 0 01-1.5 0v-2.5zm.75 5a.75.75 0 100-1.5.75.75 0 000 1.5z"
                                    clip-rule="evenodd"
                                />
                            </svg>
                            {{ tag }}
                        </span>
                    </div>

                    <!-- Rating -->
                    <div class="text-yellow-400 text-sm">
                        <span v-for="i in 5" :key="i">
                            <i
                                class="fas"
                                :class="
                                    i <= item.rating
                                        ? 'fa-star'
                                        : 'fa-star-half-alt text-gray-300'
                                "
                            ></i>
                        </span>
                    </div>

                    <!-- Giá -->
                    <div class="text-black font-bold text-sm">
                        {{ item.price }}₫
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup>
const products = [
    {
        title: "Kem Chocolate Sundae Bánh",
        image: "images/kem_star_1.png",
        tags: ["Kem lạnh", "Trà"],
        rating: 5,
        price: "25.000",
    },
    {
        title: "Sữa Kem Lắc Dâu Tây Bánh",
        image: "images/kem_star_2.png",
        tags: [],
        rating: 5,
        price: "25.000",
    },
    {
        title: "Super Sundae Trân Châu Đường Đen Bánh",
        image: "images/kem_star_3.png",
        tags: [],
        rating: 2,
        price: "25.000",
    },
    {
        title: "Hồng Trà Kem Bánh",
        image: "images/kem_star_4.png",
        tags: [],
        rating: 2,
        price: "25.000",
    },
    {
        title: "Super Sundae Socola Bánh",
        image: "images/kem_star_5.png",
        tags: [],
        rating: 1,
        price: "25.000",
    },
    {
        title: "Super Sundae Socola Bánh",
        image: "images/kem_star_6.png",
        tags: [],
        rating: 1,
        price: "25.000",
    },
];
</script>

<style scoped>
/* FontAwesome cho rating icon nếu bạn dùng CDN hoặc plugin */
@import url("https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css");
</style>
