<script>
    import { data } from './faqs.js';

    let open = false;
</script>

<div class="flex justify-center items-center">
    <div class="flex flex-col justify-center items-center w-10/12">
        <div class="mt-20">
            <h1 class="font-bold text-5xl text-center">FAQs</h1>
            <p class="p-10 text-base font-light text-center">We answered most of your frequently asked questions.</p>
        </div>

        {#each data as {heading, body}}
            <div class="faq mt-10 mb-10">
                <div class="question flex justify-between items-center">
                    <h3 class="text-[1.1rem]">{heading}</h3>

                    <button class="accordion" on:click={() => open = !open} class:active={open}>
                        <ion-icon name="chevron-down-outline"></ion-icon>
                    </button>
                </div>

                <div class="answer" class:open-answer={open}>
                    <p class="pt-10 leading-[1.6] text-[1rem] font-thin">
                        {body}
                    </p>
                </div>
            </div>
        {/each}
    </div>
</div>

<style>
    .faq {
        max-width: 700px;
    }

    div.answer {
        overflow: auto;
        height: 0;
        transition: all .5s;
    }

    div.open-answer {
        height: 100px;
    }
</style>