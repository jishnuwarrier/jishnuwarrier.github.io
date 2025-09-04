---
layout: page
permalink: /projects/
title: Projects
description: ""
nav: true
nav_order: 3
---

<h2 style="font-size: 1.8rem; font-weight: 600; color: var(--global-theme-color); margin-top: 1rem; margin-bottom: 1.0rem;">SpotifyBuddies: Organic Playlist Recommender</h2>
<p style="margin-bottom: 0.5rem; font-weight: 500; color: #666;">Jan 2025 – May 2025 &nbsp;·&nbsp; <a href="https://github.com/jishnuwarrier/MLOps_G47_SpotifyBuddies" target="_blank">GitHub</a></p>
<ul style="margin-left: 1.5rem; margin-bottom: 2rem;">
  <li style="margin-bottom: 0.8rem;">Built a 40 GB data-prep pipeline (Pandas + SciPy sparse) that merged Million Playlist and Echo Nest datasets, computed <strong>100M+</strong> user–playlist overlaps in minutes, and produced <strong>20M</strong> contrastive triplets for model training.</li>
  <li style="margin-bottom: 0.8rem;">Implemented a FastAPI micro-service (multi-stage Docker, <code>uv</code> installer) delivering <strong>1000-user batch recommendations &lt; 300ms on CPU</strong>, shrinking image size 6GB → 2GB and build time by <strong>85%</strong>.</li>
  <li style="margin-bottom: 0.8rem;"><strong>Deployed an end-to-end MLOps pipeline on Chameleon Cloud</strong> with Terraform &amp; Ansible: Kubernetes for orchestration, MLflow + MinIO for experiment tracking, Airflow DAGs for scheduled retraining, and Prometheus/Grafana dashboards for real-time latency, throughput, and cold-start drift.</li>
</ul>

<h2 style="font-size: 1.8rem; font-weight: 600; color: var(--global-theme-color); margin-top: 2rem; margin-bottom: 1.0rem;">EfficientDebates: Pruning‑Based Multi‑Agent Reasoning with Small LLMs</h2>
<p style="margin-bottom: 0.5rem; font-weight: 500; color: #666;">Feb 2025 – May 2025 &nbsp;·&nbsp; <a href="https://github.com/jishnuwarrier/Multi-agent-debate" target="_blank">GitHub</a></p>
<ul style="margin-left: 1.5rem; margin-bottom: 2rem;">
  <li style="margin-bottom: 0.8rem;">Designed an adaptive pruning-based multi-agent debate protocol that boosts reasoning accuracy of small LLMs (LLaMA 3B/8B, Phi 3 Mini) on GSM8K to <strong>90.3%</strong>, rivaling LLaMA 70B while reducing compute cost by <strong>4.3x</strong>.</li>
  <li style="margin-bottom: 0.8rem;">Reduced average inference to <strong>3.27 LLM calls</strong> per sample by asynchronously triggering debates only when agents disagree, avoiding unnecessary debating rounds in <strong>92%</strong> of cases.</li>
  <li style="margin-bottom: 0.8rem;">Benchmarked against Self-Consistency baselines, demonstrating that model diversity and early-exit gating lead to cost-efficient accuracy improvements in multi-step reasoning.</li>
</ul>

<h2 style="font-size: 1.8rem; font-weight: 600; color: var(--global-theme-color); margin-top: 2rem; margin-bottom: 1.0rem;">License Plate Recognition</h2>
<p style="margin-bottom: 0.5rem; font-weight: 500; color: #666;">Jan 2022 – May 2022</p>
<ul style="margin-left: 1.5rem; margin-bottom: 2rem;">
  <li style="margin-bottom: 0.8rem;">Curated and pre-processed a custom dataset of Indian license-plate images; applied augmentation and OpenCV transforms to handle diverse lighting and viewing angles.</li>
  <li style="margin-bottom: 0.8rem;">Built a <strong>YOLOv5</strong> detector plus contour-based character segmentation and CNN OCR, topped with a novel rule-based state-code auto-correction layer that significantly boosted end-to-end accuracy.</li>
</ul>
