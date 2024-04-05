<script>
    // Define props to receive data from the parent component
    export let tender;

    // Destructure the tender object to extract its properties
    const { image, category, publishedDate, closeDate, link } = tender;
</script>

<div class=" mt-8 flex-row justify-center items-center gap-8 md:flex">
    <div class="shadow-xl">
        <img class="w-[600px]" src={image} alt="tender-ss" />
    </div>

    <div class="shadow-xl p-4">
        <div class="flex gap-4">
            <p class="font-bold">Category:</p>
            <p>{category}</p>
        </div>

        <div class="flex gap-4">
            <p class="font-bold">Published Date:</p>
            <p>{publishedDate}</p>
        </div>

        <div class="flex gap-4">
            <p class="font-bold">Closing Date:</p>
            <p>{closeDate}</p>
        </div>

        <div class="flex gap-4">
            <p class="font-bold">Tender Link:</p>
            <a class="text-blue-400 underline" href={link} target="_blank"
                >See details of the tender</a
            >
        </div>
    </div>
</div>
