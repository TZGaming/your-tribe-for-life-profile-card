<script>
    let { data } = $props();
    const person = $derived(data.person);

    const customData = $derived(JSON.parse(person.custom));
</script>

<main>
    <article id="info">
        <div class="general-info-split">
            <div class="info-text">
                <h1>{ person.name }</h1>
                <p>{@html person.bio }</p>
            </div>
            <div class="info-mugshot">
                <img src="https://fdnd.directus.app/assets/{person.mugshot}?height=300" alt="" width="250" height="250"/>
            </div>
        </div>
    </article>

    <article id="socials">
        <h1>Socials</h1>
        <p>Discord: { customData.socials.discord }</p>
        <p>YouTube: { customData.socials.youtube }</p>
        <p>Github: { person.github_handle }</p>
    </article>

    <article id="extra">
        <h1>Extra content</h1>

        <div class="games-grid">
            {#each Object.entries(customData.games) as [key, game]}
                <div class="game-card">
                    <img src={game.image} width="100" height="100" alt={game.title} />
                    <p>{game.title}</p>
                </div>
            {/each}
        </div>
    </article>

    <div class="info-buttons">
        <a href="#info">Algemene info</a>
        <a href="#socials">Socials</a>
        <a href="#extra">Extra content</a>
    </div>
</main>