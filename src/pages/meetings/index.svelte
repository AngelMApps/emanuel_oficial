<script>
    import {meetLinks} from '../../components/meeting_links'
    import CompMeet from '../../components/meetings/meet_comp.svelte'
    let indices=[];
    const recorreArray = (arr) => {
        for( let i=0;i<=arr.length-1; i++){
            console.log(i);
            indices.push(i);
        }
    }

    recorreArray(meetLinks);
    console.log(indices);
</script>

<main>
    {#each indices as i }
        <CompMeet iTitle={meetLinks[i].name} iURL={meetLinks[i].iURL} mt={meetLinks[i].mt}/>
    {/each}
</main>

<style>
    main{
        width: 100%;
        display: flex;
        flex-direction: column;
    }
</style>

