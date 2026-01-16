---
layout: default
title: R-Lab Projects
permalink: /lab/
---

<section class="bg-clinic-dark text-white py-20 relative overflow-hidden">
    <!-- Abstract tech background elements could go here -->
    <div class="container mx-auto px-6 relative z-10 text-center">
        <span class="inline-block px-3 py-1 mb-4 text-xs font-bold tracking-widest uppercase bg-clinic-blue text-clinic-dark rounded-full">
            Engineering Health
        </span>
        <h1 class="text-4xl md:text-5xl font-bold mb-6">Ryu Lab</h1>
        <p class="text-xl max-w-2xl mx-auto text-gray-300">
            Where traditional medical wisdom meets modern software engineering. 
            Developing tools to advance diagnosis, treatment, and practice management.
        </p>
    </div>
</section>

<section class="py-20 bg-gray-50">
    <div class="container mx-auto px-6">
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
            <!-- Render from _data/projects.yml -->
            {% for project in site.data.projects %}
            <article class="bg-white rounded-xl shadow-md overflow-hidden hover:shadow-xl transition-shadow border border-gray-100 flex flex-col h-full">
                <div class="h-48 bg-gray-200 relative overflow-hidden group">
                    {% if project.image %}
                    <img src="{{ project.image }}" alt="{{ project.name }}" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500">
                    {% else %}
                     <div class="w-full h-full flex items-center justify-center bg-clinic-dark text-gray-600">
                        <i class="fas fa-microchip text-4xl opacity-30"></i>
                    </div>
                    {% endif %}
                    <div class="absolute top-4 right-4">
                         <span class="px-2 py-1 text-xs font-bold rounded bg-white/90 backdrop-blur-sm shadow-sm
                            {% if project.status == 'In Development' %}text-yellow-600
                            {% elsif project.status == 'Live' %}text-green-600
                            {% else %}text-gray-600{% endif %}">
                            {{ project.status }}
                        </span>
                    </div>
                </div>
                
                <div class="p-6 flex-1 flex flex-col">
                    <h3 class="text-xl font-bold text-gray-900 mb-2">{{ project.name }}</h3>
                    <p class="text-gray-600 text-sm mb-4 flex-1">{{ project.description }}</p>
                    
                    <div class="flex flex-wrap gap-2 mb-6">
                        {% for tech in project.tech_stack %}
                        <span class="text-xs px-2 py-1 bg-gray-100 text-gray-500 rounded border border-gray-200">{{ tech }}</span>
                        {% endfor %}
                    </div>
                    
                    <a href="{{ project.github_url }}" class="block text-center w-full py-2 border border-gray-300 rounded-lg hover:bg-gray-50 text-sm font-medium transition-colors">
                        View Project
                    </a>
                </div>
            </article>
            {% endfor %}
            
            <!-- Recruitment / Vision Card -->
            <div class="bg-clinic-dark rounded-xl shadow-md overflow-hidden p-8 flex flex-col justify-center items-center text-center text-white">
                <div class="w-16 h-16 bg-white/10 rounded-full flex items-center justify-center mb-6">
                    <i class="fas fa-lightbulb text-2xl text-clinic-blue"></i>
                </div>
                <h3 class="text-xl font-bold mb-4">Have an Idea?</h3>
                <p class="text-gray-300 text-sm mb-6">
                    We are always looking for new ways to integrate technology into clinical practice.
                </p>
                <a href="mailto:dev@ryu.clinic" class="text-clinic-blue hover:text-white font-medium text-sm transition-colors">
                    Contact R-Lab &rarr;
                </a>
            </div>
        </div>
    </div>
</section>
