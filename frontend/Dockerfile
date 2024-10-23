# Menggunakan image resmi Node.js sebagai image dasar
FROM node:16

# Menetapkan direktori kerja
WORKDIR /app

# Menyalin package.json dan package-lock.json
COPY package*.json ./

# Menginstal dependensi
RUN npm install

# Menyalin sisa kode aplikasi
COPY . .

# Membangun aplikasi untuk produksi
RUN npm run build

# Menginstal serve untuk menyajikan aplikasi
RUN npm install -g serve

# Mengekspos port tempat aplikasi berjalan
EXPOSE 3000

# Perintah untuk menjalankan aplikasi
CMD ["serve", "-s", "dist"]
