<script>
    import Tabs from "./Tabs.svelte";

    let items = ['Wash and Fold', 'Dry Cleaning'];
    let activeItem = 'Wash and Fold';
    const tabChange = (e) => {
        activeItem = e.detail;
    }
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

            <Tabs {activeItem} {items} on:tabChange={tabChange} />
            {#if activeItem === 'Wash and Fold'}
                <div class="flex flex-col justify-center items-center md:mt-20 mt-10 w-[93%]">
                    <div class="flex justify-between items-center">
                        <div class="md:text-left text-center">
                            <h1 class="text-3xl font-bold py-4">{activeItem}</h1>
                            <div class="md:w-3/4 w-auto mt-3">
                                <p>This is the ideal service for your everyday laundry needs.</p>
                                <p class="pt-5">Save 3+ hours every week by having us pick up your clothes right from your door and return them freshly clean and perfectly folded.</p>
                            </div>
                        </div>
    
                        <video width="500" height="240" autoplay muted class="md:block hidden rounded-md">
                            <source src="/assets/videos/callandclean.webm">
                            Your browser does not support this video tag.
                        </video>
                    </div>

                    <div class="flex flex-col md:flex-row justify-around items-center w-[99%] mt-20 md:gap-9 gap-0">
                        <div class="flex flex-col justify-center items-center md:w-[25%] w-auto text-center mb-14">
                            <img src="/assets/icons/services/Search.svg" alt="Trust" width="50">
                            <h1 class="text-lg font-bold p-3">Detailed Inspection</h1>
                            <p class="text-base leading-6">Your pockets and clothes are inspected (so nothing ends up in the wash that shouldn't) before being placed in their own machine.</p>
                        </div>
                        <div class="flex flex-col justify-center items-center md:w-[25%] w-auto text-center mb-14">
                            <img src="/assets/icons/services/Sparkling.svg" alt="Trust" width="50">
                            <h1 class="text-lg font-bold p-3">Premium cleaning</h1>
                            <p class="text-base leading-6">Your lights and darks are separated and all your clothes are washed using cold water to preserve color (and save energy).</p>
                        </div>
                        <div class="flex flex-col justify-center items-center md:w-[25%] w-auto text-center mb-14">
                            <img src="/assets/icons/services/Content.svg" alt="Trust" width="50">
                            <h1 class="text-lg font-bold p-3">Your preferences</h1>
                            <p class="text-base leading-6">Need hypoallergenic detergent? 
                                No problem — just select the laundry preferences that are right for you.</p>
                        </div>
                        <div class="flex flex-col justify-center items-center md:w-[25%] w-auto text-center mb-14">
                            <img src="/assets/icons/services/Clothes.svg" alt="Trust" width="50">
                            <h1 class="text-lg font-bold p-3">Neatly folded</h1>
                            <p class="text-base leading-6">Your clothes are crisply folded and your socks are paired, ready to be put away upon delivery, anytime, anywhere.</p>
                        </div>
                    </div>
                </div>
            {:else if activeItem === 'Dry Cleaning'}
            <div class="flex flex-col justify-center items-center md:mt-20 mt-10 w-[93%]">
                <div class="flex justify-between items-center">
                    <div class="md:text-left text-center">
                        <h1 class="text-3xl font-bold py-4">{activeItem}</h1>
                        <div class="md:w-3/4 w-auto mt-3">
                            <p>This is the perfect service for items you want professionally cleaned and returned pressed and on a hanger (this service includes both Dry Cleaning and Launder & Press).</p>
                            <p class="pt-5">Enjoy premium cleaning from the comfort of your home and never go to the dry cleaners again.</p>
                        </div>
                    </div>

                    <video width="500" height="240" autoplay muted class="md:block hidden rounded-md">
                        <source src="/assets/videos/dry-cleaning.webm">
                        Your browser does not support this video tag.
                    </video>
                </div>

                <div class="flex flex-col md:flex-row justify-around items-center w-[99%] mt-20 md:gap-9 gap-0">
                    <div class="flex flex-col justify-center items-center md:w-[25%] w-auto text-center mb-14">
                        <img src="/assets/icons/services/Search.svg" alt="Trust" width="50">
                        <h1 class="text-lg font-bold p-3">Detailed Inspection</h1>
                        <p class="text-base leading-6">Your pockets and clothes are inspected (so nothing ends up in the wash that shouldn't) before being placed in their own machine.</p>
                    </div>
                    <div class="flex flex-col justify-center items-center md:w-[25%] w-auto text-center mb-14">
                        <img src="/assets/icons/services/Sparkling.svg" alt="Trust" width="50">
                        <h1 class="text-lg font-bold p-3">Premium cleaning</h1>
                        <p class="text-base leading-6">Your lights and darks are separated and all your clothes are washed using cold water to preserve color (and save energy).</p>
                    </div>
                    <div class="flex flex-col justify-center items-center md:w-[25%] w-auto text-center mb-14">
                        <img src="/assets/icons/services/Content.svg" alt="Trust" width="50">
                        <h1 class="text-lg font-bold p-3">Your preferences</h1>
                        <p class="text-base leading-6">Need hypoallergenic detergent? 
                            No problem — just select the laundry preferences that are right for you.</p>
                    </div>
                    <div class="flex flex-col justify-center items-center md:w-[25%] w-auto text-center mb-14">
                        <img src="/assets/icons/services/Clothes.svg" alt="Trust" width="50">
                        <h1 class="text-lg font-bold p-3">Neatly folded</h1>
                        <p class="text-base leading-6">Your clothes are crisply folded and your socks are paired, ready to be put away upon delivery, anytime, anywhere.</p>
                    </div>
                </div>
            </div>
            {/if}

        </div>
    </div>
</div>

<style>
    .h__one {
        line-height: 4rem;
    }
</style>