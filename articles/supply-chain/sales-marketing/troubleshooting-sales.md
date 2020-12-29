---
title: Satış siparişleri ile ilgili sorun giderme
description: Bu konu, satış siparişleri üzerinde çalışırken karşılaşabileceğiniz sorunların nasıl düzeltileceğini açıklamaktadır.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTable, SalesTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 6e51723915892f465ce09d09ee9ed622bab9451e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439255"
---
# <a name="troubleshoot-sales-orders"></a>Satış siparişleri ile ilgili sorun giderme

Bu konu, satış siparişleri üzerinde çalışırken karşılaşabileceğiniz sorunların nasıl düzeltileceğini açıklamaktadır.

## <a name="the-tax-information-isnt-updated-if-i-change-the-location-on-a-sales-order-header"></a>Satış siparişi başlığındaki konumu değiştirdiğimde vergi bilgileri güncelleştirilmiyor.

### <a name="issue-description"></a>Sorun açıklaması

Bir satış siparişi başlığında veya satır düzeyinde tesis, ambar veya teslimat adresi değiştirilirse, duruma ait vergi bilgileri satırlar için otomatik olarak güncelleştirilmez.

### <a name="issue-resolution"></a>Sorunun çözümü

Bu davranış tasarımdan kaynaklanır. Bu sorun, teslimat adresi, tesis ve ambarın satır düzeyinde otomatik olarak değiştirilemediğinden de oluşur. Bunları el ile güncelleştirmelisiniz.

## <a name="if-there-are-two-trade-agreements-for-the-same-period-or-overlapping-periods-the-same-agreement-line-is-always-selected"></a>Aynı dönem veya çakışan dönemler için iki ticari sözleşme varsa, her zaman aynı sözleşme satırı seçilir.

### <a name="issue-description"></a>Sorun açıklaması

İki ticari sözleşme aynı dönem veya örtüşen dönemler için tanımlanmışsa, bu malzemeleri içeren satış siparişi satırları oluşturduğunuzda, aynı ticari sözleşme her seferinde seçilmiş olarak görünür.

### <a name="issue-resolution"></a>Sorunun çözümü

Belirli bir tarihe ait birden fazla ticari sözleşme varsa, en düşük fiyata sahip olan ticari sözleşme her zaman seçilir. Daha fazla bilgi için, aşağıdaki teknik incelemeyi karşıdan yükleyin: [Microsoft Dynamics AX 2012'de ticari sözleşmeler](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).

## <a name="can-i-link-a-purchase-order-to-a-sales-order-to-fulfill-demand"></a>Talebi karşılamak için bir satınalma siparişini bir satış siparişine bağlayabilir miyim?

Satış siparişinden satınalma siparişi oluşturabilirsiniz. Daha fazla bilgi için, bkz. [Satış siparişinden satınalma siparişi oluşturma](tasks/create-purchase-order-sales-order.md).

## <a name="i-cant-cancel-or-delete-a-return-order-or-a-sales-order"></a>İade siparişi veya satış siparişini iptal edemiyor veya silemiyorum.

Yalnızca, *Oluşturuldu* durumundaki satış siparişlerini ve iade siparişlerini iptal edebilirsiniz. Daha fazla bilgi için bkz. [İade siparişlerini iptal etme](../service-management/cancel-return-order.md).

## <a name="when-i-try-to-cancel-a-sales-order-i-receive-a-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations-error"></a>Bir satış siparişini iptal etmeyi denediğimde, "Rezervasyonlara dayanan iş oluşturulduğu için rezervasyonlar silinemedi" hatasını alıyorum.

İş bir satış siparişiyle ilişkilendirilmişse, iş iptal edilene ve ters çevrilinceye kadar satış siparişini iptal edemezsiniz. Bu gereksinim, satış siparişiyle ilişkilendirilmiş iş kapatılmış olsa bile geçerlidir.

Bu sorunu düzeltmek için şu adımları izleyin.

1. İşi iptal edin ve stoku istenen konuma geri koyun. Satış siparişinin ilgili yüküne gidin ve yükleme satırında **Çekilen miktarı azalt** ya da Eylem Bölmesi'ndeki **İşi tersine çevir**'i seçin.

    İş artık *İptal edildi* durumunda olur ve yeni stok hareketi işi otomatik olarak oluşturulur stoku ters çevirme işlemi sırasında tanımlanan konuma geri yerleştirmek için işlenir.

2. Yükü silin. Sevkiyat da silinir.
3. Artık satış siparişine gidip iptal edebilirsiniz.

## <a name="i-cant-cancel-an-intercompany-purchase-order-that-is-linked-to-a-sales-order"></a>Bir satış siparişiyle bağlantılı şirketlerarası satınalma siparişini iptal edemiyorum.

### <a name="issue-description"></a>Sorun açıklaması

Bir satış siparişiyle bağlantılı şirketlerarası satınalma siparişini iptal etmeyi denerseniz, aşağıdaki hata iletisini alabilirsiniz: "Kalan güncelleştirme miktarının işareti değiştiğinden miktar azaltılamaz."

### <a name="issue-resolution"></a>Sorunun çözümü

Bu sorun Microsoft Dynamics 365 Supply Chain Management 10.0.13 sürümünde giderilmiştir. Bu sürümde ve sonraki sürümlerde artık bir satış siparişiyle bağlantılı olan bir şirketlerarası satınalma siparişini iptal edebilirsiniz.

## <a name="can-i-restore-an-invoiced-sales-order-that-was-deleted"></a>Silinmiş bir faturalandırılmış satış siparişini geri yükleyebilir miyim?

### <a name="issue-description"></a>Sorun açıklaması

Faturalandırılmış bir satış siparişi yanlışlıkla silindi ve geri yüklemek veya ayrıntılarını görüntülemek istiyorsunuz.

### <a name="issue-resolution"></a>Sorunun çözümü

Silinen satış siparişi zaten faturalanmışsa, **Müşteri hesabı \> Hareketler \> Özgün belge \> Ayrıntıları görüntüle** ögesine gidin. Aradığınız faturayı bulun ve ayrıntılarını görüntülemek için seçin. Bu ayrıntılar satış siparişi referansını içerir. Ayrıca, bu sayfadan satış siparişi ayrıntılarına de erişebilmelisiniz.

## <a name="the-deadline-of-a-sales-order-header-cant-be-found-in-the-salesorderheaderv2entity-data-entity"></a>Satış siparişi başlığının son tarihi SalesOrderHeaderV2Entity veri varlığı içinde bulunamıyor.

*SalesOrderHeaderV2Entity* varlığında son tarih alanı yok.

## <a name="i-must-delete-orphaned-sales-order-records"></a>Sahipsiz satış siparişi kayıtlarını silmem gerekiyor.

Sahipsiz satış siparişi kayıtlarını temizlemek için, aşağıdaki yerlerden birine giderek *Satış siparişi silme* dönemsel işini çalıştırın:

- Satış ve pazarlama \> Dönemsel görevler \> Temizle \> Satış siparişlerini sil
- Retail and commerce \> Retail and commerce IT \> Temizleme \> Satış siparişlerini sil

## <a name="is-there-a-way-to-calculate-commissions-on-invoices-that-have-already-been-posted"></a>Deftere nakledilmiş olan faturalardaki komisyonları hesaplanmanın bir yolu var mı?

Supply Chain Management, şu anda deftere nakledilen faturaların komisyonlarını hesaplamayı desteklememektedir.

## <a name="a-bundle-item-isnt-supported-in-an-intercompany-process"></a>Bir paket malzeme şirketlerarası bir işlemde desteklenmiyor.

Paket satış öğesi satınalma siparişlerinde kullanılmaz; çünkü paket satış öğesi için satış siparişi satırlarını incelerseniz miktarın *0* (sıfır) olduğunu ve durumun *İptal edildi* olduğunu fark edildiğini göreceksiniz. Bu davranış tasarımdan kaynaklanır. Satış siparişi yalnızca paket satış öğesinin bileşenlerini satın alır. Paket satış öğesinin kendisini satın almaz.

Bir paket satın almanız gerekiyorsa, bunu paket satış öğesi olarak işaretlemenizin gerekip gerekmediğiniz gözden geçirin; çünkü bu işlev gerçekte gelir tanıma senaryoları için tasarlanmıştır. Paket satış öğeleri hakkında daha fazla bilgi için bkz. [Paket satış öğeleri](../../finance/accounts-receivable/revenue-recognition-setup.md#bundles).
