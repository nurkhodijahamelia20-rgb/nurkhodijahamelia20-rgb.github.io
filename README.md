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
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        :root {
            --bg-color: #0f172a;
            --card-bg: #1e293b;
            --text-main: #f8fafc;
            --text-muted: #94a3b8;
            --primary: #38bdf8;
            --accent: #818cf8;
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
            padding: 20px 10%;
            background-color: rgba(15, 23, 42, 0.9);
            position: sticky;
            top: 0;
            z-index: 100;
            backdrop-filter: blur(10px);
            border-bottom: 1px solid #334155;
        }

        .logo {
            font-size: 1.2rem;
            font-weight: bold;
            color: var(--primary);
        }

        nav a {
            color: var(--text-muted);
            text-decoration: none;
            margin-left: 20px;
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
            min-height: 70vh;
            text-align: center;
            padding: 40px 20px;
        }

        .hero h1 {
            font-size: 2.8rem;
            margin-bottom: 10px;
            background: linear-gradient(to right, var(--primary), var(--accent));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .hero h3 {
            color: var(--primary);
            font-weight: 500;
            margin-bottom: 15px;
        }

        .hero p {
            font-size: 1.05rem;
            color: var(--text-muted);
            max-width: 750px;
            margin-bottom: 25px;
        }

        .btn {
            display: inline-block;
            padding: 12px 28px;
            background: linear-gradient(to right, var(--primary), var(--accent));
            color: #0f172a;
            font-weight: bold;
            border-radius: 25px;
            text-decoration: none;
            transition: transform 0.2s, box-shadow 0.2s;
        }

        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(56, 189, 248, 0.3);
        }

        section {
            padding: 60px 10%;
        }

        .section-title {
            font-size: 2rem;
            margin-bottom: 30px;
            text-align: center;
            position: relative;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 50px;
            height: 4px;
            background: var(--primary);
            margin: 10px auto 0;
            border-radius: 2px;
        }

        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 20px;
        }

        .card {
            background-color: var(--card-bg);
            padding: 25px;
            border-radius: 12px;
            border: 1px solid #334155;
            transition: transform 0.3s, border-color 0.3s;
        }

        .card:hover {
            transform: translateY(-5px);
            border-color: var(--primary);
        }

        .card i {
            font-size: 2rem;
            color: var(--primary);
            margin-bottom: 15px;
        }

        .card h3 {
            margin-bottom: 8px;
            color: var(--text-main);
        }

        .card h4 {
            color: var(--primary);
            font-size: 0.95rem;
            margin-bottom: 10px;
        }

        .card p, .card ul {
            color: var(--text-muted);
            font-size: 0.95rem;
        }

        .card ul {
            padding-left: 20px;
        }

        .skills-container {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
            justify-content: center;
        }

        .skill-badge {
            background-color: var(--card-bg);
            border: 1px solid #334155;
            color: var(--primary);
            padding: 8px 16px;
            border-radius: 20px;
            font-size: 0.95rem;
        }

        .socials {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 20px;
        }

        .socials a {
            color: var(--text-main);
            font-size: 1.5rem;
            transition: color 0.3s;
        }

        .socials a:hover {
            color: var(--primary);
        }

        footer {
            text-align: center;
            padding: 30px;
            background-color: #0b1120;
            color: var(--text-muted);
            font-size: 0.9rem;
            border-top: 1px solid #334155;
        }

        @media (max-width: 768px) {
            .hero h1 { font-size: 2.2rem; }
            header { padding: 15px 5%; }
            section { padding: 40px 5%; }
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
            <a href="#contact">Kontak</a>
        </nav>
    </header>

    <section class="hero">
        <h1>Nur Khodijah Amelia</h1>
        <h3>S1 Sistem Informasi | Universitas Gunadarma</h3>
        <p>Mahasiswa Sistem Informasi dengan IPK 3.83 dan latar belakang Teknik Komputer dan Jaringan. Memiliki keahlian teknis dalam pemrograman Java, database SQL, administrasi data, hingga perakitan hardware dan jaringan.</p>
        <a href="#contact" class="btn">Hubungi Saya</a>
    </section>

    <section id="about">
        <h2 class="section-title">Tentang Saya</h2>
        <div style="text-align: center; max-width: 800px; margin: 0 auto; color: var(--text-muted);">
            <p>Memiliki pengalaman langsung melalui program Praktik Kerja Lapangan (PKL) di Singa Asia - Harco Mangga Dua dalam bidang administrasi, teknisi perangkat keras, dan layanan pelanggan. Aktif dalam organisasi sekolah sebagai Pengurus OSIS yang mengasah kemampuan kepemimpinan, komunikasi, dan kerja sama tim. Merupakan pribadi yang teliti, bertanggung jawab, komunikatif, dan siap memberikan kontribusi terbaik.</p>
        </div>
    </section>

    <section id="education">
        <h2 class="section-title">Pendidikan</h2>
        <div class="grid">
            <div class="card">
                <i class="fa-solid fa-graduation-cap"></i>
                <h3>Universitas Gunadarma</h3>
                <h4>S1 Sistem Informasi (2024 - Present)</h4>
                <p>IPK: 3.83 / 4.00</p>
            </div>
            <div class="card">
                <i class="fa-solid fa-school"></i>
                <h3>SMK AD-DA'WAH</h3>
                <h4>Teknik Komputer dan Jaringan (2021 - 2024)</h4>
                <p>Nilai Rata-rata: 81 / 100</p>
            </div>
        </div>
    </section>

    <section id="skills">
        <h2 class="section-title">Kemampuan & Keahlian</h2>
        <div class="skills-container">
            <span class="skill-badge">Pemrograman Java</span>
            <span class="skill-badge">SQL Database</span>
            <span class="skill-badge">Microsoft Excel & Word</span>
            <span class="skill-badge">Administrasi Data</span>
            <span class="skill-badge">Perakitan & Instalasi Hardware/Software</span>
            <span class="skill-badge">Infrastruktur Jaringan</span>
            <span class="skill-badge">Visual Studio Code</span>
            <span class="skill-badge">Customer Service</span>
        </div>
    </section>

    <section id="experience">
        <h2 class="section-title">Pengalaman Kerja & Organisasi</h2>
        <div class="grid">
            <div class="card">
                <i class="fa-solid fa-briefcase"></i>
                <h3>Praktik Kerja Lapangan (PKL)</h3>
                <h4>Singa Asia - Harco Mangga Dua (Jan - Apr 2023)</h4>
                <ul>
                    <li><strong>Administrasi & Manajemen Data:</strong> Mengelola alur barang masuk/keluar dan pembaruan data harga pada sistem.</li>
                    <li><strong>Teknisi Perangkat Keras:</strong> Perakitan PC, instalasi Windows, dan pengecekan hardware.</li>
                    <li><strong>Layanan Pelanggan:</strong> Menangani keluhan pelanggan dan berkoordinasi dengan tim untuk solusi cepat.</li>
                </ul>
            </div>
            <div class="card">
                <i class="fa-solid fa-users"></i>
                <h3>Pengurus OSIS</h3>
                <h4>SMK AD-DA'WAH (2022 - 2023)</h4>
                <ul>
                    <li>Merencanakan dan mengeksekusi berbagai program kerja serta kegiatan kesiswaan.</li>
                    <li>Mengasah kemampuan kepemimpinan dan kerja sama tim dalam mengelola acara sekolah.</li>
                    <li>Membangun komunikasi yang baik antara siswa dan pihak sekolah.</li>
                </ul>
            </div>
        </div>
    </section>

    <section id="certifications">
        <h2 class="section-title">Sertifikasi & Kegiatan</h2>
        <div class="grid">
            <div class="card">
                <i class="fa-solid fa-certificate"></i>
                <h3>Belajar Dasar Manajemen Proyek</h3>
                <p>Dicoding (2026)</p>
            </div>
            <div class="card">
                <i class="fa-solid fa-building"></i>
                <h3>Kunjungan Industri</h3>
                <p>PT. Primarindo Asia Infrastructure (2023)</p>
            </div>
            <div class="card">
                <i class="fa-solid fa-chalkboard-user"></i>
                <h3>Seminar SDM</h3>
                <p>SDM Kompeten & Berdaya Saing Tinggi di Era Industri</p>
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
