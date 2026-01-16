---
layout: default
title: Clinical Services
permalink: /services/
---

<section class="bg-clinic-teal text-white py-20">
    <div class="container mx-auto px-6 text-center">
        <h1 class="text-4xl md:text-5xl font-bold mb-6">Clinical Services</h1>
        <p class="text-xl max-w-2xl mx-auto opacity-90">
            Comprehensive care combining acupuncture, herbal medicine, and modern structural alignment techniques.
        </p>
    </div>
</section>

<section class="py-20">
    <div class="container mx-auto px-6">
        <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
            {% for service in site.data.services %}
            <div class="bg-white p-8 rounded-xl shadow-lg hover:shadow-xl transition-shadow border border-gray-100 flex gap-6">
                <div class="w-16 h-16 shrink-0 bg-teal-50 text-clinic-teal rounded-full flex items-center justify-center text-2xl">
                    <i class="{{ service.icon }}"></i>
                </div>
                <div>
                    <h3 class="text-2xl font-bold text-gray-900 mb-3">{{ service.name }}</h3>
                    <p class="text-gray-600 leading-relaxed mb-4">{{ service.description }}</p>
                </div>
            </div>
            {% endfor %}
        </div>
        
        <div class="mt-20 bg-gray-50 rounded-2xl p-8 md:p-12 text-center">
             <h2 class="text-3xl font-bold text-gray-900 mb-6">Ready to optimize your health?</h2>
             <p class="text-lg text-gray-600 mb-8">
                 Booking is easy with our online system. Direct billing is available for most major insurance providers.
             </p>
             <a href="/booking/" class="btn-primary inline-flex items-center gap-2">
                 Book Appointment Now <i class="fas fa-arrow-right"></i>
             </a>
        </div>
    </div>
</section>
