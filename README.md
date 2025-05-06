# ppdbmanuba-pengumuman
Pengumuman kelulusan PPDB SMK Ma'arif Banyumas gelombang 1
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Pengumuman Kelulusan PPDB</title>
  <style>
    body { font-family: Arial, sans-serif; padding: 20px; background-color: #f9f9f9; }
    .container { max-width: 400px; margin: auto; background: white; padding: 20px; border-radius: 8px; box-shadow: 0 0 10px rgba(0,0,0,0.1); }
    input[type="number"] { width: 100%; padding: 10px; margin: 10px 0; }
    button { padding: 10px 20px; background-color: #28a745; color: white; border: none; cursor: pointer; }
    .result { margin-top: 20px; font-size: 1.1em; }
  </style>
</head>
<body>
  <div class="container">
    <h2>Pengumuman Kelulusan PPDB<br>SMK Ma'arif Banyumas</h2>
    <label for="noUrut">Masukkan No. Urut Anda:</label>
    <input type="number" id="noUrut" placeholder="Contoh: 1">
    <button onclick="cekKelulusan()">Cek Kelulusan</button>
    <div class="result" id="hasil"></div>
  </div>

  <script>
    const data = {
  0: { nama: "0", status: "0" },
  1: { nama: "Ragafa Agustira", status: "MAAF, Anda belum mengikuti tes dan harus mengikuti tes gelombang kedua" },
  2: { nama: "Dika Pratama", status: "SELAMAT, Anda diterima di SMK Ma'arif Banyumas" },
  3: { nama: "Zakky Ba'alana", status: "SELAMAT, Anda diterima di SMK Ma'arif Banyumas" },
  4: { nama: "Tri Fikriyanto", status: "SELAMAT, Anda diterima di SMK Ma'arif Banyumas" },
  5: { nama: "Alivvatun Haniva", status: "SELAMAT, Anda diterima di SMK Ma'arif Banyumas" },
  6: { nama: "Dafa Rizky Maulana Aulia", status: "SELAMAT, Anda diterima di SMK Ma'arif Banyumas" },
  7: { nama: "Intan Dela Safitri", status: "SELAMAT, Anda diterima di SMK Ma'arif Banyumas" },
  8: { nama: "Rara Annisa Fauziah", status: "SELAMAT, Anda diterima di SMK Ma'arif Banyumas" },
  9: { nama: "Adellia Dwi Octaviani", status: "SELAMAT, Anda diterima di SMK Ma'arif Banyumas" },
  10: { nama: "Syifa Marhatus Sholeha", status: "MAAF, Anda belum mengikuti tes dan harus mengikuti tes gelombang kedua" }
};

    function cekKelulusan() {
      const no = document.getElementById('noUrut').value;
      const hasilDiv = document.getElementById('hasil');
      if (data[no]) {
        hasilDiv.innerHTML = `<strong>Nama:</strong> ${data[no].nama}<br><strong>Status:</strong> ${data[no].status}`;
      } else {
        hasilDiv.innerHTML = "Data tidak ditemukan. Pastikan No. Urut yang Anda masukkan benar.";
      }
    }
  </script>
</body>
</html>
