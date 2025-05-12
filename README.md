# Web-undangan-pernikahan-
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Undangan Pernikahan</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            text-align: center;
            background-color: #f9f3f3;
            color: #555;
            margin: 0;
            padding: 0;
        }
        .container {
            max-width: 600px;
            margin: 0 auto;
            padding: 20px;
        }
        h1 {
            color: #d48a8a;
        }
        .couple-names {
            font-size: 24px;
            margin: 20px 0;
        }
        .date-place {
            background-color: #d48a8a;
            color: white;
            padding: 15px;
            border-radius: 5px;
            margin: 20px 0;
        }
        .btn {
            display: inline-block;
            background-color: #d48a8a;
            color: white;
            padding: 10px 20px;
            text-decoration: none;
            border-radius: 5px;
            margin: 10px;
        }
        .countdown {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin: 30px 0;
        }
        .countdown-box {
            background: white;
            padding: 10px;
            border-radius: 5px;
            box-shadow: 0 3px 6px rgba(0,0,0,0.1);
            min-width: 70px;
        }
        .countdown-number {
            font-size: 28px;
            font-weight: bold;
            color: #d48a8a;
        }
        .countdown-label {
            font-size: 12px;
            text-transform: uppercase;
        }
        img {
            width: 100%;
            max-width: 400px;
            margin: 20px 0;
            border-radius: 5px;
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Foto utama -->
        <img src="https://via.placeholder.com/400x300?text=Foto+Pengantin" alt="Foto Pengantin">
        
        <h1>Undangan Pernikahan</h1>
        <p>Dengan memohon rahmat Tuhan Yang Maha Esa, kami mengundang Anda untuk hadir dalam acara pernikahan kami:</p>
        
        <div class="couple-names">
            <strong>John Doe</strong><br>
            &<br>
            <strong>Jane Smith</strong>
        </div>
        
        <!-- Countdown Timer -->
        <div id="countdown">
            <h3>Menuju Hari Bahagia Kami</h3>
            <div class="countdown">
                <div class="countdown-box">
                    <div class="countdown-number" id="days">00</div>
                    <div class="countdown-label">Hari</div>
                </div>
                <div class="countdown-box">
                    <div class="countdown-number" id="hours">00</div>
                    <div class="countdown-label">Jam</div>
                </div>
                <div class="countdown-box">
                    <div class="countdown-number" id="minutes">00</div>
                    <div class="countdown-label">Menit</div>
                </div>
                <div class="countdown-box">
                    <div class="countdown-number" id="seconds">00</div>
                    <div class="countdown-label">Detik</div>
                </div>
            </div>
        </div>
        
        <div class="date-place">
            <p>Hari/Tanggal: Sabtu, 12 Desember 2025</p>
            <p>Waktu: 10.00 WIB - Selesai</p>
            <p>Tempat: Gedung Serba Guna, Kota Anda</p>
        </div>
        
        <p>Merupakan suatu kehormatan dan kebahagiaan bagi kami apabila Bapak/Ibu/Saudara/i berkenan hadir untuk memberikan doa restu.</p>
        
        <a href="#form" class="btn">Konfirmasi Kehadiran</a>
        <a href="#lokasi" class="btn">Lihat Lokasi</a>
        
        <!-- Galeri Foto -->
        <div style="margin-top: 40px;">
            <h2>Galeri Kami</h2>
            <div style="display: flex; flex-wrap: wrap; justify-content: center; gap: 10px;">
                <img src="https://via.placeholder.com/150?text=Foto+1" style="max-width: 150px;">
                <img src="https://via.placeholder.com/150?text=Foto+2" style="max-width: 150px;">
                <img src="https://via.placeholder.com/150?text=Foto+3" style="max-width: 150px;">
            </div>
        </div>
        
        <div id="form" style="margin-top: 40px;">
            <h2>Konfirmasi Kehadiran</h2>
            <form>
                <input type="text" placeholder="Nama Anda" style="padding: 8px; width: 80%; margin: 5px;"><br>
                <input type="email" placeholder="Email/No. HP" style="padding: 8px; width: 80%; margin: 5px;"><br>
                <select style="padding: 8px; width: 83%; margin: 5px;">
                    <option>Jumlah yang hadir</option>
                    <option>1 orang</option>
                    <option>2 orang</option>
                    <option>3 orang</option>
                </select><br>
                <button type="submit" style="padding: 10px 20px; background-color: #d48a8a; color: white; border: none; border-radius: 5px; margin: 10px;">Kirim Konfirmasi</button>
            </form>
        </div>
        
        <div id="lokasi" style="margin-top: 40px;">
            <h2>Lokasi Acara</h2>
            <!-- Ganti dengan embed Google Maps Anda -->
            <iframe src="https://maps.google.com/maps?q=your+address&output=embed" width="100%" height="300" frameborder="0" style="border:0;" allowfullscreen=""></iframe>
        </div>
    </div>

    <script>
        // Set the date we're counting down to (Format: Tahun, Bulan-1, Hari)
        const countDownDate = new Date("Dec 12, 2025 10:00:00").getTime();

        // Update the count down every 1 second
        const countdownFunction = setInterval(function() {
            // Get today's date and time
            const now = new Date().getTime();
            
            // Find the distance between now and the count down date
            const distance = countDownDate - now;
            
            // Time calculations for days, hours, minutes and seconds
            const days = Math.floor(distance / (1000 * 60 * 60 * 24));
            const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const minutes = Math.floor((distance % (1000 * 60 * 60)) /
