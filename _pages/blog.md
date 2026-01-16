---
layout: default
title: Blog
permalink: /blog/
---

<section class="container mx-auto px-4 py-12">
    <div class="max-w-4xl mx-auto">
        <h1 class="text-4xl font-bold text-gray-900 mb-8 text-center">Blog</h1>
        <p class="text-xl text-gray-600 text-center mb-12">Insights on Health, TCM, and Technology</p>

        <div class="max-w-2xl mx-auto divide-y divide-gray-100">
            {% for post in site.posts %}
            <article class="py-8 group">
                <div class="flex flex-col md:flex-row gap-6 items-start">
                    <div class="flex-1">
                        <!-- Author/Date Meta -->
                        <div class="flex items-center gap-2 mb-3 text-xs font-medium text-gray-500">
                            {% if post.author %}
                            <span class="text-gray-900">{{ post.author }}</span>
                            <span>·</span>
                            {% endif %}
                            <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %d, %Y" }}</time>
                        </div>
                        
                        <a href="{{ post.url }}" class="block group">
                            <h2 class="text-2xl font-bold text-gray-900 mb-2 group-hover:text-clinic-teal transition-colors leading-tight">
                                {{ post.title }}
                            </h2>
                            <p class="text-gray-600 line-clamp-2 mb-4 leading-relaxed font-serif">
                                {{ post.excerpt | strip_html | truncatewords: 30 }}
                            </p>
                        </a>

                        <div class="flex items-center gap-4 text-xs text-gray-500">
                             <a href="{{ post.url }}" class="flex items-center text-clinic-blue font-medium hover:underline">
                                Read more <i class="fas fa-arrow-right ml-1"></i>
                             </a>
                             <span>·</span>
                             {% assign words = post.content | number_of_words %}
                             {% if words < 360 %}
                                1 min read
                             {% else %}
                                {{ words | divided_by: 180 }} min read
                             {% endif %}
                        </div>
                    </div>

                    <!-- Image or Placeholder -->
                    <a href="{{ post.url }}" class="shrink-0 order-first md:order-last">
                        {% if post.header.teaser %}
                        <div class="w-full md:w-40 aspect-[4/3] rounded-lg overflow-hidden bg-gray-100">
                             <img src="{{ post.header.teaser }}" alt="{{ post.title }}" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500">
                        </div>
                        {% elsif post.header.overlay_image %}
                        <div class="w-full md:w-40 aspect-[4/3] rounded-lg overflow-hidden bg-gray-100">
                             <img src="{{ post.header.overlay_image }}" alt="{{ post.title }}" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500">
                        </div>
                        {% else %}
                        <div class="w-full md:w-40 aspect-[4/3] rounded-lg overflow-hidden bg-gray-50 flex items-center justify-center border border-gray-100 group-hover:border-clinic-teal transition-colors">
                             <i class="fas fa-newspaper text-3xl text-gray-300 group-hover:text-clinic-teal/50 transition-colors"></i>
                        </div>
                        {% endif %}
                    </a>
                </div>
            </article>
            {% endfor %}
        </div>
    </div>
</section>
