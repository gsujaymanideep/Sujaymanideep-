<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>RFS 10TH BATCH 2026–27</title>

  <meta name="description"
        content="RFS 10TH BATCH 2026–27 — Your Digital Study Companion">

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

  <link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Playfair+Display:wght@600;700;800&display=swap"
        rel="stylesheet">

  <script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>

  <style>
    /* =========================================================
       RFS 10TH BATCH 2026–27
       PREMIUM CLASSIC ACADEMIC DESIGN
       ========================================================= */

    :root {
      --navy: #10243b;
      --navy2: #173653;
      --cream: #f7f3ea;
      --paper: #fffdf8;
      --gold: #b89554;
      --gold2: #d5bd82;
      --ink: #1c2936;
      --muted: #6f7881;
      --line: #e8e0d2;
      --danger: #9c4b42;

      --shadow: 0 18px 45px rgba(16, 36, 59, .09);
      --small-shadow: 0 8px 25px rgba(16, 36, 59, .08);

      --radius: 9px;
      --container: 1160px;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      background: var(--paper);
      color: var(--ink);
      font-family: "DM Sans", sans-serif;
      line-height: 1.6;
      overflow-x: hidden;
    }

    body.modal-open {
      overflow: hidden;
    }

    h1,
    h2,
    h3,
    h4 {
      font-family: "Playfair Display", serif;
      line-height: 1.15;
    }

    button,
    input,
    textarea,
    select {
      font: inherit;
    }

    button {
      cursor: pointer;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    .container {
      width: min(var(--container), calc(100% - 40px));
      margin: auto;
    }

    /* =========================================================
       HEADER
       ========================================================= */

    header {
      position: sticky;
      top: 0;
      z-index: 1000;

      height: 76px;

      background: rgba(255, 253, 248, .94);
      backdrop-filter: blur(16px);
      -webkit-backdrop-filter: blur(16px);

      border-bottom: 1px solid var(--line);
    }

    .nav {
      height: 76px;

      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 25px;
    }

    .brand {
      display: flex;
      align-items: center;
      gap: 12px;
      min-width: 190px;
    }

    .brand-mark {
      width: 44px;
      height: 44px;

      display: grid;
      place-items: center;

      border: 2px solid var(--gold);
      border-radius: 50%;

      color: var(--navy);
      font-family: "Playfair Display", serif;
      font-weight: 800;
      font-size: 13px;
    }

    .brand-text strong {
      display: block;
      color: var(--navy);
      font-size: 14px;
      letter-spacing: 1.5px;
    }

    .brand-text span {
      display: block;
      color: var(--muted);
      font-size: 11px;
      letter-spacing: 1px;
      margin-top: 1px;
    }

    .nav-links {
      display: flex;
      align-items: center;
      gap: 28px;
    }

    .nav-links a {
      position: relative;

      color: var(--ink);
      font-size: 13px;
      font-weight: 600;

      transition: color .2s ease;
    }

    .nav-links a::after {
      content: "";

      position: absolute;
      left: 0;
      bottom: -7px;

      width: 0;
      height: 2px;

      background: var(--gold);

      transition: width .2s ease;
    }

    .nav-links a:hover {
      color: var(--gold);
    }

    .nav-links a:hover::after {
      width: 100%;
    }

    .nav-action {
      border: 0;
      background: var(--navy);
      color: white;

      padding: 10px 17px;
      border-radius: 6px;

      font-size: 12px;
      font-weight: 700;

      transition: .2s ease;
    }

    .nav-action:hover {
      background: var(--navy2);
      transform: translateY(-1px);
    }

    .menu-button {
      display: none;

      width: 42px;
      height: 42px;

      border: 1px solid var(--line);
      background: white;
      border-radius: 7px;

      color: var(--navy);
      font-size: 22px;
    }

    /* =========================================================
       MOBILE MENU
       ========================================================= */

    .mobile-menu {
      display: none;

      position: fixed;
      top: 76px;
      left: 0;
      right: 0;

      background: var(--paper);
      border-bottom: 1px solid var(--line);

      padding: 18px 20px;

      box-shadow: var(--small-shadow);
      z-index: 999;
    }

    .mobile-menu.open {
      display: block;
    }

    .mobile-menu a,
    .mobile-menu button {
      display: block;
      width: 100%;

      text-align: left;

      padding: 13px 5px;

      border: 0;
      border-bottom: 1px solid var(--line);

      background: transparent;
      color: var(--ink);

      font-weight: 600;
    }

    /* =========================================================
       HERO
       ========================================================= */

    .hero {
      position: relative;
      min-height: 650px;

      display: flex;
      align-items: center;

      overflow: hidden;

      background:
        radial-gradient(
          circle at 80% 45%,
          rgba(184, 149, 84, .17),
          transparent 32%
        ),
        var(--navy);

      color: white;
    }

    .hero-content {
      position: relative;
      z-index: 2;

      max-width: 760px;
      padding: 100px 0;
    }

    .eyebrow {
      color: var(--gold);
      font-size: 11px;
      font-weight: 700;

      letter-spacing: 2.8px;
      text-transform: uppercase;

      margin-bottom: 16px;
    }

    .hero h1 {
      font-size: clamp(48px, 7vw, 86px);
      letter-spacing: -2px;
      margin-bottom: 22px;
    }

    .hero h1 span {
      display: block;
      color: var(--gold2);
    }

    .hero-subtitle {
      max-width: 580px;

      color: rgba(255, 255, 255, .82);

      font-size: clamp(17px, 2vw, 21px);
      margin-bottom: 35px;
    }

    .hero-buttons {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
    }

    .btn {
      border-radius: 6px;

      padding: 13px 20px;

      font-size: 13px;
      font-weight: 700;

      border: 1px solid transparent;

      transition: .2s ease;
    }

    .btn-primary {
      background: var(--gold);
      color: white;
    }

    .btn-primary:hover {
      background: #a78347;
      transform: translateY(-2px);
    }

    .btn-ghost {
      background: transparent;
      color: white;
      border-color: rgba(255,255,255,.35);
    }

    .btn-ghost:hover {
      border-color: var(--gold2);
      color: var(--gold2);
    }

    .motto {
      margin-top: 55px;

      display: flex;
      align-items: center;
      gap: 12px;

      color: rgba(255,255,255,.7);

      font-size: 11px;
      font-weight: 700;

      letter-spacing: 2px;
      text-transform: uppercase;
    }

    .motto i {
      width: 5px;
      height: 5px;
      background: var(--gold);
      border-radius: 50%;
    }

    .hero-pattern {
      position: absolute;
      right: -120px;
      bottom: -150px;

      width: 580px;
      height: 580px;

      border: 1px solid rgba(213,189,130,.18);
      border-radius: 50%;
    }

    .hero-pattern::before,
    .hero-pattern::after {
      content: "";

      position: absolute;

      border: 1px solid rgba(213,189,130,.13);
      border-radius: 50%;
    }

    .hero-pattern::before {
      inset: 70px;
    }

    .hero-pattern::after {
      inset: 145px;
    }

    .hero-star {
      position: absolute;
      right: 21%;
      top: 25%;

      color: var(--gold2);
      font-size: 70px;
      opacity: .3;
    }

    /* =========================================================
       GENERAL SECTIONS
       ========================================================= */

    section {
      padding: 92px 0;
    }

    .section-heading {
      margin-bottom: 42px;
    }

    .section-heading h2 {
      color: var(--navy);
      font-size: clamp(34px, 4vw, 45px);
      margin-bottom: 12px;
    }

    .section-heading p {
      max-width: 650px;
      color: var(--muted);
      font-size: 15px;
    }

    /* =========================================================
       SUBJECTS
       ========================================================= */

    #subjects {
      background: var(--paper);
    }

    .subject-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 18px;
    }

    .subject-card {
      position: relative;

      min-height: 150px;

      padding: 25px;

      background: white;
      border: 1px solid var(--line);
      border-radius: var(--radius);

      box-shadow: 0 3px 15px rgba(16,36,59,.025);

      overflow: hidden;

      cursor: pointer;

      transition: transform .25s ease,
                  box-shadow .25s ease,
                  border-color .25s ease;
    }

    .subject-card:hover {
      transform: translateY(-5px);
      box-shadow: var(--shadow);
      border-color: rgba(184,149,84,.55);
    }

    .subject-number {
      color: var(--gold);
      font-size: 11px;
      font-weight: 800;
      letter-spacing: 1.5px;
    }

    .subject-icon {
      position: absolute;
      right: 20px;
      top: 18px;

      color: rgba(184,149,84,.17);

      font-family: "Playfair Display", serif;
      font-size: 58px;
      font-weight: 800;
    }

    .subject-card h3 {
      position: relative;
      z-index: 1;

      color: var(--navy);
      font-size: 25px;

      margin-top: 28px;
      margin-bottom: 7px;
    }

    .subject-card p {
      position: relative;
      z-index: 1;

      color: var(--muted);
      font-size: 12px;
    }

    /* =========================================================
       SEARCH
       ========================================================= */

    #search {
      background: var(--cream);
    }

    .search-box {
      max-width: 850px;
      margin: auto;
    }

    .search-input-wrap {
      position: relative;
    }

    .search-input {
      width: 100%;
      height: 62px;

      padding: 0 22px;

      border: 1px solid var(--line);
      border-radius: 8px;

      outline: none;

      background: white;
      color: var(--ink);

      font-size: 15px;

      box-shadow: var(--small-shadow);

      transition: border .2s ease,
                  box-shadow .2s ease;
    }

    .search-input:focus {
      border-color: var(--gold);
      box-shadow: 0 0 0 4px rgba(184,149,84,.09);
    }

    .search-results {
      margin-top: 18px;

      display: grid;
      gap: 10px;
    }

    .search-result {
      background: white;
      border: 1px solid var(--line);
      border-radius: 8px;

      padding: 18px;

      cursor: pointer;

      transition: .2s ease;
    }

    .search-result:hover {
      transform: translateY(-2px);
      box-shadow: var(--small-shadow);
      border-color: var(--gold2);
    }

    .result-meta {
      color: var(--gold);
      font-size: 10px;
      font-weight: 800;
      letter-spacing: 1px;
      text-transform: uppercase;
      margin-bottom: 7px;
    }

    .search-result h4 {
      color: var(--navy);
      font-size: 19px;
    }

    /* =========================================================
       RECENT
       ========================================================= */

    .recent-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 18px;
    }

    .answer-card {
      background: white;
      border: 1px solid var(--line);
      border-radius: var(--radius);

      padding: 23px;

      cursor: pointer;

      transition: .2s ease;
    }

    .answer-card:hover {
      transform: translateY(-4px);
      box-shadow: var(--shadow);
      border-color: var(--gold2);
    }

    .answer-meta {
      color: var(--gold);

      font-size: 10px;
      font-weight: 800;

      letter-spacing: 1px;
      text-transform: uppercase;

      margin-bottom: 12px;
    }

    .answer-card h3 {
      color: var(--navy);
      font-size: 19px;

      margin-bottom: 10px;
    }

    .answer-preview {
      color: var(--muted);
      font-size: 13px;
    }

    /* =========================================================
       ANNOUNCEMENTS
       ========================================================= */

    #announcements {
      background: var(--cream);
    }

    .announcement-list {
      display: grid;
      gap: 12px;
    }

    .announcement {
      display: grid;
      grid-template-columns: 40px 1fr auto;
      gap: 18px;
      align-items: start;

      padding: 21px;

      background: white;
      border: 1px solid var(--line);
      border-radius: 8px;
    }

    .announcement-star {
      width: 32px;
      height: 32px;

      display: grid;
      place-items: center;

      color: var(--gold);
      background: var(--cream);

      border-radius: 50%;
    }

    .announcement h3 {
      color: var(--navy);
      font-size: 19px;
      margin-bottom: 5px;
    }

    .announcement p {
      color: var(--muted);
      font-size: 13px;
      white-space: pre-line;
    }

    .announcement-date {
      color: var(--muted);
      font-size: 11px;
      white-space: nowrap;
    }

    /* =========================================================
       EMPTY / NOTICE
       ========================================================= */

    .empty-state {
      padding: 30px;

      text-align: center;

      border: 1px dashed var(--line);
      border-radius: 8px;

      color: var(--muted);
      background: rgba(255,255,255,.4);
    }

    .setup-notice {
      margin: 20px auto;
      max-width: 800px;

      padding: 17px 20px;

      border: 1px solid #dfc98f;
      background: #fff8df;

      border-radius: 7px;

      color: #66552e;

      font-size: 13px;
    }

    /* =========================================================
       MODALS
       ========================================================= */

    .modal {
      position: fixed;
      inset: 0;

      display: none;
      align-items: center;
      justify-content: center;

      padding: 20px;

      background: rgba(9,20,32,.72);

      z-index: 5000;
    }

    .modal.open {
      display: flex;
    }

    .modal-card {
      width: min(900px, 100%);
      max-height: 90vh;

      overflow: auto;

      background: var(--paper);

      border-radius: 10px;

      box-shadow: 0 30px 80px rgba(0,0,0,.25);

      padding: 34px;
    }

    .modal-card.small {
      width: min(480px, 100%);
    }

    .modal-header {
      display: flex;
      justify-content: space-between;
      align-items: start;
      gap: 20px;

      margin-bottom: 25px;
    }

    .modal-header h2 {
      color: var(--navy);
      font-size: 31px;
    }

    .close-btn {
      width: 38px;
      height: 38px;

      flex: 0 0 auto;

      border: 1px solid var(--line);
      background: white;

      border-radius: 6px;

      color: var(--navy);
      font-size: 20px;
    }

    .close-btn:hover {
      border-color: var(--gold);
    }

    /* =========================================================
       READER
       ========================================================= */

    .reader-breadcrumb {
      color: var(--gold);
      font-size: 11px;
      font-weight: 800;

      letter-spacing: 1.3px;
      text-transform: uppercase;

      margin-bottom: 13px;
    }

    .reader-question {
      color: var(--navy);
      font-size: clamp(25px, 4vw, 38px);
      margin-bottom: 25px;
    }

    .reader-answer {
      color: var(--ink);
      font-size: 15px;
      line-height: 1.85;
      white-space: normal;
    }

    .reader-footer {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 15px;

      margin-top: 30px;
      padding-top: 20px;

      border-top: 1px solid var(--line);
    }

    .reader-date {
      color: var(--muted);
      font-size: 11px;
    }

    /* =========================================================
       CHAPTER LIST
       ========================================================= */

    .chapter-list {
      display: grid;
      gap: 10px;
    }

    .chapter-item {
      display: flex;
      justify-content: space-between;
      align-items: center;

      padding: 17px 18px;

      background: white;
      border: 1px solid var(--line);
      border-radius: 7px;

      cursor: pointer;

      transition: .2s ease;
    }

    .chapter-item:hover {
      transform: translateX(3px);
      border-color: var(--gold);
    }

    .chapter-name {
      color: var(--navy);
      font-family: "Playfair Display", serif;
      font-size: 18px;
    }

    .chapter-count {
      color: var(--muted);
      font-size: 11px;
    }

    /* =========================================================
       AUTH
       ========================================================= */

    .auth-tabs {
      display: flex;
      border-bottom: 1px solid var(--line);
      margin-bottom: 25px;
    }

    .auth-tab {
      padding: 11px 15px;

      border: 0;
      border-bottom: 2px solid transparent;

      background: transparent;

      color: var(--muted);

      font-size: 13px;
      font-weight: 700;
    }

    .auth-tab.active {
      color: var(--navy);
      border-color: var(--gold);
    }

    .form-group {
      margin-bottom: 17px;
    }

    .form-group label {
      display: block;

      color: var(--navy);

      font-size: 11px;
      font-weight: 800;

      letter-spacing: .8px;
      text-transform: uppercase;

      margin-bottom: 7px;
    }

    .form-control {
      width: 100%;

      padding: 12px 13px;

      border: 1px solid var(--line);
      border-radius: 6px;

      outline: none;

      background: white;
      color: var(--ink);

      font-size: 13px;
    }

    .form-control:focus {
      border-color: var(--gold);
      box-shadow: 0 0 0 3px rgba(184,149,84,.08);
    }

    textarea.form-control {
      min-height: 130px;
      resize: vertical;
    }

    .form-error {
      display: none;

      padding: 11px 13px;
      margin-bottom: 15px;

      border-radius: 6px;

      background: #fff0ee;
      border: 1px solid #e7c1bd;

      color: var(--danger);

      font-size: 12px;
    }

    .form-error.show {
      display: block;
    }

    /* =========================================================
       ACCOUNT
       ========================================================= */

    .account-info {
      padding: 20px;

      background: var(--cream);
      border: 1px solid var(--line);
      border-radius: 7px;

      margin-bottom: 20px;
    }

    .account-info strong {
      display: block;
      color: var(--navy);
      font-family: "Playfair Display", serif;
      font-size: 23px;
    }

    .account-info span {
      color: var(--muted);
      font-size: 12px;
    }

    /* =========================================================
       ADMIN
       ========================================================= */

    .admin-top {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 20px;

      margin-bottom: 28px;
    }

    .admin-top small {
      color: var(--muted);
    }

    .admin-stats {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 12px;

      margin-bottom: 30px;
    }

    .stat {
      padding: 18px;

      background: white;
      border: 1px solid var(--line);
      border-radius: 7px;
    }

    .stat span {
      display: block;

      color: var(--muted);

      font-size: 10px;
      font-weight: 800;

      letter-spacing: 1px;
      text-transform: uppercas
