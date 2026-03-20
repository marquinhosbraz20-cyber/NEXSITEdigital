    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }

    html {
        scroll-behavior: smooth;
    }

    body {
        font-family: 'Inter', sans-serif;
        background: var(--darker);
        color: var(--text-primary);
        line-height: 1.6;
        overflow-x: hidden;
    }

    /* Background Effects */
    .bg-grid {
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background-image: 
            linear-gradient(rgba(0, 242, 254, 0.03) 1px, transparent 1px),
            linear-gradient(90deg, rgba(0, 242, 254, 0.03) 1px, transparent 1px);
        background-size: 50px 50px;
        z-index: -3;
        pointer-events: none;
    }

    .bg-gradient {
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background: 
            radial-gradient(ellipse at 20% 20%, rgba(0, 242, 254, 0.15) 0%, transparent 50%),
            radial-gradient(ellipse at 80% 80%, rgba(171, 39, 255, 0.15) 0%, transparent 50%),
            radial-gradient(ellipse at 50% 50%, rgba(0, 242, 254, 0.05) 0%, transparent 70%);
        z-index: -2;
        pointer-events: none;
    }

    #matrix {
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        z-index: -1;
        opacity: 0.08;
        pointer-events: none;
    }

    /* Scrollbar */
    ::-webkit-scrollbar {
        width: 8px;
    }

    ::-webkit-scrollbar-track {
        background: var(--dark);
    }

    ::-webkit-scrollbar-thumb {
        background: var(--primary);
        border-radius: 4px;
    }

    /* Navigation */
    .navbar {
        position: fixed;
        top: 0;
        left: 0;
        right: 0;
        z-index: 1000;
        padding: 20px 5%;
        display: flex;
        justify-content: space-between;
        align-items: center;
        transition: all 0.3s ease;
        background: transparent;
    }

    .navbar.scrolled {
        background: rgba(3, 7, 18, 0.95);
        backdrop-filter: blur(20px);
        padding: 15px 5%;
        border-bottom: 1px solid var(--border);
    }

    /* LOGO ESTILIZADA ADICIONADA */
    .logo {
        display: flex !important;
        align-items: center;
        gap: 12px;
        cursor: pointer;
        text-decoration: none;
    }

    .logo img {
        height: 50px;
        width: auto;
        max-width: 200px;
        display: block;
    }

    .logo-text {
        font-size: 2.2rem;
        font-weight: 800;
        letter-spacing: -1px;
        line-height: 1;
        color: #ffffff;
        font-family: 'Inter', sans-serif;
    }

    .logo-text span {
        background: linear-gradient(135deg, #00f2fe, #ab27ff);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
    }

    .nav-links {
        display: flex;
        gap: 40px;
        list-style: none;
    }

    .nav-links a {
        color: var(--text-secondary);
        text-decoration: none;
        font-weight: 500;
        font-size: 0.95rem;
        transition: all 0.3s ease;
        position: relative;
    }

    .nav-links a:hover {
        color: var(--primary);
    }

    .nav-links a::after {
        content: '';
        position: absolute;
        bottom: -5px;
        left: 0;
        width: 0;
        height: 2px;
        background: var(--gradient-primary);
        transition: width 0.3s ease;
    }

    .nav-links a:hover::after {
        width: 100%;
    }

    .nav-cta {
        padding: 12px 28px;
        background: var(--gradient-primary);
        border: none;
        border-radius: 50px;
        color: white;
        font-weight: 700;
        cursor: pointer;
        transition: all 0.3s ease;
        text-decoration: none;
        display: inline-block;
        box-shadow: 0 4px 15px rgba(0, 242, 254, 0.3);
    }

    .nav-cta:hover {
        transform: translateY(-2px);
        box-shadow: 0 6px 25px rgba(0, 242, 254, 0.5);
    }

    .mobile-menu {
        display: none;
        flex-direction: column;
        gap: 5px;
        cursor: pointer;
        z-index: 1001;
    }

    .mobile-menu span {
        width: 25px;
        height: 2px;
        background: var(--primary);
        transition: all 0.3s ease;
    }

    /* Hero Section */
    .hero {
        min-height: 100vh;
        display: flex;
        align-items: center;
        justify-content: center;
        padding: 120px 5% 80px;
        position: relative;
        overflow: hidden;
    }

    .hero-content {
        max-width: 900px;
        text-align: center;
        z-index: 2;
    }

    .hero-badge {
        display: inline-flex;
        align-items: center;
        gap: 8px;
        padding: 8px 20px;
        background: var(--glass-light);
        border: 1px solid var(--border);
        border-radius: 50px;
        font-size: 0.85rem;
        color: var(--primary);
        margin-bottom: 30px;
        animation: fadeInUp 0.8s ease;
    }

    .hero-badge i {
        animation: pulse 2s infinite;
    }

    .hero h1 {
        font-size: clamp(2.5rem, 6vw, 4.5rem);
        font-weight: 900;
        line-height: 1.1;
        margin-bottom: 25px;
        animation: fadeInUp 0.8s ease 0.1s both;
    }

    .hero h1 .gradient-text {
        background: var(--gradient-primary);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        background-clip: text;
        position: relative;
    }

    .hero-description {
        font-size: 1.25rem;
        color: var(--text-secondary);
        max-width: 600px;
        margin: 0 auto 40px;
        animation: fadeInUp 0.8s ease 0.2s both;
    }

    .hero-buttons {
        display: flex;
        gap: 20px;
        justify-content: center;
        flex-wrap: wrap;
        animation: fadeInUp 0.8s ease 0.3s both;
    }

    .btn-primary {
        padding: 16px 40px;
        background: var(--gradient-primary);
        border: none;
        border-radius: 50px;
        color: white;
        font-weight: 700;
        font-size: 1rem;
        cursor: pointer;
        transition: all 0.3s ease;
        text-decoration: none;
        display: inline-flex;
        align-items: center;
        gap: 10px;
        box-shadow: 0 4px 20px rgba(0, 242, 254, 0.4);
        position: relative;
        overflow: hidden;
    }

    .btn-primary::before {
        content: '';
        position: absolute;
        top: 0;
        left: -100%;
        width: 100%;
        height: 100%;
        background: linear-gradient(90deg, transparent, rgba(255,255,255,0.3), transparent);
        transition: left 0.5s ease;
    }

    .btn-primary:hover::before {
        left: 100%;
    }

    .btn-primary:hover {
        transform: translateY(-3px);
        box-shadow: 0 8px 30px rgba(0, 242, 254, 0.6);
    }

    .btn-secondary {
        padding: 16px 40px;
        background: transparent;
        border: 2px solid var(--border);
        border-radius: 50px;
        color: white;
        font-weight: 700;
        font-size: 1rem;
        cursor: pointer;
        transition: all 0.3s ease;
        text-decoration: none;
        display: inline-flex;
        align-items: center;
        gap: 10px;
    }

    .btn-secondary:hover {
        background: var(--glass-light);
        border-color: var(--primary);
        transform: translateY(-3px);
    }

    .hero-stats {
        display: flex;
        justify-content: center;
        gap: 60px;
        margin-top: 60px;
        animation: fadeInUp 0.8s ease 0.4s both;
    }

    .stat-item {
        text-align: center;
    }

    .stat-number {
        font-size: 2.5rem;
        font-weight: 900;
        background: var(--gradient-primary);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        background-clip: text;
    }

    .stat-label {
        font-size: 0.9rem;
        color: var(--text-muted);
        text-transform: uppercase;
        letter-spacing: 1px;
    }

    /* Section Common Styles */
    section {
        padding: 100px 5%;
        position: relative;
    }

    .section-header {
        text-align: center;
        max-width: 700px;
        margin: 0 auto 60px;
    }

    .section-tag {
        display: inline-block;
        padding: 6px 16px;
        background: var(--glass-light);
        border: 1px solid var(--border);
        border-radius: 50px;
        font-size: 0.8rem;
        color: var(--primary);
        font-weight: 600;
        text-transform: uppercase;
        letter-spacing: 1px;
        margin-bottom: 15px;
    }

    .section-title {
        font-size: clamp(2rem, 4vw, 3rem);
        font-weight: 800;
        margin-bottom: 20px;
        line-height: 1.2;
    }

    .section-subtitle {
        font-size: 1.1rem;
        color: var(--text-secondary);
    }

    /* Services Section */
    .services-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
        gap: 30px;
        max-width: 1200px;
        margin: 0 auto;
    }

    .service-card {
        background: var(--glass);
        border: 1px solid var(--border);
        border-radius: 20px;
        padding: 40px 30px;
        transition: all 0.4s ease;
        position: relative;
        overflow: hidden;
        backdrop-filter: blur(10px);
    }

    .service-card::before {
        content: '';
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 3px;
        background: var(--gradient-primary);
        transform: scaleX(0);
        transition: transform 0.4s ease;
    }

    .service-card:hover {
        transform: translateY(-10px);
        border-color: var(--primary);
        box-shadow: var(--shadow-glow);
    }

    .service-card:hover::before {
        transform: scaleX(1);
    }

    .service-icon {
        width: 70px;
        height: 70px;
        background: var(--gradient-primary);
        border-radius: 16px;
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 1.8rem;
        color: white;
        margin-bottom: 25px;
        box-shadow: 0 10px 30px rgba(0, 242, 254, 0.3);
    }

    .service-card h3 {
        font-size: 1.4rem;
        margin-bottom: 15px;
        font-weight: 700;
    }

    .service-card p {
        color: var(--text-secondary);
        line-height: 1.7;
        margin-bottom: 20px;
    }

    .service-features {
        list-style: none;
        margin-top: 20px;
    }

    .service-features li {
        display: flex;
        align-items: center;
        gap: 10px;
        margin-bottom: 10px;
        color: var(--text-secondary);
        font-size: 0.95rem;
    }

    .service-features i {
        color: var(--success);
        font-size: 0.9rem;
    }

    /* Portfolio Section */
    .portfolio {
        background: linear-gradient(180deg, var(--dark) 0%, rgba(10,15,28,0.5) 50%, var(--dark) 100%);
    }

    .portfolio-filter {
        display: flex;
        justify-content: center;
        gap: 15px;
        margin-bottom: 40px;
        flex-wrap: wrap;
    }

    .filter-btn {
        padding: 10px 25px;
        background: transparent;
        border: 1px solid var(--border);
        border-radius: 50px;
        color: var(--text-secondary);
        cursor: pointer;
        transition: all 0.3s ease;
        font-weight: 500;
    }

    .filter-btn.active,
    .filter-btn:hover {
        background: var(--gradient-primary);
        border-color: transparent;
        color: white;
    }

    .portfolio-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
        gap: 30px;
        max-width: 1200px;
        margin: 0 auto;
    }

    .portfolio-item {
        position: relative;
        border-radius: 20px;
        overflow: hidden;
        aspect-ratio: 16/10;
        cursor: pointer;
        group: portfolio;
    }

    .portfolio-item img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        transition: transform 0.5s ease;
    }

    .portfolio-overlay {
        position: absolute;
        inset: 0;
        background: linear-gradient(180deg, transparent 0%, rgba(3,7,18,0.95) 100%);
        display: flex;
        flex-direction: column;
        justify-content: flex-end;
        padding: 30px;
        opacity: 0;
        transition: all 0.4s ease;
    }

    .portfolio-item:hover .portfolio-overlay {
        opacity: 1;
    }

    .portfolio-item:hover img {
        transform: scale(1.1);
    }

    .portfolio-category {
        color: var(--primary);
        font-size: 0.85rem;
        font-weight: 600;
        text-transform: uppercase;
        letter-spacing: 1px;
        margin-bottom: 8px;
    }

    .portfolio-title {
        font-size: 1.3rem;
        font-weight: 700;
        margin-bottom: 15px;
    }

    .portfolio-link {
        display: inline-flex;
        align-items: center;
        gap: 8px;
        color: white;
        text-decoration: none;
        font-weight: 600;
        transition: gap 0.3s ease;
    }

    .portfolio-link:hover {
        gap: 12px;
        color: var(--primary);
    }

    /* Pricing Section */
    .pricing-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
        gap: 30px;
        max-width: 1000px;
        margin: 0 auto;
        align-items: start;
    }

    .pricing-card {
        background: var(--glass);
        border: 1px solid var(--border);
        border-radius: 24px;
        padding: 40px 30px;
        position: relative;
        transition: all 0.4s ease;
        backdrop-filter: blur(10px);
    }

    .pricing-card.featured {
        transform: scale(1.05);
        border-color: var(--primary);
        box-shadow: var(--shadow-glow);
    }

    .pricing-card.featured::before {
        content: 'MAIS POPULAR';
        position: absolute;
        top: -12px;
        left: 50%;
        transform: translateX(-50%);
        background: var(--gradient-primary);
        padding: 6px 20px;
        border-radius: 50px;
        font-size: 0.75rem;
        font-weight: 800;
        letter-spacing: 1px;
    }

    .pricing-card:hover {
        transform: translateY(-10px);
        border-color: var(--primary);
    }

    .pricing-card.featured:hover {
        transform: scale(1.05) translateY(-10px);
    }

    .pricing-header {
        text-align: center;
        margin-bottom: 30px;
        padding-bottom: 30px;
        border-bottom: 1px solid var(--glass-light);
    }

    .pricing-name {
        font-size: 1.3rem;
        font-weight: 700;
        margin-bottom: 10px;
    }

    .pricing-price {
        font-size: 3.5rem;
        font-weight: 900;
        background: var(--gradient-primary);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        background-clip: text;
        line-height: 1;
    }

    .pricing-price span {
        font-size: 1rem;
        color: var(--text-muted);
        -webkit-text-fill-color: var(--text-muted);
        font-weight: 500;
    }

    .pricing-description {
        color: var(--text-secondary);
        font-size: 0.95rem;
        margin-top: 10px;
    }

    .pricing-features {
        list-style: none;
        margin-bottom: 30px;
    }

    .pricing-features li {
        display: flex;
        align-items: center;
        gap: 12px;
        margin-bottom: 15px;
        color: var(--text-secondary);
    }

    .pricing-features i {
        color: var(--success);
        width: 20px;
    }

    .pricing-features li.not-included {
        color: var(--text-muted);
        text-decoration: line-through;
    }

    .pricing-features li.not-included i {
        color: var(--error);
    }

    .pricing-btn {
        width: 100%;
        padding: 16px;
        background: transparent;
        border: 2px solid var(--border);
        border-radius: 12px;
        color: white;
        font-weight: 700;
        cursor: pointer;
        transition: all 0.3s ease;
        font-size: 1rem;
    }

    .pricing-btn:hover {
        background: var(--gradient-primary);
        border-color: transparent;
        transform: translateY(-2px);
        box-shadow: 0 5px 20px rgba(0, 242, 254, 0.4);
    }

    .pricing-card.featured .pricing-btn {
        background: var(--gradient-primary);
        border-color: transparent;
    }

    /* Testimonials */
    .testimonials {
        background: var(--dark);
    }

    .testimonials-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
        gap: 30px;
        max-width: 1200px;
        margin: 0 auto;
    }

    .testimonial-card {
        background: var(--glass);
        border: 1px solid var(--border);
        border-radius: 20px;
        padding: 35px;
        position: relative;
        backdrop-filter: blur(10px);
    }

    .testimonial-card::before {
        content: '"';
        position: absolute;
        top: 20px;
        right: 30px;
        font-size: 6rem;
        color: var(--primary);
        opacity: 0.2;
        font-family: serif;
        line-height: 1;
    }

    .testimonial-stars {
        color: var(--warning);
        margin-bottom: 20px;
        font-size: 1.1rem;
    }

    .testimonial-text {
        color: var(--text-secondary);
        font-size: 1.05rem;
        line-height: 1.8;
        margin-bottom: 25px;
        font-style: italic;
    }

    .testimonial-author {
        display: flex;
        align-items: center;
        gap: 15px;
    }

    .author-avatar {
        width: 50px;
        height: 50px;
        border-radius: 50%;
        background: var(--gradient-primary);
        display: flex;
        align-items: center;
        justify-content: center;
        font-weight: 700;
        font-size: 1.2rem;
    }

    .author-info h4 {
        font-weight: 700;
        margin-bottom: 3px;
    }

    .author-info p {
        color: var(--text-muted);
        font-size: 0.9rem;
    }

    /* Contact Section */
    .contact-container {
        max-width: 800px;
        margin: 0 auto;
        background: var(--glass);
        border: 1px solid var(--border);
        border-radius: 24px;
        padding: 50px;
        backdrop-filter: blur(10px);
    }

    .contact-form {
        display: grid;
        gap: 20px;
    }

    .form-row {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 20px;
    }

    .form-group {
        position: relative;
    }

    .form-group label {
        display: block;
        margin-bottom: 8px;
        color: var(--text-secondary);
        font-size: 0.9rem;
        font-weight: 500;
    }

    .form-group input,
    .form-group select,
    .form-group textarea {
        width: 100%;
        padding: 14px 18px;
        background: rgba(0,0,0,0.3);
        border: 1px solid var(--border);
        border-radius: 12px;
        color: white;
        font-size: 1rem;
        transition: all 0.3s ease;
        font-family: 'Inter', sans-serif;
    }

    .form-group input:focus,
    .form-group select:focus,
    .form-group textarea:focus {
        outline: none;
        border-color: var(--primary);
        box-shadow: 0 0 0 3px rgba(0, 242, 254, 0.1);
    }

    .form-group textarea {
        resize: vertical;
        min-height: 120px;
    }

    .submit-btn {
        padding: 16px 40px;
        background: var(--gradient-primary);
        border: none;
        border-radius: 12px;
        color: white;
        font-weight: 700;
        font-size: 1rem;
        cursor: pointer;
        transition: all 0.3s ease;
        display: inline-flex;
        align-items: center;
        justify-content: center;
        gap: 10px;
        margin-top: 10px;
    }

    .submit-btn:hover {
        transform: translateY(-2px);
        box-shadow: 0 10px 30px rgba(0, 242, 254, 0.4);
    }

    /* Footer */
    footer {
        background: var(--darker);
        border-top: 1px solid var(--border);
        padding: 60px 5% 30px;
    }

    .footer-content {
        max-width: 1200px;
        margin: 0 auto;
        display: grid;
        grid-template-columns: 2fr 1fr 1fr 1fr;
        gap: 60px;
        margin-bottom: 50px;
    }

    .footer-brand {
        max-width: 300px;
    }

    .footer-logo {
        display: flex;
        align-items: center;
        gap: 12px;
        margin-bottom: 20px;
    }

    .footer-logo-icon {
        width: 40px;
        height: 40px;
        background: var(--gradient-primary);
        border-radius: 10px;
        display: flex;
        align-items: center;
        justify-content: center;
        font-weight: 900;
        color: white;
    }

    .footer-logo-text {
        font-size: 1.3rem;
        font-weight: 800;
    }

    .footer-logo-text span {
        background: var(--gradient-primary);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
    }

    .footer-description {
        color: var(--text-secondary);
        line-height: 1.8;
        margin-bottom: 25px;
    }

    .social-links {
        display: flex;
        gap: 15px;
    }

    .social-links a {
        width: 45px;
        height: 45px;
        background: var(--glass-light);
        border: 1px solid var(--border);
        border-radius: 12px;
        display: flex;
        align-items: center;
        justify-content: center;
        color: var(--text-secondary);
        text-decoration: none;
        transition: all 0.3s ease;
        font-size: 1.2rem;
    }

    .social-links a:hover {
        background: var(--gradient-primary);
        border-color: transparent;
        color: white;
        transform: translateY(-3px);
    }

    .footer-column h4 {
        font-size: 1.1rem;
        margin-bottom: 25px;
        color: white;
    }

    .footer-links {
        list-style: none;
    }

    .footer-links li {
        margin-bottom: 12px;
    }

    .footer-links a {
        color: var(--text-secondary);
        text-decoration: none;
        transition: all 0.3s ease;
        display: inline-flex;
        align-items: center;
        gap: 8px;
    }

    .footer-links a:hover {
        color: var(--primary);
        padding-left: 5px;
    }

    .footer-bottom {
        border-top: 1px solid var(--glass-light);
        padding-top: 30px;
        text-align: center;
        color: var(--text-muted);
        font-size: 0.9rem;
    }

    /* Modal */
    .modal {
        display: none;
        position: fixed;
        inset: 0;
        background: rgba(0,0,0,0.9);
        z-index: 2000;
        align-items: center;
        justify-content: center;
        padding: 20px;
        backdrop-filter: blur(10px);
    }

    .modal.active {
        display: flex;
    }

    .modal-content {
        background: var(--glass);
        border: 1px solid var(--border);
        border-radius: 24px;
        max-width: 500px;
        width: 100%;
        padding: 40px;
        position: relative;
        animation: modalIn 0.3s ease;
    }

    @keyframes modalIn {
        from {
            opacity: 0;
            transform: scale(0.9) translateY(20px);
        }
        to {
            opacity: 1;
            transform: scale(1) translateY(0);
        }
    }

    .modal-close {
        position: absolute;
        top: 20px;
        right: 20px;
        width: 40px;
        height: 40px;
        background: var(--glass-light);
        border: 1px solid var(--border);
        border-radius: 50%;
        display: flex;
        align-items: center;
        justify-content: center;
        color: var(--text-secondary);
        cursor: pointer;
        transition: all 0.3s ease;
        font-size: 1.2rem;
    }

    .modal-close:hover {
        background: var(--error);
        color: white;
        border-color: var(--error);
    }

    .modal h2 {
        margin-bottom: 10px;
        font-size: 1.8rem;
    }

    .modal p {
        color: var(--text-secondary);
        margin-bottom: 25px;
    }

    /* Admin Panel (Hidden) */
    #master-panel {
        display: none;
        position: fixed;
        inset: 0;
        background: rgba(0,0,0,0.98);
        z-index: 3000;
        padding: 20px;
        overflow-y: auto;
    }

    .admin-container {
        max-width: 1200px;
        margin: 0 auto;
        background: var(--glass);
        border: 1px solid var(--border);
        border-radius: 24px;
        min-height: 80vh;
        display: flex;
        overflow: hidden;
    }

    .admin-sidebar {
        width: 280px;
        background: rgba(0,0,0,0.3);
        border-right: 1px solid var(--border);
        padding: 40px 0;
    }

    .admin-nav-item {
        padding: 18px 30px;
        cursor: pointer;
        color: var(--text-secondary);
        font-weight: 600;
        transition: all 0.3s ease;
        border-left: 3px solid transparent;
        display: flex;
        align-items: center;
        gap: 12px;
    }

    .admin-nav-item:hover,
    .admin-nav-item.active {
        background: rgba(0, 242, 254, 0.1);
        color: var(--primary);
        border-left-color: var(--primary);
    }

    .admin-content {
        flex: 1;
        padding: 40px;
        overflow-y: auto;
    }

    .admin-header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 30px;
        padding-bottom: 20px;
        border-bottom: 1px solid var(--border);
    }

    .admin-close {
        width: 45px;
        height: 45px;
        background: var(--glass-light);
        border: 1px solid var(--border);
        border-radius: 12px;
        display: flex;
        align-items: center;
        justify-content: center;
        color: var(--text-secondary);
        cursor: pointer;
        transition: all 0.3s ease;
        font-size: 1.5rem;
    }

    .admin-close:hover {
        background: var(--error);
        color: white;
        border-color: var(--error);
    }

    /* Animations */
    @keyframes fadeInUp {
        from {
            opacity: 0;
            transform: translateY(30px);
        }
        to {
            opacity: 1;
            transform: translateY(0);
        }
    }

    @keyframes pulse {
        0%, 100% { opacity: 1; }
        50% { opacity: 0.5; }
    }

    .reveal {
        opacity: 0;
        transform: translateY(30px);
        transition: all 0.8s ease;
    }

    .reveal.active {
        opacity: 1;
        transform: translateY(0);
    }

    /* Toast Notification */
    .toast {
        position: fixed;
        bottom: 30px;
        right: 30px;
        background: var(--glass);
        border: 1px solid var(--border);
        border-radius: 12px;
        padding: 20px 25px;
        display: flex;
        align-items: center;
        gap: 15px;
        box-shadow: 0 10px 40px rgba(0,0,0,0.5);
        transform: translateX(400px);
        transition: transform 0.3s ease;
        z-index: 4000;
        backdrop-filter: blur(10px);
    }

    .toast.show {
        transform: translateX(0);
    }

    .toast-icon {
        width: 40px;
        height: 40px;
        border-radius: 50%;
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 1.2rem;
    }

    .toast.success .toast-icon {
        background: rgba(34, 197, 94, 0.2);
        color: var(--success);
    }

    .toast.error .toast-icon {
        background: rgba(239, 68, 68, 0.2);
        color: var(--error);
    }

    /* Responsive */
    @media (max-width: 968px) {
        .nav-links {
            display: none;
        }

        .mobile-menu {
            display: flex;
        }

        .hero-stats {
            gap: 30px;
        }

        .footer-content {
            grid-template-columns: 1fr 1fr;
            gap: 40px;
        }

        .pricing-card.featured {
            transform: scale(1);
        }

        .form-row {
            grid-template-columns: 1fr;
        }

        .logo-text {
            font-size: 1.6rem;
        }
        
        .logo img {
            height: 40px;
        }
    }

    @media (max-width: 640px) {
        .hero-buttons {
            flex-direction: column;
            width: 100%;
            padding: 0 20px;
        }

        .btn-primary,
        .btn-secondary {
            width: 100%;
            justify-content: center;
        }

        .hero-stats {
            flex-direction: column;
            gap: 20px;
        }

        .services-grid,
        .portfolio-grid,
        .testimonials-grid {
            grid-template-columns: 1fr;
        }

        .footer-content {
            grid-template-columns: 1fr;
            text-align: center;
        }

        .footer-logo,
        .social-links {
            justify-content: center;
        }

        .contact-container {
            padding: 30px 20px;
        }

        .admin-container {
            flex-direction: column;
        }

        .admin-sidebar {
            width: 100%;
            padding: 20px 0;
        }
    }

    /* Loading Animation */
    .loader {
        position: fixed;
        inset: 0;
        background: var(--dark);
        z-index: 5000;
        display: flex;
        align-items: center;
        justify-content: center;
        transition: opacity 0.5s ease, visibility 0.5s ease;
    }

    .loader.hidden {
        opacity: 0;
        visibility: hidden;
    }

    .loader-content {
        text-align: center;
    }

    .loader-spinner {
        width: 60px;
        height: 60px;
        border: 3px solid var(--glass-light);
        border-top-color: var(--primary);
        border-radius: 50%;
        animation: spin 1s linear infinite;
        margin: 0 auto 20px;
    }

    @keyframes spin {
        to { transform: rotate(360deg); }
    }

    .loader-text {
        color: var(--primary);
        font-weight: 600;
        letter-spacing: 2px;
        animation: pulse 1.5s infinite;
    }
</style>
