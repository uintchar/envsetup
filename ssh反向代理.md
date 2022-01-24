- [1. 正向代理和反向代理](#1-正向代理和反向代理)
- [2. ssh反向代理内网服务器](#2-ssh反向代理内网服务器)
  - [2.1. 反向代理设置](#21-反向代理设置)
  - [2.2. 正向代理设置](#22-正向代理设置)
  - [2.3. 稳定连接设置](#23-稳定连接设置)

# 1. 正向代理和反向代理

# 2. ssh反向代理内网服务器

SSH反向代理时，服务端主动发起SSH连接到代理服务器，将代理服务器指定端口接受到的请求通过SSH隧道转发到服务端的指定的端口上。

- https://blog.csdn.net/anychenp/article/details/104416200?utm_medium=distribute.pc_relevant.none-task-blog-BlogCommendFromMachineLearnPai2-4.nonecase&depth_1-utm_source=distribute.pc_relevant.none-task-blog-BlogCommendFromMachineLearnPai2-4.nonecase

- https://blog.csdn.net/xuxile/article/details/90179699?utm_medium=distribute.pc_relevant.none-task-blog-2~default~baidujs_title~default-0.pc_relevant_paycolumn_v3&spm=1001.2101.3001.4242.1&utm_relevant_index=3

**记得先为端口开放防火墙**

## 2.1. 反向代理设置

ssh -fCNR 1111:localhost:22 ubuntu@124.223.82.120

## 2.2. 正向代理设置

ssh -fCNL *:2222:localhost:1111 localhost


## 2.3. 稳定连接设置