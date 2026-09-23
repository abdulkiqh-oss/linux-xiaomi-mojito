# linux-xiaomi-mojito: postmarketOS Kernel Package for Xiaomi Redmi Note 10

This repository contains the downstream Linux kernel package (`linux-xiaomi-mojito`) build configuration for **postmarketOS** targeting the **Xiaomi Redmi Note 10** (codename: `mojito`)[cite: 2].

It builds a downstream Android kernel (Linux Kernel 4.14.190) adapted for postmarketOS on the `aarch64` architecture[cite: 2].

---

## 📂 Repository Contents

* **`APKBUILD`**: Alpine Linux build script defining the build steps, cross-compilation options, and dependencies (e.g., `flex`, `bison`, `openssl-dev`, `linux-headers`)[cite: 2].
* **`config-xiaomi-mojito.aarch64`**: The main kernel configuration file containing enabled drivers and hardware options for `mojito`[cite: 2].
* **`compiler-gcc.h`**: Compiler header compatibility file used during kernel compilation[cite: 2].

---

## 🛠️ How to Build

1. Place this repository in your local `pmaports` tree under `main/linux-xiaomi-mojito` or `testing/linux-xiaomi-mojito`.
2. Build the kernel package using `pmbootstrap`:
   ```bash
   pmbootstrap build linux-xiaomi-mojito
