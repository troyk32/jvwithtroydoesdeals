<!DOCTYPE html>
<html lang="en" data-theme="light">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JVwithTroyDoesDeals | Premium Real Estate Partnerships</title>
    <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">
    <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
    <style>
        :root {
            --primary: #2563eb;
            --secondary: #1e40af;
            --gradient: linear-gradient(135deg, #2563eb 0%, #1e40af 100%);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
        }

        body {
            background: #f8fafc;
            min-height: 100vh;
            color: #1e293b;
        }

        .hero {
            background: var(--gradient);
            padding: 4rem 2rem;
            color: white;
            text-align: center;
            clip-path: polygon(0 0, 100% 0, 100% 90%, 0 100%);
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
        }

        .form-card {
            background: white;
            border-radius: 1.5rem;
            padding: 3rem;
            box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.1);
            transform: translateY(-5rem);
            margin-bottom: -5rem;
        }

        .input-group {
            margin-bottom: 2rem;
            position: relative;
        }

        .input-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 600;
            color: #334155;
        }

        .input-group input,
        .input-group select,
        .input-group textarea {
            width: 100%;
            padding: 1rem;
            border: 2px solid #e2e8f0;
            border-radius: 0.75rem;
            font-size: 1rem;
            transition: all 0.3s ease;
        }

        .input-group input:focus,
        .input-group select:focus {
            border-color: var(--primary);
            box-shadow: 0 0 0 3px rgba(37, 99, 235, 0.1);
            outline: none;
        }

        .file-upload {
            border: 2px dashed #cbd5e1;
            padding: 2rem;
            text-align: center;
            border-radius: 1rem;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .file-upload:hover {
            border-color: var(--primary);
            background: rgba(37, 99, 235, 0.05);
        }

        .submit-btn {
            background: var(--gradient);
            color: white;
            padding: 1.25rem 2.5rem;
            border: none;
            border-radius: 0.75rem;
            font-size: 1.1rem;
            font-weight: 600;
            cursor: pointer;
            transition: transform 0.2s ease;
            width: 100%;
        }

        .submit-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1);
        }

        .feature-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin: 4rem 0;
        }

        .feature-card {
            background: white;
            padding: 2rem;
            border-radius: 1rem;
            text-align: center;
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
        }

        @media (max-width: 768px) {
            .form-card {
                padding: 2rem;
            }
        }
    </style>
</head>
<body>
    <div class="hero">
        <div class="container">
            <h1 style="font-size: 3rem; margin-bottom: 1rem;">JV with TroyDoesDeals</h1>
            <p style="font-size: 1.25rem; opacity: 0.95;">Premium Real Estate Investment Partnerships</p>
        </div>
    </div>

    <div class="container">
        <div class="form-card">
            <form id="dealForm" action="https://formspree.io/f/YOUR_FORM_ID" method="POST" enctype="multipart/form-data">
                <div class="input-group">
                    <label>Your Information</label>
                    <input type="text" name="name" placeholder="Full Name" required>
                    <input type="tel" name="phone" placeholder="Phone Number" style="margin-top: 1rem;" required>
                    <input type="email" name="email" placeholder="Email Address" style="margin-top: 1rem;" required>
                </div>

                <div class="input-group">
                    <label>Contract Details</label>
                    <div class="file-upload">
                        <p>Drag & Drop Contract PDF or Click to Upload</p>
                        <input type="file" name="contract" accept=".pdf" required style="display: none;">
                    </div>
                </div>

                <div class="input-group">
                    <label>Financial Metrics</label>
                    <input type="number" name="lockup_price" placeholder="Lockup Price ($)" step="0.01" required>
                    <input type="number" name="sale_price" placeholder="Estimated Sale Price ($)" step="0.01" style="margin-top: 1rem;" required>
                    <input type="number" name="arv_percent" placeholder="% Below ARV" step="0.01" style="margin-top: 1rem;" required>
                    <input type="number" name="zestimate_percent" placeholder="% Below Zestimate" step="0.01" style="margin-top: 1rem;" required>
                </div>

                <button type="submit" class="submit-btn">Submit Deal for Review →</button>
            </form>
        </div>

        <div class="feature-grid">
            <div class="feature-card">
                <h3>24-Hour Review</h3>
                <p>Guaranteed response within one business day</p>
            </div>
            <div class="feature-card">
                <h3>Secure Processing</h3>
                <p>Bank-level encryption for all submissions</p>
            </div>
            <div class="feature-card">
                <h3>Premium Network</h3>
                <p>Access to our nationwide buyer network</p>
            </div>
        </div>
    </div>

    <script>
        // Initialize animations
        AOS.init({
            duration: 1000,
            once: true
        });

        // File upload interaction
        const fileUpload = document.querySelector('.file-upload');
        const fileInput = document.querySelector('input[type="file"]');

        fileUpload.addEventListener('click', () => fileInput.click());
        fileInput.addEventListener('change', () => {
            if(fileInput.files.length) {
                fileUpload.innerHTML = `<p>Selected: ${fileInput.files[0].name}</p>`;
            }
        });

        // Form submission handling
        document.getElementById('dealForm').addEventListener('submit', async (e) => {
            e.preventDefault();
            const formData = new FormData(e.target);
            
            // Show loading state
            const submitBtn = document.querySelector('.submit-btn');
            submitBtn.innerHTML = 'Processing...';
            submitBtn.disabled = true;

            try {
                const response = await fetch(e.target.action, {
                    method: 'POST',
                    body: formData,
                    headers: {
                        'Accept': 'application/json'
                    }
                });

                if(response.ok) {
                    alert('Deal submitted successfully! Troy will contact you within 24 hours.');
                    e.target.reset();
                } else {
                    alert('Error submitting deal. Please try again.');
                }
            } catch (error) {
                alert('Connection error. Please check your network.');
            }

            submitBtn.innerHTML = 'Submit Deal for Review →';
            submitBtn.disabled = false;
        });
    </script>
</body>
</html>
