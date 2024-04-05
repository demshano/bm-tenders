<script>
    // Define props to receive data from the parent component
    export let tender;

    // Destructure the tender object to extract its properties
    const { image, category, publishedDate, closeDate, link } = tender;
</script>

<div>
    <div>
        <img src={image} alt="tender-ss" />
    </div>

    <div class="flex">
        <p>Category:</p>
        <p>{category}</p>
    </div>

    <div class="flex">
        <p>Published Date:</p>
        <p>{publishedDate}</p>
    </div>

    <div class="flex">
        <p>Closing Date:</p>
        <p>{closeDate}</p>
    </div>

    <div class="flex">
        <p>Tender Link:</p>
        <a href={link} target="_blank">See details of the tender</a>
    </div>
</div>
