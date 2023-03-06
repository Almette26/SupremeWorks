<script setup>
import { Head, Link } from '@inertiajs/vue3';

defineProps({
    canLogin: Boolean,
    canRegister: Boolean,
    laravelVersion: String,
    phpVersion: String,
});
</script>

<template>
    <Head title="Welcome" />

    <div class="navbar sticky top-0 h-[52px] ">
        <button
            class="float-right mt-1 mr-1 inline-block rounded bg-primary px-4 py-4 pt-3 pb-3 text-xs font-medium uppercase leading-normal text-white shadow-[0_4px_9px_-4px_#3b71ca] transition duration-150 ease-in-out hover:bg-primary-600 hover:shadow-[0_8px_9px_-4px_rgba(59,113,202,0.3),0_4px_18px_0_rgba(59,113,202,0.2)] focus:bg-primary-600 focus:shadow-[0_8px_9px_-4px_rgba(59,113,202,0.3),0_4px_18px_0_rgba(59,113,202,0.2)] focus:outline-none focus:ring-0 active:bg-primary-700 active:shadow-[0_8px_9px_-4px_rgba(59,113,202,0.3),0_4px_18px_0_rgba(59,113,202,0.2)]"
            type="button"
            data-te-offcanvas-toggle
            data-te-target="#offcanvasTop"
            aria-controls="offcanvasTop"
            data-te-ripple-init
            data-te-ripple-color="light">
            <div class="space-y-2">
                <div class="w-6 h-0.5 bg-white"></div>
                <div class="w-6 h-0.5 bg-white"></div>
                <div class="w-6 h-0.5 bg-white"></div>
            </div>
        </button>
    </div>

    <div
        class="invisible fixed bottom-0 top-0 left-0 right-0 z-[1045] flex h-1/3 max-h-full max-w-full -translate-y-full flex-col border-none bg-white bg-clip-padding text-neutral-700 shadow-sm outline-none transition duration-300 ease-in-out dark:bg-neutral-800 dark:text-neutral-200 [&[data-te-offcanvas-show]]:transform-none"
        tabindex="-1"
        id="offcanvasTop"
        aria-labelledby="offcanvasTopLabel"
        data-te-offcanvas-init>
        <div class="flex items-center justify-between p-4">
            <h5 class="mb-0 font-semibold leading-normal" id="offcanvasTopLabel">
                Offcanvas top
            </h5>
            <button
                type="button"
                class="box-content rounded-none border-none opacity-50 hover:no-underline hover:opacity-75 focus:opacity-100 focus:shadow-none focus:outline-none"
                data-te-offcanvas-dismiss>
      <span
          class="w-[1em] focus:opacity-100 disabled:pointer-events-none disabled:select-none disabled:opacity-25 [&.disabled]:pointer-events-none [&.disabled]:select-none [&.disabled]:opacity-25">
        <svg
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            stroke-width="1.5"
            stroke="currentColor"
            class="h-6 w-6">
          <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M6 18L18 6M6 6l12 12" />
        </svg>
      </span>
            </button>
        </div>
        <div class="flex-grow overflow-y-auto p-4">...</div>
    </div>

    <div
        id="carouselExampleCaptions"
        class="relative"
        data-te-carousel-init
        data-te-carousel-slide>
        <div
            class="absolute right-0 bottom-0 left-0 z-[2] mx-[15%] mb-4 flex list-none justify-center p-0"
            data-te-carousel-indicators>
            <button
                type="button"
                data-te-target="#carouselExampleCaptions"
                data-te-slide-to="0"
                data-te-carousel-active
                class="mx-[3px] box-content h-[3px] w-[30px] flex-initial cursor-pointer border-0 border-y-[10px] border-solid border-transparent bg-white bg-clip-padding p-0 -indent-[999px] opacity-50 transition-opacity duration-[600ms] ease-[cubic-bezier(0.25,0.1,0.25,1.0)] motion-reduce:transition-none"
                aria-current="true"
                aria-label="Slide 1"></button>
            <button
                type="button"
                data-te-target="#carouselExampleCaptions"
                data-te-slide-to="1"
                class="mx-[3px] box-content h-[3px] w-[30px] flex-initial cursor-pointer border-0 border-y-[10px] border-solid border-transparent bg-white bg-clip-padding p-0 -indent-[999px] opacity-50 transition-opacity duration-[600ms] ease-[cubic-bezier(0.25,0.1,0.25,1.0)] motion-reduce:transition-none"
                aria-label="Slide 2"></button>
            <button
                type="button"
                data-te-target="#carouselExampleCaptions"
                data-te-slide-to="2"
                class="mx-[3px] box-content h-[3px] w-[30px] flex-initial cursor-pointer border-0 border-y-[10px] border-solid border-transparent bg-white bg-clip-padding p-0 -indent-[999px] opacity-50 transition-opacity duration-[600ms] ease-[cubic-bezier(0.25,0.1,0.25,1.0)] motion-reduce:transition-none"
                aria-label="Slide 3"></button>
        </div>
        <div
            class="relative w-full overflow-hidden after:clear-both after:block after:content-['']">
            <div
                class="relative float-left -mr-[100%] w-full transition-transform duration-[600ms] ease-in-out motion-reduce:transition-none"
                data-te-carousel-active
                data-te-carousel-item
                style="backface-visibility: hidden">
                <img
                    src="https://tecdn.b-cdn.net/img/Photos/Slides/img%20(15).jpg"
                    class="block w-full"
                    alt="..." />
                <div
                    class="absolute inset-x-[15%] bottom-5 hidden py-5 text-center text-white md:block">
                    <h5 class="text-xl">First slide label</h5>
                    <p>
                        Some representative placeholder content for the first slide.
                    </p>
                </div>
            </div>
            <div
                class="relative float-left -mr-[100%] hidden w-full transition-transform duration-[600ms] ease-in-out motion-reduce:transition-none"
                data-te-carousel-item
                style="backface-visibility: hidden">
                <img
                    src="https://tecdn.b-cdn.net/img/Photos/Slides/img%20(22).jpg"
                    class="block w-full"
                    alt="..." />
                <div
                    class="absolute inset-x-[15%] bottom-5 hidden py-5 text-center text-white md:block">
                    <h5 class="text-xl">Second slide label</h5>
                    <p>
                        Some representative placeholder content for the second slide.
                    </p>
                </div>
            </div>
            <div
                class="relative float-left -mr-[100%] hidden w-full transition-transform duration-[600ms] ease-in-out motion-reduce:transition-none"
                data-te-carousel-item
                style="backface-visibility: hidden">
                <img
                    src="https://tecdn.b-cdn.net/img/Photos/Slides/img%20(23).jpg"
                    class="block w-full"
                    alt="..." />
                <div
                    class="absolute inset-x-[15%] bottom-5 hidden py-5 text-center text-white md:block">
                    <h5 class="text-xl">Third slide label</h5>
                    <p>
                        Some representative placeholder content for the third slide.
                    </p>
                </div>
            </div>
        </div>
        <button
            class="absolute top-0 bottom-0 left-0 z-[1] flex w-[15%] items-center justify-center border-0 bg-none p-0 text-center text-white opacity-50 transition-opacity duration-150 ease-[cubic-bezier(0.25,0.1,0.25,1.0)] hover:text-white hover:no-underline hover:opacity-90 hover:outline-none focus:text-white focus:no-underline focus:opacity-90 focus:outline-none motion-reduce:transition-none"
            type="button"
            data-te-target="#carouselExampleCaptions"
            data-te-slide="prev">
    <span class="inline-block h-8 w-8">
      <svg
          xmlns="http://www.w3.org/2000/svg"
          fill="none"
          viewBox="0 0 24 24"
          stroke-width="1.5"
          stroke="currentColor"
          class="h-6 w-6">
        <path
            stroke-linecap="round"
            stroke-linejoin="round"
            d="M15.75 19.5L8.25 12l7.5-7.5" />
      </svg>
    </span>
            <span
                class="!absolute !-m-px !h-px !w-px !overflow-hidden !whitespace-nowrap !border-0 !p-0 ![clip:rect(0,0,0,0)]"
            >Previous</span
            >
        </button>
        <button
            class="absolute top-0 bottom-0 right-0 z-[1] flex w-[15%] items-center justify-center border-0 bg-none p-0 text-center text-white opacity-50 transition-opacity duration-150 ease-[cubic-bezier(0.25,0.1,0.25,1.0)] hover:text-white hover:no-underline hover:opacity-90 hover:outline-none focus:text-white focus:no-underline focus:opacity-90 focus:outline-none motion-reduce:transition-none"
            type="button"
            data-te-target="#carouselExampleCaptions"
            data-te-slide="next">
    <span class="inline-block h-8 w-8">
      <svg
          xmlns="http://www.w3.org/2000/svg"
          fill="none"
          viewBox="0 0 24 24"
          stroke-width="1.5"
          stroke="currentColor"
          class="h-6 w-6">
        <path
            stroke-linecap="round"
            stroke-linejoin="round"
            d="M8.25 4.5l7.5 7.5-7.5 7.5" />
      </svg>
    </span>
            <span
                class="!absolute !-m-px !h-px !w-px !overflow-hidden !whitespace-nowrap !border-0 !p-0 ![clip:rect(0,0,0,0)]"
            >Next</span
            >
        </button>
    </div>

</template>

<style>
.bg-dots-darker {
    background-image: url("data:image/svg+xml,%3Csvg width='30' height='30' viewBox='0 0 30 30' fill='none' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M1.22676 0C1.91374 0 2.45351 0.539773 2.45351 1.22676C2.45351 1.91374 1.91374 2.45351 1.22676 2.45351C0.539773 2.45351 0 1.91374 0 1.22676C0 0.539773 0.539773 0 1.22676 0Z' fill='rgba(0,0,0,0.07)'/%3E%3C/svg%3E");
}
@media (prefers-color-scheme: dark) {
    .dark\:bg-dots-lighter {
        background-image: url("data:image/svg+xml,%3Csvg width='30' height='30' viewBox='0 0 30 30' fill='none' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M1.22676 0C1.91374 0 2.45351 0.539773 2.45351 1.22676C2.45351 1.91374 1.91374 2.45351 1.22676 2.45351C0.539773 2.45351 0 1.91374 0 1.22676C0 0.539773 0.539773 0 1.22676 0Z' fill='rgba(255,255,255,0.07)'/%3E%3C/svg%3E");
    }
}
</style>
