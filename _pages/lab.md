---
layout: default
title: R-Lab Projects
permalink: /lab/
---

<section class="relative py-32 overflow-hidden">
    <div class="absolute inset-0 z-0">
        <img src="/assets/images/hero_tcm_tech_blend.png" alt="Ryu Lab" class="w-full h-full object-cover">
        <div class="absolute inset-0 bg-linear-to-b from-clinic-dark/95 via-clinic-dark/85 to-clinic-dark/95 backdrop-blur-sm"></div>
    </div>
    
    <!-- Abstract tech background elements -->
    <div class="absolute inset-0 z-0 opacity-20 pointer-events-none">
        <div class="absolute top-1/4 right-1/4 w-96 h-96 bg-clinic-blue rounded-full blur-[120px]"></div>
        <div class="absolute bottom-1/4 left-1/4 w-96 h-96 bg-clinic-teal rounded-full blur-[120px]"></div>
    </div>

    <div class="container mx-auto px-6 relative z-10 text-center">
        <span class="inline-block px-4 py-1.5 mb-6 text-xs font-bold tracking-[0.3em] uppercase bg-clinic-blue/10 text-clinic-blue border border-clinic-blue/20 rounded-full backdrop-blur-md animate-fade-in">
            Engineering Health
        </span>
        <h1 class="text-5xl md:text-7xl font-extrabold text-white mb-8 tracking-tight animate-fade-in-up">Ryu Lab</h1>
        <p class="text-xl md:text-2xl max-w-2xl mx-auto text-gray-300 font-light leading-relaxed animate-fade-in-up delay-100">
            Where Ancient Medical Wisdom meets <span class="text-white font-medium">Modern Software Engineering</span>. 
            Architecting the future of clinical precision.
        </p>
    </div>
</section>

<section class="py-32 section-gradient">
    <div class="container mx-auto px-6">
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-10">
            {% for project in site.data.projects %}
            <article class="glass-card group !p-0 overflow-hidden hover:border-clinic-blue/40 transition-all duration-500 flex flex-col h-full shadow-2xl">
                <div class="h-56 relative overflow-hidden group">
                    {% if project.image %}
                    <img src="{{ project.image }}" alt="{{ project.name }}" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-700">
                    {% else %}
                     <div class="w-full h-full flex items-center justify-center bg-slate-900 text-slate-700 group-hover:text-clinic-blue transition-colors duration-500">
                        <i class="fas fa-microchip text-6xl opacity-20 group-hover:opacity-40 transition-opacity"></i>
                    </div>
                    {% endif %}
                    
                    <div class="absolute inset-0 bg-linear-to-t from-clinic-dark/60 via-transparent to-transparent"></div>
                    
                    <div class="absolute top-6 right-6">
                         <span class="px-3 py-1 text-[10px] font-bold rounded-full backdrop-blur-xl border shadow-lg uppercase tracking-widest
                            {% if project.status == 'In Development' %}bg-amber-500/20 text-amber-300 border-amber-500/30
                            {% elsif project.status == 'Live' %}bg-emerald-500/20 text-emerald-300 border-emerald-500/30
                            {% else %}bg-slate-500/20 text-slate-300 border-slate-500/30{% endif %}">
                            {{ project.status }}
                        </span>
                    </div>
                </div>
                
                <div class="p-8 md:p-10 flex-1 flex flex-col">
                    <h3 class="text-2xl font-bold text-clinic-dark mb-4 group-hover:text-clinic-blue transition-colors">{{ project.name }}</h3>
                    <p class="text-gray-600 text-base mb-8 flex-1 leading-relaxed font-light">{{ project.description }}</p>
                    
                    <div class="flex flex-wrap gap-2 mb-10">
                        {% for tech in project.tech_stack %}
                        <span class="text-[10px] uppercase tracking-wider px-3 py-1 bg-slate-50 text-slate-500 font-bold rounded-lg border border-slate-100 group-hover:border-clinic-blue/10 transition-colors">{{ tech }}</span>
                        {% endfor %}
                    </div>
                    
                    <a href="{{ project.github_url }}" class="group/btn relative inline-flex items-center justify-center w-full py-4 bg-clinic-dark rounded-2xl text-white text-sm font-bold transition-all overflow-hidden">
                        <span class="relative z-10 flex items-center gap-3">
                            Explore Repository <i class="fab fa-github text-lg group-hover/btn:rotate-12 transition-transform"></i>
                        </span>
                        <div class="absolute inset-0 bg-linear-to-r from-clinic-teal to-clinic-blue opacity-0 group-hover/btn:opacity-100 transition-opacity duration-500"></div>
                    </a>
                </div>
            </article>
            {% endfor %}
            
            <!-- Vision Card -->
            <div class="relative group h-full">
                <div class="absolute -inset-1 bg-linear-to-r from-clinic-teal to-clinic-blue rounded-[2.5rem] blur opacity-20 group-hover:opacity-40 transition duration-1000"></div>
                <div class="relative h-full bg-slate-900 rounded-[2rem] p-12 flex flex-col justify-center items-center text-center text-white overflow-hidden">
                    <div class="absolute -top-12 -right-12 w-32 h-32 bg-clinic-blue/10 rounded-full blur-2xl"></div>
                    
                    <div class="w-20 h-20 bg-white/5 backdrop-blur-xl rounded-2xl flex items-center justify-center mb-8 border border-white/10 shadow-inner group-hover:scale-110 group-hover:rotate-12 transition-all duration-500">
                        <i class="fas fa-terminal text-3xl text-clinic-blue"></i>
                    </div>
                    <h3 class="text-2xl font-bold mb-6 tracking-tight">Systematic Healing</h3>
                    <p class="text-gray-400 text-base mb-10 font-light leading-relaxed">
                        We are building tools that bridge the gap between clinical intuition and algorithmic precision.
                    </p>
                    <a href="mailto:dev@ryu.clinic" class="inline-flex items-center gap-3 text-clinic-blue hover:text-white font-bold text-sm tracking-widest uppercase transition-all group-hover:gap-5">
                        Initiate Collaboration <i class="fas fa-arrow-right"></i>
                    </a>
                </div>
            </div>
        </div>
    </div>
</section>
