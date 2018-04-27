--- 
title: "Sabit kıymetleri yeniden sınıflandırma"
description: "Sabit kıymeti yeniden sınıflandırmak için yeni bir sabit kıymet grubuna transfer etmeniz veya kıymete aynı grup içerisinde yeni bir sabit kıymet numarası atamanız gerekir."
author: saraschi2
manager: AnnBe
ms.date: 10/30/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: cafd499e849570cae7b7f58bf2d487a7ac0093e6
ms.openlocfilehash: 6bce294329c7ec6dc436c3d3baf6597e0283c9bd
ms.contentlocale: tr-tr
ms.lasthandoff: 10/30/2017

---
# <a name="reclassify-fixed-assets"></a>Sabit kıymetleri yeniden sınıflandırma

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Sabit kıymeti yeniden sınıflandırmak için yeni bir sabit kıymet grubuna transfer etmeniz veya kıymete aynı grup içerisinde yeni bir sabit kıymet numarası atamanız gerekir. 

Bir sabit kıymet yeniden sınıflandırıldığında:

• Varolan sabit kıymete yönelik tüm değer modelleri, yeni sabit kıymet için oluşturulur. Özgün sabit kıymet için oluşturulan bilgiler yeni sabit kıymete kopyalanır. Özgün sabit kıymete yönelik değer modellerinin durumu Kapalı'dır. 

• Yeni sabit kıymete yönelik yeni değer modelleri Alım tarihi alanındaki yeniden sınıflandırma tarihini içerir. İlk amortisman göreceği tarih alanındaki tarih, özgün kıymet bilgilerinden kopyalanır. Amortisman önceden başlamışsa Amortismanın son çalıştırıldığı tarih alanında yeniden sınıflandırma tarihi görüntülenir. 

• Özgün sabit kıymetlere yönelik mevcut sabit kıymet hareketleri iptal edilir ve yeni sabit kıymet için yeniden oluşturulur.

1. Sabit kıymetler > Dönemsel görevler > Yeniden sınıflandırma öğesine gidin.
2. Sabit kıymet grubu alanında, yeniden sınıflandırılacak grubu seçin.
3. Sabit kıymet numarası alanında, yeniden sınıflandırılacak sabit kıymeti seçin.
4. Yeni sabit kıymet grubu alanında, sabit kıymetin transfer edileceği grubu seçin.
    * Yeni sabit kıymet grubu bir numara serisine eklenmişse Yeni sabit kıymet numarası alanı, yeni sabit kıymet grubu numara serisindeki numara ile güncelleştirilir. Aksi takdirde, Yeni sabit kıymet numarası alanı Sabit kıymet parametreleri sayfasında ayarlanan numara serisindeki numara ile güncelleştirilir. Numara serisi Sabit kıymet parametreleri sayfasında ayarlanmadıysa Yeni sabit kıymet numarası alanına bir numara girin.  
5. Yeniden sınıflandırma tarihi alanına bir tarih girin.
6. Fiş serisi alanına bir değer girin veya bir değer seçin.
7. Tamam'a tıklayın.


