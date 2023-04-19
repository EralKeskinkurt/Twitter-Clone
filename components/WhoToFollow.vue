<template>
<div class="w-full h-auto px-5 mt-2">
    <div class="bg-useGray h-auto rounded-xl overflow-hidden">
        <h3 class="text-normalWhite px-2 py-3 font-bold">Who to follow</h3>
        <ul>
            <li v-for="follow in followProfile" :key="follow.id" class="flex p-3 gap-2 items-center justify-center cursor-pointer hover:bg-lowWhite transition duration-200">
                <div class="overflow-hidden">
                    <img :src="follow.p_image" class="w-10 h-10 object-cover rounded-full hover:brightness-90 transition duration-200" alt="profile image" />
                </div>
                <div class="flex flex-col flex-grow text-[13px]">
                    <span class="font-semibold text-normalWhite">{{ follow.p_name }}</span>
                    <span class="font-light text-lowsWhite">{{ follow.p_at }}</span>
                </div>
                <button class="bg-normalWhite px-3 py-1 rounded-l-2xl rounded-r-2xl text-[13px] font-semibold hover:brightness-90 transition duration-200">Follow</button>
            </li>
            <li class="text-sm text-useGreen p-2 py-4 hover:bg-lowWhite cursor-pointer">Show More</li>
        </ul>
    </div>
</div>
</template>

<script setup>
const followProfile = ref([
    {id:1, p_image:'/images/1.jpg', p_name:'Sigara Boregi', p_at:'@sigara_boregi'},
    {id:2, p_image:'/images/2.jpg', p_name:'Yogurtlu Biber', p_at:'@yogurtlu-biber'},
    {id:3, p_image:'/images/3.jpg', p_name:'Barbunya Pilaki', p_at:'@barbunya_pilaki'},
])

</script>

