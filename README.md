<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Biodata</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #B82132;
            color: white;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }
        .container {
            background-color: #D2665A;
            padding: 20px;
            border-radius: 15px;
            box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.2);
            text-align: center;
            width: 80%;
            max-width: 500px;
        }
        img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            margin-bottom: 15px;
            border: 3px solid white;
            transition: transform 0.3s ease;
        }
        img:hover {
            transform: scale(1.2);
        }
        .gallery img {
            width: 80px;
            height: 80px;
            border-radius: 10px;
            margin: 5px;
        }
        button {
            background-color: white;
            color: #B82132;
            border: none;
            padding: 10px 15px;
            border-radius: 5px;
            cursor: pointer;
            margin-top: 15px;
            font-weight: bold;
        }
        button:hover {
            background-color: #f5f5f5;
        }
    </style>
</head>
<body>
    <div class="container" id="content">
        <h2 id="title">Halaman 1: Informasi Pribadi</h2>
        <img id="image" src="Picture 1.jpeg" alt="Foto Profil">
        <div class="gallery">
            <img src="Picture 1.jpeg" alt="Gambar 1">
            <img src="Picture 2.jpeg" alt="Gambar 2">
            <img src="Picture 3.jpeg" alt="Gambar 3">
        </div>
        <p id="info1"><strong>Nama:</strong> Asma Lutfi</p>
        <p id="info2"><strong>Tempat & tanggal lahir:</strong> Siwalempu, 07 Mei 2005</p>
        <p id="info3"><strong>Alamat:</strong> Jl. Lengaru, Palu Timur</p>
        <button onclick="togglePage()" id="toggleButton">Lanjut ke Halaman 2</button>
    </div>
    <script>
    let page = 1;
    function togglePage() {
        if (page === 1) {
            document.getElementById('title').innerText = "Halaman 2: Pendidikan & Keterampilan";
            document.getElementById('image').src = "Universitas Tadulako.jpg";
            document.getElementById('image').alt = "Pendidikan";
            document.querySelector('.gallery').innerHTML = `
                <img src="edu1.jpg" alt="Edu 1">
                <img src="edu2.jpg" alt="Edu 2">
                <img src="edu3.jpg" alt="Edu 3">
            `;
            document.getElementById('info1').innerHTML = "<strong>Universitas:</strong> Tadulako";
            document.getElementById('info2').innerHTML = "<strong>Fakultas:</strong> Teknik";
            document.getElementById('info3').innerHTML = "<strong>Program Studi:</strong> S1 Sistem Informasi";
            document.getElementById('toggleButton').innerText = "Kembali ke Halaman 1";
            page = 2;
        } else {
            document.getElementById('title').innerText = "Halaman 1: Informasi Pribadi";
            document.getElementById('image').src = "Picture 1.jpeg";
            document.getElementById('image').alt = "Foto Profil";
            document.querySelector('.gallery').innerHTML = `
                <img src="Picture 1.jpg" alt="Gambar 1">
                <img src="Picture 2.jpep" alt="Gambar 2">
                <img src="Picture 3.jpeg" alt="Gambar 3">
            `;
            document.getElementById('info1').innerHTML = "<strong>Nama:</strong> Asma Lutfi";
            document.getElementById('info2').innerHTML = "<strong>Tempat & tanggal lahir:</strong> Siwalempu, 07 Mei 2005";
            document.getElementById('info3').innerHTML = "<strong>Alamat:</strong> Jl. Lengaru, Palu Timur";
            document.getElementById('toggleButton').innerText = "Lanjut ke Halaman 2";
            page = 1;
        }
    }
    </script>
</body>
</html>
