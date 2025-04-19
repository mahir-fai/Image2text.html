# Image2text.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Free online tool to extract text from images (OCR). Convert JPG, PNG, PDF to editable text instantly. No registration required.">
    <meta name="keywords" content="image to text, OCR online, extract text from image, JPG to text, PNG to text, PDF to text, free OCR">
    <title>Image2Text Pro | Advanced OCR Converter</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-YOUR_PUBLISHER_ID" crossorigin="anonymous"></script>
    <style>
        :root {
            --primary: #4361ee;
            --primary-light: #4895ef;
            --secondary: #3f37c9;
            --accent: #f72585;
            --dark: #1a1a2e;
            --light: #f8f9fa;
            --success: #4cc9f0;
            --warning: #f8961e;
            --danger: #ef233c;
            --gray: #6c757d;
            --light-gray: #e9ecef;
            --gradient: linear-gradient(135deg, #4361ee 0%, #3f37c9 100%);
            --shadow-sm: 0 1px 3px rgba(0,0,0,0.12);
            --shadow-md: 0 4px 6px rgba(0,0,0,0.1);
            --shadow-lg: 0 10px 15px rgba(0,0,0,0.1);
            --transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            line-height: 1.6;
            color: var(--dark);
            background-color: var(--light);
            overflow-x: hidden;
        }

        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header */
        header {
            background: white;
            box-shadow: var(--shadow-sm);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 0;
        }

        .logo {
            display: flex;
            align-items: center;
            text-decoration: none;
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--primary);
        }

        .logo i {
            margin-right: 0.5rem;
            color: var(--accent);
        }

        .nav-links {
            display: flex;
            list-style: none;
        }

        .nav-links li {
            margin-left: 1.5rem;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--dark);
            font-weight: 500;
            transition: var(--transition);
            position: relative;
            padding: 0.5rem 0;
        }

        .nav-links a:after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: 0;
            left: 0;
            background-color: var(--accent);
            transition: var(--transition);
        }

        .nav-links a:hover:after {
            width: 100%;
        }

        .cta-button {
            background: var(--gradient);
            color: white;
            border: none;
            padding: 0.5rem 1.25rem;
            border-radius: 50px;
            font-weight: 600;
            cursor: pointer;
            transition: var(--transition);
            box-shadow: 0 4px 15px rgba(67, 97, 238, 0.3);
        }

        .cta-button:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(67, 97, 238, 0.4);
        }

        /* Hero Section */
        .hero {
            padding: 5rem 0 3rem;
            text-align: center;
            background: url('https://images.unsplash.com/photo-1551288049-bebda4e38f71?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80') no-repeat center center/cover;
            position: relative;
            color: white;
        }

        .hero:before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(26, 26, 46, 0.7);
        }

        .hero-content {
            position: relative;
            z-index: 1;
            max-width: 800px;
            margin: 0 auto;
        }

        .hero h1 {
            font-size: 3rem;
            margin-bottom: 1.5rem;
            font-weight: 700;
            line-height: 1.2;
        }

        .hero p {
            font-size: 1.25rem;
            margin-bottom: 2rem;
            opacity: 0.9;
        }

        .hero-buttons {
            display: flex;
            justify-content: center;
            gap: 1rem;
            margin-top: 2rem;
        }

        /* Tool Section */
        .tool-section {
            padding: 4rem 0;
            position: relative;
        }

        .section-title {
            text-align: center;
            margin-bottom: 3rem;
        }

        .section-title h2 {
            font-size: 2.5rem;
            color: var(--dark);
            margin-bottom: 1rem;
            position: relative;
            display: inline-block;
        }

        .section-title h2:after {
            content: '';
            position: absolute;
            width: 50%;
            height: 4px;
            bottom: -10px;
            left: 25%;
            background: var(--gradient);
            border-radius: 2px;
        }

        .section-title p {
            color: var(--gray);
            max-width: 700px;
            margin: 0 auto;
        }

        .tool-container {
            background: white;
            border-radius: 15px;
            box-shadow: var(--shadow-lg);
            overflow: hidden;
            margin-bottom: 3rem;
        }

        .tool-header {
            background: var(--gradient);
            color: white;
            padding: 1.5rem;
            text-align: center;
        }

        .tool-header h3 {
            font-size: 1.5rem;
            margin-bottom: 0.5rem;
        }

        .tool-content {
            display: flex;
            flex-direction: column;
            padding: 2rem;
        }

        @media (min-width: 992px) {
            .tool-content {
                flex-direction: row;
                gap: 2rem;
            }
        }

        .upload-section {
            flex: 1;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            padding: 2rem;
            border: 2px dashed var(--light-gray);
            border-radius: 10px;
            transition: var(--transition);
            cursor: pointer;
            background: rgba(233, 236, 239, 0.3);
            position: relative;
            overflow: hidden;
        }

        .upload-section:hover {
            border-color: var(--primary-light);
            background: rgba(72, 149, 239, 0.1);
        }

        .upload-section.active {
            border-color: var(--success);
            background: rgba(76, 201, 240, 0.1);
        }

        .upload-icon {
            font-size: 3.5rem;
            color: var(--primary);
            margin-bottom: 1.5rem;
            transition: var(--transition);
        }

        .upload-section:hover .upload-icon {
            transform: scale(1.1);
            color: var(--primary-light);
        }

        .upload-section h4 {
            font-size: 1.25rem;
            margin-bottom: 0.5rem;
            color: var(--dark);
        }

        .upload-section p {
            color: var(--gray);
            text-align: center;
            margin-bottom: 1.5rem;
        }

        .file-input {
            display: none;
        }

        .result-section {
            flex: 1;
            display: flex;
            flex-direction: column;
        }

        .result-actions {
            display: flex;
            justify-content: space-between;
            margin-bottom: 1rem;
            gap: 0.5rem;
        }

        .result-box {
            flex-grow: 1;
            border: 1px solid var(--light-gray);
            border-radius: 10px;
            padding: 1.5rem;
            min-height: 300px;
            background: white;
            overflow-y: auto;
            font-family: 'Courier New', monospace;
            line-height: 1.8;
            color: var(--dark);
            box-shadow: inset 0 1px 3px rgba(0,0,0,0.1);
            transition: var(--transition);
        }

        .result-box:focus {
            outline: none;
            border-color: var(--primary);
            box-shadow: 0 0 0 3px rgba(67, 97, 238, 0.2);
        }

        .preview-image {
            max-width: 100%;
            max-height: 250px;
            margin-bottom: 1.5rem;
            display: none;
            border-radius: 8px;
            box-shadow: var(--shadow-md);
            object-fit: contain;
            background: #f5f5f5;
            padding: 0.5rem;
        }

        /* Buttons */
        .btn {
            padding: 0.5rem 1.25rem;
            border-radius: 50px;
            font-weight: 500;
            cursor: pointer;
            transition: var(--transition);
            border: none;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 0.5rem;
        }

        .btn-primary {
            background: var(--gradient);
            color: white;
            box-shadow: 0 4px 15px rgba(67, 97, 238, 0.3);
        }

        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(67, 97, 238, 0.4);
        }

        .btn-secondary {
            background: white;
            color: var(--primary);
            border: 1px solid var(--primary);
        }

        .btn-secondary:hover {
            background: var(--primary);
            color: white;
        }

        .btn-success {
            background: var(--success);
            color: white;
        }

        .btn-success:hover {
            background: #3ab4d9;
        }

        .btn-danger {
            background: var(--danger);
            color: white;
        }

        .btn-danger:hover {
            background: #d90429;
        }

        /* Features */
        .features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin: 4rem 0;
        }

        .feature-card {
            background: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: var(--shadow-md);
            transition: var(--transition);
            text-align: center;
            border-top: 3px solid var(--primary);
        }

        .feature-card:hover {
            transform: translateY(-5px);
            box-shadow: var(--shadow-lg);
        }

        .feature-icon {
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 1.5rem;
            background: linear-gradient(135deg, var(--primary) 0%, var(--secondary) 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .feature-card h3 {
            font-size: 1.25rem;
            margin-bottom: 1rem;
            color: var(--dark);
        }

        .feature-card p {
            color: var(--gray);
            font-size: 0.95rem;
        }

        /* How It Works */
        .steps {
            display: flex;
            flex-direction: column;
            gap: 2rem;
            margin: 3rem 0;
            position: relative;
        }

        .step {
            display: flex;
            gap: 1.5rem;
            position: relative;
            padding-left: 3rem;
        }

        .step-number {
            position: absolute;
            left: 0;
            top: 0;
            width: 2.5rem;
            height: 2.5rem;
            background: var(--gradient);
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: 600;
            box-shadow: 0 4px 10px rgba(67, 97, 238, 0.3);
        }

        .step-content {
            flex: 1;
        }

        .step h3 {
            font-size: 1.25rem;
            margin-bottom: 0.5rem;
            color: var(--dark);
        }

        .step p {
            color: var(--gray);
        }

        /* FAQ */
        .faq-container {
            max-width: 800px;
            margin: 0 auto;
        }

        .faq-item {
            margin-bottom: 1rem;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: var(--shadow-sm);
        }

        .faq-question {
            background: white;
            padding: 1.25rem;
            font-weight: 500;
            cursor: pointer;
            display: flex;
            justify-content: space-between;
            align-items: center;
            transition: var(--transition);
        }

        .faq-question:hover {
            background: var(--light);
        }

        .faq-question i {
            transition: var(--transition);
        }

        .faq-answer {
            background: var(--light);
            padding: 0 1.25rem;
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.3s ease;
        }

        .faq-item.active .faq-question {
            background: var(--primary);
            color: white;
        }

        .faq-item.active .faq-question i {
            transform: rotate(180deg);
        }

        .faq-item.active .faq-answer {
            max-height: 500px;
            padding: 1.25rem;
        }

        /* Ad Banner */
        .ad-banner {
            background: white;
            padding: 1rem;
            margin: 2rem 0;
            text-align: center;
            border-radius: 8px;
            box-shadow: var(--shadow-sm);
        }

        /* Footer */
        footer {
            background: var(--dark);
            color: white;
            padding: 4rem 0 2rem;
            margin-top: 4rem;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
            margin-bottom: 3rem;
        }

        .footer-column h3 {
            font-size: 1.25rem;
            margin-bottom: 1.5rem;
            position: relative;
            display: inline-block;
        }

        .footer-column h3:after {
            content: '';
            position: absolute;
            width: 50%;
            height: 2px;
            bottom: -8px;
            left: 0;
            background: var(--primary);
        }

        .footer-column ul {
            list-style: none;
        }

        .footer-column ul li {
            margin-bottom: 0.75rem;
        }

        .footer-column ul li a {
            color: #adb5bd;
            text-decoration: none;
            transition: var(--transition);
        }

        .footer-column ul li a:hover {
            color: white;
            padding-left: 5px;
        }

        .social-links {
            display: flex;
            gap: 1rem;
            margin-top: 1.5rem;
        }

        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 36px;
            height: 36px;
            background: rgba(255,255,255,0.1);
            border-radius: 50%;
            color: white;
            transition: var(--transition);
        }

        .social-links a:hover {
            background: var(--primary);
            transform: translateY(-3px);
        }

        .copyright {
            text-align: center;
            padding-top: 2rem;
            border-top: 1px solid rgba(255,255,255,0.1);
            color: #adb5bd;
            font-size: 0.9rem;
        }

        /* Loading spinner */
        .spinner {
            display: none;
            width: 40px;
            height: 40px;
            margin: 1rem auto;
            border: 4px solid rgba(0, 0, 0, 0.1);
            border-radius: 50%;
            border-top: 4px solid var(--primary);
            animation: spin 1s linear infinite;
        }

        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        /* Responsive adjustments */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.25rem;
            }
            
            .hero p {
                font-size: 1.1rem;
            }
            
            .navbar {
                flex-direction: column;
                padding: 1rem 0;
            }
            
            .nav-links {
                margin-top: 1rem;
                flex-wrap: wrap;
                justify-content: center;
            }
            
            .nav-links li {
                margin: 0.5rem;
            }
            
            .hero-buttons {
                flex-direction: column;
                gap: 0.5rem;
            }
            
            .result-actions {
                flex-direction: column;
            }
            
            .btn {
                width: 100%;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container navbar">
            <a href="/" class="logo">
                <i class="fas fa-text-height"></i>Image2Text Pro
            </a>
            <ul class="nav-links">
                <li><a href="#features">Features</a></li>
                <li><a href="#how-it-works">How It Works</a></li>
                <li><a href="#faq">FAQ</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
            <button class="cta-button">Premium</button>
        </div>
    </header>
    
    <section class="hero">
        <div class="container hero-content">
            <h1>Extract Text From Images With AI Precision</h1>
            <p>Convert scanned documents, photos, and PDFs into editable text in seconds with our advanced OCR technology.</p>
            <div class="hero-buttons">
                <button class="btn btn-primary" id="startConvertingBtn">
                    <i class="fas fa-bolt"></i> Start Converting Now
                </button>
                <button class="btn btn-secondary">
                    <i class="fas fa-play-circle"></i> Watch Demo
                </button>
            </div>
        </div>
    </section>
    
    <section class="tool-section">
        <div class="container">
            <div class="section-title">
                <h2>Image to Text Converter</h2>
                <p>Upload your image or PDF file and get editable text in seconds</p>
            </div>
            
            <div class="ad-banner">
                <!-- AdSense Ad Unit -->
                <ins class="adsbygoogle"
                     style="display:block"
                     data-ad-client="ca-app-pub-9529109133395287/4661214987"
                     data-ad-slot="4661214987"
                     data-ad-format="auto"
                     data-full-width-responsive="true"></ins>
                <script>
                     (adsbygoogle = window.adsbygoogle || []).push({});
                </script>
            </div>
            
            <div class="tool-container">
                <div class="tool-header">
                    <h3>Drag & Drop Your Files Here</h3>
                    <p>Supports JPG, PNG, PDF and more</p>
                </div>
                
                <div class="tool-content">
                    <div class="upload-section" id="dropArea">
                        <div class="upload-icon">
                            <i class="fas fa-cloud-upload-alt"></i>
                        </div>
                        <h4>Select or Drop Files</h4>
                        <p>Files should be less than 10MB</p>
                        <input type="file" id="fileInput" class="file-input" accept="image/*,.pdf">
                        <button class="btn btn-primary" id="uploadBtn">
                            <i class="fas fa-folder-open"></i> Browse Files
                        </button>
                        <div class="spinner" id="uploadSpinner"></div>
                    </div>
                    
                    <div class="result-section">
                        <div class="result-actions">
                            <button class="btn btn-success" id="copyBtn" disabled>
                                <i class="fas fa-copy"></i> Copy Text
                            </button>
                            <button class="btn btn-secondary" id="downloadBtn" disabled>
                                <i class="fas fa-download"></i> Download
                            </button>
                            <button class="btn btn-danger" id="clearBtn" disabled>
                                <i class="fas fa-trash-alt"></i> Clear
                            </button>
                        </div>
                        <img id="previewImage" class="preview-image" alt="Uploaded image preview">
                        <div class="result-box" id="resultText" contenteditable="true" placeholder="Extracted text will appear here..."></div>
                    </div>
                </div>
            </div>
            
            <div class="ad-banner">
                <!-- AdSense Ad Unit -->
                <ins class="adsbygoogle"
                     style="display:block"
                     data-ad-client="ca-app-pub-9529109133395287/4661214987"
                     data-ad-slot="4661214987"
                     data-ad-format="auto"
                     data-full-width-responsive="true"></ins>
                <script>
                     (adsbygoogle = window.adsbygoogle || []).push({});
                </script>
            </div>
        </div>
    </section>
    
    <section class="container" id="features">
        <div class="section-title">
            <h2>Why Choose Our OCR Tool</h2>
            <p>Experience the most advanced image to text conversion technology</p>
        </div>
        
        <div class="features">
            <div class="feature-card">
                <div class="feature-icon">
                    <i class="fas fa-tachometer-alt"></i>
                </div>
                <h3>Lightning Fast</h3>
                <p>Process documents in seconds with our optimized OCR engine that handles even complex layouts with ease.</p>
            </div>
            <div class="feature-card">
                <div class="feature-icon">
                    <i class="fas fa-language"></i>
                </div>
                <h3>100+ Languages</h3>
                <p>Supports text extraction in multiple languages including English, Spanish, Chinese, Arabic and more.</p>
            </div>
            <div class="feature-card">
                <div class="feature-icon">
                    <i class="fas fa-shield-alt"></i>
                </div>
                <h3>Secure Processing</h3>
                <p>Your documents are processed securely and never stored on our servers after conversion.</p>
            </div>
        </div>
    </section>
    
    <section class="container" id="how-it-works">
        <div class="section-title">
            <h2>How It Works</h2>
            <p>Convert your images to text in just 3 simple steps</p>
        </div>
        
        <div class="steps">
            <div class="step">
                <div class="step-number">1</div>
                <div class="step-content">
                    <h3>Upload Your File</h3>
                    <p>Drag and drop your image or PDF file into the upload area or click to browse your files.</p>
                </div>
            </div>
            <div class="step">
                <div class="step-number">2</div>
                <div class="step-content">
                    <h3>AI Processing</h3>
                    <p>Our advanced OCR technology analyzes your document and extracts text with high accuracy.</p>
                </div>
            </div>
            <div class="step">
                <div class="step-number">3</div>
                <div class="step-content">
                    <h3>Get Your Text</h3>
                    <p>View, edit, copy or download the extracted text in your preferred format.</p>
                </div>
            </div>
        </div>
    </section>
    
    <section class="container" id="faq">
        <div class="section-title">
            <h2>Frequently Asked Questions</h2>
            <p>Find answers to common questions about our OCR tool</p>
        </div>
        
        <div class="faq-container">
            <div class="faq-item">
                <div class="faq-question">
                    What file formats do you support?
                    <i class="fas fa-chevron-down"></i>
                </div>
                <div class="faq-answer">
                    <p>We support JPG, PNG, BMP, TIFF, and PDF files. The maximum file size is 10MB. For best results, use clear, high-resolution images with good contrast between text and background.</p>
                </div>
            </div>
            <div class="faq-item">
                <div class="faq-question">
                    Is there a limit to how many images I can convert?
                    <i class="fas fa-chevron-down"></i>
                </div>
                <div class="faq-answer">
                    <p>No, you can convert as many images as you need. Our free version has no limits, though we may implement rate limiting for very high volume usage to ensure service quality for all users.</p>
                </div>
            </div>
            <div class="faq-item">
                <div class="faq-question">
                    How accurate is the text extraction?
                    <i class="fas fa-chevron-down"></i>
                </div>
                <div class="faq-answer">
                    <p>Accuracy depends on image quality, but our advanced OCR technology typically achieves 95%+ accuracy for clear images. Handwriting recognition accuracy varies more but works well for neat handwriting.</p>
                </div>
            </div>
            <div class="faq-item">
                <div class="faq-question">
                    Is my data secure?
                    <i class="fas fa-chevron-down"></i>
                </div>
                <div class="faq-answer">
                    <p>Absolutely. Your files are processed securely and automatically deleted from our servers after conversion. We don't store your documents or extracted text unless you explicitly choose to save them.</p>
                </div>
            </div>
        </div>
    </section>
    
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>Image2Text Pro</h3>
                    <p>Advanced OCR technology to convert your images and documents into editable text quickly and accurately.</p>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-linkedin-in"></i></a>
                    </div>
                </div>
                <div class="footer-column">
                    <h3>Quick Links</h3>
                    <ul>
                        <li><a href="#">Home</a></li>
                        <li><a href="#features">Features</a></li>
                        <li><a href="#how-it-works">How It Works</a></li>
                        <li><a href="#faq">FAQ</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Resources</h3>
                    <ul>
                        <li><a href="#">Blog</a></li>
                        <li><a href="#">Documentation</a></li>
                        <li><a href="#">API</a></li>
                        <li><a href="#">Support</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Legal</h3>
                    <ul>
                        <li><a href="#">Privacy Policy</a></li>
                        <li><a href="#">Terms of Service</a></li>
                        <li><a href="#">Cookie Policy</a></li>
                        <li><a href="#">GDPR</a></li>
                    </ul>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2023 Image2Text Pro. All rights reserved.</p>
            </div>
        </div>
    </footer>
    
    <script>
        document.addEventListener('DOMContentLoaded', function() {
            // File upload elements
            const fileInput = document.getElementById('fileInput');
            const uploadBtn = document.getElementById('uploadBtn');
            const dropArea = document.getElementById('dropArea');
            const previewImage = document.getElementById('previewImage');
            const resultText = document.getElementById('resultText');
            const copyBtn = document.getElementById('copyBtn');
            const downloadBtn = document.getElementById('downloadBtn');
            const clearBtn = document.getElementById('clearBtn');
            const uploadSpinner = document.getElementById('uploadSpinner');
            const startConvertingBtn = document.getElementById('startConvertingBtn');
            
            // Scroll to tool section when "Start Converting" is clicked
            startConvertingBtn.addEventListener('click', function() {
                document.querySelector('.tool-section').scrollIntoView({
                    behavior: 'smooth'
                });
            });
            
            // Handle file selection via button
            uploadBtn.addEventListener('click', function() {
                fileInput.click();
            });
            
            // Handle file selection
            fileInput.addEventListener('change', function(e) {
                if (e.target.files.length) {
                    handleFile(e.target.files[0]);
                }
            });
            
            // Drag and drop functionality
            ['dragenter', 'dragover', 'dragleave', 'drop'].forEach(eventName => {
                dropArea.addEventListener(eventName, preventDefaults, false);
            });
            
            function preventDefaults(e) {
                e.preventDefault();
                e.stopPropagation();
            }
            
            ['dragenter', 'dragover'].forEach(eventName => {
                dropArea.addEventListener(eventName, highlight, false);
            });
            
            ['dragleave', 'drop'].forEach(eventName => {
                dropArea.addEventListener(eventName, unhighlight, false);
            });
            
            function highlight() {
                dropArea.classList.add('active');
            }
            
            function unhighlight() {
                dropArea.classList.remove('active');
            }
            
            dropArea.addEventListener('drop', function(e) {
                const dt = e.dataTransfer;
                const file = dt.files[0];
                handleFile(file);
            });
            
            // Process the selected file
            function handleFile(file) {
                // Check file type
                const validTypes = ['image/jpeg', 'image/png', 'image/bmp', 'image/tiff', 'application/pdf'];
                if (!validTypes.includes(file.type)) {
                    showAlert('Please upload a valid image file (JPG, PNG, BMP, TIFF) or PDF', 'error');
                    return;
                }
                
                // Check file size (max 10MB)
                if (file.size > 10 * 1024 * 1024) {
                    showAlert('File size exceeds 10MB limit', 'error');
                    return;
                }
                
                // Show preview for images (not PDF)
                if (file.type.includes('image')) {
                    const reader = new FileReader();
                    reader.onload = function(e) {
                        previewImage.src = e.target.result;
                        previewImage.style.display = 'block';
                    };
                    reader.readAsDataURL(file);
                } else {
                    previewImage.style.display = 'none';
                }
                
                // Simulate OCR processing (in a real app, you would use Tesseract.js or an API)
                uploadSpinner.style.display = 'block';
                resultText.textContent = "Processing your file...";
                dropArea.classList.add('active');
                
                setTimeout(function() {
                    // This is a simulation - in a real app, you would use actual OCR here
                    uploadSpinner.style.display = 'none';
                    resultText.textContent = "This is a simulation of extracted text from your image.\n\nIn a real implementation, you would use Tesseract.js or an OCR API like Google Cloud Vision to extract actual text from the image.\n\nFirst line of extracted text\nSecond line of extracted text\nThird line with some more content\n\nYou can edit this text directly or use the buttons below to copy or download it.";
                    
                    // Enable buttons
                    copyBtn.disabled = false;
                    downloadBtn.disabled = false;
                    clearBtn.disabled = false;
                    
                    showAlert('Text extracted successfully!', 'success');
                }, 2000);
            }
            
            // Copy text to clipboard
            copyBtn.addEventListener('click', function() {
                const text = resultText.textContent;
                navigator.clipboard.writeText(text).then(function() {
                    copyBtn.innerHTML = '<i class="fas fa-check"></i> Copied!';
                    setTimeout(function() {
                        copyBtn.innerHTML = '<i class="fas fa-copy"></i> Copy Text';
                    }, 2000);
                }).catch(function() {
                    showAlert('Failed to copy text', 'error');
                });
            });
            
            // Download text as file
            downloadBtn.addEventListener('click', function() {
                const text = resultText.textContent;
                const blob = new Blob([text], {type: 'text/plain'});
                const url = URL.createObjectURL(blob);
                const a = document.createElement('a');
                a.href = url;
                a.download = 'extracted-text.txt';
                document.body.appendChild(a);
                a.click();
                document.body.removeChild(a);
                URL.revokeObjectURL(url);
            });
            
            // Clear everything
            clearBtn.addEventListener('click', function() {
                fileInput.value = '';
                previewImage.style.display = 'none';
                resultText.textContent = '';
                copyBtn.disabled = true;
                downloadBtn.disabled = true;
                clearBtn.disabled = true;
                dropArea.classList.remove('active');
            });
            
            // FAQ accordion
            const faqItems = document.querySelectorAll('.faq-item');
            faqItems.forEach(item => {
                const question = item.querySelector('.faq-question');
                question.addEventListener('click', () => {
                    item.classList.toggle('active');
                });
            });
            
            // Show alert message
            function showAlert(message, type) {
                // In a real app, you would implement a proper alert/notification system
                console.log(`${type}: ${message}`);
            }
        });
    </script>
    
    <!-- Structured data for SEO -->
    <script type="application/ld+json">
    {
      "@context": "https://schema.org",
      "@type": "WebApplication",
      "name": "Image2Text Pro - Advanced OCR Converter",
      "url": "https://yourwebsite.com/image-to-text",
      "description": "Free online tool to extract text from images (OCR). Convert JPG, PNG, PDF to editable text instantly with AI-powered technology.",
      "applicationCategory": "UtilityApplication",
      "operatingSystem": "Any",
      "offers": {
        "@type": "Offer",
        "price": "0",
        "priceCurrency": "USD"
      },
      "creator": {
        "@type": "Organization",
        "name": "Image2Text Pro"
      },
      "aggregateRating": {
        "@type": "AggregateRating",
        "ratingValue": "4.8",
        "reviewCount": "124"
      }
    }
    </script>
</body>
</html>
