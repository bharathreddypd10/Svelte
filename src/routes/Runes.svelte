<script>
    let count= $state(0);
    let doubled = $derived(count * 2);
    let numbers= $state([1,2,3]);

    function addnumber(){
        numbers.push(numbers.length + 1);
    }
</script>

<button onclick={()=>count++}>
clicks: {count}
</button>
<h2>doubled: {doubled}</h2>
{#if count > 5}
<p>{count} is greater than 5</p>    
{/if
}
<button onclick={addnumber}>
    push
</button>
{#each numbers as number}
    <p>{number}</p>
{/each}