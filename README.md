# 2025cloud

This repository contains two simple Docker applications:
- `image1`: Prints "Hello from image 1"
- `image2`: Prints "Hello from image 2"

These images are designed for demonstration and are built from minimal `Dockerfile`s using Alpine Linux.

---

## 🐳 How to Build Docker Images Locally

You can manually build each image with the following commands:

### 🔧 Build `image1`

```bash
docker build -t image1:latest ./image1
```

### 🔧 Build `image2`

```bash
docker build -t image2:latest ./image2
```
---
### 如何將映像檔推送至 Docker Hub

步驟一：登入 Docker Hub
```bash
docker login
```
步驟二：推送兩個版本的 image
```bash
docker push yourusername/2025cloud:v1
docker push yourusername/2025cloud:v2
```

