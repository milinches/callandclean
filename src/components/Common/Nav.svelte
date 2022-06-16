<script>
	const navItems = [
		{ name: 'Why Us?', link: '/whyus' },
		{ name: 'Services', link: '/services' },
		{ name: 'Pricing', link: '/' },
		{ name: 'Contact Us?', link: '/' }
	];

    let open = false
</script>

<div class="px-6 shadow-lg md:flex justify-between items-center bg-white">
    <div class="flex justify-between items-center">
        <span class="ml-0 md:ml-20">
            <a href="/" class="p-2"><img src="/favicon.png" alt="call and clean logo" class="w-10"></a>
        </span>
    </div>

    <div on:click={() => open = !open} class='text-3xl absolute right-8 top-6 cursor-pointer md:hidden'>
        <ion-icon name={open ? 'close':'menu'}></ion-icon>
    </div>

    <ul 
        class="md:mr-20 mr-20 md:flex md:items-center md:px-0 px-5 md:pb-0 pb-10 md:static absolute bg-white md:w-auto w-full top-16 duration-700 ease-in {open ? 'left-0' : 'hidden'}"
        >
        {#each navItems as items}
            <li class="md:mx-4 md:my-0 my-6">
                <a href={items.link} class="text-black p-3 text-base">{items.name}</a>
            </li>
        {/each}

        <button class="navbar__btn text-white duration-500 px-6 py-2 mx-3 bg-[#03A84E] rounded">
            Get started
        </button>
    </ul>
</div>


<style>
    
    @media screen and (max-width: 517px) {
        .navbar__btn {
            width: 100%;
        }
    } 
</style>
