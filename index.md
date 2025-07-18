<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vaibhav Bommisetty - Portfolio</title>
    <!-- Load Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* Custom font import for EB Garamond (serif) */
        @import url('https://fonts.googleapis.com/css2?family=EB+Garamond:wght@400;500;600;700&display=swap');

        body {
            font-family: 'EB Garamond', serif; /* All text uses serif font */
            background-color: #FFFFFF; /* White background for the entire page */
            color: #443850; /* English Violet text for general content */
        }
        h1, h2, h3, h4, h5, h6 {
            font-family: 'EB Garamond', serif; /* Ensure headings are serif */
            color: #443850; /* English Violet for headings */
        }
        /* Smooth scroll for anchor links */
        html {
            scroll-behavior: smooth;
        }

        /* Custom Tailwind Colors - Defined for direct use */
        .bg-citron { background-color: #bbbe64; }
        .text-citron { color: #bbbe64; }
        .hover\:bg-citron-darker:hover { background-color: #a1a445; } /* Citron 400 */

        .bg-magenta_haze { background-color: #8e5572; }
        .text-magenta_haze { color: #8e5572; }
        .hover\:bg-magenta_haze-darker:hover { background-color: #73455d; } /* Magenta haze 400 */

        .bg-mint_cream { background-color: #f2f7f2; } /* Used for panes/cards */
        .text-mint_cream { color: #f2f7f2; }
        .bg-mint_cream-darker { background-color: #f7faf7; } /* Mint cream 700 for subtle hover/border */

        .bg-khaki { background-color: #bcaa99; }
        .text-khaki { color: #bcaa99; }
        .hover\:bg-khaki-darker:hover { background-color: #a28870; } /* Khaki 400 */
        .bg-khaki-lighter { background-color: #d7ccc2; } /* Khaki 700 for tags */


        .bg-english_violet { background-color: #443850; }
        .text-english_violet { color: #443850; }
        .hover\:bg-english_violet-darker:hover { background-color: #372d41; } /* English Violet 400 */


        /* General Interactive Element Transition */
        .interactive-element {
            transition: all 0.3s ease-in-out;
        }

        /* Header Navigation Links */
        .nav-link {
            position: relative;
            padding: 0.5rem 0.75rem;
            border-radius: 0.5rem;
            transition: all 0.3s ease-in-out;
        }
        .nav-link::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            background-color: #8e5572; /* Magenta Haze */
            transition: width 0.3s ease-in-out;
        }
        .nav-link:hover::after {
            width: calc(100% - 1.5rem); /* Adjust width based on padding */
        }
        .nav-link:hover {
            color: #8e5572; /* Magenta Haze */
            background-color: #f2f7f2; /* Mint Cream */
        }

        /* Button Styles */
        .btn-primary {
            background-color: #8e5572; /* Magenta Haze */
            color: white;
            font-weight: 600;
            padding: 0.75rem 2rem;
            border-radius: 0.5rem;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
            transition: all 0.3s ease-in-out;
        }
        .btn-primary:hover {
            background-color: #73455d; /* Magenta Haze 400 */
            transform: translateY(-3px); /* More pronounced lift */
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.2); /* More prominent shadow */
        }

        .btn-secondary {
            background-color: #bcaa99; /* Khaki */
            color: #443850; /* English Violet */
            font-weight: 600;
            padding: 0.5rem 1.5rem;
            border-radius: 0.5rem;
            box-shadow: 0 1px 2px rgba(0, 0, 0, 0.05);
            transition: all 0.3s ease-in-out;
        }
        .btn-secondary:hover {
            background-color: #a28870; /* Khaki 400 */
            transform: translateY(-3px); /* More pronounced lift */
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); /* More prominent shadow */
        }

        /* Tag Styles */
        .tag {
            background-color: #d7ccc2; /* Khaki 700 */
            color: #443850; /* English Violet */
            font-size: 0.8rem;
            padding: 0.25rem 0.75rem;
            border-radius: 0.375rem;
            margin-right: 0.5rem;
            margin-bottom: 0.5rem;
            transition: all 0.2s ease-in-out;
        }
        .tag:hover {
            background-color: #bcaa99; /* Khaki */
            transform: translateY(-1px);
        }

        /* Card Hover Effects (Skills, Projects, Research) */
        .card-hover-effect {
            transition: all 0.3s ease-in-out;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08); /* Initial subtle shadow */
        }
        .card-hover-effect:hover {
            transform: translateY(-5px); /* Lift effect */
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.15); /* More prominent shadow */
            border-color: #8e5572; /* Magenta Haze border on hover */
        }

        /* Image Hover Effects */
        .image-hover-effect {
            transition: all 0.3s ease-in-out;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08); /* Initial subtle shadow */
        }
        .image-hover-effect:hover {
            transform: scale(1.03); /* Slight zoom */
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.15); /* More prominent shadow */
        }

        /* Profile Picture Hover Effect */
        .profile-pic-hover-effect {
            transition: all 0.3s ease-in-out;
            border-color: #bcaa99; /* Khaki */
        }
        .profile-pic-hover-effect:hover {
            transform: scale(1.05); /* Zoom, no rotation */
            border-color: #8e5572; /* Magenta Haze border on hover */
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.2);
        }
    </style>
</head>
<body class="antialiased">

    <!-- Header Section -->
    <header class="bg-white shadow-sm py-4 px-6 md:px-12 sticky top-0 z-50 rounded-b-lg">
        <nav class="container mx-auto flex justify-between items-center">
            <a href="#hero" class="text-2xl font-bold text-english_violet rounded-lg p-2 hover:bg-mint_cream transition duration-300">Vaibhav Bommisetty</a>
            <div class="space-x-4">
                <a href="#about" class="nav-link text-english_violet font-medium">About</a>
                <a href="#skills" class="nav-link text-english_violet font-medium">Skills</a>
                <a href="#projects" class="nav-link text-english_violet font-medium">Projects</a>
                <a href="#me" class="nav-link text-english_violet font-medium">Me!</a>
                <a href="#contact" class="nav-link text-english_violet font-medium">Contact</a>
            </div>
        </nav>
    </header>

    <!-- Hero/About Section -->
    <section id="hero" class="relative bg-gradient-to-r from-citron to-english_violet text-mint_cream py-20 md:py-32 flex items-center justify-center min-h-screen-75 rounded-b-3xl shadow-xl">
        <div class="container mx-auto text-center px-6">
            <!-- Place your professional headshot here -->
            <img src="https://placehold.co/150x150/443850/f2f7f2?text=Your+Photo" alt="Vaibhav Bommisetty" class="profile-pic-hover-effect rounded-full w-32 h-32 md:w-40 md:h-40 mx-auto mb-6 border-4 shadow-lg">
            <h1 class="text-4xl md:text-6xl font-extrabold leading-tight mb-4">
                Hi, I'm Vaibhav Bommisetty
            </h1>
            <p class="text-xl md:text-2xl font-light mb-8 max-w-3xl mx-auto text-khaki">
                A passionate Data Scientist and aspiring Software Data Engineer, building scalable solutions for complex data challenges.
            </p>
            <a href="#projects" class="btn-primary">
                View My Work
            </a>
        </div>
    </section>

    <!-- About Me Section (More detailed bio) -->
    <section id="about" class="py-16 md:py-24 bg-white mx-4 md:mx-auto max-w-6xl mt-8">
        <div class="container mx-auto px-6">
            <h2 class="text-4xl font-bold text-center mb-12">About Me</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-12 items-center">
                <div class="text-lg leading-relaxed text-english_violet space-y-4">
                    <p>I'm a recent graduate from the University of California - San Diego with a Bachelor of Science in Data Science, driven by a passion for transforming raw data into actionable insights and robust, scalable systems.</p>
                    <p>My academic journey and extensive project work have equipped me with a strong foundation in distributed computing, machine learning, and data pipeline development. I thrive on tackling complex data challenges, from designing efficient ETL processes to building predictive models and optimizing large-scale data workflows.</p>
                    <p>I am particularly excited about the intersection of data engineering and health technology, seeking to contribute to innovative solutions that leverage data for real-world impact. My goal is to engineer high-quality, reliable data platforms that empower advanced analytics and drive product development.</p>
                </div>
                <div class="card-hover-effect bg-mint_cream p-8 rounded-xl border border-english_violet">
                    <h3 class="text-2xl font-semibold mb-4 text-magenta_haze">Education</h3>
                    <p class="text-lg text-english_violet mb-2">**University of California - San Diego**</p>
                    <p class="text-md text-english_violet">Bachelor of Science in Data Science</p>
                    <p class="text-md text-english_violet">Expected Graduation: August 2025</p>
                    <ul class="list-disc list-inside text-english_violet mt-4 space-y-1">
                        <li>Relevant Coursework: Data Science in Practice (Python, Git, PySpark), Relational Databases (SQL, PostgreSQL), Scalable Analytics (AWS, Apache Spark, Cloud Data Warehousing), Data Visualization, Statistical Modeling, Machine Learning.</li>
                        <li>Activities: VP of Public Relations & Marketing, VP of Membership Alpha Kappa Psi, Data Science Students Society.</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills" class="py-16 md:py-24 bg-white mx-4 md:mx-auto max-w-6xl mt-8">
        <div class="container mx-auto px-6">
            <h2 class="text-4xl font-bold text-center mb-12">My Skills</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Skill Category 1 -->
                <div class="card-hover-effect bg-mint_cream p-6 rounded-xl border border-english_violet">
                    <h3 class="text-2xl font-semibold text-magenta_haze mb-4">Programming Languages & Frameworks</h3>
                    <ul class="list-disc list-inside text-english_violet space-y-2">
                        <li>Python (Object-Oriented, Functional, Pandas, NumPy, PySpark, TensorFlow, PyTorch, Sklearn)</li>
                        <li>SQL (PostgreSQL, MySQL)</li>
                        <li>Java</li>
                        <li>Shell Scripting</li>
                        <li>R, JavaScript</li>
                    </ul>
                </div>
                <!-- Skill Category 2 -->
                <div class="card-hover-effect bg-mint_cream p-6 rounded-xl border border-english_violet">
                    <h3 class="text-2xl font-semibold text-magenta_haze mb-4">Distributed Computing & Cloud Platforms</h3>
                    <ul class="list-disc list-inside text-english_violet space-y-2">
                        <li>Apache Spark, Hadoop, PySpark, SparkSQL</li>
                        <li>AWS (S3, EMR, EC2)</li>
                        <li>Azure, Kubernetes</li>
                        <li>ETL Processes, Data Cleansing</li>
                    </ul>
                </div>
                <!-- Skill Category 3 -->
                <div class="card-hover-effect bg-mint_cream p-6 rounded-xl border border-english_violet">
                    <h3 class="text-2xl font-semibold text-magenta_haze mb-4">Data Engineering & Development Tools</h3>
                    <ul class="list-disc list-inside text-english_violet space-y-2">
                        <li>Git, GitHub, Terminal</li>
                        <li>Jupyter Notebook</li>
                        <li>Microsoft Excel, Microsoft Office</li>
                        <li>Tableau, Power BI</li>
                        <li>Feature Engineering, Data Quality</li>
                    </ul>
                </div>
                <!-- Skill Category 4 (Combined Analytics & ML for conciseness) -->
                <div class="card-hover-effect bg-mint_cream p-6 rounded-xl border border-english_violet col-span-1 md:col-span-2 lg:col-span-1">
                    <h3 class="text-2xl font-semibold text-magenta_haze mb-4">Analytics & Machine Learning</h3>
                    <ul class="list-disc list-inside text-english_violet space-y-2">
                        <li>Statistical Modeling, Machine Learning</li>
                        <li>Exploratory Data Analysis (EDA)</li>
                        <li>Data Visualization, Scalable ML Workloads</li>
                        <li>Signal Processing, Numeric Methods</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="py-16 md:py-24 bg-white mx-4 md:mx-auto max-w-6xl mt-8">
        <div class="container mx-auto px-6">
            <h2 class="text-4xl font-bold text-center mb-12">My Projects</h2>

            <!-- Project 1: Recipes -->
            <div class="project-card card-hover-effect bg-mint_cream p-8 rounded-xl mb-12 border border-english_violet">
                <img src="https://placehold.co/600x300/bbbe64/443850?text=Recipe+Predictor" alt="Recipe Predictor Project" class="project-image">
                <h3 class="text-3xl font-bold text-magenta_haze mb-4">Recipes: User Interaction Predictor (Recommender System)</h3>
                <p class="text-english_violet mb-4 leading-relaxed">
                    This project involved developing a sophisticated predictive model to classify user interactions with recipes from a large dataset. By leveraging advanced popularity heuristics and similarity functions, the model achieved strong predictive performance. The work included comprehensive exploratory data analysis, meticulous feature engineering, and robust data cleaning processes to ensure model stability and performance.
                </p>
                <div class="mb-6">
                    <span class="tag">Python</span>
                    <span class="tag">Scikit-learn</span>
                    <span class="tag">Predictive Modeling</span>
                    <span class="tag">Feature Engineering</span>
                    <span class="tag">EDA</span>
                    <span class="tag">Data Cleaning</span>
                </div>
                <div class="mt-6 flex flex-wrap gap-4">
                    <a href="https://github.com/vbommisetty/Recipes" target="_blank" class="btn-primary">
                        View Code
                    </a>
                    <a href="https://github.com/vbommisetty/Recipes/blob/main/Assignment%202%20Write%20Up%20(1).pdf" target="_blank" class="btn-secondary">
                        View Write-up
                    </a>
                </div>
            </div>

            <!-- Project 2: Hierarchical Latent Variable Models for Neural Data Analysis -->
            <div class="project-card card-hover-effect bg-mint_cream p-8 rounded-xl mb-12 border border-english_violet">
                <img src="https://placehold.co/600x300/bbbe64/443850?text=Neural+Data+Analysis" alt="Neural Data Analysis Project" class="project-image">
                <h3 class="text-3xl font-bold text-magenta_haze mb-4">Hierarchical Latent Variable Models for Neural Data Analysis</h3>
                <p class="text-english_violet mb-4 leading-relaxed">
                    This project focused on engineering sophisticated Python-based data pipelines to ingest, clean, and filter complex neural recordings, preparing high-quality data for in-depth scientific analysis. It involved designing and implementing advanced data transformation logic to convert raw spike data into structured formats, optimizing the dataset for hierarchical latent variable modeling. The outcome was a robust framework of modular and reusable Python functions for analyzing diverse and complex neurophysiological datasets.
                </p>
                <div class="mb-6">
                    <span class="tag">Python</span>
                    <span class="tag">Data Pipelines</span>
                    <span class="tag">Neural Data</span>
                    <span class="tag">Data Transformation</span>
                    <span class="tag">Statistical Modeling</span>
                </div>
                <div class="mt-6 flex flex-wrap gap-4">
                    <a href="https://github.com/vbommisetty/Hierarchical-Latent-Variable-Models-for-Neural-Data-Analysis" target="_blank" class="btn-primary">
                        View Code
                    </a>
                </div>
            </div>

            <!-- Project 3: League of Legends Game Predictions -->
            <div class="project-card card-hover-effect bg-mint_cream p-8 rounded-xl mb-12 border border-english_violet">
                <img src="https://placehold.co/600x300/bbbe64/443850?text=LoL+Game+Predictions" alt="League of Legends Predictions Project" class="project-image">
                <h3 class="text-3xl font-bold text-magenta_haze mb-4">League of Legends Game Predictions</h3>
                <p class="text-english_violet mb-4 leading-relaxed">
                    This initiative involved constructing robust data pipelines for professional League of Legends match records, implementing rigorous cleaning and NMAR (Not Missing At Random) analysis, and validation routines to ensure high-quality data. The project innovated by engineering novel features, significantly boosting prediction accuracy by refining model inputs and mitigating overfitting. It also focused on optimizing large-scale dataset structures to enhance model efficiency for early-game outcome prediction.
                </p>
                <div class="mb-6">
                    <span class="tag">Python</span>
                    <span class="tag">Scikit-learn</span>
                    <span class="tag">Data Pipelines</span>
                    <span class="tag">NMAR Analysis</span>
                    <span class="tag">Feature Engineering</span>
                    <span class="tag">Predictive Analytics</span>
                </div>
                <div class="mt-6 flex flex-wrap gap-4">
                    <a href="https://github.com/QuennieZeng/League-of-Legends-Game-Predictions" target="_blank" class="btn-primary">
                        View Code
                    </a>
                    <a href="https://quenniezeng.github.io/League-Of-Legends-Early-Stats-Analysis/" target="_blank" class="btn-secondary">
                        View Exploratory Analysis
                    </a>
                </div>
            </div>

            <!-- Project 4: Malaria Diagnosis Algorithm -->
            <div class="project-card card-hover-effect bg-mint_cream p-8 rounded-xl mb-12 border border-english_violet">
                <img src="https://placehold.co/600x300/bbbe64/443850?text=Malaria+Diagnosis+AI" alt="Malaria Diagnosis AI Project" class="project-image">
                <h3 class="text-3xl font-bold text-magenta_haze mb-4">Malaria Diagnosis Algorithm</h3>
                <p class="text-english_violet mb-4 leading-relaxed">
                    This project involved designing and implementing scalable data ingestion pipelines to efficiently process a vast dataset of blood cell smear images, programmatically organizing them for machine learning applications. Key tasks included orchestrating image data preprocessing workflows using ImageDataGenerator for efficient scaling and batching, ensuring high-quality input for a Convolutional Neural Network (CNN) model. The optimized CNN model was successfully deployed to Android devices using TensorFlow Lite, achieving significant speed and size reductions for rapid, on-device diagnosis.
                </p>
                <div class="mb-6">
                    <span class="tag">Python</span>
                    <span class="tag">TensorFlow</span>
                    <span class="tag">CNN</span>
                    <span class="tag">Data Ingestion</span>
                    <span class="tag">Mobile Deployment</span>
                    <span class="tag">Image Processing</span>
                </div>
                <div class="mt-6 flex flex-wrap gap-4">
                    <a href="https://github.com/vbommisetty/Malaria-Diagnosis" target="_blank" class="btn-primary">
                        View Code
                    </a>
                </div>
            </div>

            <!-- Project 5: Amazon Reviews Data Engineering with Dask on AWS -->
            <div class="project-card card-hover-effect bg-mint_cream p-8 rounded-xl mb-12 border border-english_violet">
                <img src="https://placehold.co/600x300/bbbe64/443850?text=Dask+AWS+Data+Engineering" alt="Dask AWS Data Engineering Project" class="project-image">
                <h3 class="text-3xl font-bold text-magenta_haze mb-4">Scalable Data Engineering with Dask on AWS</h3>
                <p class="text-english_violet mb-4 leading-relaxed">
                    This project focused on constructing and optimizing distributed data pipelines using Dask on AWS EC2 instances. It involved scaling data processing from single-node environments to a multi-node cluster to efficiently handle terabytes of Amazon Reviews and Products datasets that exceeded conventional memory limits. Key contributions included designing and implementing feature engineering logic to build comprehensive user profiles and executing robust data consistency checks, ensuring high data quality across distributed systems.
                </p>
                <div class="mb-6">
                    <span class="tag">Python</span>
                    <span class="tag">Dask</span>
                    <span class="tag">AWS EC2</span>
                    <span class="tag">Distributed Computing</span>
                    <span class="tag">Feature Engineering</span>
                    <span class="tag">Data Quality</span>
                </div>
                <div class="mt-6 flex flex-wrap gap-4">
                    <a href="https://github.com/vbommisetty/DSC102-Dask-Amazon-Reviews" target="_blank" class="btn-primary">
                        View Code
                    </a>
                    <!-- Placeholder for Write-up if you create one for this specific project -->
                    <!-- <a href="#" target="_blank" class="btn-secondary">
                        View Write-up
                    </a> -->
                </div>
            </div>

            <!-- Project 6: Scalable ML Feature Engineering and Model Training with Apache Spark -->
            <div class="project-card card-hover-effect bg-mint_cream p-8 rounded-xl mb-12 border border-english_violet">
                <img src="https://placehold.co/600x300/bbbe64/443850?text=Spark+ML+Pipeline" alt="Spark ML Pipeline Project" class="project-image">
                <h3 class="text-3xl font-bold text-magenta_haze mb-4">Scalable ML Pipeline Development with Apache Spark</h3>
                <p class="text-english_violet mb-4 leading-relaxed">
                    This project involved engineering complex feature pipelines and training machine learning models using Apache Spark on a DSMLP cluster. It focused on processing large Amazon product and review datasets to prepare data for scalable machine learning. Key tasks included implementing diverse data transformations, such as flattening nested data, imputing missing values, and generating text embeddings with Word2Vec. The project culminated in applying dimensionality reduction (One-Hot Encoding, PCA) and training/tuning Decision Tree Regression models, demonstrating end-to-end ML pipeline development at scale.
                </p>
                <div class="mb-6">
                    <span class="tag">Python</span>
                    <span class="tag">Apache Spark</span>
                    <span class="tag">PySpark</span>
                    <span class="tag">Feature Engineering</span>
                    <span class="tag">Machine Learning</span>
                    <span class="tag">Distributed ML</span>
                </div>
                <div class="mt-6 flex flex-wrap gap-4">
                    <a href="https://github.com/vbommisetty/DSC102-Spark-ML-Features" target="_blank" class="btn-primary">
                        View Code
                    </a>
                    <!-- Placeholder for Write-up if you create one for this specific project -->
                    <!-- <a href="#" target="_blank" class="btn-secondary">
                        View Write-up
                    </a> -->
                </div>
            </div>

            <!-- Applied Learning & Research Section -->
            <h2 class="text-4xl font-bold text-center mb-12 mt-16">Applied Learning & Research</h2>

            <!-- Experience 1: UC San Diego, Design Lab -->
            <div class="card-hover-effect bg-mint_cream p-8 rounded-xl mb-12 border border-english_violet">
                <h3 class="text-3xl font-bold text-magenta_haze mb-4">University of California - San Diego, Design Lab</h3>
                <p class="text-english_violet mb-4">Scaling Paid Undergraduate Research (SPUR) Research Assistant - 20 hrs./week</p>
                <p class="text-english_violet mb-4">August 2023 - March 2024 | La Jolla, CA</p>
                <p class="text-english_violet mb-4 leading-relaxed">
                    In this research role, I analyzed and synthesized multimodal feedback from numerous interviews and surveys, leveraging Natural Language Processing techniques to extract key sentiments and inform stakeholder needs. I collaborated closely with faculty and students to gather critical feedback for an innovative online portal, ensuring it met the research community's needs, and successfully presented the completed portal to a team of faculty and administrators. A key initiative involved leading the funding group for SPUR, streamlining the process and facilitating access to significant financial support for students and their labs, enhancing research efficiency and resource allocation.
                </p>
                <div class="mb-6">
                    <span class="tag">NLP</span>
                    <span class="tag">Data Analysis</span>
                    <span class="tag">Stakeholder Communication</span>
                    <span class="tag">Project Leadership</span>
                </div>
            </div>

            <!-- Experience 2: UC Irvine - Chemistry at the Space-Time Limit -->
            <div class="card-hover-effect bg-mint_cream p-8 rounded-xl mb-12 border border-english_violet">
                <h3 class="text-3xl font-bold text-magenta_haze mb-4">University of California Irvine - Chemistry at the Space-Time Limit</h3>
                <p class="text-english_violet mb-4">Research Assistant - 40 hrs./week</p>
                <p class="text-english_violet mb-4">June 2019 - September 2019 | Irvine, CA</p>
                <p class="text-english_violet mb-4 leading-relaxed">
                    As a Research Assistant, I established standardized Python-based data processing procedures, implementing cluster and PCA algorithms to analyze and interpret large volumes of multi-dimensional Raman Spectra data, enabling efficient identification of molecular structure and composition. I pioneered an algorithm utilizing singular value decomposition (SVD) to decompose spectral data for Gaussian post-factor analysis, achieving precise determination of material crystallinity and constituents. Furthermore, I automated complex data processing workflows using PowerShell and SQL, significantly streamlining data extraction, cleaning, and formatting, which boosted data processing productivity and enhanced data quality and efficiency.
                </p>
                <div class="mb-6">
                    <span class="tag">Python</span>
                    <span class="tag">Data Processing</span>
                    <span class="tag">Automation (PowerShell, SQL)</span>
                    <span class="tag">PCA</span>
                    <span class="tag">SVD</span>
                </div>
            </div>

        </div>
    </section>

    <!-- Me! Section (Moved to be before Contact) -->
    <section id="me" class="py-16 md:py-24 bg-white mx-4 md:mx-auto max-w-6xl mt-8">
        <div class="container mx-auto px-6">
            <h2 class="text-4xl font-bold text-center mb-12">Me! Beyond the Code</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-12 items-center">
                <div class="text-lg leading-relaxed text-english_violet space-y-4">
                    <p>When I'm not immersed in data pipelines or machine learning models, I enjoy [mention a hobby, e.g., exploring hiking trails, reading historical fiction, playing competitive games]. I believe that a well-rounded life fuels creativity and problem-solving in my professional endeavors.</p>
                    <p>I'm passionate about [mention another interest, e.g., contributing to open-source projects, learning new languages, volunteering]. These experiences have taught me [mention a skill gained, e.g., the value of community, perseverance, cross-cultural communication].</p>
                    <p>I also find joy in [mention a third interest, e.g., cooking new recipes, photography, traveling]. It's through these diverse activities that I find inspiration and maintain a fresh perspective on the world and its challenges.</p>
                </div>
                <div class="grid grid-cols-1 sm:grid-cols-2 gap-6">
                    <img src="https://placehold.co/300x200/bbbe64/443850?text=Hobby+1" alt="Personal Hobby 1" class="image-hover-effect w-full h-auto rounded-xl shadow-sm border border-citron">
                    <img src="https://placehold.co/300x200/8e5572/f2f7f2?text=Hobby+2" alt="Personal Hobby 2" class="image-hover-effect w-full h-auto rounded-xl shadow-sm border border-magenta_haze">
                    <img src="https://placehold.co/300x200/bcaa99/443850?text=Hobby+3" alt="Personal Hobby 3" class="image-hover-effect w-full h-auto rounded-xl shadow-sm border border-khaki">
                    <img src="https://placehold.co/300x200/443850/f2f7f2?text=Hobby+4" alt="Personal Hobby 4" class="image-hover-effect w-full h-auto rounded-xl shadow-sm border border-english_violet">
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-16 md:py-24 bg-white mx-4 md:mx-auto max-w-6xl mt-8">
        <div class="container mx-auto text-center px-6">
            <h2 class="text-4xl font-bold mb-8">Get In Touch</h2>
            <p class="text-lg text-english_violet mb-8 max-w-2xl mx-auto">
                I'm always open to discussing new projects, collaborations, or opportunities. Feel free to reach out!
            </p>
            <div class="flex flex-col md:flex-row justify-center items-center gap-6">
                <a href="mailto:bommisettyvaibhav@gmail.com" class="btn-primary inline-flex items-center">
                    <svg class="w-5 h-5 mr-3" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path d="M2.003 5.884L10 9.882l7.997-3.998A2 2 0 0016 4H4a2 2 0 00-1.997 1.884z"></path><path d="M18 8.118l-8 4-8-4V14a2 2 0 002 2h12a2 2 0 002-2V8.118z"></path></svg>
                    Email Me
                </a>
                <a href="https://linkedin.com/in/vaibhav-bommisetty/" target="_blank" class="inline-flex items-center bg-khaki text-english_violet font-semibold py-3 px-8 rounded-full shadow-lg hover:bg-khaki-darker transition duration-300 transform hover:scale-105">
                    <svg class="w-5 h-5 mr-3" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true"><path d="M0 0h24v24H0z" fill="none"/><path d="M19 3a2 2 0 012 2v14a2 2 0 01-2 2H5a2 2 0 01-2-2V5a2 2 0 012-2h14m-.5 15.5v-5.3h-2.7v5.3h-3.2V9.5h3.2v1.8c.4-.7 1.2-1.8 2.9-1.8 2.1 0 3.7 1.4 3.7 4.5v6.3h-3.2zM7 8.3c-1.1 0-1.8-.7-1.8-1.6 0-.9.7-1.6 1.8-1.6 1.1 0 1.8.7 1.8 1.6 0 .9-.7 1.6-1.8 1.6zM8.6 19.5H5.4V9.5h3.2v10z"/></svg>
                    LinkedIn
                </a>
                <a href="https://github.com/vbommisetty/" target="_blank" class="inline-flex items-center bg-english_violet text-mint_cream font-semibold py-3 px-8 rounded-full shadow-lg hover:bg-english_violet-darker transition duration-300 transform hover:scale-105">
                    <svg class="w-5 h-5 mr-3" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M10 0C4.477 0 0 4.477 0 10c0 4.418 2.865 8.167 6.839 9.488.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.604-3.369-1.34-3.369-1.34-.455-1.157-1.11-1.464-1.11-1.464-.908-.62.069-.608.069-.608 1.004.07 1.532 1.03 1.532 1.03.89 1.529 2.34 1.087 2.91.83.09-.645.348-1.087.634-1.337-2.22-.253-4.555-1.11-4.555-4.943 0-1.09.39-1.984 1.03-2.68-.104-.253-.448-1.27.098-2.65 0 0 .84-.268 2.75 1.025.798-.222 1.644-.333 2.488-.337.844.004 1.69.115 2.488.337 1.91-1.293 2.75-1.025 2.75-1.025.546 1.38.202 2.397.098 2.65.64.696 1.03 1.59 1.03 2.68 0 3.841-2.339 4.686-4.567 4.935.359.308.678.915.678 1.846 0 1.337-.012 2.419-.012 2.747 0 .268.18.579.688.482C17.14 18.167 20 14.418 20 10c0-5.523-4.477-10-10-10z" clip-rule="evenodd"></path></svg>
                    GitHub
                </a>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-english_violet text-mint_cream py-8 mt-12 rounded-t-lg">
        <div class="container mx-auto text-center px-6">
            <p>&copy; 2025 Vaibhav Bommisetty. All rights reserved.</p>
            <div class="flex justify-center space-x-6 mt-4">
                <a href="https://linkedin.com/in/vaibhav-bommisetty/" target="_blank" class="text-khaki hover:text-mint_cream transition duration-300">LinkedIn</a>
                <a href="https://github.com/vbommisetty/" target="_blank" class="text-khaki hover:text-mint_cream transition duration-300">GitHub</a>
                <a href="mailto:bommisettyvaibhav@gmail.com" class="text-khaki hover:text-mint_cream transition duration-300">Email</a>
            </div>
        </div>
    </footer>

</body>
</html>
