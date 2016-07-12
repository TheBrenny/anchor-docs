---
layout: page
title: Articles
---

# Articles

### `article_author`

Returns the name of the post author as a string.

`<p id="author"><?php echo article_author(); ?></p>`

### `article_author_bio`

Returns the biography of the current post author.

`<p id="bio"><?php echo article_author_bio(); ?></p>`

### `article_author_id`

Returns the database ID of the current post author.

`<?php echo article_author_id(); ?>`

### `article_author_email`

Returns the email address of the current post author.

`<?php echo article_author_email(); ?>`

### `article_css`

If custom CSS was added, returns the custom CSS. Should be used like this:

``` php
<?php if(article_css()): ?>
    <style><?php echo article_css(); ?></style>
<?php endif; ?>
```

### `article_custom_field($key, $fallback = '')`

Retrieves a custom field with the key $key, with an optional fallback parameter ($fallback). Used like so:

``` php
<small class="attribution">
    Thanks to <?php echo article_custom_field('attribution', 'Mike'); ?>
</small>
```

### `article_date`

Returns a date-formatted version of `article_time()`. Default format is jS M, Y (24th January, 2012).

`<time><?php echo article_date(); ?></time>`

### `article_description`

Returns a short description, as set in the "description" field of the admin area.

`<p class="article-description"><?php echo article_description(); ?></p>`

### `article_html`

Returns the content of the blog post, as a HTML string.

`<article><?php echo article_html(); ?></article>`

### `article_markdown`

Returns the raw markdown of the blog post, as a HTML string.

`<article><?php echo article_markdown(); ?></article>`

### `article_id`

Returns the database-assigned ID of the current article, as a number. Used for uniquely identifying a post.

`<?php echo article_id(); ?>`

### `article_js`

Similar to article_css(), but with Javascript. Should be used like this:

``` php
<?php if(article_js()): ?>
    <script><?php echo article_js(); ?></script>
<?php endif; ?>
```

### `article_slug`

Returns the slug of the current article. Should not be used in posts.php (you should use `article_url()` instead, which will correctly calculate the URL).

`<?php echo article_slug(); ?>`

### `article_status`

Returns a string which contains the current status of the article. Can be either draft, archived, published.

`<?php echo article_status(); ?>`

### `article_time`

Returns a UNIX timestamp from when the post was added, which can be used to add custom timestamps. If you want to use the default timestamp, use `article_date()` instead.

`<?php echo article_time(); ?>`

### `article_title`

Returns the title of the current article as a string, as set in the admin area.

`<h1><?php echo article_title(); ?></h1>`

### `article_total_comments`

Returns the total number of published comments for the current article.

<span class="total-comments"><?php echo article_total_comments(); ?></span>

### `article_url`

Returns a fully-built URL string, which serves as a permalink. Should be used like so:

``` php
<a href="<?php echo article_url(); ?>">
    <?php echo article_title(); ?>
</a>
```

### `article_customised`

Alias for `customised` to matched prefixed fuction theme.

### `customised`

Returns true if an article has custom CSS or Javascript attached to it, false if not.

``` php
<?php if(customised()) : ?>
<p>This page has custom CSS or JS</p>
<?php else : ?>
<p>This page does not have custom CSS or JS</p>
<?php endif; ?>
```

### `article_number`

Returns the number of the article. Your 3rd published article will return 3.

`<p>This is article number <?php echo article_number(); ?></p>`

### `article_adjacent_url($side = 'next', $draft = false, $archive = false)`

Returns the url to an adjacent article. Takes `$side` (next|prev|previous) and flags to include drafted or archived articles.

``` php
<a href="<?php echo article_adjacent_url('prev'); ?>">Previous</a>
<a href="<?php echo article_adjacent_url('next'); ?>">Next</a>
```

### `article_previous_url($draft = false, $archive = false)`

Returns the url to the previous page. Takes flags to include drafted or archived articles.

`<a href="<?php echo article_previous_url(); ?>">Previous</a>`

### `article_next_url($draft = false, $archive = false)`

Returns the url to the next page. Takes flags to include drafted or archived articles.

`<a href="<?php echo article_next_url(); ?>">Previous</a>`

### `article_category`

Returns the name of the category this article is in.

`<p>This article is in: <?php echo article_category(); ?></p>`

### `article_category_id`

Returns the ID of the category this article is in.

`<p><?php echo article_category_id(); ?></p>`

### `article_category_slug`

Returns the slug of the category this article is in.

`<p>This article is in: <?php echo article_category_slug(); ?></p>`

### `article_category_url`

Returns the url of the category which this article is in.

`<a href="<?php echo article_category_url(); ?>"><?php echo article_category(); ?></a>`

### `article_object`

Returns the article as an object.

`<?php $article = article_object(); echo $article->title; ?>`

### `related_posts($n)`

Returns `n` number of related posts as an array of `Post` objects.

`<?php $related = related_posts(5); ?>`
