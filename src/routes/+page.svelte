<script>
    let { data } = $props();
    const person = data.person;
</script>

<article>
    <h1>{ person.name }</h1>
    <p>{@html person.bio }</p>
</article>