<script>
    import TenderCard from "./TenderCard.svelte";
    import ss1 from "../../assets/ss1.png";
    const tenderDetails = [
        {
            image: ss1,
            category: "Contingent workforce",
            publishedDate: "2-Apr-2024",
            closeDate: "6-May-2024 2:00pm",
            link: "https://www.tenders.nsw.gov.au/?dept=health&event=public.rft.show&RFTUUID=25695F21-0A8E-ABB0-0D24439CBE13D313",
        },
    ];
</script>

<div class="mt-36">
    {#each tenderDetails as tender}
        <!-- Render TenderCard component for each tender -->
        <TenderCard {tender} />
    {/each}
</div>
