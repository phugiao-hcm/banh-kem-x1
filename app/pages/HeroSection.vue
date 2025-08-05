<template>
    <section class="py-16 bg-white">
        <div
            class="max-w-7xl mx-auto grid grid-cols-1 md:grid-cols-2 gap-12 items-center px-6"
        >
            <!-- Left content -->
            <div class="space-y-6">
                <!-- Nhãn nhỏ -->
                <div>
                    <p class="text-pink-500 font-semibold">Bánh kem Phú Giáo</p>
                    <button
                        class="bg-blue-500 hover:bg-blue-600 text-white px-4 py-1.5 rounded-full inline-flex items-center text-sm font-semibold mt-2"
                    >
                        <svg
                            class="w-4 h-4 mr-1"
                            fill="currentColor"
                            viewBox="0 0 20 20"
                        >
                            <path
                                fill-rule="evenodd"
                                d="M10 18a8 8 0 100-16 8 8 0 000 16zm-.75-9.25a.75.75 0 011.5 0v2.5a.75.75 0 01-1.5 0v-2.5zm.75 5a.75.75 0 100-1.5.75.75 0 000 1.5z"
                                clip-rule="evenodd"
                            />
                        </svg>
                        Super Sundae Trân Châu Đường Đen
                    </button>
                </div>

                <!-- Tiêu đề -->
                <h1 class="text-5xl font-extrabold text-[#ff4e4e]">
                    Bánh kem Phú Giáo
                </h1>

                <!-- Mô tả -->
                <p class="text-gray-700 leading-relaxed">
                    Bánh kem Phú Giáo trang cập nhật thông tin về sản phẩm, kem,
                    <a href="#" class="underline">trà sữa</a> Bánh kem Phú Giáo,
                    quán Bánh kem Phú Giáo gần đây,
                    <span class="text-pink-500"
                        >Menu Bánh kem Phú Giáo, thông tin tuyển dụng Bánh kem
                        Phú Giáo, nhượng quyền Bánh kem Phú Giáo...</span
                    >
                    Bánh kem Phú Giáo có cửa hàng tại các khu vực của Phú Giáo
                    như Bánh kem Phước Hòa, Bánh kem Vĩnh Hòa,...
                </p>
            </div>

            <!-- Right content (Image + Nút) -->
            <div class="relative text-center">
                <img
                    src="/images/banh_kem_1.png"
                    alt="Bánh kem Phú Giáo Mascot"
                    class="w-full max-w-sm mx-auto"
                />
                <!-- Nút bên dưới hình -->
                <div class="mt-6">
                    <button
                        class="bg-blue-500 hover:bg-blue-600 text-white px-4 py-1.5 rounded-full inline-flex items-center text-sm font-semibold"
                    >
                        <svg
                            class="w-4 h-4 mr-1"
                            fill="currentColor"
                            viewBox="0 0 20 20"
                        >
                            <path
                                fill-rule="evenodd"
                                d="M10 18a8 8 0 100-16 8 8 0 000 16zm-.75-9.25a.75.75 0 011.5 0v2.5a.75.75 0 01-1.5 0v-2.5zm.75 5a.75.75 0 100-1.5.75.75 0 000 1.5z"
                                clip-rule="evenodd"
                            />
                        </svg>
                        Super Sundae Trân Châu Đường Đen
                    </button>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup>
// Không cần logic JS
</script>

<style scoped>
/* Tuỳ chọn: điều chỉnh kích thước hoặc spacing nếu cần */
</style>
