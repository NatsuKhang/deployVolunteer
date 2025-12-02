# 1. Chọn môi trường Node.js (phiên bản nhẹ)
FROM node:22-alpine

# 2. Tạo thư mục làm việc trong container
WORKDIR /app

# 3. Copy file quy định thư viện trước (để tận dụng bộ nhớ đệm của Docker)
COPY package.json package-lock.json ./

# 4. Cài đặt thư viện
RUN npm install

# 5. Copy toàn bộ code frontend vào
COPY . .

# 6. Mở port 5173 (Port của Vite)
EXPOSE 5173

# 7. Chạy lệnh start (Thêm --host để Docker cho phép truy cập từ bên ngoài)
CMD ["npm", "run", "dev", "--", "--host"]