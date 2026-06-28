# Partnership
Those who supports
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>EHEPS · Google for Startups</title>
  <!-- Font Awesome for icons (clean, free) -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: #f4f7fc;
      font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
      padding: 2rem 1.5rem;
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      color: #1e293b;
    }

    /* card – mimics a support case / announcement panel */
    .case-card {
      max-width: 1100px;
      width: 100%;
      background: #ffffff;
      border-radius: 28px;
      box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.15);
      overflow: hidden;
      transition: all 0.2s ease;
      border: 1px solid rgba(66, 133, 244, 0.08);
    }

    /* header with google-inspired accent */
    .case-header {
      padding: 1.8rem 2.2rem 1.2rem 2.2rem;
      background: linear-gradient(145deg, #fafcff 0%, #ffffff 100%);
      border-bottom: 1px solid #eef2f6;
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      align-items: center;
    }

    .case-header h1 {
      font-size: 1.7rem;
      font-weight: 600;
      letter-spacing: -0.02em;
      background: linear-gradient(135deg, #1a2639, #2c3e66);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      display: flex;
      align-items: center;
      gap: 0.6rem;
      flex-wrap: wrap;
    }

    .case-header h1 i {
      background: #4285f4;
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      font-size: 1.8rem;
    }

    .meta-badge {
      display: flex;
      gap: 1.2rem;
      align-items: center;
      flex-wrap: wrap;
    }

    .badge-google {
      background: #e8f0fe;
      color: #1a73e8;
      font-weight: 500;
      padding: 0.35rem 1rem;
      border-radius: 40px;
      font-size: 0.8rem;
      letter-spacing: 0.3px;
      border: 1px solid #d2e3fc;
      display: inline-flex;
      align-items: center;
      gap: 6px;
    }

    .badge-google i {
      font-size: 0.9rem;
    }

    .case-meta-info {
      padding: 0.5rem 2.2rem 1.2rem 2.2rem;
      background: #f9fbfd;
      display: flex;
      flex-wrap: wrap;
      gap: 1.2rem 2.5rem;
      border-bottom: 1px solid #edf2f7;
      font-size: 0.9rem;
      color: #3b4a5e;
    }

    .case-meta-info span {
      display: flex;
      align-items: center;
      gap: 8px;
    }

    .case-meta-info i {
      color: #5f7a9a;
      width: 1.1rem;
      font-size: 0.95rem;
    }

    .case-meta-info .highlight {
      color: #0b2b4c;
      font-weight: 500;
    }

    .case-body {
      padding: 2rem 2.2rem 2.5rem 2.2rem;
    }

    /* grid: overview + details */
    .overview-grid {
      display: grid;
      grid-template-columns: 1.2fr 2.2fr;
      gap: 2rem;
      margin-bottom: 2.2rem;
    }

    @media (max-width: 750px) {
      .overview-grid {
        grid-template-columns: 1fr;
        gap: 1.5rem;
      }
      .case-header {
        flex-direction: column;
        align-items: flex-start;
        gap: 0.8rem;
      }
      .case-meta-info {
        flex-direction: column;
        gap: 0.5rem;
      }
    }

    .issue-block {
      background: #f8faff;
      padding: 1.4rem 1.6rem;
      border-radius: 20px;
      border: 1px solid #eaf0f8;
    }

    .issue-block .label {
      font-size: 0.7rem;
      text-transform: uppercase;
      letter-spacing: 0.6px;
      color: #5c7392;
      font-weight: 600;
    }

    .issue-block .value {
      font-weight: 500;
      margin-top: 0.25rem;
      font-size: 1rem;
      display: flex;
      flex-wrap: wrap;
      align-items: baseline;
      gap: 8px;
    }

    .issue-block .value .status-new {
      background: #d4edda;
      color: #0b5e2e;
      font-size: 0.7rem;
      font-weight: 600;
      padding: 0.15rem 0.8rem;
      border-radius: 40px;
      letter-spacing: 0.3px;
    }

    .category-tag {
      background: #e6edf8;
      padding: 0.2rem 1rem;
      border-radius: 30px;
      font-size: 0.75rem;
      font-weight: 500;
      color: #1e3a6b;
      display: inline-block;
    }

    .case-description {
      margin-top: 0.5rem;
      line-height: 1.6;
      color: #1f2a3f;
    }

    .case-description strong {
      color: #0b2b4c;
    }

    /* announcement rich content */
    .announcement-content {
      background: #fbfdff;
      padding: 1.6rem 1.8rem;
      border-radius: 24px;
      border: 1px solid #eaf0f8;
      margin-top: 1.8rem;
    }

    .announcement-content h2 {
      font-size: 1.3rem;
      font-weight: 600;
      letter-spacing: -0.3px;
      display: flex;
      align-items: center;
      gap: 10px;
      color: #0a1c31;
      margin-bottom: 0.75rem;
    }

    .announcement-content h2 i {
      color: #4285f4;
      font-size: 1.5rem;
    }

    .announcement-content p {
      margin: 1rem 0;
      line-height: 1.7;
    }

    .highlight-box {
      background: #f0f6ff;
      padding: 1.2rem 1.6rem;
      border-radius: 18px;
      border-left: 4px solid #4285f4;
      margin: 1.5rem 0 1rem 0;
    }

    .highlight-box strong {
      color: #0e2a4b;
    }

    .two-col-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 1.5rem;
      margin: 1.2rem 0 0.5rem 0;
    }

    @media (max-width: 600px) {
      .two-col-grid {
        grid-template-columns: 1fr;
        gap: 0.8rem;
      }
    }

    .support-item {
      background: white;
      border-radius: 16px;
      padding: 0.9rem 1.2rem;
      box-shadow: 0 2px 6px rgba(0,20,40,0.03);
      border: 1px solid #e3ecf7;
      display: flex;
      align-items: center;
      gap: 14px;
    }

    .support-item i {
      color: #4285f4;
      font-size: 1.3rem;
      width: 2rem;
      text-align: center;
    }

    .support-item .info {
      font-size: 0.95rem;
    }

    .support-item .info .tag {
      font-weight: 600;
      color: #0b2b4c;
      display: block;
    }

    .support-item .info .sub {
      font-size: 0.8rem;
      color: #4d688b;
    }

    .footer-meta {
      margin-top: 2rem;
      padding-top: 1rem;
      border-top: 1px solid #e9eff5;
      font-size: 0.8rem;
      color: #4d688b;
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      align-items: center;
    }

    .footer-meta i {
      margin-right: 4px;
      color: #5f7a9a;
    }

    .btn-google {
      background: #1a73e8;
      color: white;
      border: none;
      border-radius: 40px;
      padding: 0.4rem 1.2rem;
      font-weight: 500;
      font-size: 0.8rem;
      display: inline-flex;
      align-items: center;
      gap: 8px;
      cursor: default;
      opacity: 0.9;
    }

    .tag-all-softwares {
      background: #e6f0fa;
      border-radius: 40px;
      padding: 0.2rem 1rem 0.2rem 0.8rem;
      display: inline-flex;
      align-items: center;
      gap: 4px;
      font-size: 0.7rem;
      font-weight: 500;
      color: #1a4b7a;
      border: 1px solid #c5d9f0;
      margin-left: 0.5rem;
    }

    .tag-all-softwares i {
      font-size: 0.7rem;
      color: #1a73e8;
    }

    /* small tweaks */
    .text-google-blue {
      color: #1a73e8;
    }
    .fw-500 { font-weight: 500; }
    .mt-1 { margin-top: 0.5rem; }
    .mb-1 { margin-bottom: 0.5rem; }
  </style>
</head>
<body>

<div class="case-card">

  <!-- Header: case title + Google badge -->
  <div class="case-header">
    <h1>
      <i class="fas fa-bullhorn"></i> 
      Announcement: EHEPS Secures Strategic Partnership with Google for Startups
      <span class="tag-all-softwares">
        <i class="fas fa-tag"></i> Google · all softwares
      </span>
    </h1>
    <div class="meta-badge">
      <span class="badge-google"><i class="fab fa-google"></i> Google for Startups</span>
      <span class="badge-google" style="background:#e6f0fa; color:#0d3b6b;"><i class="fas fa-check-circle"></i> Scale Tier</span>
    </div>
  </div>

  <!-- Meta info row -->
  <div class="case-meta-info">
    <span><i class="fas fa-user-circle"></i> Created by <span class="highlight">Mohammad ewaz Nazari</span> &lt;executive@eheps.com&gt;</span>
    <span><i class="fas fa-building"></i> EHEPS organization</span>
    <span><i class="fas fa-calendar-alt"></i> Jun 28, 2026, 3:57:48 PM</span>
    <span><i class="fas fa-hashtag"></i> Case 72734924</span>
  </div>

  <!-- BODY -->
  <div class="case-body">

    <!-- overview grid: issue type & category -->
    <div class="overview-grid">
      <div class="issue-block">
        <div class="label"><i class="fas fa-tasks"></i> Issue type</div>
        <div class="value">Licensing Specialist (Ordering) <span class="status-new"><i class="fas fa-circle" style="font-size: 0.5rem; vertical-align: middle; margin-right: 4px;"></i> New</span></div>
        <div class="label" style="margin-top: 1rem;"><i class="fas fa-building"></i> Company with issue</div>
        <div class="value">EHEPS organization</div>
      </div>
      <div class="issue-block">
        <div class="label"><i class="fas fa-pen-fancy"></i> Case title</div>
        <div class="value" style="font-weight: 600;">Announcement: EHEPS Secures Strategic Partnership with Google for Startups <span style="font-weight:400; color:#3d5c7c; font-size:0.8rem; margin-left:6px;">74 / 140</span></div>
        <div class="label" style="margin-top: 1rem;"><i class="fas fa-folder-open"></i> Category</div>
        <div class="value"><span class="category-tag"><i class="fab fa-google"></i> Google Workspace for Education Licensing Specialist</span></div>
        <div style="margin-top: 0.5rem;"><span class="category-tag" style="background:#eef3fa;"><i class="fas fa-globe"></i> English</span></div>
      </div>
    </div>

    <!-- Case description (original) -->
    <div class="case-description">
      <p><strong><i class="fas fa-quote-left" style="color:#4285f4; margin-right:4px;"></i> Case description</strong></p>
      <p style="margin-top: 0.2rem; background: #f6faff; padding: 0.8rem 1.2rem; border-radius: 16px; border:1px solid #e3edf8;">
        We are thrilled to announce that EHEPS has officially joined the Google for Startups Cloud Program (Scale Tier). 
        This partnership marks a significant milestone in our mission to integrate Education, Humanitarian Relief, and Environmental Sustainability.
      </p>
    </div>

    <!-- ============ ANNOUNCEMENT CONTENT (full rich text) ============= -->
    <div class="announcement-content">
      <h2><i class="fas fa-handshake"></i> EHEPS · Google for Startups (Scale Tier)</h2>
      
      <p><strong>EHEPS</strong> has officially joined the <strong>Google for Startups Cloud Program (Scale Tier)</strong>. This partnership accelerates our ability to deliver data-driven logistics, predictive modeling for climate‑driven displacement, and scalable digital education in vulnerable regions.</p>
      
      <div class="highlight-box">
        <i class="fas fa-rocket" style="color:#4285f4; margin-right:10px;"></i> <strong>Scale Tier access</strong> — comprehensive resources to scale our technical capabilities and impact.
      </div>

      <!-- Financial & Technical Support -->
      <h3 style="font-size: 1.05rem; margin: 1.2rem 0 0.6rem 0; display: flex; align-items: center; gap: 8px;"><i class="fas fa-coins" style="color:#1a73e8;"></i> Financial & Technical Support</h3>
      <div class="two-col-grid">
        <div class="support-item"><i class="fas fa-cloud-upload-alt"></i><div class="info"><span class="tag">Google Cloud Credits</span><span class="sub">Up to $200,000 over 2 years</span></div></div>
        <div class="support-item"><i class="fas fa-microchip"></i><div class="info"><span class="tag">AI‑Specific Acceleration</span><span class="sub">$150,000 in credits for Vertex AI</span></div></div>
        <div class="support-item"><i class="fas fa-headset"></i><div class="info"><span class="tag">Enhanced Support</span><span class="sub">$12,000 credits · “Hub in a Box”</span></div></div>
        <div class="support-item"><i class="fas fa-map-marked-alt"></i><div class="info"><span class="tag">Google Maps Platform</span><span class="sub">$600 monthly in credits</span></div></div>
      </div>

      <!-- Operational & Educational -->
      <h3 style="font-size: 1.05rem; margin: 1.5rem 0 0.6rem 0; display: flex; align-items: center; gap: 8px;"><i class="fas fa-graduation-cap" style="color:#1a73e8;"></i> Operational & Educational Benefits</h3>
      <div class="two-col-grid">
        <div class="support-item"><i class="fas fa-envelope"></i><div class="info"><span class="tag">Google Workspace</span><span class="sub">12 months free · Business Plus</span></div></div>
        <div class="support-item"><i class="fas fa-user-graduate"></i><div class="info"><span class="tag">Professional Development</span><span class="sub">$500 in Google Skills credits</span></div></div>
        <div class="support-item"><i class="fas fa-cube"></i><div class="info"><span class="tag">Innovation Ecosystem</span><span class="sub">Web3 Program · success manager</span></div></div>
        <div class="support-item"><i class="fas fa-hand-holding-heart"></i><div class="info"><span class="tag">Dedicated business support</span><span class="sub">from a success manager</span></div></div>
      </div>

      <!-- Looking ahead -->
      <div style="margin-top: 1.8rem; background: #eef5fe; padding: 1rem 1.6rem; border-radius: 20px;">
        <p style="font-weight: 500; display: flex; gap: 10px; align-items: center;"><i class="fas fa-binoculars" style="color:#1a73e8;"></i> <span>Looking Ahead</span></p>
        <p style="margin: 0.3rem 0 0 0; line-height:1.6;">This partnership allows EHEPS to move beyond reactive aid, utilizing Google Cloud to predict humanitarian needs and pre‑position resources effectively. We are grateful for this opportunity to collaborate with Google as we build resilient, tech‑driven solutions for climate‑stressed communities.</p>
      </div>

      <!-- footer with tags: all Google softwares mentioned -->
      <div style="margin-top: 1.8rem; display: flex; flex-wrap: wrap; gap: 8px 12px; align-items: center; border-top: 1px dashed #d6e3f0; padding-top: 1.2rem;">
        <span style="font-weight:500; font-size:0.8rem; color:#1b3b5e;"><i class="fas fa-tags"></i> Google softwares tagged:</span>
        <span class="badge-google" style="background:#e3edf7;"><i class="fab fa-google"></i> Google Cloud</span>
        <span class="badge-google" style="background:#e3edf7;"><i class="fas fa-brain"></i> Vertex AI</span>
        <span class="badge-google" style="background:#e3edf7;"><i class="fas fa-map"></i> Google Maps Platform</span>
        <span class="badge-google" style="background:#e3edf7;"><i class="fas fa-users"></i> Google Workspace</span>
        <span class="badge-google" style="background:#e3edf7;"><i class="fas fa-code"></i> Web3 Program</span>
        <span class="badge-google" style="background:#e3edf7;"><i class="fas fa-chart-line"></i> AI-first</span>
      </div>

      <!-- footer meta: all cases / settings / home -->
      <div class="footer-meta">
        <div>
          <i class="fas fa-home"></i> Home · <i class="fas fa-list-ul"></i> All cases · <i class="fas fa-cog"></i> Settings
        </div>
        <div>
          <span class="btn-google"><i class="fab fa-google"></i> Case 72734924</span>
          <span style="margin-left: 1rem;"><i class="far fa-clock"></i> updated Jun 28, 2026</span>
        </div>
      </div>

    </div> <!-- end announcement-content -->
  </div> <!-- end case-body -->
</div> <!-- end case-card -->

</body>
</html>.. 
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>EHEPS · Google for Startups</title>
  <!-- Font Awesome for icons (clean, free) -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: #f4f7fc;
      font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
      padding: 2rem 1.5rem;
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      color: #1e293b;
    }

    /* card – mimics a support case / announcement panel */
    .case-card {
      max-width: 1100px;
      width: 100%;
      background: #ffffff;
      border-radius: 28px;
      box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.15);
      overflow: hidden;
      transition: all 0.2s ease;
      border: 1px solid rgba(66, 133, 244, 0.08);
    }

    /* header with google-inspired accent */
    .case-header {
      padding: 1.8rem 2.2rem 1.2rem 2.2rem;
      background: linear-gradient(145deg, #fafcff 0%, #ffffff 100%);
      border-bottom: 1px solid #eef2f6;
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      align-items: center;
    }

    .case-header h1 {
      font-size: 1.7rem;
      font-weight: 600;
      letter-spacing: -0.02em;
      background: linear-gradient(135deg, #1a2639, #2c3e66);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      display: flex;
      align-items: center;
      gap: 0.6rem;
      flex-wrap: wrap;
    }

    .case-header h1 i {
      background: #4285f4;
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      font-size: 1.8rem;
    }

    .meta-badge {
      display: flex;
      gap: 1.2rem;
      align-items: center;
      flex-wrap: wrap;
    }

    .badge-google {
      background: #e8f0fe;
      color: #1a73e8;
      font-weight: 500;
      padding: 0.35rem 1rem;
      border-radius: 40px;
      font-size: 0.8rem;
      letter-spacing: 0.3px;
      border: 1px solid #d2e3fc;
      display: inline-flex;
      align-items: center;
      gap: 6px;
    }

    .badge-google i {
      font-size: 0.9rem;
    }

    .case-meta-info {
      padding: 0.5rem 2.2rem 1.2rem 2.2rem;
      background: #f9fbfd;
      display: flex;
      flex-wrap: wrap;
      gap: 1.2rem 2.5rem;
      border-bottom: 1px solid #edf2f7;
      font-size: 0.9rem;
      color: #3b4a5e;
    }

    .case-meta-info span {
      display: flex;
      align-items: center;
      gap: 8px;
    }

    .case-meta-info i {
      color: #5f7a9a;
      width: 1.1rem;
      font-size: 0.95rem;
    }

    .case-meta-info .highlight {
      color: #0b2b4c;
      font-weight: 500;
    }

    .case-body {
      padding: 2rem 2.2rem 2.5rem 2.2rem;
    }

    /* grid: overview + details */
    .overview-grid {
      display: grid;
      grid-template-columns: 1.2fr 2.2fr;
      gap: 2rem;
      margin-bottom: 2.2rem;
    }

    @media (max-width: 750px) {
      .overview-grid {
        grid-template-columns: 1fr;
        gap: 1.5rem;
      }
      .case-header {
        flex-direction: column;
        align-items: flex-start;
        gap: 0.8rem;
      }
      .case-meta-info {
        flex-direction: column;
        gap: 0.5rem;
      }
    }

    .issue-block {
      background: #f8faff;
      padding: 1.4rem 1.6rem;
      border-radius: 20px;
      border: 1px solid #eaf0f8;
    }

    .issue-block .label {
      font-size: 0.7rem;
      text-transform: uppercase;
      letter-spacing: 0.6px;
      color: #5c7392;
      font-weight: 600;
    }

    .issue-block .value {
      font-weight: 500;
      margin-top: 0.25rem;
      font-size: 1rem;
      display: flex;
      flex-wrap: wrap;
      align-items: baseline;
      gap: 8px;
    }

    .issue-block .value .status-new {
      background: #d4edda;
      color: #0b5e2e;
      font-size: 0.7rem;
      font-weight: 600;
      padding: 0.15rem 0.8rem;
      border-radius: 40px;
      letter-spacing: 0.3px;
    }

    .category-tag {
      background: #e6edf8;
      padding: 0.2rem 1rem;
      border-radius: 30px;
      font-size: 0.75rem;
      font-weight: 500;
      color: #1e3a6b;
      display: inline-block;
    }

    .case-description {
      margin-top: 0.5rem;
      line-height: 1.6;
      color: #1f2a3f;
    }

    .case-description strong {
      color: #0b2b4c;
    }

    /* announcement rich content */
    .announcement-content {
      background: #fbfdff;
      padding: 1.6rem 1.8rem;
      border-radius: 24px;
      border: 1px solid #eaf0f8;
      margin-top: 1.8rem;
    }

    .announcement-content h2 {
      font-size: 1.3rem;
      font-weight: 600;
      letter-spacing: -0.3px;
      display: flex;
      align-items: center;
      gap: 10px;
      color: #0a1c31;
      margin-bottom: 0.75rem;
    }

    .announcement-content h2 i {
      color: #4285f4;
      font-size: 1.5rem;
    }

    .announcement-content p {
      margin: 1rem 0;
      line-height: 1.7;
    }

    .highlight-box {
      background: #f0f6ff;
      padding: 1.2rem 1.6rem;
      border-radius: 18px;
      border-left: 4px solid #4285f4;
      margin: 1.5rem 0 1rem 0;
    }

    .highlight-box strong {
      color: #0e2a4b;
    }

    .two-col-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 1.5rem;
      margin: 1.2rem 0 0.5rem 0;
    }

    @media (max-width: 600px) {
      .two-col-grid {
        grid-template-columns: 1fr;
        gap: 0.8rem;
      }
    }

    .support-item {
      background: white;
      border-radius: 16px;
      padding: 0.9rem 1.2rem;
      box-shadow: 0 2px 6px rgba(0,20,40,0.03);
      border: 1px solid #e3ecf7;
      display: flex;
      align-items: center;
      gap: 14px;
    }

    .support-item i {
      color: #4285f4;
      font-size: 1.3rem;
      width: 2rem;
      text-align: center;
    }

    .support-item .info {
      font-size: 0.95rem;
    }

    .support-item .info .tag {
      font-weight: 600;
      color: #0b2b4c;
      display: block;
    }

    .support-item .info .sub {
      font-size: 0.8rem;
      color: #4d688b;
    }

    .footer-meta {
      margin-top: 2rem;
      padding-top: 1rem;
      border-top: 1px solid #e9eff5;
      font-size: 0.8rem;
      color: #4d688b;
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      align-items: center;
    }

    .footer-meta i {
      margin-right: 4px;
      color: #5f7a9a;
    }

    .btn-google {
      background: #1a73e8;
      color: white;
      border: none;
      border-radius: 40px;
      padding: 0.4rem 1.2rem;
      font-weight: 500;
      font-size: 0.8rem;
      display: inline-flex;
      align-items: center;
      gap: 8px;
      cursor: default;
      opacity: 0.9;
    }

    .tag-all-softwares {
      background: #e6f0fa;
      border-radius: 40px;
      padding: 0.2rem 1rem 0.2rem 0.8rem;
      display: inline-flex;
      align-items: center;
      gap: 4px;
      font-size: 0.7rem;
      font-weight: 500;
      color: #1a4b7a;
      border: 1px solid #c5d9f0;
      margin-left: 0.5rem;
    }

    .tag-all-softwares i {
      font-size: 0.7rem;
      color: #1a73e8;
    }

    /* small tweaks */
    .text-google-blue {
      color: #1a73e8;
    }
    .fw-500 { font-weight: 500; }
    .mt-1 { margin-top: 0.5rem; }
    .mb-1 { margin-bottom: 0.5rem; }
  </style>
</head>
<body>

<div class="case-card">

  <!-- Header: case title + Google badge -->
  <div class="case-header">
    <h1>
      <i class="fas fa-bullhorn"></i> 
      Announcement: EHEPS Secures Strategic Partnership with Google for Startups
      <span class="tag-all-softwares">
        <i class="fas fa-tag"></i> Google · all softwares
      </span>
    </h1>
    <div class="meta-badge">
      <span class="badge-google"><i class="fab fa-google"></i> Google for Startups</span>
      <span class="badge-google" style="background:#e6f0fa; color:#0d3b6b;"><i class="fas fa-check-circle"></i> Scale Tier</span>
    </div>
  </div>

  <!-- Meta info row -->
  <div class="case-meta-info">
    <span><i class="fas fa-user-circle"></i> Created by <span class="highlight">Mohammad ewaz Nazari</span> &lt;executive@eheps.com&gt;</span>
    <span><i class="fas fa-building"></i> EHEPS organization</span>
    <span><i class="fas fa-calendar-alt"></i> Jun 28, 2026, 3:57:48 PM</span>
    <span><i class="fas fa-hashtag"></i> Case 72734924</span>
  </div>

  <!-- BODY -->
  <div class="case-body">

    <!-- overview grid: issue type & category -->
    <div class="overview-grid">
      <div class="issue-block">
        <div class="label"><i class="fas fa-tasks"></i> Issue type</div>
        <div class="value">Licensing Specialist (Ordering) <span class="status-new"><i class="fas fa-circle" style="font-size: 0.5rem; vertical-align: middle; margin-right: 4px;"></i> New</span></div>
        <div class="label" style="margin-top: 1rem;"><i class="fas fa-building"></i> Company with issue</div>
        <div class="value">EHEPS organization</div>
      </div>
      <div class="issue-block">
        <div class="label"><i class="fas fa-pen-fancy"></i> Case title</div>
        <div class="value" style="font-weight: 600;">Announcement: EHEPS Secures Strategic Partnership with Google for Startups <span style="font-weight:400; color:#3d5c7c; font-size:0.8rem; margin-left:6px;">74 / 140</span></div>
        <div class="label" style="margin-top: 1rem;"><i class="fas fa-folder-open"></i> Category</div>
        <div class="value"><span class="category-tag"><i class="fab fa-google"></i> Google Workspace for Education Licensing Specialist</span></div>
        <div style="margin-top: 0.5rem;"><span class="category-tag" style="background:#eef3fa;"><i class="fas fa-globe"></i> English</span></div>
      </div>
    </div>

    <!-- Case description (original) -->
    <div class="case-description">
      <p><strong><i class="fas fa-quote-left" style="color:#4285f4; margin-right:4px;"></i> Case description</strong></p>
      <p style="margin-top: 0.2rem; background: #f6faff; padding: 0.8rem 1.2rem; border-radius: 16px; border:1px solid #e3edf8;">
        We are thrilled to announce that EHEPS has officially joined the Google for Startups Cloud Program (Scale Tier). 
        This partnership marks a significant milestone in our mission to integrate Education, Humanitarian Relief, and Environmental Sustainability.
      </p>
    </div>

    <!-- ============ ANNOUNCEMENT CONTENT (full rich text) ============= -->
    <div class="announcement-content">
      <h2><i class="fas fa-handshake"></i> EHEPS · Google for Startups (Scale Tier)</h2>
      
      <p><strong>EHEPS</strong> has officially joined the <strong>Google for Startups Cloud Program (Scale Tier)</strong>. This partnership accelerates our ability to deliver data-driven logistics, predictive modeling for climate‑driven displacement, and scalable digital education in vulnerable regions.</p>
      
      <div class="highlight-box">
        <i class="fas fa-rocket" style="color:#4285f4; margin-right:10px;"></i> <strong>Scale Tier access</strong> — comprehensive resources to scale our technical capabilities and impact.
      </div>

      <!-- Financial & Technical Support -->
      <h3 style="font-size: 1.05rem; margin: 1.2rem 0 0.6rem 0; display: flex; align-items: center; gap: 8px;"><i class="fas fa-coins" style="color:#1a73e8;"></i> Financial & Technical Support</h3>
      <div class="two-col-grid">
        <div class="support-item"><i class="fas fa-cloud-upload-alt"></i><div class="info"><span class="tag">Google Cloud Credits</span><span class="sub">Up to $200,000 over 2 years</span></div></div>
        <div class="support-item"><i class="fas fa-microchip"></i><div class="info"><span class="tag">AI‑Specific Acceleration</span><span class="sub">$150,000 in credits for Vertex AI</span></div></div>
        <div class="support-item"><i class="fas fa-headset"></i><div class="info"><span class="tag">Enhanced Support</span><span class="sub">$12,000 credits · “Hub in a Box”</span></div></div>
        <div class="support-item"><i class="fas fa-map-marked-alt"></i><div class="info"><span class="tag">Google Maps Platform</span><span class="sub">$600 monthly in credits</span></div></div>
      </div>

      <!-- Operational & Educational -->
      <h3 style="font-size: 1.05rem; margin: 1.5rem 0 0.6rem 0; display: flex; align-items: center; gap: 8px;"><i class="fas fa-graduation-cap" style="color:#1a73e8;"></i> Operational & Educational Benefits</h3>
      <div class="two-col-grid">
        <div class="support-item"><i class="fas fa-envelope"></i><div class="info"><span class="tag">Google Workspace</span><span class="sub">12 months free · Business Plus</span></div></div>
        <div class="support-item"><i class="fas fa-user-graduate"></i><div class="info"><span class="tag">Professional Development</span><span class="sub">$500 in Google Skills credits</span></div></div>
        <div class="support-item"><i class="fas fa-cube"></i><div class="info"><span class="tag">Innovation Ecosystem</span><span class="sub">Web3 Program · success manager</span></div></div>
        <div class="support-item"><i class="fas fa-hand-holding-heart"></i><div class="info"><span class="tag">Dedicated business support</span><span class="sub">from a success manager</span></div></div>
      </div>

      <!-- Looking ahead -->
      <div style="margin-top: 1.8rem; background: #eef5fe; padding: 1rem 1.6rem; border-radius: 20px;">
        <p style="font-weight: 500; display: flex; gap: 10px; align-items: center;"><i class="fas fa-binoculars" style="color:#1a73e8;"></i> <span>Looking Ahead</span></p>
        <p style="margin: 0.3rem 0 0 0; line-height:1.6;">This partnership allows EHEPS to move beyond reactive aid, utilizing Google Cloud to predict humanitarian needs and pre‑position resources effectively. We are grateful for this opportunity to collaborate with Google as we build resilient, tech‑driven solutions for climate‑stressed communities.</p>
      </div>

      <!-- footer with tags: all Google softwares mentioned -->
      <div style="margin-top: 1.8rem; display: flex; flex-wrap: wrap; gap: 8px 12px; align-items: center; border-top: 1px dashed #d6e3f0; padding-top: 1.2rem;">
        <span style="font-weight:500; font-size:0.8rem; color:#1b3b5e;"><i class="fas fa-tags"></i> Google softwares tagged:</span>
        <span class="badge-google" style="background:#e3edf7;"><i class="fab fa-google"></i> Google Cloud</span>
        <span class="badge-google" style="background:#e3edf7;"><i class="fas fa-brain"></i> Vertex AI</span>
        <span class="badge-google" style="background:#e3edf7;"><i class="fas fa-map"></i> Google Maps Platform</span>
        <span class="badge-google" style="background:#e3edf7;"><i class="fas fa-users"></i> Google Workspace</span>
        <span class="badge-google" style="background:#e3edf7;"><i class="fas fa-code"></i> Web3 Program</span>
        <span class="badge-google" style="background:#e3edf7;"><i class="fas fa-chart-line"></i> AI-first</span>
      </div>

      <!-- footer meta: all cases / settings / home -->
      <div class="footer-meta">
        <div>
          <i class="fas fa-home"></i> Home · <i class="fas fa-list-ul"></i> All cases · <i class="fas fa-cog"></i> Settings
        </div>
        <div>
          <span class="btn-google"><i class="fab fa-google"></i> Case 72734924</span>
          <span style="margin-left: 1rem;"><i class="far fa-clock"></i> updated Jun 28, 2026</span>
        </div>
      </div>

    </div> <!-- end announcement-content -->
  </div> <!-- end case-body -->
</div> <!-- end case-card -->

</body>
</html>
