<script>
    const navItems = [
        {name: "Why Us?", link: "/"},
        {name: "Services", link: "/services"},
        {name: "Companies", link: "/"},
        {name: "Pricing", link: "/"},
        {name: "Contact Us?", link: "/"},
    ]
    
    let open = false

    const menuOpen = () => {
        open = !open
    }
</script>

<nav class="py-3.5 px-6 md:flex justify-between items-center bg-white w-10/12">
    <div class="flex items-center cursor-pointer">
        <span class="ml-0 md:ml-20">
            <a href="/"><img src="/assets/images/logo.png" alt="call and clean logo" class="w-40"></a>
        </span>
    </div>

    <span on:click="{menuOpen}" class="absolute md:hidden right-6 top-1.5 cursor-pointer text-4xl">
        <i class="{open ? 'bi bi-x' : 'bi bi-filter-left'}"></i>
    </span>

    <ul class="md:mr-20 mr-20 md:flex md:items-center md:px-0 px-10 md:pb-0 pb-10 md:static absolute bg-white md:w-auto w-full top-14 duration-700 ease-in">
        {#each navItems as items}
            <li class="md:mx-4 md:my-0 my-6">
                <a href={items.link} class="text-black">{items.name}</a>
            </li>
        {/each}
    </ul>
</nav>

