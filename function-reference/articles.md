---
layout: page
---

# Articles

### `article_author`

Returns the name of the post author as a string.
	
	<p id="author"><?php echo article_author(); ?></p>

### `article_author_bio`

Returns the biography of the current post author.

	<p id="bio"><?php echo article_author_bio(); ?></p>

### `article_author_id`

Returns the database ID of the current post author.

	<?php echo article_author_id(); ?>

### `article_css`

If custom CSS was added, returns the custom CSS. Should be used like this:

	<?php if(article_css()): ?>
	    <style><?php echo article_css(); ?></style>
	<?php endif; ?>

### `article_custom_field($key, $fallback = '')`

Retrieves a custom field with the key $key, with an optional fallback parameter ($fallback). Used like so:

	<small class="attribution">
	    Thanks to <?php echo article_custom_field('attribution', 'Mike'); ?>
	</small>

### `article_date`

Returns a date-formatted version of `article_time()`. Default format is jS M, Y (24th January, 2012).

	<time><?php echo article_date(); ?></time>

### `article_description`

Returns a short description, as set in the "description" field of the admin area.
	
	<p class="article-description"><?php echo article_description(); ?></p>

### `article_html`

Returns the content of the blog post, as a HTML string.

	<article><?php echo article_html(); ?></article>

### `article_id`

Returns the database-assigned ID of the current article, as a number. Used for uniquely identifying a post.
	
	<?php echo article_id(); ?>

### `article_js`

Similar to article_css(), but with Javascript. Should be used like this:

	<?php if(article_js()): ?>
	    <script><?php echo article_js(); ?></script>
	<?php endif; ?>

### `article_slug`

Returns the slug of the current article. Should not be used in posts.php (you should use `article_url()` instead, which will correctly calculate the URL).

	<?php echo article_slug(); ?>

### `article_status`

Returns a string which contains the current status of the article. Can be either draft, archived, published.
	
	<?php echo article_status(); ?>

### `article_time`

Returns a UNIX timestamp from when the post was added, which can be used to add custom timestamps. If you want to use the default timestamp, use `article_date()` instead.

	<?php echo article_time(); ?>

### `article_title`

Returns the title of the current article as a string, as set in the admin area.
	
	<h1><?php echo article_title(); ?></h1>

### `article_total_comments`

Returns the total number of published comments for the current article.

	<span class="total-comments"><?php echo article_total_comments(); ?></span>

### `article_url`

Returns a fully-built URL string, which serves as a permalink. Should be used like so:

	<a href="<?php echo article_url(); ?>">
	    <?php echo article_title(); ?>
	</a>

### `customised`

Returns true if an article has custom CSS or Javascript attached to it, false if not.

	<?php if(customised()) : ?>
		<p>This page has custom CSS or JS</p>
	<?php else : ?>
		<p>This page does not have custom CSS or JS</p>
	<?php endif; ?>
