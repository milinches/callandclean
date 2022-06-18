<script>
    let items = ['Wash and Fold', 'Dry Cleaning'];
    let activeItem = 'Wash and Fold';
</script>

<div class="flex justify-center items-center bg-slate-50">
    <div class="flex justify-center md:mt-15 mt-20 mb-10 items-center w-10/12">
        <div class="justify-center items-center flex flex-col">
            <h1 class="h__one md:text-6xl md:font-extrabold text-center text-5xl font-extrabold pb-4 tracking-normal text-[#03A84E] leading-10">
                Here are
                <span class="leading-4">
                    some of our
                </span>
                <br>
                services we offer.
            </h1>

            <p class="text-center p-10">
                From everyday laundry to professional dry cleaning, we have a service that will meet your needs. <br> Save 3-4 hours a week and let the experts handle it!
            </p>

            <ul class="flex justify-center">
                {#each items as item}
                    <li class:active={item === activeItem} class="px-5 py-3">
                        {item}
                    </li>
                {/each}
            </ul>
        </div>
    </div>
</div>

<style>
    .h__one {
        line-height: 4rem;
    }

    .active {
        color: #d91b42;
        border-bottom: 2px solid #d91b42;
    }
</style>