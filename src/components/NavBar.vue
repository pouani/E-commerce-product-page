<template lang="">
    <nav class="nav flex justify-between border-b">
        <div class="flex items-center gap-16">
            <ul class="list-none p-0 flex gap-6 items-center">
                <li class="nav-button md:hidden py-6 cursor-pointer">
                    <img src="@/assets/images/icon-menu.svg" alt="">
                </li>
                <li class="cursor-pointer py-6">
                    <img src="@/assets/images/logo.svg" alt="">
                </li>
            </ul>
            <ul class="list-none md:flex gap-8 md:pt-1 nav_links hidden">
                <li class="nav_links-item cursor-pointer py-6">Collections</li>
                <li class="nav_links-item cursor-pointer py-6">Men</li>
                <li class="nav_links-item cursor-pointer py-6">Women</li>
                <li class="nav_links-item cursor-pointer py-6">About</li>
                <li class="nav_links-item cursor-pointer py-6">Contact</li>
            </ul>
        </div>
        <ul class="flex items-center gap-6 list-none">
            <li><i class="fa-solid fa-cart-shopping"></i></li>
            <li class="w-8 h-8 overflow-hidden border-2 border-gray-400 rounded-full">
                <img src="@/assets/images/image-avatar.png" class="object-cover w-full h-full" alt="avatar">
            </li>
        </ul>
    </nav>
</template>
<script>
export default {
    
}
</script>
<style lang="">
    
</style>