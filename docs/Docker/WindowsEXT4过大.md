# Windows EXT4.vhdx 过大

## 清理Docker

```bash
docker system prune
```

## 关闭虚拟机

```bash
wsl --shutdown
```

## 清理vhdx

```bash
diskpart
select vdisk file="C:\Users\lsqtz\AppData\Local\Docker\wsl\data\ext4.vhdx"
attach vdisk readonly
compact vdisk
detach vdisk
exit
```

## Ref

https://blog.csdn.net/lsqtzj/article/details/120960306
