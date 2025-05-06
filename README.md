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
