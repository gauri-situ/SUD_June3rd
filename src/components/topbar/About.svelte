<script>
    let about_in_view = false;
</script>

<button
    id="about_text"
    class="text_level1 noselect"
    style="color:{about_in_view ? 'white' : ''}"
    on:click={() => {
        about_in_view = !about_in_view;
    }}><span> about </span></button
>

{#if about_in_view}
    <div class="modal_container">
        <div class="box modal_content text_level3" id="about_modal">
            <div style="color:white">
                <div>
                    <div class="text_level1">DESCRIPTION</div>
                    <p>
                        Text description of project (IN PROGRESS)
                    </p>

                    <p>
                        (IN PROGRESS)
                    </p>
                </div>
                <div>
                    <div class="text_level1">ATTRIBUTION</div>
                  

                    <p style="color:var(--grey2)">
                        For non-commercial projects or entities, Mapbox may be
                        able to provide account support and discounts. Contact
                        community@mapbox.com to describe your Codec use case and
                        request Mapbox account support.
                    </p>

                    <p style="color:var(--grey2)">
                        Graphic identity and UI consultancy by <a
                            href="https://scasascia.com/"
                            target="_blank"
                            rel="noopener noreferrer">Studio Scasascia</a
                        >.
                    </p>

                    <p style="color:var(--grey2)">
                        <a
                            href="https://choosealicense.com/licenses/agpl-3.0/"
                            target="_blank"
                            rel="noopener noreferrer"
                        >
                            License
                        </a>
                    </p>
                </div>
            </div>
            <span
                on:click={() => (about_in_view = false)}
                id="about_close_button">&#215;</span
            >
        </div>
    </div>
{/if}

<style>
    #about_text {
        color: var(--grey2);
        text-align: center;
        margin-left: auto;
    }

    span {
        display: inline-block;
        vertical-align: middle;
        line-height: normal;
        padding: 1px 0;
    }

    #about_modal {
        display: flex;
        flex-flow: row nowrap;
        padding: var(--grid-size);
    }

    #about_modal > div {
        flex-grow: 1;
        display: flex;
        flex-flow: row wrap;
    }

    #about_modal > div > div {
        flex: 1 1 350px;
        margin-right: var(--grid-size);
    }

    #about_close_button {
        cursor: pointer;
        color: white;
    }
</style>
