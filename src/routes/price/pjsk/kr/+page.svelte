<script>
    let a = 'nothing'
    import Crystal from "./Crystal.svelte"
    import Items from "./Items.svelte"
    import ServerNavigation from '../ServerNavigation.svelte'

</script>

<main class="justify-center text-center items-center flex mt-2">
    <div>

        <ServerNavigation/>

    <div class="card card-hover w-full text-primary-900 m-auto left-0 right-0 mb-3 rounded-2xl p-2 drop-shadow-lg">
        <header class='h2'>
            Server: <strong>Korean</strong>
        </header>
    </div>



    </div>
</main>

<main class="justify-center text-center items-center flex mt-2">
    <div class="card xl:max-w-[700px] text-primary-900 m-auto left-0 right-0 mb-3 rounded-2xl p-2 drop-shadow-lg">
        <header>
            <button class="btn variant-soft-secondary text-xl" on:click={() => {a='crystal'}}>Crystal</button>
            <button class="btn variant-soft-success text-xl" on:click={() => {a='items'}}>Vật Phẩm</button>
            <button class="btn variant-soft-secondary text-xl" on:click={() => {a='costume'}}>Costume</button>
            <button class="btn variant-soft-primary text-xl" on:click={() => {a='support'}}>Gói hỗ trợ</button>
        </header>
        <section class="p-2 text-xl mt-2">
            {#if a == "nothing"}
                Bấm vào thứ bạn muốn xem
            {:else if a == "crystal"}
                <strong>Crystal</strong>
                <Crystal />
            {:else if a == "items"}
                <strong>Vật Phẩm</strong>
                <Items />
            {:else if a == "costume"}
                Costume
                <span class="text-3xl">
                    <img src="/img/prices/prsk/kr/18.PNG" class="m-auto left-0 right-0" alt="">
                </span>
            {:else if a == "support"}
                Gói hỗ trợ
                <span>
                    <img src="/img/prices/prsk/kr/19.png" class="m-auto left-0 right-0" alt="">
                </span>
                <span>
                    <img src="/img/prices/prsk/kr/20.PNG" class="m-auto left-0 right-0" alt="">
                </span>
            {/if}
        </section>
    </div>
</main>