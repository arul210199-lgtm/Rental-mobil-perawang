<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mustang Rent Car - Rental Mobil Perawang</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- FontAwesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts (Poppins) -->
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        body { font-family: 'Poppins', sans-serif; }
    </style>
</head>
<body class="bg-slate-900 text-slate-100 min-h-screen flex flex-col">

    <!-- NAVIGASI / HEADER -->
    <header class="bg-slate-950 border-b border-slate-800 sticky top-0 z-50">
        <div class="max-w-7xl mx-auto px-4 py-3 flex justify-between items-center">
            <div class="flex items-center space-x-3">
                <div class="bg-amber-500 text-slate-950 font-black p-2 rounded-lg text-xl tracking-wider shadow-lg">
                    MUSTANG
                </div>
                <div>
                    <h1 class="text-lg font-bold leading-none text-white">MUSTANG RENT CAR</h1>
                    <p class="text-xs text-amber-400 font-medium">Rental Mobil Perawang & Sekitarnya</p>
                </div>
            </div>
            
            <div class="flex items-center space-x-2">
                <button onclick="toggleAdminModal()" class="text-xs bg-slate-800 hover:bg-slate-700 text-slate-300 border border-slate-700 px-3 py-2 rounded-lg transition flex items-center gap-1.5">
                    <i class="fa-solid fa-lock text-amber-400"></i>
                    <span>Admin</span>
                </button>
                <a href="https://wa.me/6281234567890?text=Halo%20Mustang%20Rent%20Car,%20saya%20ingin%20tanya%20sewa%20mobil" target="_blank" class="text-xs bg-amber-500 hover:bg-amber-400 text-slate-950 font-semibold px-3 py-2 rounded-lg transition flex items-center gap-1.5">
                    <i class="fa-brands fa-whatsapp text-base"></i>
                    <span class="hidden sm:inline">Hubungi Kami</span>
                </a>
            </div>
        </div>
    </header>

    <!-- HERO BANNER -->
    <section class="relative bg-gradient-to-b from-slate-950 to-slate-900 py-12 px-4 border-b border-slate-800">
        <div class="max-w-4xl mx-auto text-center space-y-4">
            <span class="bg-amber-500/10 text-amber-400 border border-amber-500/30 text-xs px-3.5 py-1.5 rounded-full font-medium inline-block">
                ⚡ Sewa Mobil Mudah, Murah & Terpercaya
            </span>
            <h2 class="text-3xl sm:text-5xl font-extrabold text-white tracking-tight leading-tight">
                Layanan Rental Mobil Terbaik di <span class="text-amber-400">Perawang</span>
            </h2>
            <p class="text-sm sm:text-base text-slate-400 max-w-2xl mx-auto">
                Menyediakan armada terawat untuk kebutuhan harian, perjalanan dinas, acara keluarga, hingga luar kota. Bebas pilih Lepas Kunci atau Dengan Supir.
            </p>
            <div class="pt-2 flex flex-wrap justify-center gap-3">
                <a href="#armada" class="bg-amber-500 hover:bg-amber-400 text-slate-950 font-bold px-6 py-3 rounded-xl transition shadow-lg shadow-amber-500/20 text-sm">
                    Lihat Pilihan Armada
                </a>
                <a href="#syarat" class="bg-slate-800 hover:bg-slate-700 text-slate-200 border border-slate-700 font-medium px-6 py-3 rounded-xl transition text-sm">
                    Syarat & Ketentuan
                </a>
            </div>
        </div>
    </section>

    <!-- KATALOG MOBIL / ARMADA -->
    <main id="armada" class="max-w-7xl mx-auto px-4 py-12 flex-grow w-full">
        <div class="flex flex-col sm:flex-row sm:items-center justify-between gap-4 mb-8">
            <div>
                <h3 class="text-2xl font-bold text-white flex items-center gap-2">
                    <i class="fa-solid fa-car-side text-amber-400"></i> Daftar Armada Mobil
                </h3>
                <p class="text-xs text-slate-400 mt-1">Pilih armada sesuai kebutuhan perjalanan Anda</p>
            </div>
            <!-- Filter Transmisi -->
            <div class="flex gap-2">
                <button onclick="filterCars('all')" class="filter-btn active text-xs px-3.5 py-2 rounded-lg bg-amber-500 text-slate-950 font-semibold border border-amber-500">
                    Semua Unit
                </button>
                <button onclick="filterCars('Manual')" class="filter-btn text-xs px-3.5 py-2 rounded-lg bg-slate-800 text-slate-300 border border-slate-700 hover:bg-slate-700">
                    Manual
                </button>
                <button onclick="filterCars('Matic')" class="filter-btn text-xs px-3.5 py-2 rounded-lg bg-slate-800 text-slate-300 border border-slate-700 hover:bg-slate-700">
                    Matic
                </button>
            </div>
        </div>

        <!-- GRID KATALOG MOBIL -->
        <div id="carGrid" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
            <!-- Data mobil akan ditampilkan di sini secara dinamis melalui JavaScript -->
        </div>
    </main>

    <!-- SYARAT & KETENTUAN -->
    <section id="syarat" class="bg-slate-950 py-12 border-t border-slate-800">
        <div class="max-w-7xl mx-auto px-4">
            <div class="text-center mb-8">
                <h3 class="text-2xl font-bold text-white">Syarat & Ketentuan Sewa</h3>
                <p class="text-xs text-slate-400 mt-1">Persyaratan sederhana untuk kemudahan transaksi Anda</p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 gap-6 max-w-4xl mx-auto">
                <!-- Lepas Kunci -->
                <div class="bg-slate-900 border border-slate-800 rounded-2xl p-6">
                    <div class="flex items-center gap-3 mb-4">
                        <div class="bg-amber-500/10 p-3 rounded-xl text-amber-400">
                            <i class="fa-solid fa-key text-xl"></i>
                        </div>
                        <h4 class="text-lg font-bold text-white">Sewa Lepas Kunci</h4>
                    </div>
                    <ul class="space-y-2.5 text-xs text-slate-300">
                        <li class="flex items-start gap-2">
                            <i class="fa-solid fa-check text-amber-400 mt-0.5"></i>
                            <span>E-KTP Asli Penyewa</span>
                        </li>
                        <li class="flex items-start gap-2">
                            <i class="fa-solid fa-check text-amber-400 mt-0.5"></i>
                            <span>SIM A Masih Berlaku</span>
                        </li>
                        <li class="flex items-start gap-2">
                            <i class="fa-solid fa-check text-amber-400 mt-0.5"></i>
                            <span>Sepeda Motor + STNK Asli (Jaminan)</span>
                        </li>
                        <li class="flex items-start gap-2">
                            <i class="fa-solid fa-check text-amber-400 mt-0.5"></i>
                            <span>Bersedia Difoto Saat Serah Terima Unit</span>
                        </li>
                    </ul>
                </div>

                <!-- Dengan Driver -->
                <div class="bg-slate-900 border border-slate-800 rounded-2xl p-6">
                    <div class="flex items-center gap-3 mb-4">
                        <div class="bg-amber-500/10 p-3 rounded-xl text-amber-400">
                            <i class="fa-solid fa-user-tie text-xl"></i>
                        </div>
                        <h4 class="text-lg font-bold text-white">Sewa + Supir</h4>
                    </div>
                    <ul class="space-y-2.5 text-xs text-slate-300">
                        <li class="flex items-start gap-2">
                            <i class="fa-solid fa-check text-amber-400 mt-0.5"></i>
                            <span>Tanpa Jaminan Dokumen/Motor</span>
                        </li>
                        <li class="flex items-start gap-2">
                            <i class="fa-solid fa-check text-amber-400 mt-0.5"></i>
                            <span>Cukup Konfirmasi Lokasi & Jadwal Penjemputan</span>
                        </li>
                        <li class="flex items-start gap-2">
                            <i class="fa-solid fa-check text-amber-400 mt-0.5"></i>
                            <span>Harga Belum Termasuk BBM, Tol, & Parkir (Kecuali Paket All-In)</span>
                        </li>
                        <li class="flex items-start gap-2">
                            <i class="fa-solid fa-check text-amber-400 mt-0.5"></i>
                            <span>Supir Pengalaman & Paham Rute Wilayah Riau</span>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- FOOTER -->
    <footer class="bg-slate-950 border-t border-slate-800 text-slate-400 py-8 text-xs">
        <div class="max-w-7xl mx-auto px-4 grid grid-cols-1 md:grid-cols-3 gap-6">
            <div>
                <h4 class="text-white font-bold text-base mb-2">MUSTANG RENT CAR</h4>
                <p class="leading-relaxed">Layanan sewa mobil terpercaya di Perawang, Siak. Siap melayani kebutuhan transportasi harian, bulanan, maupun dinas.</p>
            </div>
            <div>
                <h4 class="text-white font-bold text-base mb-2">LOKASI & KONTAK</h4>
                <p class="mb-1"><i class="fa-solid fa-location-dot text-amber-400 mr-2"></i> Perawang, Kec. Tualang, Kab. Siak, Riau</p>
                <p class="mb-1"><i class="fa-brands fa-whatsapp text-amber-400 mr-2"></i> 0812-3456-7890</p>
                <p><i class="fa-solid fa-clock text-amber-400 mr-2"></i> Buka 24 Jam</p>
            </div>
            <div>
                <h4 class="text-white font-bold text-base mb-2">KEUNGGULAN</h4>
                <p>• Armada Selalu Bersih & Terawat</p>
                <p>• Harga Bersaing & Transparan</p>
                <p>• Proses Syarat Sewa Cepat</p>
            </div>
        </div>
        <div class="max-w-7xl mx-auto px-4 mt-6 pt-4 border-t border-slate-900 text-center text-slate-500">
            &copy; Mustang Rent Car Perawang. All rights reserved.
        </div>
    </footer>

    <!-- MODAL POPUP LOGIN ADMIN -->
    <div id="adminAuthModal" class="fixed inset-0 bg-slate-950/80 backdrop-blur-sm z-50 flex items-center justify-center p-4 hidden">
        <div class="bg-slate-900 border border-slate-800 rounded-2xl max-w-sm w-full p-6 relative">
            <button onclick="toggleAdminModal()" class="absolute top-4 right-4 text-slate-400 hover:text-white">
                <i class="fa-solid fa-xmark text-lg"></i>
            </button>
            <div class="text-center mb-5">
                <div class="w-12 h-12 bg-amber-500/10 text-amber-400 rounded-full flex items-center justify-center mx-auto mb-3">
                    <i class="fa-solid fa-lock text-xl"></i>
                </div>
                <h3 class="text-lg font-bold text-white">Login Kelola Mobil</h3>
                <p class="text-xs text-slate-400 mt-1">Masukkan PIN default untuk membuka panel update mobil (PIN: <span class="text-amber-400 font-mono">1234</span>)</p>
            </div>
            <form onsubmit="handleAdminLogin(event)" class="space-y-4">
                <div>
                    <input type="password" id="adminPin" placeholder="Masukkan PIN" class="w-full bg-slate-950 border border-slate-800 rounded-xl px-4 py-3 text-white text-center tracking-widest text-lg focus:outline-none focus:border-amber-500">
                </div>
                <button type="submit" class="w-full bg-amber-500 hover:bg-amber-400 text-slate-950 font-bold py-3 rounded-xl transition text-sm">
                    Masuk Dashboard
                </button>
            </form>
        </div>
    </div>

    <!-- MODAL DASHBOARD ADMIN (TAMBAH / UPDATE MOBIL) -->
    <div id="adminDashboardModal" class="fixed inset-0 bg-slate-950/90 backdrop-blur-md z-50 overflow-y-auto p-4 hidden">
        <div class="max-w-3xl mx-auto bg-slate-900 border border-slate-800 rounded-2xl p-6 my-8 relative">
            <div class="flex justify-between items-center border-b border-slate-800 pb-4 mb-6">
                <div>
                    <h3 class="text-xl font-bold text-white flex items-center gap-2">
                        <i class="fa-solid fa-sliders text-amber-400"></i> Kelola Armada Mobil
                    </h3>
                    <p class="text-xs text-slate-400">Tambah, ubah status, atau hapus unit mobil sewa</p>
                </div>
                <button onclick="closeAdminDashboard()" class="bg-slate-800 hover:bg-slate-700 text-slate-300 px-3 py-1.5 rounded-lg text-xs">
                    Keluar Admin
                </button>
            </div>

            <!-- FORM TAMBAH MOBIL BARU -->
            <form onsubmit="saveCar(event)" class="bg-slate-950 p-4 border border-slate-800 rounded-xl mb-8 space-y-4">
                <h4 class="text-sm font-bold text-amber-400 uppercase tracking-wider">Tambah / Input Unit Mobil Baru</h4>
                <div class="grid grid-cols-1 sm:grid-cols-2 gap-3">
                    <div>
                        <label class="text-xs text-slate-400 mb-1 block">Nama / Model Mobil</label>
                        <input type="text" id="carName" required placeholder="Contoh: Daihatsu Xenia Silver" class="w-full bg-slate-900 border border-slate-800 rounded-lg px-3 py-2 text-xs text-white focus:outline-none focus:border-amber-500">
                    </div>
                    <div>
                        <label class="text-xs text-slate-400 mb-1 block">Tahun / Varian</label>
                        <input type="text" id="carYear" required placeholder="Contoh: 2016 / Type R" class="w-full bg-slate-900 border border-slate-800 rounded-lg px-3 py-2 text-xs text-white focus:outline-none focus:border-amber-500">
                    </div>
                    <div>
                        <label class="text-xs text-slate-400 mb-1 block">Transmisi</label>
                        <select id="carTransmission" class="w-full bg-slate-900 border border-slate-800 rounded-lg px-3 py-2 text-xs text-white focus:outline-none focus:border-amber-500">
                            <option value="Manual">Manual</option>
                            <option value="Matic">Matic</option>
                        </select>
                    </div>
                    <div>
                        <label class="text-xs text-slate-400 mb-1 block">Kapasitas Kursi</label>
                        <input type="text" id="carSeats" required placeholder="Contoh: 7 Kursi" class="w-full bg-slate-900 border border-slate-800 rounded-lg px-3 py-2 text-xs text-white focus:outline-none focus:border-amber-500">
                    </div>
                    <div>
                        <label class="text-xs text-slate-400 mb-1 block">Harga Sewa / Hari (Rp)</label>
                        <input type="number" id="carPrice" required placeholder="Contoh: 300000" class="w-full bg-slate-900 border border-slate-800 rounded-lg px-3 py-2 text-xs text-white focus:outline-none focus:border-amber-500">
                    </div>
                    <div>
                        <label class="text-xs text-slate-400 mb-1 block">URL Foto Mobil (Opsional)</label>
                        <input type="url" id="carImage" placeholder="https://..." class="w-full bg-slate-900 border border-slate-800 rounded-lg px-3 py-2 text-xs text-white focus:outline-none focus:border-amber-500">
                    </div>
                </div>
                <button type="submit" class="w-full bg-amber-500 hover:bg-amber-400 text-slate-950 font-bold py-2.5 rounded-lg transition text-xs">
                    + Simpan & Tambahkan Mobil
                </button>
            </form>

            <!-- DAFTAR KELOLA MOBIL -->
            <div>
                <h4 class="text-sm font-bold text-white mb-3">Daftar Mobil Saat Ini</h4>
                <div id="adminCarList" class="space-y-3">
                    <!-- Ditampilkan via JS -->
                </div>
            </div>
        </div>
    </div>

    <!-- JAVASCRIPT LOGIC -->
    <script>
        // Data Mobil Default
        const defaultCars = [
            {
                id: 1,
                name: "Daihatsu Xenia Silver",
                year: "2016",
                transmission: "Manual",
                seats: "7 Kursi",
                price: 300000,
                status: "Tersedia",
                image: "https://images.unsplash.com/photo-1549399542-7e3f8b79c341?w=600&auto=format&fit=crop&q=60"
            },
            {
                id: 2,
                name: "Toyota Grand New Avanza",
                year: "2018",
                transmission: "Manual",
                seats: "7 Kursi",
                price: 350000,
                status: "Tersedia",
                image: "https://images.unsplash.com/photo-1552519507-da3b142c6e3d?w=600&auto=format&fit=crop&q=60"
            },
            {
                id: 3,
                name: "Honda Brio Satya",
                year: "2020",
                transmission: "Matic",
                seats: "5 Kursi",
                price: 300000,
                status: "Tersewa",
                image: "https://images.unsplash.com/photo-1590362891991-f776e747a588?w=600&auto=format&fit=crop&q=60"
            }
        ];

        // Ambil Data dari LocalStorage
        function getCars() {
            const stored = localStorage.getItem('mustang_cars');
            return stored ? JSON.parse(stored) : defaultCars;
        }

        // Simpan Data ke LocalStorage
        function saveCarsToStorage(cars) {
            localStorage.setItem('mustang_cars', JSON.stringify(cars));
        }

        let currentFilter = 'all';

        // Render Katalog Mobil untuk Pengunjung
        function renderCars() {
            const cars = getCars();
            const grid = document.getElementById('carGrid');
            grid.innerHTML = '';

            const filteredCars = currentFilter === 'all' 
                ? cars 
                : cars.filter(c => c.transmission === currentFilter);

            if (filteredCars.length === 0) {
                grid.innerHTML = `
                    <div class="col-span-full text-center py-12 text-slate-500 text-xs">
                        Tidak ada unit mobil dengan filter pilihan ini.
                    </div>
                `;
                return;
            }

            filteredCars.forEach(car => {
                const isAvailable = car.status === 'Tersedia';
                const waMessage = encodeURIComponent(`Halo Mustang Rent Car, saya ingin bertanya/sewa unit ${car.name} (${car.transmission}).`);
                const waUrl = `https://wa.me/6281234567890?text=${waMessage}`;

                grid.innerHTML += `
                    <div class="bg-slate-950 border border-slate-800 rounded-2xl overflow-hidden hover:border-slate-700 transition group flex flex-col">
                        <div class="relative h-48 bg-slate-900 overflow-hidden">
                            <img src="${car.image || 'https://images.unsplash.com/photo-1549399542-7e3f8b79c341?w=600'}" alt="${car.name}" class="w-full h-full object-cover group-hover:scale-105 transition duration-300">
                            <span class="absolute top-3 right-3 text-[10px] font-bold uppercase tracking-wider px-2.5 py-1 rounded-md border ${
                                isAvailable 
                                ? 'bg-emerald-500/20 text-emerald-400 border-emerald-500/40' 
                                : 'bg-rose-500/20 text-rose-400 border-rose-500/40'
                            }">
                                ${car.status}
                            </span>
                        </div>
                        <div class="p-5 flex-grow flex flex-col justify-between">
                            <div>
                                <div class="flex justify-between items-start mb-2">
                                    <h4 class="text-base font-bold text-white">${car.name}</h4>
                                    <span class="text-xs text-amber-400 font-semibold bg-amber-400/10 px-2 py-0.5 rounded">${car.year}</span>
                                </div>
                                <div class="flex items-center gap-3 text-xs text-slate-400 mb-4">
                                    <span><i class="fa-solid fa-gears text-amber-400 mr-1"></i> ${car.transmission}</span>
                                    <span>•</span>
                                    <span><i class="fa-solid fa-users text-amber-400 mr-1"></i> ${car.seats}</span>
                                </div>
                            </div>
                            <div class="pt-3 border-t border-slate-900 flex items-center justify-between mt-2">
                                <div>
                                    <span class="text-[10px] text-slate-500 block">Tarif Sewa</span>
                                    <span class="text-base font-extrabold text-amber-400">Rp ${Number(car.price).toLocaleString('id-ID')}</span>
                                    <span class="text-[10px] text-slate-400">/24 Jam</span>
                                </div>
                                <a href="${waUrl}" target="_blank" class="bg-amber-500 hover:bg-amber-400 text-slate-950 font-bold px-4 py-2 rounded-xl transition text-xs flex items-center gap-1.5">
                                    <i class="fa-brands fa-whatsapp text-sm"></i> Sewa
                                </a>
                            </div>
                        </div>
                    </div>
                `;
            });
        }

        // Filter Mobil
        function filterCars(type) {
            currentFilter = type;
            document.querySelectorAll('.filter-btn').forEach(btn => {
                btn.classList.remove('bg-amber-500', 'text-slate-950');
                btn.classList.add('bg-slate-800', 'text-slate-300');
            });
            event.target.classList.remove('bg-slate-800', 'text-slate-300');
            event.target.classList.add('bg-amber-500', 'text-slate-950');
            renderCars();
        }

        // Modal Admin Toggle
        function toggleAdminModal() {
            const modal = document.getElementById('adminAuthModal');
            modal.classList.toggle('hidden');
        }

        // Login Admin PIN
        function handleAdminLogin(e) {
            e.preventDefault();
            const pin = document.getElementById('adminPin').value;
            if (pin === '1234') {
                toggleAdminModal();
                document.getElementById('adminDashboardModal').classList.remove('hidden');
                renderAdminCarList();
                document.getElementById('adminPin').value = '';
            } else {
                alert('PIN Salah! Masukkan PIN: 1234');
            }
        }

        function closeAdminDashboard() {
            document.getElementById('adminDashboardModal').classList.add('hidden');
        }

        // Render List Mobil di Admin Dashboard
        function renderAdminCarList() {
            const cars = getCars();
            const list = document.getElementById('adminCarList');
            list.innerHTML = '';

            cars.forEach(car => {
                list.innerHTML += `
                    <div class="bg-slate-950 border border-slate-800 p-3 rounded-xl flex items-center justify-between gap-3 text-xs">
                        <div class="flex items-center gap-3">
                            <img src="${car.image || 'https://images.unsplash.com/photo-1549399542-7e3f8b79c341?w=600'}" class="w-12 h-12 rounded-lg object-cover">
                            <div>
                                <h5 class="font-bold text-white">${car.name} (${car.year})</h5>
                                <p class="text-slate-400">Rp ${Number(car.price).toLocaleString('id-ID')} - ${car.transmission}</p>
                            </div>
                        </div>
                        <div class="flex items-center gap-2">
                            <button onclick="toggleCarStatus(${car.id})" class="px-2.5 py-1 rounded font-semibold ${car.status === 'Tersedia' ? 'bg-emerald-500/20 text-emerald-400 border border-emerald-500/30' : 'bg-rose-500/20 text-rose-400 border border-rose-500/30'}">
                                ${car.status}
                            </button>
                            <button onclick="deleteCar(${car.id})" class="bg-slate-800 hover:bg-rose-600 text-slate-400 hover:text-white p-2 rounded transition">
                                <i class="fa-solid fa-trash"></i>
                            </button>
                        </div>
                    </div>
                `;
            });
        }

        // Tambah Mobil Baru
        function saveCar(e) {
            e.preventDefault();
            const cars = getCars();
            const newCar = {
                id: Date.now(),
                name: document.getElementById('carName').value,
                year: document.getElementById('carYear').value,
                transmission: document.getElementById('carTransmission').value,
                seats: document.getElementById('carSeats').value,
                price: Number(document.getElementById('carPrice').value),
                status: 'Tersedia',
                image: document.getElementById('carImage').value || 'https://images.unsplash.com/photo-1549399542-7e3f8b79c341?w=600'
            };

            cars.unshift(newCar);
            saveCarsToStorage(cars);
            renderCars();
            renderAdminCarList();
            e.target.reset();
            alert('Mobil berhasil ditambahkan!');
        }

        // Ubah Status Available/Tersewa
        function toggleCarStatus(id) {
            const cars = getCars();
            const index = cars.findIndex(c => c.id === id);
            if (index !== -1) {
                cars[index].status = cars[index].status === 'Tersedia' ? 'Tersewa' : 'Tersedia';
                saveCarsToStorage(cars);
                renderCars();
                renderAdminCarList();
            }
        }

        // Hapus Mobil
        function deleteCar(id) {
            if (confirm('Yakin ingin menghapus mobil ini dari katalog?')) {
                let cars = getCars();
                cars = cars.filter(c => c.id !== id);
                saveCarsToStorage(cars);
                renderCars();
                renderAdminCarList();
            }
        }

        // Inisialisasi awal
        renderCars();
    </script>
</body>
</html>
