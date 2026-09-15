<script>
    let { data } = $props();
    const person = data.person;
</script>

<main>
    <article>
        <h1>{ person.name }</h1>
        <p>{@html person.bio }</p>
    </article>

    <div class="info-buttons">
        <button>Knop 1</button>
        <button>Knop 2</button>
        <button>Knop 3</button>
    </div>
</main>