---
layout: default
title: Patient Guides
permalink: /guides/
---

<section class="bg-clinic-dark text-white py-20 relative overflow-hidden">
    <div class="container mx-auto px-6 relative z-10 text-center">
        <span class="inline-block px-3 py-1 mb-4 text-xs font-bold tracking-widest uppercase bg-clinic-teal text-white rounded-full">
            Patient Resources
        </span>
        <h1 class="text-4xl md:text-5xl font-bold mb-6">Patient Guides</h1>
        <p class="text-xl max-w-2xl mx-auto text-gray-300">
            Comprehensive resources to help you understand your condition, manage recovery, and maximize treatment benefits.
        </p>
    </div>
</section>

<section class="py-20 bg-gray-50">
    <div class="container mx-auto px-6">
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
            {% for guide in site.guides %}
            <article class="bg-white rounded-xl shadow-md overflow-hidden hover:shadow-xl transition-shadow border border-gray-100 flex flex-col h-full group">
                <a href="{{ guide.url }}" class="h-40 bg-teal-50 relative overflow-hidden flex items-center justify-center group-hover:bg-teal-100 transition-colors">
                    <div class="text-clinic-teal opacity-40 group-hover:opacity-60 transition-opacity transform group-hover:scale-110 duration-500">
                         <i class="fas fa-book-medical text-5xl"></i>
                    </div>
                    <div class="absolute top-3 right-3">
                         <span class="px-2 py-0.5 text-[10px] font-bold rounded bg-white/90 backdrop-blur-sm shadow-sm text-clinic-blue uppercase tracking-wide">
                            Guide
                        </span>
                    </div>
                </a>
                
                <div class="p-5 flex-1 flex flex-col">
                    <h3 class="text-lg font-bold text-gray-900 mb-2 group-hover:text-clinic-teal transition-colors leading-tight">
                        <a href="{{ guide.url }}">{{ guide.title }}</a>
                    </h3>
                    <p class="text-gray-600 text-xs mb-4 flex-1 line-clamp-3 leading-relaxed">
                        {{ guide.excerpt | strip_html }}
                    </p>
                    
                    <a href="{{ guide.url }}" class="block text-center w-full py-1.5 border border-gray-200 rounded-lg hover:bg-clinic-teal hover:text-white hover:border-clinic-teal text-xs font-semibold transition-all">
                        Read Guide
                    </a>
                </div>
            </article>
            {% endfor %}
            
            <!-- Book Appointment Card -->
            <div class="bg-clinic-dark rounded-xl shadow-md overflow-hidden p-8 flex flex-col justify-center items-center text-center text-white">
                <div class="w-16 h-16 bg-white/10 rounded-full flex items-center justify-center mb-6">
                    <i class="far fa-calendar-check text-2xl text-clinic-teal"></i>
                </div>
                <h3 class="text-xl font-bold mb-4">Need Personal Advice?</h3>
                <p class="text-gray-300 text-sm mb-6">
                    Every patient is unique. Book a consultation to discuss your specific needs with Dr. Ryu.
                </p>
                <a href="/booking/" class="text-clinic-teal hover:text-white font-medium text-sm transition-colors border border-clinic-teal hover:bg-clinic-teal px-6 py-2 rounded-lg">
                    Book Appointment &rarr;
                </a>
            </div>
        </div>
    </div>
</section>
