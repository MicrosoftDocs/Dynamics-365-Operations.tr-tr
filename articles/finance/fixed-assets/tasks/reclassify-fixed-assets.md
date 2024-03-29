---
title: Sabit kıymetleri yeniden sınıflandırma
description: Bu makale, kıymetleri tekrar sınıflandırma işlemini açıklar. Sabit kıymeti yeniden sınıflandırmak için yeni bir sabit kıymet grubuna transfer etmeniz veya kıymete aynı grup içerisinde yeni bir sabit kıymet numarası atamanız gerekir.
author: moaamer
ms.date: 05/14/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4bd901b1709f0b006cecfbbf6d8c170b56f89d19
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284378"
---
# <a name="reclassify-fixed-assets"></a>Sabit kıymetleri yeniden sınıflandırma

[!include [banner](../../includes/banner.md)]

Sabit kıymeti yeniden sınıflandırmak için yeni bir sabit kıymet grubuna transfer etmeniz veya kıymete aynı grup içerisinde yeni bir sabit kıymet numarası atamanız gerekir. 

Bir sabit kıymet yeniden sınıflandırıldığında:

- Varolan sabit kıymete yönelik tüm defterler, yeni sabit kıymet için oluşturulur. Özgün sabit kıymet için oluşturulan bilgiler yeni sabit kıymete kopyalanır. Özgün sabit kıymete yönelik defterlerin durumu Kapalı'dır. 

- Yeni sabit kıymete yönelik yeni defterler **Alım tarihi** alanındaki yeniden sınıflandırma tarihini içerir. **İlk amortisman göreceği tarih** alanındaki tarih, özgün kıymet bilgilerinden kopyalanır. Amortisman önceden başlamışsa **Amortismanın son çalıştırıldığı tarih** alanında yeniden sınıflandırma tarihi görüntülenir. 

- Özgün sabit kıymetlere yönelik mevcut sabit kıymet hareketleri iptal edilir ve yeni sabit kıymet için yeniden oluşturulur.

- Transfer hareketi olan bir varlık yeniden sınıflandırıldığında sistem, bir transfer hareketinin yeniden sınıflandırma işlemi sırasında tamamlanmadığını belirtmek üzere **Eylem merkezi**'nde bir ileti görüntüler. Varolan yeniden sınıflandırma hareketlerini uygun mali boyutlara taşımak için bir transfer hareketini tamamlamak gereklidir. 

   Yeniden sınıflandırma işlemi sırasında, sistem varlık bakiyesini orijinal varlıktan yeni varlığa sınıflandırmak için aşağıdaki eylemleri çalıştırır. 
   
   - Yeniden sınıflama işlemi, verileri orijinal sabit varlık defterinden yeni sabit varlık defterine kopyalar.

   - Yeniden sınıflama hareketi, alım hareketine dahil edilen mali boyut bilgilerini içeren orijinal deftere nakledilen edinme bilgilerini kullanır.  
   
   - Aynı zamanda, yeniden sınıflama işlemi, orijinal varlık alımı ve varlık transfer hareketini tersine çevirir. 

Aşağıdaki diyagram ve prosedür, yeniden sınıflandırma işlemine bir örnek verir. 

[![Yeniden sınıflandırma işlemini gösteren diyagram.](../media/reclassification-process-01.png)](../media/reclassification-process-01.png)

Bir sabit kıymeti yeniden sınıflandırmak için şu adımları Izleyin:

1. **Sabit kıymetler > Dönemsel görevler > Yeniden sınıflandırma** öğesine gidin.
2. **Sabit kıymet grubu** alanında, yeniden sınıflandırılacak grubu seçin.
3. **Sabit kıymet numarası** alanında, yeniden sınıflandırılacak sabit kıymeti seçin.
4. **Yeni sabit kıymet grubu** alanında, sabit kıymetin transfer edileceği grubu seçin.
    * Yeni sabit kıymet grubu bir numara serisine eklenmişse **Yeni sabit kıymet numarası** alanı, yeni sabit kıymet grubu numara serisindeki numara ile güncelleştirilir. Aksi takdirde, **Yeni sabit kıymet numarası** alanı **Sabit kıymet parametreleri** sayfasında ayarlanan numara serisindeki numara ile güncelleştirilir. Numara serisi **Sabit kıymet parametreleri** sayfasında ayarlanmadıysa **Yeni sabit kıymet numarası** alanına bir numara girin.  
5. **Yeniden sınıflandırma tarihi** alanına bir tarih girin.
6. **Fiş serisi** alanına bir değer girin veya bir değer seçin.
7. **Tamam**'ı seçin.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
