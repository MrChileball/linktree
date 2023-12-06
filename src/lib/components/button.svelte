<script>

    export let text = "ejemplo";

    export let link = "https://google.com"

    $: copy = false;


    export function copyURL () {

        copy = true;


        navigator.clipboard.writeText(link);

        setTimeout(() => {
            copy = false;
        }, 2000);
        copy = copy;
        
    }
    export function openTab (url) {
        window.open(url, "_blank");
    }

</script>

<div>

    <div class="button-container">


        <button on:click="{() => openTab(link)}" target="_blank" class="text"  >
            <div class=""> · {text} · </div>    
        </button>
        <!-- svelte-ignore a11y-no-static-element-interactions -->
        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <div on:click="{() => copyURL()}" class="share-link">
            
            {#if copy == true }
                <div class="copied-container scale-up-bottom"> 
                    <h3>¡Copiado!</h3>
                </div>
            {:else}

            <div></div>

                
            {/if}
            <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-copy" width="44" height="44" viewBox="0 0 24 24" stroke-width="1.5" stroke="#ffffff" fill="none" stroke-linecap="round" stroke-linejoin="round">
                <path stroke="none" d="M0 0h24v24H0z" fill="none"/>
                <path d="M8 8m0 2a2 2 0 0 1 2 -2h8a2 2 0 0 1 2 2v8a2 2 0 0 1 -2 2h-8a2 2 0 0 1 -2 -2z" />
                <path d="M16 8v-2a2 2 0 0 0 -2 -2h-8a2 2 0 0 0 -2 2v8a2 2 0 0 0 2 2h2" />
              </svg>
        </div>
        
        

    </div>

 
</div>


<style>

    .button-container{
        display:flex;
        flex-direction: row;

        width: clamp(200px,  60vw, 720px);
        height: 64px;

        align-items: center;
        align-content: center;
        min-height: 30px;
        max-height: 50px;
        
        background-color: #27272a;
        backdrop-filter: blur(15px) opacity(50%);
        background-color: rgba(0, 0, 0, 0.7);

        color: rgb(255, 255, 255);
        transition: transform 0.15s cubic-bezier(0, 0.2, 0.5, 3) 0s;
        box-shadow: rgba(10, 11, 13, 0.08) 0px 2px 4px 0px;
        border-radius: 4px;
        justify-content: space-between;


    }
    .button-container:hover, .button-container:active {
        background-color: rgba(0, 0, 0, 0.9);

        transform: scaleX(1) scaleY(1) scaleZ(1)  rotateZ(2deg) translateX(0px) translateY(0px) translateZ(0px) skewX(0deg) skewY(0deg);
        transform: scale(1.02) rotateX(5deg) rotateY(0deg);

    }
    .share-link{
        position: absolute;
        left: 90%;
        width: 100%;
        max-width: 48px;
        display: flex;

        height:auto;
    }
    .icon{
        width: 100%;
        max-width: 32px;
        height: 100%;
    }
    .copied-container{
        position: absolute;
        left: -55%;
        top: -60%;
        background-color: #27272a;
        padding: 4px 12px;
        border-radius: 4px;
        transition: 0.4s all cubic-bezier(0.075, 0.82, 0.165, 1);

    }
    .text{
        display: flex;
        justify-content: center;
        justify-items: center;
        align-items: center;
        align-content: center;
        width: 100%;
        height: 100%;
    }

</style>