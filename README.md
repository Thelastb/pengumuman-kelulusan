# pengumuman-kelulusan
PENGUMUMAN KELAS 6 SD NEGERI 6 SUDIMOROHARJO 
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <title>Pengumuman Kelulusan - SDN 6 Sudimoroharjo</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f0f8ff;
      display: flex;
      flex-direction: column;
      align-items: center;
      padding-top: 100px;
    }
    h1 {
      color: #2c3e50;
    }
    .form-container {
      background-color: #ffffff;
      padding: 30px;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
      width: 100%;
      max-width: 400px;
    }
    input[type="text"] {
      width: 100%;
      padding: 12px;
      margin: 10px 0;
      border: 1px solid #ccc;
      border-radius: 8px;
    }
    button {
      width: 100%;
      padding: 12px;
      background-color: #2ecc71;
      color: white;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      font-size: 16px;
    }
    button:hover {
      background-color: #27ae60;
    }
    .result {
      margin-top: 20px;
      font-size: 18px;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <h1>Pengumuman Kelulusan</h1>
  <h2>SD Negeri 6 Sudimoroharjo Wilangan</h2>
  <h3>Tahun Ajaran 2024/2025</h3>
  <div class="form-container">
    <label for="nisn">NISN:</label>
    <input type="text" id="nisn" placeholder="Masukkan NISN">

    <label for="nama">Nama Lengkap:</label>
    <input type="text" id="nama" placeholder="Masukkan Nama Lengkap">

    <button onclick="cekKelulusan()">Cek Kelulusan</button>

    <div class="result" id="hasil"></div>
  </div>

  <script>
    const dataLulus = [
      { nama: "ADELIA CILLA MAYANG SARI", nisn: "0128021660" },
      { nama: "AKRATUL KARIMAH", nisn: "0127195192" },
      { nama: "ANDIKA DWI PRADESTA", nisn: "3126510332" },
      { nama: "DEWI RETNO WULAN", nisn: "0137596175" },
      { nama: "FARADIVA SALSABILLAH JANNAH", nisn: "0134148002" },
      { nama: "GERY MAULANA", nisn: "0125978159" },
      { nama: "HAMDAN MAULANA FERNANDA", nisn: "0139380360" },
      { nama: "ICHA NUR AGUSTIN", nisn: "3126655208" },
      { nama: "JUNIOR ANDIKA PRASTIYO", nisn: "0135083666" },
      { nama: "MUHAMMAD NUR AMIN", nisn: "3139086813" },
      { nama: "SILVA WIJAYANTI", nisn: "0127265593" },
      { nama: "VADISA IKBAL IBRAHIM", nisn: "0128659804" },
      { nama: "YODHA PRASETYA JONATA", nisn: "0123229094" },
      { nama: "YUWAN DARIANTO", nisn: "0128226891" },
    ];

    function cekKelulusan() {
      const nisnInput = document.getElementById("nisn").value.trim();
      const namaInput = document.getElementById("nama").value.trim().toUpperCase();
      const hasil = document.getElementById("hasil");

      const ditemukan = dataLulus.find(siswa =>
        siswa.nisn === nisnInput && siswa.nama === namaInput
      );

      if (ditemukan) {
        hasil.style.color = "green";
        hasil.innerText = "Selamat! Anda dinyatakan LULUS.";
      } else {
        hasil.style.color = "red";
        hasil.innerText = "Data tidak ditemukan atau tidak lulus.";
      }
    }
  </script>
</body>
</html>
