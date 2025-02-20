amd-smi
===

# Official

https://rocm.docs.amd.com/projects/amdsmi/en/latest/how-to/amdsmi-py-lib.html

https://rocm.docs.amd.com/projects/amdsmi/en/latest/reference/amdsmi-py-api.html

## Clone Source Code

https://github.com/ROCm/amdsmi

```bash
git clone https://github.com/ROCm/amdsmi.git

cd amdsmi
```

## Change Branch

```bash
git checkout -b rocm-6.2.x origin/rocm-6.2.x
```

## Build `amdsmi`

```bash
mkdir -p build
cd build
cmake ..
make -j $(nproc)

# Install
sudo make install
```

## Change Ubuntu Mirrors

```bash
vim py-interface/Dockerfile
```

https://mirrors.huaweicloud.com/mirrorDetail/5ea14ecab05943f36fb75ee7?mirrorName=ubuntu&catalog=os

Add under line before `apt update`

```Dockerfile
RUN    sed -i "s@http://.*archive.ubuntu.com@http://mirrors.huaweicloud.com@g" /etc/apt/sources.list \
	&& sed -i "s@http://.*security.ubuntu.com@http://mirrors.huaweicloud.com@g" /etc/apt/sources.list
```

## Update Python binding

```bash
./update_wrapper.sh
```

# Unofficial Python binding

```bash
pip install amdsmi
```

**Notice:**

Need `libamd_smi.so`!

https://github.com/ml-energy/amdsmi

# Ref
