---
title: Sabit kıymetleri yeniden sınıflandırma
description: Sabit kıymeti yeniden sınıflandırmak için yeni bir sabit kıymet grubuna transfer etmeniz veya kıymete aynı grup içerisinde yeni bir sabit kıymet numarası atamanız gerekir.
author: saraschi2
ms.date: 05/14/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8935213c4629de408a48df5e54a2122324e1b3e7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823944"
---
# <a name="reclassify-fixed-assets"></a>Sabit kıymetleri yeniden sınıflandırma

[!include [banner](../../includes/banner.md)]

Sabit kıymeti yeniden sınıflandırmak için yeni bir sabit kıymet grubuna transfer etmeniz veya kıymete aynı grup içerisinde yeni bir sabit kıymet numarası atamanız gerekir. 

Bir sabit kıymet yeniden sınıflandırıldığında:

* Varolan sabit kıymete yönelik tüm defterler, yeni sabit kıymet için oluşturulur. Özgün sabit kıymet için oluşturulan bilgiler yeni sabit kıymete kopyalanır. Özgün sabit kıymete yönelik defterlerin durumu Kapalı'dır. 

* Yeni sabit kıymete yönelik yeni defterler **Alım tarihi** alanındaki yeniden sınıflandırma tarihini içerir. **İlk amortisman göreceği tarih** alanındaki tarih, özgün kıymet bilgilerinden kopyalanır. Amortisman önceden başlamışsa **Amortismanın son çalıştırıldığı tarih** alanında yeniden sınıflandırma tarihi görüntülenir. 

* Özgün sabit kıymetlere yönelik mevcut sabit kıymet hareketleri iptal edilir ve yeni sabit kıymet için yeniden oluşturulur.

Bir sabit kıymeti yeniden sınıflandırmak için şu adımları Izleyin:

1. **Sabit kıymetler > Dönemsel görevler > Yeniden sınıflandırma** öğesine gidin.
2. **Sabit kıymet grubu** alanında, yeniden sınıflandırılacak grubu seçin.
3. **Sabit kıymet numarası** alanında, yeniden sınıflandırılacak sabit kıymeti seçin.
4. **Yeni sabit kıymet grubu** alanında, sabit kıymetin transfer edileceği grubu seçin.
    * Yeni sabit kıymet grubu bir numara serisine eklenmişse **Yeni sabit kıymet numarası** alanı, yeni sabit kıymet grubu numara serisindeki numara ile güncelleştirilir. Aksi takdirde, **Yeni sabit kıymet numarası** alanı **Sabit kıymet parametreleri** sayfasında ayarlanan numara serisindeki numara ile güncelleştirilir. Numara serisi **Sabit kıymet parametreleri** sayfasında ayarlanmadıysa **Yeni sabit kıymet numarası** alanına bir numara girin.  
5. **Yeniden sınıflandırma tarihi** alanına bir tarih girin.
6. **Fiş serisi** alanına bir değer girin veya bir değer seçin.
7. **Tamam**'a tıklayın.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]