<script>

export let article;

</script>

<article class="uk-article" style="color:white">

    <h1 class="uk-article-title" style="color:white"><a class="uk-link-reset" href={article.href}>{article.heading}</a></h1>

    <p class="uk-article-meta" style="color:white">Written by {article.author} on {article.releaseDate}. Posted in Blog</p>

    <p class="uk-text-lead" style="color:white"> 
    {article.content}
    <div class="uk-grid-small uk-child-width-auto" uk-grid>
        <div style="color:white">
            Read more
        </div>
        <div style="color:white">
            5 Comments
        </div>
    </div>

</article>