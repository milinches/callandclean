<script>
    let open = false
</script>

<div class="flex justify-center items-center">
    <div class="flex flex-col justify-center items-center w-10/12">
        <div class="mt-20">
            <h1 class="font-bold text-5xl text-center">FAQs</h1>
            <p class="p-10 text-base font-light">We answered most of your frequently asked questions.</p>
        </div>

        <div class="faq mt-20">
            <div class="question flex justify-between items-center">
                <h3 class="text-[1.3rem]">Who are we?</h3>

                <button on:click={() => open = !open} class:active={open}>
                    <ion-icon name="chevron-down-outline" ></ion-icon>
                </button>
            </div>

            <div class="answer">
                <p class="pt-10 leading-[1.6] text-[1rem] font-thin">
                    We are a a full time dry cleaning and house cleaning service, that brings the convenience of room services across Africa.
                </p>
                
            </div>
        </div>
    </div>
</div>

<style>
    .faq {
        max-width: 700px;
    }

    .answer {
        max-height: 0;
        overflow: hidden;
    }

    .faq:active .answer {
        max-height: 300px;
    }

    /* .answer {
        transition: linear 1.4s ease;
    } */
</style>