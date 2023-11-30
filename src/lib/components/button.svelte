<script>

    export let texto1 = "ejemplo";
    export let texto2 = "ejemplo dos";

</script>

<div>

    <div href="/" class="button-container">


        <div class=""  >{texto1} aaa</div>
        <div class="">{texto2}</div>
    </div>

 
</div>


<style>

    .button-container{
        display:flex;
        flex-direction: column;

        width: clamp(200px,  60vw, 720px);
        border-radius: 12px;
        justify-content: center;
        align-items: center;
        align-content: center;
        min-height: 30px;
        max-height: 50px;
        
        background-color: var(--color-bg-02);
        transition: all 0.3s ease;
    }
    .button-container:hover, .button-container:active {
        background-color: var(--color-accent-01);
        transform: scaleX(1) scaleY(1) scaleZ(1)  rotateZ(2deg) translateX(0px) translateY(0px) translateZ(0px) skewX(0deg) skewY(0deg);
        transform: scale(1.1) rotateX(10deg) rotateY(12deg);

    }

</style>