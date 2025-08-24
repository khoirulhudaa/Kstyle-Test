Project React Vite
Proyek ini adalah aplikasi React dengan Vite dan TypeScript, termasuk fungsi utilitas untuk memformat angka ke Rupiah Indonesia (IDR).
Penjelasan Props dengan TypeScript
Props adalah cara untuk mengirim data dari parent ke child component di React. Props bersifat read-only, membuat komponen lebih modular dan reusable. Dengan TypeScript, kita bisa mendefinisikan tipe untuk props agar aman dan mencegah error.
Contoh:
interface MyComponentProps {
  name: string;
  age?: number;
  onClick: () => void;
}

const MyComponent: React.FC<MyComponentProps> = ({ name, age, onClick }) => {
  return (
    <div>
      <p>Hello, {name}!</p>
      {age && <p>Age: {age}</p>}
      <button onClick={onClick}>Click Me</button>
    </div>
  );
};

Keuntungan:

Type safety mencegah kesalahan tipe data.
Autocompletion di IDE.
Optional props dengan ? dan default props didukung.

Penjelasan TanStack
TanStack adalah kumpulan library open-source untuk mengelola data, state, dan UI di aplikasi JavaScript/TypeScript. Contohnya:

TanStack Query: Untuk fetching, caching, dan sync data API.
TanStack Table: Untuk tabel dengan sorting dan filtering.
TanStack Router: Router modern untuk React.

Keuntungan:

Modular, headless, dan TypeScript-first.
Performa tinggi untuk aplikasi skala besar.
Dokumentasi lengkap di tanstack.com.

Prasyarat

Node.js (versi 18 atau lebih tinggi).
npm sebagai package manager.
Git (opsional untuk cloning).

Langkah Menjalankan Proyek

Clone Repository:
git clone <repository-url>
cd <project-directory>


Install Dependencies:
npm i --legacy-peer-deps


Jalankan Server:
npm run dev


Akses Aplikasi:

Buka http://localhost:3000 di browser.



Struktur Proyek

src/: Kode sumber.
components/: Komponen React.
utils/: Fungsi utilitas seperti formatToRupiah.ts.


public/: Aset statis.
vite.config.ts: Konfigurasi Vite.
tsconfig.json: Konfigurasi TypeScript.

Contoh Penggunaan
import formatToRupiah from './utils/formatToRupiah';

const App = () => {
  return <div>{formatToRupiah(100000)}</div>; // Output: Rp100.000
};

Troubleshooting

Port Conflict: Cek terminal untuk port alternatif jika 3000 sudah digunakan.
Error Dependencies: Hapus node_modules/ dan package-lock.json, lalu jalankan npm i --legacy-peer-deps.
TanStack: Install dengan npm i @tanstack/react-query --legacy-peer-deps dan lihat tanstack.com.
