<script setup>
import CreateIcon from './icons/CreateIcon.vue';
import FriendIcon from './icons/FriendIcon.vue';
import HomepageIcon from './icons/HomepageIcon.vue';
import MenuIcon from './icons/MenuIcon.vue';
import SearchIcon from './icons/SearchIcon.vue';


</script>

<template>

    <div class="drawer lg:drawer-open">
    <input id="my-drawer-4" type="checkbox" class="drawer-toggle" />
    <div class="drawer-content">
        <!-- Navbar -->
        <nav class="navbar w-full bg-base-100 shadow-xs">
             <div class="navbar-start">
                <label for="my-drawer-4" aria-label="open sidebar" class="btn btn-square btn-ghost">
            <!-- Sidebar toggle icon -->
                    <MenuIcon/>
                </label>
                <div class="px-2 font-bold text-xl">AIBoyFriends</div>
             </div>   
             <div class="navbar-center w-4/5 max-w-180 flex justify-center">
                <div class="join w-4/5 flex justify-center">
                    <input class="input join-item rounded-l-full w-4/5" placeholder="搜索你感兴趣的内容" />
                    <button class="btn join-item rounded-r-full gap-0">
                        <SearchIcon/>
                        搜索</button>
                    </div>
             </div>
             <div class="navbar-end">
                <button class="btn btn-ghost text-lg">登录</button>
             </div>
       
        </nav>
        <!-- Page content here -->
        <slot></slot>
    </div>

 

    <div class="drawer-side is-drawer-close:overflow-visible">
        <label for="my-drawer-4" aria-label="close sidebar" class="drawer-overlay"></label>
        <div class="flex min-h-full flex-col items-start bg-base-200 is-drawer-close:w-16 is-drawer-open:w-64">
        <!-- Sidebar content here -->
        <ul class="menu w-full grow">
            <!-- List item -->
            <li>
            <button class="is-drawer-close:tooltip is-drawer-close:tooltip-right" data-tip="首页">
                <!-- Home icon -->
                <HomepageIcon/>
                <span class="is-drawer-close:hidden text-base ml-2 py-3 whitesapce-nowrap">首页</span>
            </button>
            </li>

            <!-- List item -->
           <li>
            <button class="is-drawer-close:tooltip is-drawer-close:tooltip-right " data-tip="好友">
                <!-- Home icon -->
                <FriendIcon/>
                <span class="is-drawer-close:hidden text-base ml-2 py-3 whitesapce-nowrap">好友</span>
            </button>
            </li>

              <!-- List item -->
           <li>
            <button class="is-drawer-close:tooltip is-drawer-close:tooltip-right" data-tip="创作">
                <!-- Home icon -->
                <CreateIcon/>
                <span class="is-drawer-close:hidden text-base ml-2 py-3 whitesapce-nowrap">创作</span>
            </button>
            </li>

        </ul>
        </div>
    </div>
    </div>
</template>

<style scoped>
</style>
