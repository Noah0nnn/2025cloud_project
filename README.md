# 2025cloud 專案

本專案為一個公開的 Docker 專案示範，包含兩個不同版本的應用程式，並對應至兩個以上的 container image，分別為 `v1` 和 `v2`。這些映像檔皆已發布至 Docker Hub 公開倉庫 [`naoh0nnn/2025cloud`](https://hub.docker.com/repository/docker/noah0nnn/2025cloud)。



---
## 🚀 自動化建置流程架構圖

```plaintext
Push 到 main 分支 or PR → GitHub Action 觸發
              │
              ▼
    對 image1 執行 docker build（tag: v1）
    對 image2 執行 docker build（tag: v2）
              │
              ▼
   登入 Docker Hub 並 push 至：
   - docker.io/你的帳號/2025cloud:v1
   - docker.io/你的帳號/2025cloud:v2
```

---

## 🐳 如何 Build Docker Images 

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
### 如何 Run Container

可以選擇「從本地 build 的 image」或「從 Docker Hub 上下載的 image」來執行 container。

✅ 方法一：使用本地建置的 image 執行
```bash
docker run --rm noah0nnn/2025cloud:v1
docker run --rm noah0nnn/2025cloud:v2
```
✅ 方法二：直接從 Docker Hub 拉取並執行
```bash
docker run --rm noah0nnn/2025cloud:v1
docker run --rm noah0nnn/2025cloud:v2
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

🧩 標籤（Tag）設計邏輯

採用 固定版本標籤設計：

Image 資料夾	Docker Tag	說明:
```
image1/	v1	對應第一個應用程式版本
image2/	v2	對應第二個應用程式版本
```

✏️ 每個 image 都有獨立的 Dockerfile、功能與對應 tag，方便追蹤與維護。





