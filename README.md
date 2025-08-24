## Penjelasan Props dengan TypeScript

**Props** adalah cara untuk mengirim data dari *parent* ke *child component* di React. Props bersifat **read-only**, yang membuat komponen lebih **modular** dan **reusable**. Dengan **TypeScript**, kita bisa mendefinisikan tipe untuk props agar aman dan mencegah error.

### Contoh:
```tsx
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

## ✅ Keuntungan Menggunakan TypeScript untuk Props

- ✅ Type safety mencegah kesalahan tipe data.
- ✅ Autocompletion di IDE.
- ✅ Mendukung optional props (`?`) dan default props.

---

## 📦 Penjelasan TanStack

TanStack adalah kumpulan library open-source untuk mengelola data, state, dan UI di aplikasi JavaScript/TypeScript.

### 🔧 Beberapa Library Populer TanStack:

- 📊 **TanStack Query**: Untuk fetching, caching, dan sinkronisasi data API.
- 📋 **TanStack Table**: Untuk membuat tabel dinamis dengan fitur sorting dan filtering.
- 🧭 **TanStack Router**: Router modern untuk React yang powerful dan fleksibel.

### 🎯 Keuntungan Menggunakan TanStack:

- ✅ Modular, headless, dan TypeScript-first.
- ✅ Performa tinggi, cocok untuk aplikasi skala besar.
- ✅ Dokumentasi lengkap dan aktif di [tanstack.com](https://tanstack.com)


# 🚀 Langkah Menjalankan Proyek

1. **Clone Repository**
```bash
git clone <repository-url>
cd <project-directory>
npm i --legacy-peer-deps 
npm run dev
access => http://localhost:3000
