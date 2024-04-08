<script>
    import TenderCard from "./TenderCard.svelte";
    import Pagination from './Pagination.svelte';
    import ss1 from "../../assets/ss1.png";
    const tenderDetails = [
        {
            image: ss1,
            category: "Contingent workforce",
            publishedDate: "2-Apr-2024",
            closeDate: "6-May-2024 2:00pm",
            link: "https://www.tenders.nsw.gov.au/?dept=health&event=public.rft.show&RFTUUID=25695F21-0A8E-ABB0-0D24439CBE13D313",
        },
        {
            image: ss1,
            category: "Contingent workforce",
            publishedDate: "2-Apr-2024",
            closeDate: "6-May-2024 2:00pm",
            link: "https://www.tenders.nsw.gov.au/?dept=health&event=public.rft.show&RFTUUID=25695F21-0A8E-ABB0-0D24439CBE13D313",
        },
        {
            image: ss1,
            category: "Contingent workforce",
            publishedDate: "2-Apr-2024",
            closeDate: "6-May-2024 2:00pm",
            link: "https://www.tenders.nsw.gov.au/?dept=health&event=public.rft.show&RFTUUID=25695F21-0A8E-ABB0-0D24439CBE13D313",
        },
        {
            image: ss1,
            category: "Contingent workforce",
            publishedDate: "2-Apr-2024",
            closeDate: "6-May-2024 2:00pm",
            link: "https://www.tenders.nsw.gov.au/?dept=health&event=public.rft.show&RFTUUID=25695F21-0A8E-ABB0-0D24439CBE13D313",
        },
        {
            image: ss1,
            category: "Contingent workforce",
            publishedDate: "2-Apr-2024",
            closeDate: "6-May-2024 2:00pm",
            link: "https://www.tenders.nsw.gov.au/?dept=health&event=public.rft.show&RFTUUID=25695F21-0A8E-ABB0-0D24439CBE13D313",
        },
        {
            image: ss1,
            category: "Contingent workforce",
            publishedDate: "2-Apr-2024",
            closeDate: "6-May-2024 2:00pm",
            link: "https://www.tenders.nsw.gov.au/?dept=health&event=public.rft.show&RFTUUID=25695F21-0A8E-ABB0-0D24439CBE13D313",
        },
        {
            image: ss1,
            category: "Contingent workforce",
            publishedDate: "2-Apr-2024",
            closeDate: "6-May-2024 2:00pm",
            link: "https://www.tenders.nsw.gov.au/?dept=health&event=public.rft.show&RFTUUID=25695F21-0A8E-ABB0-0D24439CBE13D313",
        },
        {
            image: ss1,
            category: "Contingent workforce",
            publishedDate: "2-Apr-2024",
            closeDate: "6-May-2024 2:00pm",
            link: "https://www.tenders.nsw.gov.au/?dept=health&event=public.rft.show&RFTUUID=25695F21-0A8E-ABB0-0D24439CBE13D313",
        }
    ];

    let values;
</script>


{#if values}
    {#each values as tender}
        <div class="my-4">
            <!-- <img src={example.image} alt="Tender Image" class="w-32 h-32 mr-4 float-left"> -->
            <!-- <div>
                <p>Category: {example.category}</p>
                <p>Published Date: {example.publishedDate}</p>
                <p>Closing Date: {example.closeDate}</p>
                <a href={example.link} class="text-blue-500">Link</a>
            </div> -->

            <TenderCard {tender}/>
        </div>
    {/each}
{/if}

<Pagination rows={tenderDetails} perPage={3} bind:trimmedRows={values} />

<style>

</style>