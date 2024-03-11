<svelte:head>
<title>Путешествия</title>
</svelte:head>
<div class="container">
    <h1>Места из моих путешествий</h1>
    <h4>Прошлые 2 года были весьма интересными и я хотел бы поделиться своими фотографиями с вами</h4>
    <div class="blogposts">
        {#each routes as page}
            <div class="post">
                <h2>{page.title}</h2>
                <p>{page.body}</p>
                <p class="readmore">
                    Для просмотра фото 
                    <a class="link" href={`/about/travel/${page.id}`}>
                        Click here
                    </a>
                </p>
            </div>
        {/each}
    </div>
</div>

<style>
    .container {
        margin: 50px auto;
        max-width: 800px;
        padding: 0 20px;
    }

    .blogposts {
        display: grid;
        grid-template-columns: 1fr 1fr;
        grid-gap: 20px;
    }

    .post {
        border: 1px solid #8b8787;
        padding: 10px;
        box-shadow: 0 0 10px #eee;
        color: #1c856a;
    }

    .link {
        color:rgb(10, 10, 139);
        border: 2px solid rgb(189, 185, 185);
        border-radius: 10px;           
    }
    .link:hover {
        border-color: red;
    }

</style>


<script>
    import {routes} from './routes'
</script>