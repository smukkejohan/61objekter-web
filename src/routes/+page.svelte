<script lang="ts">
    import InstagramIcon from 'virtual:icons/mdi/instagram'
    import SiteIcon from 'virtual:icons/mdi/web'


    const people : {company?: string, person?: string, site?: string, ig?: string, email?: string, phone?: string }[] = [
        { company: 'Mikkel Søe Snedkeri', person: 'Mikkel Søe', site: 'https://www.mssnedkeri.com/', ig: 'mssnedkeri'},
        { company: 'Ballowitz Guitars', person: 'Henrik Guitars', ig: 'ballowitzguitars'},
        { company: 'Temporal', person: 'Johan Bichel Lindegaard', site: 'https://www.temporal.dk', ig: 'studio_temporal' },
        { company: 'JEL Instruments', person: 'Jens Erik Larsen', site: 'https://www.jelinstruments.com/',  ig: 'jel_instrumenter'},
        { company: 'Hysteria Objects', person: 'Pil Whitta', site: 'https://www.hysteria-objects.com/', ig: 'hysteria_objects' },
        { person: 'Anna Søgaard', ig: 'soegaardanna' },
        { company: '', person: 'Frederik Friberg', site: '', ig: '_moebel_' },
        { company: 'Johan.cc', person: 'Johan.cc', site: 'https://www.johan.cc' },
        { company: 'Batch Productions', site: 'https://www.batchproductions.dk/', ig: 'batch_productions', email: 'hello@batchproductions.dk' },
    ]

</script>

<ul class="grid grid-rows-3 grid-flow-col gap-4">
    {#each people as person}
        <li>
            {#if person.company}
            <h2 class="text-4xl">{person.company}</h2>

            {:else}
                {#if person.person }
                    <h2 class="text-4xl">{person.person}</h2>
                {/if}
            {/if}
            <div class="flex">
                {#if person.site}
                <a href={person.site} title="Website for {person.company || person.person}"><SiteIcon/></a>
            {/if}
            {#if person.ig}
                <!-- instragram icon -->
                <a href="https://www.instagram.com/{person.ig}/"><InstagramIcon class="w-6 h-6" /></a>
            {/if}
            {#if person.email}
                <a href="mailto:{person.email}">{person.email}</a>
            {/if}
            {#if person.phone}
                <a href="tel:{person.phone}">{person.phone}</a>
            {/if}
            </div>
            
        </li>
    {/each}
</ul>

