---
title: Hareketler işlenirken stok sahibine izin verilmiyor
description: "\"%1 stok sahibine izin verilmiyor\" hatasını alabilirsiniz. Ambar yönetimi işlemleri yalnızca tüzel kişiliklerin sahip olduğu stokları destekler."
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4ee29cfc7bad990cd1ee5deaa98fca217af772ed
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477824"
---
# <a name="inventory-owner-not-allowed-when-processing-movements-in-the-warehouse-app"></a>Ambar uygulamasında hareketler işlenirken stok sahibine izin verilmiyor

## <a name="symptoms"></a>Belirtiler

Warehouse Management mobil uygulamasında hareketler işlenirken aşağıdaki hata iletisini alabilirsiniz:

> Bu işlemde %1 stok sahibine izin verilmiyor.

## <a name="cause"></a>Nedeni

Warehouse Management mobil uygulaması hareketleri oluşturmak için kullanılırken **Sahip** izleme boyutu eksik olduğundan bu hata oluşur. Supply Chain Management istemcisinden alınan düzenli bir stok transferi günlüğü, istendiği gibi çalışır ve yalnızca **Sahip** boyutu doldurulmuşsa deftere nakledilebilir.

## <a name="resolution"></a>Çözüm

Microsoft bu sorunu değerlendirmiş ve bir özellik sınırlaması olduğunu tespit etmiştir. Şu anda, ambar yönetimi işlemleri yalnızca tüzel kişiliklerin sahip olduğu stokları destekler.
