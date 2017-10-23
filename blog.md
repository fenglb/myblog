---
layout: default 
title : "Blog Index"
---
<div class="site_content">
    {% for post in site.posts %}
    <article id="" class="post">
        <div class="post_thumbnail_wrapper">
            <a class="post-thumbnail" href="{{ post.url|prepend: site.baseurl }}" aria-hidden="true">
                <img src="{{ post.thumbnail }}" class="post-image" alt="{{ post.title }}">
            </a>
        </div>
        <div class="post_info_wrapper">
            <div class="blog_post_title">
                <h2 class="title post_title">
                    <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
                </h2>
            </div>
            <div class="blog_post_meta">
                <span class="blog_meta_item blog_meta_category">In <a href="{{ post.url | prepend: site.baseurl }}" rel="category tag">Image Posts</a></span>
                <span class="blog_meta_item blog_meta_tag">Tag <a href="" rel="category tag">people</a></span>
                <span class="blog_meta_item blog_meta_date">{{ post.date | date: "%Y-%m-%d" }}</span>
                <span class="blog_meta_item blog_meta_author">{{ post.author }}</span>
            </div>
            <div class="blog_post_text blog_post_description">
                <p>
                    {{ post.description }}
                </p>
            </div>
        </div>
    </article>
    {% endfor %}
</div>
