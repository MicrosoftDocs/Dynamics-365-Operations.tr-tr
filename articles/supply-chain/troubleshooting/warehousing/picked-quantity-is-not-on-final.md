---
title: Teslim alınmadığı için sevkiyatı onaylayamazsınız
description: Teslim alınmadığı için sevkiyatı onaylayamazsınız
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 7b57d3151852c9a2880185b7d9414e4246b7efb6429fcfce04c7cdae4ee00e37
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760936"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a>Teslim alınmadığı için sevkiyatı onaylayamazsınız

Hata kodu: LoadNotPickedAndMovedToFinalShippingLocation

## <a name="symptoms"></a>Belirtiler

Bir sevkiyatı onaylamaya çalıştığınızda, sistem aşağıdaki hata iletisini gösterir:

> %1 yükü için ihtiyaç duyulan maddelerin bazıları henüz çekilmedi ve son sevkiyat konumuna taşındı.

Bu nedenle, yükleme için sevkiyat işlemini onaylayamazsınız.

## <a name="cause"></a>Nedeni

Aşağıdaki koşullardan biri mevcut olduğu için yük veya sevkiyat mevcut durumunda onaylanamıyor:

- İlgili iş henüz teslim alınmadı ve son sevkiyat konumuna taşınmadı.
- Teslim alınan iş miktarı, yükleme satırında oluşturulan iş miktarıyla eşleşmiyor.
- Yerleşim yönergesi, paketleme yerleşimi son sevkiyat yerleşimi olarak ve Dalga şablonu konteynerlemesi kullanılarak yapılandırılmıştır.

## <a name="resolution"></a>Çözüm

Yükleme veya sevkiyat işlemi şu anda sevkiyat onayının başarısız olduğu bir durumdadır. Bu sorunu gidermek için aşağıdaki görevlerden birini tamamlayın:

- Yük satırlarınızı gözden geçirin ve tüm ilgili işlerin son sevkiyat konumunda tamamlandığından ve miktarların aynı olduğundan emin olun.
- Paketleme yerleşimi son sevkiyat yerleşimi olarak oluşturulan iş kodlarını iptal edin, konum yönergesini yeniden yapılandırın ve yükü yeniden serbest bırakın.

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Yük satırlarınızı gözden geçirin ve tüm ilgili işlerin son sevkiyat konumunda tamamlandığından ve miktarların aynı olduğundan emin olun

Yük satırlarınızı gözden geçirmek için aşağıdaki yordamı kullanın ve tüm ilgili işlerin son sevkiyat konumunda tamamlandığından ve miktarların aynı olduğundan emin olun.

1. **Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.
1. Sevkiyatın onaylanamadığı ilgili yükü seçin.
1. **Yük satırları** hızlı sekmesinde, yük satırını seçin.
1. **Oluşturulan iş miktarı** alanının değerini not alın.
1. Eylem Bölmesinde **Yüklemeler** sekmesindeki **İlgili bilgiler** grubunda **Çalışma**'yı seçin.
1. İşin son sevkiyat konumunda tamamlandığını ve teslim alınan iş miktarının yükleme satırındaki oluşturulan iş miktarıyla eşleştiğini doğrulayın.
1. Tüm ölçütlerin karşılandığından emin olmak için bu prosedürü tüm yükleme satırları için yineleyin.

### <a name="cancel-the-work-ids-that-have-been-created-with-the-packing-location-as-the-final-shipping-location-reconfigure-the-location-directive-and-rerelease-the-load"></a>Paketleme yerleşimi son sevkiyat yerleşimi olarak oluşturulan iş kodlarını iptal edin, konum yönergesini yeniden yapılandırın ve yükü yeniden serbest bırakın

Otomatik konteynerlemenin bulunduğu ile son koyma yerleşimi olarak paketleme yerleşimine sahip iş kodlarını iptal etmek için aşağıdaki yordamı kullanın.

1. **Ambar yönetimi \> Periyodik görevler \> Temizleme \>Çalışmayı iptal et**'e gidin.
1. **İşi iptal et** iletişim kutusu açılır. **İş kimliği** alanında, iptal etmek istediğiniz iş kaydının kodunu belirtin. Seçili iş kodu için **İş durumu** değeri şunlardan biri olmalıdır: *Açık*, *Devam Ediyor*, *İptal Edildi*, *Birleştirildi* veya *Kapalı*.
1. **Tamam**'ı seçin.
1. Çalışmayı iptal etmek istediğinizi onaylamak için **Evet**'i seçin.
1. Gerektiğinde diğer iş kodları için bu yordamı yineleyin.

Daha fazla bilgi için bkz. [Özel durum işleme için ambar işini iptal etme](../../warehousing/cancel-warehouse-work.md).

Yerleşim yönergesini, dalga şablonu için otomatik konteynerleme ayarlandığında son sevkiyat yerleşimi olarak paketleme yerleşimini kullanmayacak şekilde yeniden yapılandırmak için aşağıdaki yordamı kullanın.

1. **Ambar Yönetimi \> Kurulum \> Konum yönergeleri** seçeneğine gidin.
1. **İş siparişi türü** alanında *Satış siparişi*'ni seçin.
1. Otomatik konteynerleme için kullandığınız yerleşim yönergesini seçin.
1. **Yerleşim Yönergesi Eylemleri** hızlı sekmesi araç çubuğunda **Sorguyu düzenle**'yi seçin.
1. Sorgu düzenleyicisi iletişim kutusunda, **Aralık** sekmesinde, **Alan**'ın *Yerleşim profili* olarak ayarlandığı satırı bulun ve bu satırın **Ölçüt** alanının **Paketleme** *Yerleşim türüne* sahip olan bir yerleşim profiline ayarlanmadığını doğrulayın. Son koyma yerleşimini düzeltmek için **Ölçüt** alanını ayarlayın.

Yükü yeniden serbest bırakmak ve doğru son sevkiyat yerleşimine sahip iş kodları oluşturmak için aşağıdaki yordamı kullanın.

1. **Ambar yönetimi \> Yükler \> Yük planlama çalışma ekranı** öğesine gidin.
1. **Yükler** bölümünde, serbest bırakılması gereken yükü bulun.
1. **Yükler** bölümü araç çubuğunda seçili yükü ambara serbest bırakmak için **Serbest bırak \> Ambara serbest bırak** öğesini seçin.
1. Gerektiğinde diğer yükler için bu yordamı yineleyin.
