---
title: include 文件
description: include 文件
services: container-registry
author: mmacy
ms.service: container-registry
ms.topic: include
ms.date: 05/29/2018
ms.author: marsma
ms.custom: include file
ms.openlocfilehash: 92a5d162e7a0b2c752a2f8e9c5941edf43e539e3
ms.sourcegitcommit: df50934d52b0b227d7d796e2522f1fd7c6393478
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/12/2018
ms.locfileid: "38991065"
---
| 资源 | 基本 | 标准 | 高级 |
|---|---|---|---|---|
| 存储 | 10 GiB | 100 GiB| 500 GiB |
| 最大映像层大小 | 20 GiB | 20 GiB | 50 GiB |
| 每分钟读取操作数<sup>1、2</sup> | 1,000 | 3,000 | 10,000 |
| 每分钟写入操作数<sup>1、3</sup> | 100 | 500 | 2,000 |
| 下载带宽 (MBps)<sup>1</sup> | 30 | 60 | 100 |
| 上传带宽 (MBps)<sup>1</sup> | 10 | 20 | 50 |
| Webhook | 2 | 10 | 100 |
| 异地复制 | 不适用 | 不适用 | [支持](https://docs.microsoft.com/azure/container-registry/container-registry-geo-replication) |

<sup>1</sup>读取操作数、写入操作数和带宽是最小估计值。 ACR 旨在随使用情况增多提升性能。

<sup>2</sup>[docker pull](https://docs.docker.com/registry/spec/api/#pulling-an-image) 根据映像中的层数和清单检索行为转换为多个读取操作。

<sup>3</sup>[docker push](https://docs.docker.com/registry/spec/api/#pushing-an-image) 根据必须推送的层数转换为多个写入操作。 `docker push` 包含 ReadOps，用于检索现有映像的清单。
