---
layout: default
title: Blog
permalink: /blog/
---

<section class="relative py-32 overflow-hidden">
    <div class="absolute inset-0 z-0">
        <img src="/assets/images/hero_tcm_tech_blend.png" alt="Clinic Blog" class="w-full h-full object-cover">
        <div class="absolute inset-0 bg-linear-to-b from-clinic-dark/90 via-clinic-dark/80 to-clinic-dark/95 backdrop-blur-sm"></div>
    </div>
    <div class="container mx-auto px-6 relative z-10 text-center">
        <span class="text-clinic-blue font-bold tracking-[0.3em] uppercase text-xs mb-6 block">Clinic Insights</span>
        <h1 class="text-5xl md:text-7xl font-extrabold text-white mb-6 tracking-tight">Health & Innovation</h1>
        <p class="text-xl md:text-2xl text-gray-300 font-light max-w-2xl mx-auto">Exploring the intersection of Traditional Chinese Medicine, wellness, and modern technology.</p>
    </div>
</section>

<section class="py-24 px-6 section-gradient">
    <div class="container mx-auto max-w-5xl">
        <div class="grid grid-cols-1 gap-12">
            {% for post in site.posts %}
            <article class="glass-card group !p-0 overflow-hidden hover:border-clinic-teal/30 transition-all duration-500">
                <div class="flex flex-col md:flex-row">
                    <!-- Image side -->
                    <div class="md:w-2/5 relative overflow-hidden aspect-video md:aspect-auto">
                        {% if post.header.overlay_image %}
                        <img src="{{ post.header.overlay_image }}" alt="{{ post.title }}" class="absolute inset-0 w-full h-full object-cover group-hover:scale-110 transition-transform duration-700">
                        {% else %}
                        <div class="absolute inset-0 bg-slate-100 flex items-center justify-center text-slate-300">
                            <i class="fas fa-newspaper text-5xl"></i>
                        </div>
                        {% endif %}
                        <div class="absolute inset-0 bg-linear-to-t from-clinic-dark/20 to-transparent"></div>
                    </div>

                    <!-- Content side -->
                    <div class="md:w-3/5 p-8 md:p-12 flex flex-col">
                        <div class="flex items-center gap-4 mb-6">
                            <span class="px-3 py-1 bg-clinic-teal/5 text-clinic-teal text-[10px] font-bold rounded-full uppercase tracking-widest border border-clinic-teal/10">
                                {% if post.categories %}{{ post.categories | first }}{% else %}Insight{% endif %}
                            </span>
                            <time class="text-xs font-medium text-gray-400 tracking-wide" datetime="{{ post.date | date_to_xmlschema }}">
                                {{ post.date | date: "%B %d, %Y" }}
                            </time>
                        </div>

                        <h2 class="text-3xl font-bold text-clinic-dark mb-4 group-hover:text-clinic-teal transition-colors leading-tight">
                            <a href="{{ post.url }}">{{ post.title }}</a>
                        </h2>

                        <p class="text-gray-600 leading-relaxed mb-8 flex-1 line-clamp-2">
                            {{ post.excerpt | strip_html | truncatewords: 40 }}
                        </p>

                        <div class="flex items-center justify-between mt-auto">
                            <a href="{{ post.url }}" class="inline-flex items-center text-clinic-blue font-bold group/link hover:gap-3 transition-all">
                                Read Article <i class="fas fa-arrow-right ml-2 group-hover/link:translate-x-1 transition-transform"></i>
                            </a>
                            
                            <span class="text-xs font-bold text-gray-300 uppercase tracking-widest">
                                {% assign words = post.content | number_of_words %}
                                {% if words < 360 %}1 min read{% else %}{{ words | divided_by: 180 }} min read{% endif %}
                            </span>
                        </div>
                    </div>
                </div>
            </article>
            {% endfor %}
        </div>
    </div>
</section>
