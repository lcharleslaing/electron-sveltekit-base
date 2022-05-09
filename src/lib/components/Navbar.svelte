<script>
    const main_menu = [
        { title: "Home", path: "/" },
        { title: "About", path: "/" },
        { title: "Contact", path: "/" },
        { title: "Support US", path: "/" },
    ];

    const notification_menu = [
        { title: "Messages", path: "/" },
        { title: "User", path: "/" },
    ];

    const app_menu = [
        { title: "App 1", path: "/" },
        { title: "App 2", path: "/" },
    ];

    const dev_menu = [{ title: "Cusip", path: "/cusip" }];

    const user_menu = [
        { title: "Profile", path: "/" },
        { title: "Login", path: "/" },
        { title: "Register", path: "/" },
        { title: "Logout", path: "/" },
    ];
    export let showOverlay = true;
    export let hideMainMenu = true;
    export let hideNotificationMenu = true;
    export let hideAppsMenu = true;
    export let hideDevMenu = true;
    export let hideUsersMenu = true;

    const toggleOverlay = () => {
        showOverlay = !showOverlay;
    };

    const toggleMain = () => {
        toggleOverlay();
        hideMainMenu = !hideMainMenu;
        hideNotificationMenu = true;
        hideAppsMenu = true;
        hideDevMenu = true;
        hideUsersMenu = true;
    };

    const toggleNotification = () => {
        toggleOverlay();
        hideNotificationMenu = !hideNotificationMenu;
        hideMainMenu = true;
        hideAppsMenu = true;
        hideDevMenu = true;
        hideUsersMenu = true;
    };

    const toggleApps = () => {
        toggleOverlay();
        hideAppsMenu = !hideAppsMenu;
        hideMainMenu = true;
        hideNotificationMenu = true;
        hideDevMenu = true;
        hideUsersMenu = true;
    };

    const toggleDev = () => {
        toggleOverlay();
        hideDevMenu = !hideDevMenu;
        hideMainMenu = true;
        hideNotificationMenu = true;
        hideAppsMenu = true;
        hideUsersMenu = true;
    };

    const toggleUsers = () => {
        toggleOverlay();
        hideUsersMenu = !hideUsersMenu;
        hideMainMenu = true;
        hideNotificationMenu = true;
        hideAppsMenu = true;
        hideDevMenu = true;
    };
    const closeAllDrawer = () => {
        toggleOverlay();
        hideMainMenu = true;
        hideNotificationMenu = true;
        hideAppsMenu = true;
        hideDevMenu = true;
        hideUsersMenu = true;
    };
</script>

<div class="navbar bg-base-100">
    <div class="flex-none">
        <button on:click={toggleMain} class="btn btn-square btn-ghost">
            <img width="20px" src="/feather/menu.svg" alt="" />
        </button>
    </div>
    <div class="flex-1">
        <a href="/" class="btn btn-ghost normal-case text-xl">
            <img width="35px" src="/icons/icon-72x72.png" alt="Logo" />
        </a>
    </div>
    <div class="flex-none" />
    <div class="flex-none">
        <button on:click={toggleNotification} class="btn btn-square btn-ghost">
            <img width="20px" src="/feather/bell.svg" alt="" />
        </button>
    </div>
    <div class="flex-none">
        <button on:click={toggleApps} class="btn btn-square btn-ghost">
            <img width="20px" src="/feather/grid.svg" alt="" />
        </button>
    </div>
    <div class="flex-none">
        <button on:click={toggleDev} class="btn btn-square btn-ghost">
            <img width="20px" src="/feather/code.svg" alt="" />
        </button>
    </div>
    <div class="flex-none">
        <button on:click={toggleUsers} class="btn btn-square btn-ghost">
            <img width="20px" src="/feather/users.svg" alt="" />
        </button>
    </div>
</div>

<!-- Overlay -->
<div
    on:click={closeAllDrawer}
    class:hidden={showOverlay}
    class="fixed w-screen h-screen bg-neutral opacity-70"
/>

<!-- Main Menu Drawer -->
<div
    class:hidden={hideMainMenu}
    class="bg-neutral text-white sidebar w-60 absolute min-h-screen transition-transform duration-100 ease-in-out"
>
    <ul class="text-lg py-4">
        {#each main_menu as link}
            <li
                class="hovering mx-4 text-lg hover:bg-slate-700 rounded-md px-2"
            >
                <a href={link.path} class="">{link.title}</a>
            </li>
        {/each}
    </ul>
</div>

<!-- Notification Drawer -->
<div
    class:hidden={hideNotificationMenu}
    class="bg-blue-700 text-white sidebar w-60 absolute min-h-screen transition-transform duration-100 ease-in-out"
>
    <ul class="text-lg py-4">
        {#each notification_menu as link}
            <li class="hovering mx-4 text-lg hover:bg-blue-600 rounded-md px-2">
                <a href={link.path} class="">{link.title}</a>
            </li>
        {/each}
    </ul>
</div>

<!-- Apps Drawer -->
<div
    class:hidden={hideAppsMenu}
    class="bg-green-700 text-white sidebar w-60 absolute min-h-screen transition-transform duration-100 ease-in-out"
>
    <ul class="text-lg py-4">
        {#each app_menu as link}
            <li
                class="hovering mx-4 text-lg hover:bg-green-600 rounded-md px-2"
            >
                <a href={link.path} class="">{link.title}</a>
            </li>
        {/each}
    </ul>
</div>

<!-- Dev Drawer -->
<div
    class:hidden={hideDevMenu}
    class="bg-teal-700 text-white sidebar w-60 absolute min-h-screen transition-transform duration-100 ease-in-out"
>
    <ul class="text-lg py-4">
        {#each dev_menu as link}
            <li class="hovering mx-4 text-lg hover:bg-teal-600 rounded-md px-2">
                <a href={link.path} class="">{link.title}</a>
            </li>
        {/each}
    </ul>
</div>

<!-- Users Drawer -->
<div
    class:hidden={hideUsersMenu}
    class="bg-orange-700 text-white sidebar w-60 absolute min-h-screen transition-transform duration-100 ease-in-out float-right"
>
    <ul class="text-lg py-4">
        {#each user_menu as link}
            <li
                class="hovering mx-4 text-lg hover:bg-orange-600 rounded-md px-2"
            >
                <a href={link.path} class="">{link.title}</a>
            </li>
        {/each}
    </ul>
</div>

<style>
</style>
