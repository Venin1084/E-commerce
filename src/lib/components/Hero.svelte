<script>
// @ts-nocheck
   import SectionWrapper from "./SectionWrapper.svelte";
    import CTAs from "./CTAs.svelte";
</script>


<section class="bg-gray-100">
<SectionWrapper>
    <div class="lg:gap-15 flex flex-1 items-center justify-center p-2 md:pb-14 lg:px-67">
        <div class=" max-w-xl">
            <h1 class="lg:text-3xl text-2xl font-bold mb-4">Comfortable Sofa with Great Comfort</h1>
            <p class="mb-6">There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injected humour.</p>
            <CTAs/>
        </div>
        <div class="flex justify-center">
            <picture>
            <img class="w-full" src="/images/heroImg.png" alt="sedia">
            </picture>
        </div>
    </div>
</SectionWrapper>
</section>