<script>
    let a = 'nothing'
</script>

<main class="justify-center  text-primary-900 text-center items-center flex mt-2">
    <div>
    <div class="card w-full m-auto left-0 right-0 mb-3 rounded-2xl p-2 drop-shadow-lg">
        <header class='h1 p-2'>
            D4DJ (Japanese)
        </header>
    </div>
    </div>
</main>

<main class="justify-center  text-primary-900 text-center items-center flex mt-2">
    <div class="card xl:max-w-[800px] m-auto left-0 right-0 mb-3 rounded-2xl p-2 drop-shadow-lg">
        <header>
            <button class="btn variant-soft-secondary text-xl" on:click={() => {a='pass'}}>D4PASS</button>
            <button class="btn variant-soft-success text-xl" on:click={() => {a='items'}}>Vật Phẩm</button>
            <button class="btn variant-soft-tertiary text-xl" on:click={() => {a='event'}}>Sự Kiện</button>
            <button class="btn variant-soft-primary text-xl" on:click={() => {a='exp'}}>EXP</button>
            <button class="btn variant-soft-surface text-xl" on:click={() => {a='special'}}>Special Training</button>
            <button class="btn variant-soft-secondary text-xl" on:click={() => {a='diamond'}}>Diamond</button>
        </header>
        <section class="p-2 text-xl mt-2">
            {#if a == "nothing"}
                Bấm vào thứ bạn muốn xem
            {:else if a == "pass"}
                <strong>D4PASS</strong>
                <img src="/img/prices/d4dj/1.PNG" alt="">
            {:else if a == "items"}
                <strong>Vật Phẩm</strong>
                <img src="/img/prices/d4dj/4.PNG" alt="">
                <img src="/img/prices/d4dj/5.PNG" alt="">
                <img src="/img/prices/d4dj/6.PNG" alt="">
            {:else if a == "event"}
                <strong>Sự kiện</strong>
                <img src="/img/prices/d4dj/7.PNG" alt="">
            {:else if a == "exp"}
                <strong>EXP</strong>
                <img src="/img/prices/d4dj/8.PNG" alt="">
                <img src="/img/prices/d4dj/9.PNG" alt="">
            {:else if a == "special"}
                <strong>Special Training</strong>
                <img src="/img/prices/d4dj/10.PNG" alt="">
                <img src="/img/prices/d4dj/11.PNG" alt="">
            {:else if a == "diamond"}
                <strong>Diamond</strong>
                <img src="/img/prices/d4dj/12.PNG" alt="">
                <img src="/img/prices/d4dj/13.PNG" alt="">
                <img src="/img/prices/d4dj/14.PNG" alt="">
            {/if}
        </section>
    </div>
</main>