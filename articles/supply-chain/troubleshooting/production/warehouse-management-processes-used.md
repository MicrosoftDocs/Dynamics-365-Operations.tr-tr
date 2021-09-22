---
title: Ambar yönetimi işlemleri şu anda kullanılıyor
description: İş rezerve edilirken veya serbest bırakılırken ambar yönetimi işlemlerinin şu anda kullanılmakta olduğuna dair bir ileti alabilirsiniz. Bu adımlardan biriyle sorunu düzeltin.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: bfda2fae824cdc64d722310d20cf16e6306d766c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477800"
---
# <a name="cant-reserve-or-release-work-because-processes-are-currently-being-used"></a>İşlemler şu anda kullanılmakta olduğundan iş rezerve edilemiyor veya serbest bırakılamıyor

## <a name="symptoms"></a>Belirtiler

Parçalı üretim ile çalışırken aşağıdaki hatayı alırsınız:

> Ambar yönetimi işlemleri şu anda kullanılıyor. İş satırları henüz kaydedilmemişse oluşturulan işi ve herhangi bir yük veya sevkiyat satırını iptal edebilir ve ardından malzeme çekme ya da sevkiyat işlemine devam edebilirsiniz.

## <a name="cause"></a>Nedeni

Bu sorun, bir satır için çalışmayı ayırmaya veya serbest bırakmaya çalışırsanız oluşur ancak stok hareketinin, malzemenin alındığını gösteren *Teslim Alındı* durumu vardır.

## <a name="resolution"></a>Çözüm

Bu sorunu düzeltmek için şu adımlardan birini izleyin.

- Üretim siparişinin durumunu *Tahmini* veya *Serbest Bırakılmış* olarak değiştirin.
- İlgili üretim emrinin ayrıntılar sayfasını açın. Eylem bölmesinde, **Ambar** sekmesinde, **Durdurma** grubunda, tüm teslim alınmış hareketlerin çekme işlemini iptal etmek için **Durdur ve çekmeyi iptal et**'i seçin. Ardından, üretim emrini işlemek için **Durdurmayı kaldır**'ı seçin.

Burada *Çekmeyi iptal et* ve *Durdur* işlevlerinin açıklaması verilmiştir:
  
- **Çekmeyi iptal et**: Bu işlev, sipariş üzerine *Teslim Alındı*'dan *Siparişte*'ye kadar durumu olan ürün reçetesi satırları ve formül satırları için stok hareketlerinin durumunu tersine çevirir. Ham madde teslim alma işi tamamlandığında, satırların durumu *Teslim Alındı* olarak ayarlanır. Bu durum, üretim emrinin *Oluşturuldu* durumuna sıfırlanmasını önler. Bu durumda, *Teslim Alındı* durumdaki hareketleri geri almak ve ardından üretim emrini *Oluşturuldu* durumuna sıfırlamak için *Çekmeyi İptal Et* işlevini kullanabilirsiniz.
- **Durdur**: Bu işlev, siparişte herhangi bir durum güncelleştirmesini önlemek için üretim emrinde **Durduruldu** işareti ayarlar. Üretim emri ayrıntıları sayfasının **Ambar** hızlı sekmesinde **Durduruldu** işaretini bulabilirsiniz.

> [!NOTE]
>
> - Düğmeler yalnızca ambar işlemleri için etkinleştirilen maddeler için üretim emri oluşturulduğunda görünür.
> - **Durdur** grubu yalnızca üretim sırası ayrıntıları sayfasının Eylem bölmesindeki **Ambar** sekmesinde görünür. **Üretim emirleri** listesi sayfasının **Ambar** hızlı sekmesinde görünmez.
