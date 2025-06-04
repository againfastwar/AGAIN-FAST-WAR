<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>AGAIN FAST WAR ID - Form Jasa WAR</title>
  <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet" />
</head>
<body class="bg-gray-100 min-h-screen flex items-center justify-center p-4">
  <div class="bg-white p-8 rounded-lg shadow-lg max-w-lg w-full">
    <h1 class="text-2xl font-bold mb-6 text-center">Form Jasa WAR Barang</h1>
    <p class="mb-4 text-center text-gray-600">Isi form ini untuk menggunakan jasa WAR barang dari AGAIN FAST WAR ID.</p>
    <form id="warForm" class="space-y-4">
      <div>
        <label class="block mb-1 font-medium" for="nama">Nama Lengkap</label>
        <input type="text" id="nama" name="nama" required class="w-full border rounded px-3 py-2" />
      </div>
      <div>
        <label class="block mb-1 font-medium" for="alamat">Alamat Lengkap</label>
        <textarea id="alamat" name="alamat" required class="w-full border rounded px-3 py-2" rows="3"></textarea>
      </div>
      <div>
        <label class="block mb-1 font-medium" for="barang">Nama Barang</label>
        <input type="text" id="barang" name="barang" required class="w-full border rounded px-3 py-2" />
      </div>
      <div>
        <label class="block mb-1 font-medium" for="link">Link Barang Tokopedia</label>
        <input type="url" id="link" name="link" required class="w-full border rounded px-3 py-2" />
      </div>
      <div>
        <label class="block mb-1 font-medium" for="jadwal">Jadwal War</label>
        <input type="datetime-local" id="jadwal" name="jadwal" required class="w-full border rounded px-3 py-2" />
      </div>
      <div>
        <label class="block mb-1 font-medium" for="bukti">Upload Bukti Transfer (opsional)</label>
        <input type="file" id="bukti" name="bukti" accept="image/*" class="w-full border rounded px-3 py-2" />
      </div>
      <button type="submit" class="w-full bg-green-600 text-white py-2 rounded hover:bg-green-700 transition">Kirim</button>
    </form>
    <p id="status" class="mt-4 text-center text-sm"></p>
  </div>

  <script>
    const form = document.getElementById('warForm');
    const status = document.getElementById('status');

    form.addEventListener('submit', async (e) => {
      e.preventDefault();
      status.textContent = 'Mengirim data...';

      const formData = new FormData(form);

      // TODO: Implement API call to backend or Google Sheets integration
      // For demo, just simulate success:
      setTimeout(() => {
        status.textContent = 'Data berhasil dikirim! Kami akan menghubungi Anda segera.';
        form.reset();
      }, 1500);
    });
  </script>
</body>
</html>
