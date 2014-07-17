---
layout: home
---


<div class="index-content blog">
    <div class="section">
        <ul class="artical-cate">
            <li class="on"><a href="/"><span>Blog</span></a></li>
            <li style="text-align:center"><a href="/opinion"><span>Luan</span></a></li>
            <li style="text-align:right"><a href="/project"><span>Life</span></a></li>
        </ul>

        <div class="cate-bar"><span id="cateBar"></span></div>

        <ul class="artical-list">
        {% for post in site.categories.blog %}
            <li>
                <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
                <div class="title-desc">{{ post.description }}</div>
            </li>
        {% endfor %}
        </ul>
 <!-- 分页器: Pagination links -->
		<div id="post-pagination" class="pagination">
		   <hr>
		     <br/>
		  {% if paginator.previous_page %}
		  <div class="four columns">
		    {% if paginator.previous_page == 1 %}
		    <a href="/">&larr; Previous</a>
		    {% else %}
		    <a href="/page{{paginator.previous_page}}">&larr; 上一页/Previous</a>
		    {% endif %}
		  </div>
		  {% else %}
		  <div class="four columns previous disabled">
		    <span>&larr; Previous</span>
		  </div>
		  {% endif %}

		<div class="four columns">
		<span class="page_number ">Page: {{paginator.page}} of {{paginator.total_pages}}</span>
		</div>

		  {% if paginator.next_page %}
		  <div class="four columns next">
		    <a href="/page{{paginator.next_page}}">Next &rarr;</a>
		  </div>
		  {% else %}
		  <div class="four columns next disabled">
		    <span>下一页/Next &rarr;</span>
		  </div>
		  {% endif %}
		     <br/> <br/>
		</div>

  </div>


    </div>
    <div class="aside">
    </div>
</div>
