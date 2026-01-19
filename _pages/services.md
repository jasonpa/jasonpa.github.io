---
layout: default
title: Clinical Services
permalink: /services/
---

<section class="relative py-32 overflow-hidden">
    <div class="absolute inset-0 z-0">
        <img src="/assets/images/hero_tcm_tech_blend.png" alt="Clinical Services" class="w-full h-full object-cover">
        <div class="absolute inset-0 bg-linear-to-b from-clinic-dark/80 via-clinic-dark/70 to-clinic-dark/90 backdrop-blur-sm"></div>
    </div>
    <div class="container mx-auto px-6 relative z-10 text-center">
        <span class="text-teal-400 font-bold tracking-[0.3em] uppercase text-xs mb-6 block animate-fade-in">Precision Medicine</span>
        <h1 class="text-5xl md:text-7xl font-extrabold text-white mb-8 tracking-tight animate-fade-in-up">Clinical Services</h1>
        <p class="text-xl md:text-2xl max-w-2xl mx-auto text-gray-300 font-light leading-relaxed animate-fade-in-up delay-100">
            Comprehensive care merging Ancient Wisdom, <span class="text-white font-medium">Acupuncture</span>, and <span class="text-white font-medium">Modern Data Analytics</span>.
        </p>
    </div>
</section>

<section class="py-32 section-gradient">
    <div class="container mx-auto px-6">
        <div class="grid grid-cols-1 md:grid-cols-2 gap-10">
            {% for service in site.data.services %}
            <div class="glass-card group flex flex-col md:flex-row gap-8 hover:border-clinic-teal/30 transition-all duration-500">
                <div class="w-16 h-16 shrink-0 bg-teal-50 text-clinic-teal rounded-2xl flex items-center justify-center text-3xl group-hover:bg-clinic-teal group-hover:text-white transition-all duration-500 shadow-inner">
                    <i class="{{ service.icon }}"></i>
                </div>
                <div>
                    <h3 class="text-2xl font-bold text-clinic-dark mb-4 group-hover:text-clinic-teal transition-colors">{{ service.name }}</h3>
                    <p class="text-gray-600 leading-relaxed mb-6 text-lg">{{ service.description }}</p>
                    <div class="flex items-center text-clinic-blue font-bold text-sm tracking-wide">
                        Learn More <i class="fas fa-chevron-right ml-2 group-hover:translate-x-1 transition-transform"></i>
                    </div>
                </div>
            </div>
            {% endfor %}
        </div>
        
        <div class="mt-32 relative group">
             <div class="absolute -inset-1 bg-linear-to-r from-clinic-teal to-clinic-blue rounded-[2.5rem] blur opacity-20 group-hover:opacity-40 transition duration-1000"></div>
             <div class="relative bg-white/80 backdrop-blur-2xl rounded-[2rem] p-12 md:p-20 text-center border border-white/40 shadow-glass">
                 <h2 class="text-4xl md:text-5xl font-bold text-clinic-dark mb-8 tracking-tight">Ready to optimize your health?</h2>
                 <p class="text-xl text-gray-500 mb-12 font-light max-w-2xl mx-auto">
                     Join hundreds of patients who have transformed their recovery through our unique analytical approach. 
                     Direct billing available.
                 </p>
                 <a href="/booking/" class="btn-primary transform hover:scale-110 !px-12 !py-5 text-xl">
                     Book Your Session Now
                 </a>
             </div>
        </div>
    </div>
</section>
