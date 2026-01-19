---
layout: default
title: Patient Guides
permalink: /guides/
---

<section class="relative py-32 overflow-hidden">
    <div class="absolute inset-0 z-0">
        <img src="/assets/images/hero_tcm_tech_blend.png" alt="Patient Guides" class="w-full h-full object-cover">
        <div class="absolute inset-0 bg-linear-to-b from-clinic-dark/95 via-clinic-dark/85 to-clinic-dark/95 backdrop-blur-sm"></div>
    </div>
    
    <!-- Abstract tech background elements -->
    <div class="absolute inset-0 z-0 opacity-20 pointer-events-none">
        <div class="absolute top-1/4 right-1/4 w-96 h-96 bg-clinic-blue rounded-full blur-[120px]"></div>
        <div class="absolute bottom-1/4 left-1/4 w-96 h-96 bg-clinic-teal rounded-full blur-[120px]"></div>
    </div>

    <div class="container mx-auto px-6 relative z-10 text-center">
        <span class="inline-block px-4 py-1.5 mb-6 text-xs font-bold tracking-[0.3em] uppercase bg-clinic-teal/10 text-clinic-teal border border-clinic-teal/20 backdrop-blur-md rounded-full animate-fade-in">
            Patient Resources
        </span>
        <h1 class="text-5xl md:text-7xl font-extrabold text-white mb-8 tracking-tight animate-fade-in-up">Patient Guides</h1>
        <p class="text-xl md:text-2xl max-w-2xl mx-auto text-gray-300 font-light leading-relaxed animate-fade-in-up delay-100">
            Expert resources to empower your recovery journey and <span class="text-white font-medium">optimize your health</span>.
        </p>
    </div>
</section>

<section class="py-32 section-gradient">
    <div class="container mx-auto px-6">
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-10">
            
            {% comment %} Define Categories {% endcomment %}
            {% assign categories = "ICBC & Car Accident Recovery|10|20,Extended Health Benefits|20|30,Office & Workplace Pain|30|40,Sports & Active Lifestyle|40|50,Chronic Pain & Conditions|50|70,Our Approach & First Visit|70|80,Locations & Booking|80|90" | split: "," %}

            {% for cat in categories %}
                {% assign parts = cat | split: "|" %}
                {% assign title = parts[0] %}
                {% assign start = parts[1] | plus: 0 %}
                {% assign end = parts[2] | plus: 0 %}
                {% assign category_guides = site.guides | where_exp: "g", "g.order >= start" | where_exp: "g", "g.order < end" | sort: "order" %}
                
                {% if category_guides.size > 0 %}
                <article class="glass-card group !p-0 overflow-hidden hover:border-clinic-teal/40 transition-all duration-500 h-full flex flex-col shadow-2xl">
                    <div class="h-56 bg-slate-900 relative overflow-hidden group flex items-center justify-center p-10 text-center">
                        <div class="absolute inset-0 flex items-center justify-center text-clinic-teal/10 group-hover:text-clinic-teal/20 transition-all transform group-hover:scale-110 duration-1000">
                             <i class="fas {% if title contains 'ICBC' %}fa-car-crash{% elsif title contains 'Benefits' %}fa-file-invoice-dollar{% elsif title contains 'Office' %}fa-laptop-medical{% elsif title contains 'Sports' %}fa-running{% elsif title contains 'Chronic' %}fa-pills{% elsif title contains 'Approach' %}fa-user-nurse{% else %}fa-map-marker-alt{% endif %} text-9xl"></i>
                        </div>
                        
                        <div class="absolute top-6 right-6">
                             <span class="px-3 py-1 text-[10px] font-bold rounded-full bg-white/10 backdrop-blur-md border border-white/20 text-white uppercase tracking-widest">
                                Category
                            </span>
                        </div>
                        <div class="absolute inset-0 bg-linear-to-t from-clinic-dark/60 via-transparent to-transparent"></div>
                        
                        <h2 class="relative z-10 text-white font-bold text-2xl tracking-tight leading-tight group-hover:scale-105 transition-transform duration-500">{{ title }}</h2>
                    </div>
                    
                    <div class="p-8 md:p-10 flex-1 flex flex-col">
                        <ul class="space-y-4 mb-10 flex-1">
                            {% for guide in category_guides %}
                            <li class="flex items-start gap-3 group/item">
                                <i class="fas fa-chevron-right text-[10px] text-clinic-teal mt-1.5 group-hover/item:translate-x-1 transition-transform"></i>
                                <a href="{{ guide.url }}" class="text-gray-600 hover:text-clinic-teal transition-colors text-sm font-medium leading-relaxed">
                                    {{ guide.nav_title | default: guide.title }}
                                </a>
                            </li>
                            {% endfor %}
                        </ul>
                        
                        <a href="{{ category_guides.first.url }}" class="group/btn relative inline-flex items-center justify-center w-full py-4 bg-clinic-dark rounded-2xl text-white text-sm font-bold transition-all overflow-hidden">
                            <span class="relative z-10 flex items-center gap-3">
                                Explore Guides <i class="fas fa-arrow-right text-xs group-hover/btn:translate-x-1 transition-transform"></i>
                            </span>
                            <div class="absolute inset-0 bg-linear-to-r from-clinic-teal to-clinic-blue opacity-0 group-hover/btn:opacity-100 transition-opacity duration-500"></div>
                        </a>
                    </div>
                </article>
                {% endif %}
            {% endfor %}

            <!-- Book Appointment Card -->
            <div class="relative group h-full">
                <div class="absolute -inset-1 bg-linear-to-r from-clinic-teal to-clinic-blue rounded-[2.5rem] blur opacity-20 group-hover:opacity-40 transition duration-1000"></div>
                <div class="relative h-full bg-slate-900 rounded-[2rem] p-12 flex flex-col justify-center items-center text-center text-white overflow-hidden shadow-2xl">
                    <div class="absolute -top-12 -right-12 w-32 h-32 bg-clinic-teal/10 rounded-full blur-2xl"></div>
                    
                    <div class="w-20 h-20 bg-white/5 backdrop-blur-xl rounded-2xl flex items-center justify-center mb-8 border border-white/10 shadow-inner group-hover:scale-110 group-hover:rotate-12 transition-all duration-500">
                        <i class="far fa-calendar-check text-3xl text-teal-300"></i>
                    </div>
                    <h3 class="text-2xl font-bold mb-6 tracking-tight leading-tight">Need Personal Advice?</h3>
                    <p class="text-gray-400 text-base mb-10 font-light leading-relaxed">
                        Every recovery path is unique. Schedule a consultation to architect your specific health plan.
                    </p>
                    <a href="/booking/" class="btn-primary !bg-white !text-clinic-dark !px-10 !py-4 hover:scale-105 transition-transform shadow-lg shadow-white/5">
                        Book Appointment
                    </a>
                </div>
            </div>
        </div>
    </div>
</section>
