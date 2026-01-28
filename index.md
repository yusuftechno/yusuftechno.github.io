---
layout: default
title: Beranda
---

<div class="text-center py-5">
    <h2 class="display-4 fw-bold">Wellcome Yusuf Techno</h2>
    <p class="lead text-muted">Website ini berisikan semua dokumentasi saya. dan jika ada pertanyaan, silahkan menuju ke halaman contact saya.</p>
</div>

<div class="row g-4 justify-content-center">
    {% assign docs = site.docs | sort: 'konten' %}
    {% for doc in docs %}
    <div class="col-md-6 col-lg-4">
        <div class="card h-100 shadow-sm border-0 transition-hover">
            <div class="card-body p-4 text-center">
                <div class="bg-primary bg-opacity-10 text-primary rounded-circle d-inline-flex align-items-center justify-content-center mb-3" style="width: 60px; height: 60px;">
                    <span class="fs-3 fw-bold">{{ forloop.index }}</span>
                </div>
                <h4 class="card-title fw-bold">{{ doc.title }}</h4>
                <p class="card-text text-muted small">
                    Simak lebih lanjut "{{ doc.title | downcase }}" dengan menekan tombol dibawah ini.
                </p>
            </div>
            <div class="card-footer bg-transparent border-0 pb-4 text-center">
                <a href="{{ doc.url | relative_url }}" class="btn btn-outline-primary px-4 rounded-pill">Buka Dokumen</a>
            </div>
        </div>
    </div>
    {% endfor %}
</div>

<style>
.transition-hover {
    transition: transform 0.3s ease, box-shadow 0.3s ease;
}
.transition-hover:hover {
    transform: translateY(-10px);
    box-shadow: 0 10px 20px rgba(0,0,0,0.1) !important;
}
</style>
