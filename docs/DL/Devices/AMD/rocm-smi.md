rocm-smi
===

# Install

# Unable to load the rocm_smi library

```
Unable to load the rocm_smi library.
Set LD_LIBRARY_PATH to the folder containing librocm_smi64.so.1
Please refer to https://github.com/RadeonOpenCompute/rocm_smi_lib for the installation guide.
```

1. Installing python 3.11. I had the issue with python 3.12
	安装 python 3.11。我在使用 python 3.12 时遇到了问题
2. Updating the libgcc to its latest version.
	将 libgcc 更新到最新版本。

```bash
conda install -c conda-forge libgcc
```

https://github.com/ROCm/ROCm/issues/1274#issuecomment-2143487469

# Ref

https://rocm.docs.amd.com/projects/rocm_smi_lib/en/latest/how-to/use-python.html
