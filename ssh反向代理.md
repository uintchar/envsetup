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

`ssh -fCNR 1111:localhost:22 ubuntu@124.223.82.120`

建立内网服务器到公网服务器的反向代理，将公网服务器的1111端口转发到内网服务器的ssh端口（默认22），建立反向代理后，即可在公网服务器通过 `ssh -p 1111` 来ssh连接内网服务器

相当于创建了 `(192.168.1.220, 22)` 和 `(124.223.82.120, 1111)` 之间的socket连接，`(192.168.1.220, 22)` 为主动发起方

## 2.2. 正向代理设置

`ssh -fCNL *:2222:localhost:1111 localhost`

建立公网服务器的正向代理用于转发，将公网服务器本地的2222端口转发到公网服务器本地的1111端口

相当于创建了 `(124.223.82.120, 2222)` 和 `(124.223.82.120, 1111)` 之间的socket连接，`(124.223.82.120, 2222)` 为主动发起方


## 2.3. 稳定连接设置