---
title: Bir satış siparişi iptal edildiğinde miktar azaltılamaz
description: Bir satış siparişi iptal edildiğinde miktar azaltılamaz.
author: hja-ms
ms.date: 5/17/2021
ms.topic: troubleshooting
ms.search.form: SalesTable_SalesCancelOrder, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: hja
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f3453c83b5e8ead4269a6054167d73a0cd12381ba374b98bc407c01edaa68a1c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752646"
---
# <a name="the-quantity-cant-be-reduced-when-a-sales-order-is-canceled"></a>Bir satış siparişi iptal edildiğinde miktar azaltılamaz

Hata kodu: SYS138831

## <a name="symptoms"></a>Belirtiler

Sistem, aşağıdaki hata iletisini gösterir:

> Miktar azaltılamaz. Miktarı veya parçası bir çıkış siparişi veya üretim siparişi tarafından referans alındığından veya diğer hareketlere karşı işaretlendiğinden bir siparişteki stok hareketleri sayısı çok düşük.

## <a name="cause"></a>Nedeni

İş bir satış siparişiyle ilişkilendirilmişse, iş iptal edilene ve ters çevrilinceye kadar satış siparişini iptal edemezsiniz. Bu gereksinim, satış siparişiyle ilişkilendirilmiş iş kapatılmış olsa bile geçerlidir.

## <a name="resolution"></a>Çözüm

Bu sorunu gidermek için aşağıdaki görevleri tamamlayın:

1. Açık çalışmayı iptal edin.
1. Yükü silin.
1. Çekilen miktarı azaltın.

### <a name="cancel-open-work"></a>Açık çalışmayı iptal etme

Açık çalışmayı iptal etmek için aşağıdaki adımları izleyin.

1. **Ambar yönetimi \> Periyodik görevler \> Temizleme \>Çalışmayı iptal et**'e gidin.
1. **Çalışma kodu** alanında, iptal etmek istediğiniz şu anda **Çalışma durumu** değeri *Açık*, *Devam ediyor*, *İptal edildi*, *Birleştirilmiş* veya *Kapalı* olan çalışmanın kodunu belirtin.
1. **Tamam**'ı seçin.
1. Çalışmayı iptal etmek istediğinizi onaylamak için **Evet**'i seçin.

### <a name="delete-the-load"></a>Yükü silme

Yükü silmek için aşağıdaki adımları izleyin.

1. **Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.
1. İlgili satış siparişini açın.
1. **Satış siparişi satırları** hızlı sekmesinde **Ambar \> İş ayrıntıları**'nı seçin.
1. **İş** sayfasında, Eylem Bölmesinde, **İş** sekmesinde, **İş** grubunda, **İşi iptal et**'i seçin.
1. **İş durumu** alanının *İptal edildi* olarak ayarlandığını onaylayın.
1. **İş** sayfasını kapatın.
1. Satış siparişi ayrıntıları sayfasında, **Satış siparişi satırları** hızlı sekmesinde **Ambar \> Yük ayrıntıları**'nı seçin.
1. Eylem Bölmesi'nde **Sil**'i seçin.
1. Yükü silmek istediğinizi onaylamak için **Evet**'i seçin.
1. **Yük** sayfasını kapatın.

### <a name="reduce-the-picked-quantity"></a>Çekilen miktarı azaltma

Tüm işler iptal edildikten sonra çekilen miktarı azaltmak için aşağıdaki adımları izleyin.

1. **Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.
1. İlgili satış siparişini açın.
1. **Satış siparişi satırları** hızlı sekmesinde, araç çubuğundan **Satırı güncelleştir \> Malzeme çek**'i seçin.
1. **Malzeme çekme** sayfasında, **Hareketler** bölümünde, **Çıkış durumu** alanının *Malzeme çekildi* olarak ayarlandığı satırı seçin.
1. **Hareketler** bölümünde, araç çubuğundan **Malzeme çekme satırı ekle**'yi seçin.
1. **Malzeme çekme satırları** bölümünde, araç çubuğundan **Tümünü çekmeyi onayla**'yı seçin.
1. **Malzeme çekme** sayfasını kapatın.
1. Satış siparişi ayrıntıları sayfasındaki Eylem Bölmesinde, **Satış siparişi** sekmesinde **Koruma** grubunda **İptal**'i seçin.
1. Satış siparişini iptal etmek istediğinizi onaylamak için **Evet**'i seçin.
