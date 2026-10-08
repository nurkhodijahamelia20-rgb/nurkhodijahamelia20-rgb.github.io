<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portofolio - Nur Khodijah Amelia</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Plus Jakarta Sans', 'Segoe UI', sans-serif;
            scroll-behavior: smooth;
        }

        :root {
            --bg-color: #0b0f19;
            --card-bg: #151c2c;
            --text-main: #f8fafc;
            --text-muted: #94a3b8;
            --primary: #38bdf8;
            --accent: #6366f1;
            --border-color: #1e293b;
        }

        body {
            background-color: var(--bg-color);
            color: var(--text-main);
            line-height: 1.6;
        }

        header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 8%;
            background-color: rgba(11, 15, 25, 0.85);
            position: sticky;
            top: 0;
            z-index: 100;
            backdrop-filter: blur(12px);
            border-bottom: 1px solid var(--border-color);
        }

        .logo {
            font-size: 1.3rem;
            font-weight: 700;
            background: linear-gradient(to right, var(--primary), var(--accent));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        nav a {
            color: var(--text-muted);
            text-decoration: none;
            margin-left: 20px;
            font-size: 0.95rem;
            font-weight: 500;
            transition: 0.3s;
        }

        nav a:hover {
            color: var(--primary);
        }

        .hero {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            min-height: 85vh;
            text-align: center;
            padding: 40px 20px;
        }

        .profile-img {
            width: 180px;
            height: 180px;
            border-radius: 50%;
            object-fit: cover;
            border: 4px solid var(--primary);
            box-shadow: 0 0 30px rgba(56, 189, 248, 0.25);
            margin-bottom: 25px;
            transition: transform 0.3s;
        }

        .profile-img:hover {
            transform: scale(1.05);
        }

        .hero h1 {
            font-size: 3rem;
            font-weight: 800;
            margin-bottom: 10px;
            background: linear-gradient(to right, var(--primary), var(--accent));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .hero h3 {
            color: var(--primary);
            font-weight: 600;
            margin-bottom: 15px;
            letter-spacing: 0.5px;
        }

        .hero p {
            font-size: 1.1rem;
            color: var(--text-muted);
            max-width: 750px;
            margin-bottom: 30px;
        }

        .btn {
            display: inline-block;
            padding: 12px 32px;
            background: linear-gradient(135deg, var(--primary), var(--accent));
            color: #ffffff;
            font-weight: 600;
            border-radius: 30px;
            text-decoration: none;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(56, 189, 248, 0.2);
        }

        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(56, 189, 248, 0.4);
        }

        section {
            padding: 70px 8%;
        }

        .section-title {
            font-size: 2.2rem;
            font-weight: 700;
            margin-bottom: 40px;
            text-align: center;
            position: relative;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 60px;
            height: 4px;
            background: linear-gradient(to right, var(--primary), var(--accent));
            margin: 12px auto 0;
            border-radius: 2px;
        }

        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 25px;
        }

        .card {
            background-color: var(--card-bg);
            padding: 30px;
            border-radius: 16px;
            border: 1px solid var(--border-color);
            transition: all 0.3s ease;
        }

        .card:hover {
            transform: translateY(-7px);
            border-color: var(--primary);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        }

        .card i {
            font-size: 2.2rem;
            color: var(--primary);
            margin-bottom: 18px;
        }

        .card h3 {
            font-size: 1.25rem;
            margin-bottom: 8px;
            color: var(--text-main);
        }

        .card h4 {
            color: var(--primary);
            font-size: 0.95rem;
            font-weight: 600;
            margin-bottom: 12px;
        }

        .card p, .card ul {
            color: var(--text-muted);
            font-size: 0.95rem;
        }

        .card ul {
            padding-left: 20px;
        }

        .card ul li {
            margin-bottom: 8px;
        }

        .skills-container {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
            justify-content: center;
        }

        .skill-badge {
            background-color: var(--card-bg);
            border: 1px solid var(--border-color);
            color: var(--primary);
            padding: 10px 20px;
            border-radius: 30px;
            font-size: 0.95rem;
            font-weight: 500;
            transition: 0.3s;
        }

        .skill-badge:hover {
            border-color: var(--primary);
            background-color: rgba(56, 189, 248, 0.1);
        }

        /* Galeri Dokumentasi Foto */
        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 20px;
        }

        .gallery-item {
            position: relative;
            border-radius: 16px;
            overflow: hidden;
            border: 1px solid var(--border-color);
            height: 240px;
        }

        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.4s ease;
        }

        .gallery-item:hover img {
            transform: scale(1.08);
        }

        .gallery-caption {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            padding: 15px;
            background: linear-gradient(to top, rgba(11, 15, 25, 0.9), transparent);
            color: var(--text-main);
            font-size: 0.9rem;
            font-weight: 600;
        }

        .socials {
            display: flex;
            justify-content: center;
            gap: 25px;
            margin-top: 25px;
        }

        .socials a {
            color: var(--text-main);
            font-size: 1.8rem;
            transition: all 0.3s;
        }

        .socials a:hover {
            color: var(--primary);
            transform: translateY(-3px);
        }

        footer {
            text-align: center;
            padding: 30px;
            background-color: #070a12;
            color: var(--text-muted);
            font-size: 0.9rem;
            border-top: 1px solid var(--border-color);
        }

        @media (max-width: 768px) {
            .hero h1 { font-size: 2.2rem; }
            header { padding: 15px 5%; }
            section { padding: 50px 5%; }
        }
    </style>
</head>
<body>

    <header>
        <div class="logo">Nur Khodijah Amelia</div>
        <nav>
            <a href="#about">Tentang</a>
            <a href="#education">Pendidikan</a>
            <a href="#skills">Keahlian</a>
            <a href="#experience">Pengalaman</a>
            <a href="#documentation">Dokumentasi</a>
            <a href="#contact">Kontak</a>
        </nav>
    </header>

    <section class="hero">
        <img src="profile.jpg" alt="Nur Khodijah Amelia" class="profile-img">
        <h1>Nur Khodijah Amelia</h1>
        <h3>S1 Sistem Informasi | Universitas Gunadarma</h3>
        <p>Mahasiswa aktif Sistem Informasi dengan IPK 3.83. Memiliki kepemimpinan kuat sebagai mantan Ketua OSIS 2 periode, Secretariat General di Generasi Energi Bersih, serta berpengalaman dalam manajemen administrasi, pemrosesan data, hingga kreativitas media (Video & Graphic Editing).</p>
        <a href="#contact" class="btn">Hubungi Saya</a>
    </section>

    <section id="about">
        <h2 class="section-title">Tentang Saya</h2>
        <div style="text-align: center; max-width: 800px; margin: 0 auto; color: var(--text-muted);">
            <p>Mahasiswa yang aktif, komunikatif, dan terampil dalam tata kelola organisasi. Berpengalaman memimpin organisasi sekolah 2 periode berturut-turut, memegang posisi Sekretariat Jenderal di organisasi energi bersih, serta berpartisipasi aktif dalam forum nasional & internasional. Memiliki kombinasi keahlian IT (SQL, Java, AI Agent), tata kelola administrasi, serta kemampuan kreatif pembuatan konten media (Video & Photo Editing).</p>
        </div>
    </section>

    <section id="education">
        <h2 class="section-title">Pendidikan</h2>
        <div class="grid">
            <div class="card">
                <i class="fa-solid fa-graduation-cap"></i>
                <h3>Universitas Gunadarma</h3>
                <h4>S1 Sistem Informasi (2024 - Present)</h4>
                <p>IPK: 3.83 / 4.00 | Aktif dalam kegiatan akademik dan keorganisasian kampus.</p>
            </div>
            <div class="card">
                <i class="fa-solid fa-school"></i>
                <h3>SMK AD-DA'WAH</h3>
                <h4>Teknik Komputer dan Jaringan (2021 - 2024)</h4>
                <p>Nilai Rata-rata: 81 / 100 | Dipercaya menjadi Ketua OSIS selama 2 periode (Kelas 10 & 11).</p>
            </div>
        </div>
    </section>

    <section id="skills">
        <h2 class="section-title">Kemampuan & Keahlian</h2>
        <div class="skills-container">
            <span class="skill-badge"><i class="fa-solid fa-file-signature"></i> Secretariat & Administrative Management</span>
            <span class="skill-badge"><i class="fa-solid fa-crown"></i> Leadership & Strategic Planning</span>
            <span class="skill-badge"><i class="fa-solid fa-video"></i> Video Editing & Content Creation</span>
            <span class="skill-badge"><i class="fa-solid fa-image"></i> Graphic Design & Photo Editing</span>
            <span class="skill-badge"><i class="fa-solid fa-robot"></i> AI Agent Building (IBM)</span>
            <span class="skill-badge"><i class="fa-solid fa-code"></i> Pemrograman Java & SQL</span>
            <span class="skill-badge"><i class="fa-solid fa-database"></i> Microsoft Office & Administrasi Data</span>
            <span class="skill-badge"><i class="fa-solid fa-comments"></i> Public Speaking & Event Management</span>
        </div>
    </section>

    <section id="experience">
        <h2 class="section-title">Pengalaman Kerja & Organisasi</h2>
        <div class="grid">
            <div class="card">
                <i class="fa-solid fa-file-signature"></i>
                <h3>Secretariat General</h3>
                <h4>Generasi Energi Bersih (Present)</h4>
                <ul>
                    <li>Mengelola seluruh administrasi, tata kelola dokumen resmi, serta alur komunikasi internal dan eksternal organisasi.</li>
                    <li>Menyusun dan mengoordinasikan jadwal rapat, agenda kerja, serta laporan berkala organisasi.</li>
                    <li>Mendukung kampanye publik dan advokasi transisi energi bersih melalui koordinasi tim dan pengelolaan media digital.</li>
                </ul>
            </div>
            <div class="card">
                <i class="fa-solid fa-crown"></i>
                <h3>Ketua OSIS (2 Periode)</h3>
                <h4>SMK AD-DA'WAH (2021 - 2023)</h4>
                <ul>
                    <li>Dipercaya memimpin seluruh pengurus OSIS selama 2 periode berturut-turut sejak kelas 10 hingga kelas 11.</li>
                    <li>Mengarahkan, merencanakan, dan mengawasi eksekusi seluruh program kerja kesiswaan dan acara besar sekolah.</li>
                    <li>Menjadi jembatan komunikasi utama antara seluruh siswa dengan pihak sekolah.</li>
                </ul>
            </div>
            <div class="card">
                <i class="fa-solid fa-briefcase"></i>
                <h3>Praktik Kerja Lapangan (PKL)</h3>
                <h4>Singa Asia - Harco Mangga Dua (Jan - Apr 2023)</h4>
                <ul>
                    <li><strong>Administrasi Data:</strong> Mengelola alur barang masuk/keluar serta data harga sistem.</li>
                    <li><strong>Teknisi Hardware:</strong> Perakitan PC, instalasi Windows, dan pengecekan hardware.</li>
                    <li><strong>Customer Service:</strong> Menangani keluhan pelanggan dengan koordinasi solusi cepat.</li>
                </ul>
            </div>
        </div>
    </section>

    <!-- Galeri Dokumentasi Kegiatan -->
    <section id="documentation">
        <h2 class="section-title">Dokumentasi & Kegiatan</h2>
        <div class="gallery-grid">
            <div class="gallery-item">
                <img src="doc-ccs.jpg" alt="IICCS Forum 2026">
                <div class="gallery-caption">Delegate - The 4th IICCS Forum 2026</div>
            </div>
            <div class="gallery-item">
                <img src="doc-idn.jpg" alt="Ngobrol Seru IDN Times">
                <div class="gallery-caption">Peserta - Ngobrol Seru IDN Times (Subsidi Energi)</div>
            </div>
            <div class="gallery-item">
                <img src="doc-idn2.jpg" alt="Kegiatan Forum Energi">
                <div class="gallery-caption">Diskusi Ketahanan Energi Bersama IDN Times</div>
            </div>
        </div>
    </section>

    <section id="certifications">
        <h2 class="section-title">Sertifikasi & Pelatihan</h2>
        <div class="grid">
            <div class="card">
                <i class="fa-solid fa-robot"></i>
                <h3>Build an AI Agent</h3>
                <p>IBM SkillsBuild (Okt 2026)</p>
            </div>
            <div class="card">
                <i class="fa-solid fa-certificate"></i>
                <h3>Belajar Dasar Manajemen Proyek</h3>
                <p>Dicoding Indonesia (Feb 2026)</p>
            </div>
            <div class="card">
                <i class="fa-solid fa-building"></i>
                <h3>Kunjungan Industri</h3>
                <p>PT. Primarindo Asia Infrastructure (2023)</p>
            </div>
        </div>
    </section>

    <section id="contact">
        <h2 class="section-title">Hubungi Saya</h2>
        <div style="text-align: center;">
            <p style="color: var(--text-muted); margin-bottom: 10px;">Semanan, Kalideres, Jakarta Barat</p>
            <p style="color: var(--text-muted); margin-bottom: 20px;">Email: nurkhodijahamelia20@gmail.com | WA: +62 882-1100-7698</p>
            <div class="socials">
                <a href="https://github.com/nurkhodijahamelia20-rgb" target="_blank"><i class="fa-brands fa-github"></i></a>
                <a href="mailto:nurkhodijahamelia20@gmail.com"><i class="fa-solid fa-envelope"></i></a>
                <a href="https://wa.me/6288211007698" target="_blank"><i class="fa-brands fa-whatsapp"></i></a>
            </div>
        </div>
    </section>

    <footer>
        <p>&copy; 2026 Nur Khodijah Amelia. All rights reserved.</p>
    </footer>

</body>
</html>
