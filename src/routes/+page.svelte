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
        <a href="#info">Algemene info</a>
        <a href="#socials">Socials</a>
        <a href="#extra">Extra content</a>
    </div>
</main>