<template>
    <header class="bg-white shadow-sm sticky top-0 z-50">
        <div
            class="container mx-auto flex items-center justify-between py-4 px-4 md:px-6 relative"
        >
            <!-- Logo center -->
            <div class="absolute left-4 md:hidden">
                <button @click="toggleMenu" class="text-2xl text-gray-600">
                    <i class="fas fa-bars"></i>
                </button>
            </div>

            <div class="flex items-center justify-center mx-auto">
                <img
                    src="/images/kem_star_1.png"
                    alt="BÁNH Logo"
                    class="h-10 w-auto mr-2"
                />
                <span class="text-red-500 font-bold text-2xl"
                    >Bánh Kem Phú Giáo</span
                >
            </div>

            <!-- Desktop: spacer -->
            <div class="hidden md:block w-1/4"></div>
        </div>

        <!-- Desktop nav -->
        <nav class="hidden md:block border-t border-gray-100">
            <ul
                class="flex justify-center space-x-6 py-2 text-sm font-medium text-gray-700"
            >
                <li>
                    <a href="#" class="text-pink-600 hover:text-red-600"
                        >TRANG CHỦ</a
                    >
                </li>
                <li><a href="#" class="hover:text-red-600">MENU BÁNH</a></li>
                <li><a href="#" class="hover:text-red-600">KEM BÁNH</a></li>
                <li><a href="#" class="hover:text-red-600">TRÀ SỮA BÁNH</a></li>
                <li><a href="#" class="hover:text-red-600">BÁNH GẦN ĐÂY</a></li>
                <li>
                    <a href="#" class="hover:text-red-600">BÁNH TUYỂN DỤNG</a>
                </li>
                <li>
                    <a href="#" class="hover:text-red-600">NHƯỢNG QUYỀN BÁNH</a>
                </li>
                <li><a href="#" class="hover:text-red-600">LIÊN HỆ</a></li>
            </ul>
        </nav>

        <!-- Mobile nav -->
        <transition name="fade">
            <nav
                v-if="isOpen"
                class="md:hidden border-t border-gray-100 bg-white px-6 py-4"
            >
                <ul
                    class="flex flex-col space-y-3 text-sm font-medium text-gray-700"
                >
                    <li>
                        <a href="#" class="text-pink-600 hover:text-red-600"
                            >TRANG CHỦ</a
                        >
                    </li>
                    <li>
                        <a href="#" class="hover:text-red-600">MENU BÁNH</a>
                    </li>
                    <li><a href="#" class="hover:text-red-600">KEM BÁNH</a></li>
                    <li>
                        <a href="#" class="hover:text-red-600">TRÀ SỮA BÁNH</a>
                    </li>
                    <li>
                        <a href="#" class="hover:text-red-600">BÁNH GẦN ĐÂY</a>
                    </li>
                    <li>
                        <a href="#" class="hover:text-red-600"
                            >BÁNH TUYỂN DỤNG</a
                        >
                    </li>
                    <li>
                        <a href="#" class="hover:text-red-600"
                            >NHƯỢNG QUYỀN BÁNH</a
                        >
                    </li>
                    <li><a href="#" class="hover:text-red-600">LIÊN HỆ</a></li>
                </ul>
            </nav>
        </transition>
    </header>
</template>

<script setup>
import { ref } from "vue";

const isOpen = ref(false);
const toggleMenu = () => {
    isOpen.value = !isOpen.value;
};
</script>

<style scoped>
.fade-enter-active,
.fade-leave-active {
    transition: all 0.3s ease;
}
.fade-enter-from,
.fade-leave-to {
    opacity: 0;
    transform: translateY(-10px);
}
</style>

<!-- Font Awesome CDN (nếu chưa có) -->
<!-- Thêm vào file nuxt.config.ts hoặc layout nếu dùng Nuxt -->
<!--
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css">
-->
