<script>
    let { data } = $props();
    const person = $derived(data.person);
</script>

<main>
    <article>
        <div class="general-info-split">
            <div class="info-text">
                <h1>{ person.name }</h1>
                <p>{@html person.bio }</p>
            </div>
            <div class="info-mugshot">
                <img src="https://fdnd.directus.app/assets/{person.mugshot}?height=200" alt="" width="200" height="200"/>
            </div>
        </div>
    </article>

    <div class="info-buttons">
        <button>Algemene info</button>
        <button>Socials</button>
        <button>Extra content</button>
    </div>
</main>