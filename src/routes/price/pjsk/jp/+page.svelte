<script>
    let a = 'nothing'
    import Crystal from "./Crystal.svelte"
    import ServerNavigation from '../ServerNavigation.svelte'
    import Items from "./Items.svelte"
</script>

<main class="justify-center text-center items-center flex mt-2">
    <div>

        <ServerNavigation/>

    <div class="card card-hover text-primary-900 w-full xl:w-1/2 m-auto left-0 right-0 mb-3 rounded-2xl p-2 drop-shadow-lg">
        <header class='h2'>
            Server: <strong>Japan</strong>
        </header> <br>
        <section>
            Sau stream #26, Puroseka đã update giới hạn là 2 lần chuyển dữ liệu khi người chơi đạt top1000 sau 24h bắt đầu event nên bồ nào nạp cân nhắc để tránh việc acc gặp vấn đề nha 😣
        </section>       
    </div>



    </div>
</main>

<main class="justify-center text-center items-center flex mt-2">
    <div class="card xl:max-w-[700px] m-auto text-primary-900 left-0 right-0 mb-3 rounded-2xl p-2 drop-shadow-lg">
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
                    <img src="/img/prices/prsk/jp/17 - 349.000.PNG" class="m-auto left-0 right-0" alt="">
                    349.000₫
                </span>
            {:else if a == "support"}
                Gói hỗ trợ
                <span>
                    <img src="/img/prices/prsk/jp/21.png" class="m-auto left-0 right-0" alt="">
                    <br>
                </span>
                <span>
                    <img src="/img/prices/prsk/jp/18 - 79.000.PNG" class="m-auto left-0 right-0" alt="">
                    79.000₫
                </span>
                <span>
                    <img src="/img/prices/prsk/jp/19 - 249.000.PNG" class="m-auto left-0 right-0" alt="">
                    249.000₫
                </span>
                <span>
                    <img src="/img/prices/prsk/jp/20 - 499.000.PNG" class="m-auto left-0 right-0" alt="">
                    499.000₫
                </span>

            {/if}
        </section>
    </div>
</main>