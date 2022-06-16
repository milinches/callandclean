<div class="flex justify-center items-center bg-slate-50">
    <div class="flex justify-between md:mt-15 mt-20 mb-20 items-center w-10/12">
        <div class="heading">
            <div class="images">
                <img src="/assets/images/eclipse.png" alt="cirle" width="30" class="ecp">
                <img src="/assets/images/polygon.png" alt="polygon" class="poly" width="30">
                <img src="/assets/images/rectangle.png" alt="rectangle" class="rect" width="30">
            </div>
            <h1 class="h__one md:text-6xl md:font-extrabold text-center md:text-left text-5xl font-extrabold pb-4 tracking-normal text-[#03A84E] leading-10">
                Say goodbye
                <br>
                <span class="leading-4">
                    to house cleaning
                </span>
                <br>
                forever!
            </h1>

            <p class="md:text-xl text-base pt-7 font-medium md:text-justify text-center text-[#21312a]">Wash and dry your clothes at affordable prices.</p>
            
            <ul class="mx-0 my-[30px] text-[1rem] md:list-disc text-center md:text-justify md:pl-5">
                <li class="py-2">Laundry picked up and delivered. ✔️</li>
                <li>Home cleaning: executed by professional cleaners. ✔️</li>
            </ul>

            <p class="md:text-xl text-base pt-2 font-medium md:text-justify text-center text-[#21312a]">Schedule them, and never worry about them again. Ever.</p>

            <div class="flex justify-center items-center md:block">
                <button class="mt-10 text-base text-white rounded py-5 px-4 bg-[#03A84E] w-[100%] md:w-[40%]">
                    <a href="/services">Book an appointment</a>
                </button>
            </div>
        </div>
        <div class="circle__div">
            <img src="/assets/images/homepages.png" alt="mockup" width="500" class="md:block hidden">
        </div>
    </div>
</div>

<style>
    .images {
        position: relative;
    }

    .images .ecp {
        position: absolute;
        opacity: 0.3;
        top: -40px;
        left: 30%;
        transform: translate(-50%, -50%);
    }

    .images .poly {
        position: absolute;
        opacity: 0.3;
        top: 10%;
        left: 90%;
        transform: translate(-50%, -50%);
        transform: rotate(45deg);
    }
    .images .rect {
        position: absolute;
        opacity: 0.3;
        top: 200px;
        left: 10%;
        transform: translate(-50%, -50%);
        transform: rotate(20deg);
    }
    
    .h__one {
        line-height: 4rem;
    }
</style>