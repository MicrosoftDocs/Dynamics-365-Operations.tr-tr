---
title: Serbest bırakılan bir ürünü silemezsiniz
description: Serbest bırakılan bir ürünü ve tüm varyantlarını yalnızca serbest bırakılan ürünün ilgili işlemleri yoksa silebilirsiniz.
author: SmithaNataraj
ms.date: 06/11/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 2f03d45a36401314a4b02ff354fabb474568c48b
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477880"
---
# <a name="you-cant-delete-a-released-product"></a>Serbest bırakılan bir ürünü silemezsiniz

## <a name="symptoms"></a>Belirtiler

Serbest bırakılan bir ürünü ve tüm varyantlarını yalnızca serbest bırakılan ürünün ilgili işlemleri yoksa silebilirsiniz.

## <a name="resolution"></a>Çözüm

Serbest bırakılmış bir ürünü veya ürün yöneticisini silmek için aşağıdaki adımları izleyin.

1. Maddeler için tüm açık hareketleri kapatın.
1. Stoğu 0'a (sıfır) düşürün.
1. Stok kapanışı gerçekleştirin.
1. Silmek istediğiniz ana ürün için tüm ürün varyantlarını silin.
