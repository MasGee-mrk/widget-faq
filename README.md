<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>FAQ - Pos Indonesia</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f5f5f5;
            line-height: 1.6;
            color: #333;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 40px 20px;
        }

        .header {
            text-align: center;
            margin-bottom: 48px;
        }

        .header h1 {
            font-size: 32px;
            font-weight: 700;
            color: #333333;
            margin-bottom: 12px;
        }

        .header p {
            font-size: 16px;
            color: #666666;
        }

        .faq-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 24px;
        }

        .faq-category {
            background: #ffffff;
            border: 1px solid #e1e5e9;
            border-radius: 8px;
            box-shadow: 0 2px 8px rgba(0,0,0,0.08);
            overflow: hidden;
        }

        .category-header {
            background: #f8f9fa;
            padding: 16px;
            border-bottom: 1px solid #e1e5e9;
        }

        .category-title {
            font-size: 18px;
            font-weight: 600;
            color: #333333;
            margin-bottom: 4px;
        }

        .category-subtitle {
            font-size: 14px;
            color: #666666;
        }

        .faq-items {
            background: #ffffff;
        }

        .faq-item {
            border-bottom: 1px solid #f0f0f0;
        }

        .faq-item:last-child {
            border-bottom: none;
        }

        .faq-question {
            width: 100%;
            background: none;
            border: none;
            padding: 16px;
            text-align: left;
            cursor: pointer;
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-size: 16px;
            font-weight: 500;
            color: #1a73e8;
            transition: background-color 0.2s ease;
        }

        .faq-question:hover {
            background-color: #f8f9fa;
        }

        .faq-question:focus {
            outline: none;
            background-color: #f0f7ff;
        }

        .question-text {
            flex: 1;
            margin-right: 12px;
        }

        .arrow-icon {
            width: 20px;
            height: 20px;
            transition: transform 0.3s ease;
            color: #666666;
        }

        .arrow-icon.rotated {
            transform: rotate(180deg);
        }

        .faq-answer {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.3s ease, padding 0.3s ease;
            background: #ffffff;
        }

        .faq-answer.open {
            max-height: 200px;
            padding: 0 16px 16px 16px;
        }

        .answer-content {
            font-size: 14px;
            color: #555555;
            line-height: 1.6;
            padding-left: 8px;
            border-left: 3px solid #e3f2fd;
        }

        .contact-footer {
            text-align: center;
            margin-top: 48px;
            padding: 24px;
            background: #ffffff;
            border-radius: 8px;
            box-shadow: 0 2px 8px rgba(0,0,0,0.08);
            border: 1px solid #e1e5e9;
        }

        .contact-footer p {
            color: #666666;
            margin-bottom: 8px;
        }

        .contact-footer .contact-info {
            font-size: 16px;
            font-weight: 600;
            color: #1a73e8;
        }

        /* Mobile Responsive */
        @media (max-width: 768px) {
            .container {
                padding: 24px 16px;
            }

            .header h1 {
                font-size: 28px;
            }

            .faq-grid {
                grid-template-columns: 1fr;
                gap: 20px;
            }

            .faq-question {
                font-size: 15px;
                padding: 14px;
            }

            .answer-content {
                font-size: 13px;
            }

            .faq-answer.open {
                padding: 0 14px 14px 14px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header -->
        <div class="header">
            <h1>FAQ Pos Indonesia</h1>
            <p>Temukan jawaban untuk pertanyaan yang sering diajukan</p>
        </div>

        <!-- FAQ Grid -->
        <div class="faq-grid">
            <!-- General Category -->
            <div class="faq-category">
                <div class="category-header">
                    <div class="category-title">General</div>
                    <div class="category-subtitle">Pertanyaan Umum</div>
                </div>
                <div class="faq-items">
                    <div class="faq-item">
                        <button class="faq-question" onclick="toggleFAQ(this)">
                            <span class="question-text">Q: Apa itu Pos Indonesia?</span>
                            <svg class="arrow-icon" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
                            </svg>
                        </button>
                        <div class="faq-answer">
                            <div class="answer-content">
                                A: Perusahaan Milik Negara dalam bidang Jasa Pengiriman Surat dan Paket yang merupakan pelopor Jasa Kurir di Indonesia sejak tahun 1746.
                            </div>
                        </div>
                    </div>

                    <div class="faq-item">
                        <button class="faq-question" onclick="toggleFAQ(this)">
                            <span class="question-text">Q: Layanan apa saja yang tersedia di Pos Indonesia?</span>
                            <svg class="arrow-icon" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
                            </svg>
                        </button>
                        <div class="faq-answer">
                            <div class="answer-content">
                                A: Pos Kilat, Pos Express, EMS, Paket Pos, Wesel Pos, Giro Pos, Tabungan Pos, dan layanan logistik lainnya untuk kebutuhan pengiriman domestik dan internasional.
                            </div>
                        </div>
                    </div>

                    <div class="faq-item">
                        <button class="faq-question" onclick="toggleFAQ(this)">
                            <span class="question-text">Q: Berapa jam operasional kantor pos?</span>
                            <svg class="arrow-icon" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
                            </svg>
                        </button>
                        <div class="faq-answer">
                            <div class="answer-content">
                                A: Senin-Jumat: 08.00-16.00 WIB, Sabtu: 08.00-14.00 WIB. Jam operasional dapat berbeda di setiap cabang, silakan hubungi kantor pos terdekat.
                            </div>
                        </div>
                    </div>

                    <div class="faq-item">
                        <button class="faq-question" onclick="toggleFAQ(this)">
                            <span class="question-text">Q: Bagaimana cara menghubungi customer service?</span>
                            <svg class="arrow-icon" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
                            </svg>
                        </button>
                        <div class="faq-answer">
                            <div class="answer-content">
                                A: Hubungi Call Center 161 (24 jam), email: halo@posindonesia.co.id, atau melalui media sosial resmi @posindonesia di Instagram dan Facebook.
                            </div>
                        </div>
                    </div>

                    <div class="faq-item">
                        <button class="faq-question" onclick="toggleFAQ(this)">
                            <span class="question-text">Q: Apa syarat untuk mengirim barang?</span>
                            <svg class="arrow-icon" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
                            </svg>
                        </button>
                        <div class="faq-answer">
                            <div class="answer-content">
                                A: Bawa KTP/identitas diri, isi formulir pengiriman dengan lengkap, pastikan barang dikemas dengan baik, dan tidak termasuk barang terlarang.
                            </div>
                        </div>
                    </div>

                    <div class="faq-item">
                        <button class="faq-question" onclick="toggleFAQ(this)">
                            <span class="question-text">Q: Kemana saja Pos Indonesia bisa mengirimkan paket?</span>
                            <svg class="arrow-icon" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
                            </svg>
                        </button>
                        <div class="faq-answer">
                            <div class="answer-content">
                                A: Dalam Negeri ke seluruh wilayah Indonesia (34 provinsi) dan Luar Negeri ke lebih dari 200 negara di seluruh dunia melalui jaringan Universal Postal Union.
                            </div>
                        </div>
                    </div>

                    <div class="faq-item">
                        <button class="faq-question" onclick="toggleFAQ(this)">
                            <span class="question-text">Q: Apakah ada layanan pick up gratis?</span>
                            <svg class="arrow-icon" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
                            </svg>
                        </button>
                        <div class="faq-answer">
                            <div class="answer-content">
                                A: Ya, tersedia layanan pick up gratis untuk pengiriman dengan syarat dan ketentuan tertentu. Hubungi 161 untuk informasi lebih lanjut dan penjadwalan.
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Unusual Category -->
            <div class="faq-category">
                <div class="category-header">
                    <div class="category-title">Unusual</div>
                    <div class="category-subtitle">Pertanyaan Khusus</div>
                </div>
                <div class="faq-items">
                    <div class="faq-item">
                        <button class="faq-question" onclick="toggleFAQ(this)">
                            <span class="question-text">Q: Berapa batas maksimal berat dan ukuran paket?</span>
                            <svg class="arrow-icon" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
                            </svg>
                        </button>
                        <div class="faq-answer">
                            <div class="answer-content">
                                A: Maksimal 30 kg per paket untuk domestik, 20 kg untuk internasional. Ukuran maksimal 100cm (panjang) + 2x(lebar+tinggi) tidak boleh melebihi 300cm.
                            </div>
                        </div>
                    </div>

                    <div class="faq-item">
                        <button class="faq-question" onclick="toggleFAQ(this)">
                            <span class="question-text">Q: Barang apa saja yang tidak boleh dikirim?</span>
                            <svg class="arrow-icon" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
                            </svg>
                        </button>
                        <div class="faq-answer">
                            <div class="answer-content">
                                A: Barang berbahaya (bahan kimia, gas), senjata, narkoba, uang tunai, perhiasan mahal, makanan mudah busuk, dan barang yang melanggar hukum.
                            </div>
                        </div>
                    </div>

                    <div class="faq-item">
                        <button class="faq-question" onclick="toggleFAQ(this)">
                            <span class="question-text">Q: Bagaimana cara tracking paket secara real-time?</span>
                            <svg class="arrow-icon" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
                            </svg>
                        </button>
                        <div class="faq-answer">
                            <div class="answer-content">
                                A: Gunakan website posindonesia.co.id, aplikasi mobile PosAja!, atau SMS ke 8161 dengan format: CEK[spasi]NOMORKIRIMAN. Update status tersedia setiap 2-4 jam.
                            </div>
                        </div>
                    </div>

                    <div class="faq-item">
                        <button class="faq-question" onclick="toggleFAQ(this)">
                            <span class="question-text">Q: Apa saya dapat mengirimkan 1 paket dalam 1 pick up?</span>
                            <svg class="arrow-icon" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
                            </svg>
                        </button>
                        <div class="faq-answer">
                            <div class="answer-content">
                                A: Bisa, 1 paket atau berapapun paketnya akan di pick up secara gratis sesuai jadwal yang telah ditentukan dalam area jangkauan layanan pick up.
                            </div>
                        </div>
                    </div>

                    <div class="faq-item">
                        <button class="faq-question" onclick="toggleFAQ(this)">
                            <span class="question-text">Q: Bagaimana jaminan keamanan dan asuransi paket?</span>
                            <svg class="arrow-icon" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
                            </svg>
                        </button>
                        <div class="faq-answer">
                            <div class="answer-content">
                                A: Tersedia asuransi hingga Rp 10 juta dengan biaya tambahan 0,5% dari nilai barang. Paket dilacak dengan barcode dan sistem keamanan berlapis.
                            </div>
                        </div>
                    </div>

                    <div class="faq-item">
                        <button class="faq-question" onclick="toggleFAQ(this)">
                            <span class="question-text">Q: Apa yang harus dilakukan jika paket hilang atau rusak?</span>
                            <svg class="arrow-icon" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
                            </svg>
                        </button>
                        <div class="faq-answer">
                            <div class="answer-content">
                                A: Laporkan segera ke Call Center 161 dengan menyertakan nomor resi. Tim investigasi akan menindaklanjuti dalam 3x24 jam dan memberikan kompensasi sesuai ketentuan.
                            </div>
                        </div>
                    </div>

                    <div class="faq-item">
                        <button class="faq-question" onclick="toggleFAQ(this)">
                            <span class="question-text">Q: Bisakah mengubah alamat tujuan setelah paket dikirim?</span>
                            <svg class="arrow-icon" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
                            </svg>
                        </button>
                        <div class="faq-answer">
                            <div class="answer-content">
                                A: Perubahan alamat hanya bisa dilakukan jika paket belum sampai di kota tujuan. Hubungi 161 dengan biaya tambahan sesuai selisih ongkir dan biaya administrasi.
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Contact Footer -->
        <div class="contact-footer">
            <p>Masih ada pertanyaan lain?</p>
            <div class="contact-info">Hubungi Call Center 161 (24 Jam) atau email: halo@posindonesia.co.id</div>
        </div>
    </div>

    <script>
        function toggleFAQ(button) {
            const answer = button.nextElementSibling;
            const arrow = button.querySelector('.arrow-icon');
            const isOpen = answer.classList.contains('open');
            
            // Close all other FAQs in the same category
            const category = button.closest('.faq-category');
            const allAnswers = category.querySelectorAll('.faq-answer');
            const allArrows = category.querySelectorAll('.arrow-icon');
            
            allAnswers.forEach(ans => ans.classList.remove('open'));
            allArrows.forEach(arr => arr.classList.remove('rotated'));
            
            // Toggle current FAQ if it wasn't open
            if (!isOpen) {
                answer.classList.add('open');
                arrow.classList.add('rotated');
            }
        }
    </script>
<script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'983f99e2f335585b',t:'MTc1ODY4ODc5OS4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
