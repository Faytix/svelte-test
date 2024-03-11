<nav>
    <div class="nav-container">
        <a href="/" class="nav-logo" title="Back To Homepage">Александр Сорокин</a>
        <div class="nav-links">
            {#each nav as link}
            {#if link.isShow}
            <a href={link.href} class="link">{link.title}</a>
            {/if}
            {/each}
        </div>
    </div>
</nav>

<div class="container">
    <!--Pages will be injected below-->
    <slot></slot>
</div>
<script>
    const nav =[
        {
            title:'Путешествия',
            href:'/about',
            isShow: true,
        },
        {
            title:'Блог',
            href:'/blog',
            isShow: true,
        },
        {
            title:'Мои любимые фильмы',
            href:'/contact',
            isShow: true,
        },
    ]
</script>
<style>
    .container {
        max-width: 1400px;
        margin: 50px auto;
    }
    nav{
        background-color: #f3f1f1;
        border: 1px solid black;
        width: 100%;
        margin: 0;
    }
</style>