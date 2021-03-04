---
title: Malzeme çekme ve paketleme ile ilgili sorunları giderme
description: Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta malzeme çekme ve paketleme işlemlerinde karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 74854fa95837dd8a133860e2a017be4c92ff84a3
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645489"
---
# <a name="troubleshoot-picking-and-packing"></a>Malzeme çekme ve paketleme ile ilgili sorunları giderme

[!include [banner](../includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta malzeme çekme ve paketleme işlemlerinde karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.

## <a name="i-receive-the-following-error-message-dimension-location-cant-be-left-blank-if-dimension-serial-number-is-set"></a>Şu hata iletisini alıyorum: "Boyut seri numarası ayarlandığında boyut konumu boş bırakılamaz."

### <a name="issue-description"></a>Sorun açıklaması

Bu hata iletisini, gelişmiş ambar yönetimi (WMS) için etkinleştirilen bir ambarı kullanarak bir seri madde için transfer emri oluşturup ardından iş tamamlandıktan sonra sevkiyatı onaylamaya çalışırsanız alırsınız.

### <a name="issue-resolution"></a>Sorunun çözümü

**Varsayılan giriş konumu** alanı, "çıkış" ambarına ait bir transit ambar için boştur. Bu sorunu gidermek için transit ambarında varsayılan bir giriş konumu belirtin. Bu konumun plaka denetimli olduğundan emin olun.

## <a name="i-receive-the-following-error-message-invalid-license-plate"></a>Şu hata iletisini alıyorum: "Geçersiz plaka."

### <a name="issue-description"></a>Sorun açıklaması

Bu hata iletisini, bir plaka kimliğini taradığınızda ambar uygulamasında alırsınız.

### <a name="issue-resolution"></a>Sorunun çözümü

Plaka kimliğinin plaka tablosunda bulunduğundan ve plakadaki maddelerin ve miktarların kullanılabildiğinden (başka bir deyişle, engellenmemiş olduğundan) emin olun.

## <a name="i-receive-the-following-error-message-field-load-weight-1-can-only-contain-positive-numbers-update-has-been-canceled"></a>Şu hata iletisini alıyorum: "'Yük ağırlığı' alanı (=-%1) yalnızca pozitif sayılar içerebilir. Güncelleştirme iptal edildi."

### <a name="issue-description"></a>Sorun açıklaması

Bu hata iletisini, ambalaj konumlarından hazırlama konumlarına veya yerleştirme konumlarına iş işlenirken açık çalışma olduğunda alırsınız.

### <a name="issue-resolution"></a>Sorunun çözümü

Bu sorunu gidermek için **Sistem yönetimi \> Periyodik görevler \> Veritabanı \> Tutarlılık denetimi** bölümüne gidin ve **Ambar yükü ağırlık tutarlılık denetimi** için işlemi çalıştırın.

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a>Şu hata iletisini alıyorum: "Miktar %1 birimi için geçerli değil."

### <a name="issue-description"></a>Sorun açıklaması

Bu hata iletisini, çoklu toplu işler arasında bir *bölmeli malzeme çekme* işlemi gerçekleştirmeye çalıştığınızda alırsınız.

### <a name="issue-resolution"></a>Sorunun çözümü

Ambar çalışanının ambar uygulamasındaki *Kısa malzeme çekme* işlemini kullanması gerekir. Aynı konumdan birden fazla toplu iş çekmeyi deniyorsanız ambar uygulamasındaki **Tamamı** seçeneğini de kullanabilirsiniz.

## <a name="i-cant-move-inventory-to-a-location-that-is-license-platecontrolled"></a>Stoğu, plaka denetimli bir konuma taşıyamıyorum.

### <a name="issue-description"></a>Sorun açıklaması

Bir yükte çekilen malzeme miktarlarını azaltamazsınız.

### <a name="issue-resolution"></a>Sorunun çözümü

Önceki sürümlerde, bir yükte çekilen malzeme miktarlarını azaltamazsınız. Ancak, artık plaka denetimli bir konumuna malzeme çekmeyi geri alabilirsiniz. **Çekilen malzeme miktarını azalt** sayfasındaki yük satırı için hem **Konum** değerini hem de **Plaka** değerini belirtmeniz gerekir.

## <a name="can-i-print-a-delivery-note-or-packing-content-by-warehouse"></a>Ambara göre bir teslimat notu veya ambalaj içeriği yazdırabilir miyim?

### <a name="issue-description"></a>Sorun açıklaması

**İş denetim şablonu satırı güncelleştirmesi** sayfasında, teslim notu veya ambalaj içeriğini ambara veya siteye göre yazdırmak istiyorsunuz.

### <a name="issue-resolution"></a>Sorunun çözümü

Yazdırma yönetimi ayarlarını kullanarak bir belgeyi yazdırdığınızda, **İş denetim şablonu satırı güncelleştirme** sayfasında **Yazdırma ayarlarını düzenle**'yi seçmek yerine kapsamı (tesis/ambar) bunun Yazdırma yönetimi üzerinden sınırlandırın.

## <a name="i-cant-cancel-a-packing-slip-after-its-posted-from-a-sales-order"></a>Bir satış siparişinden deftere nakledildikten sonra sevk irsaliyesini iptal edemiyorum.

### <a name="issue-description"></a>Sorun açıklaması

Malzeme çekme ve sevkiyat işlemleri WMS için etkinleştirildiğinde, bir satış siparişinden deftere nakledildikten sonra sevk irsaliyesini iptal edemezsiniz.

### <a name="issue-resolution"></a>Sorunun çözümü

WMS için etkinleştirilen maddelere ait deftere nakledilen sevk irsaliyelerini düzeltmek için deftere nakletme işlemi siparişten değil, yükten oluşturulmalıdır. Microsoft bu sorunu değerlendirmiş ve bir özellik sınırlaması olduğunu tespit etmiştir. Genel olarak, ambar yönetimi işlemleri üzerinden malzemesi çekilen ve sevk edilen bir satış siparişi sevk irsaliyesi yük veya sevkiyattan ve satış siparişi belgesinden güncelleştirilen bir sevk irsaliyesi olabilir. Ancak, satış siparişini satış siparişi belgesinden güncelleştiren sevk irsaliyesi durumunda, sevk irsaliyesi tersine çevirme işlemi yükten veya satış siparişinden yapılamaz. Bu nedenle, sevk irsaliyesini yükten deftere nakletme işlemini kullanmanızı öneririz. Bu durumda, yükten gerçekleştirilmesi gereken ters işlem etkinleştirilir.

## <a name="i-receive-the-following-error-message-not-enough-work-can-be-found-for-cluster"></a>Şu hata iletisini alıyorum: "Küme için yeterli iş bulunamadı."

### <a name="issue-description"></a>Sorun açıklaması

*Sistem tarafından yönlendirilen küme malzemesi çekme* sürecini kullandığınızda, örneğin 10 pozisyonun çekildiği bir küme profili yapılandırırsanız işlem, 10 pozisyona kadar malzeme çekme için yeterli iş olduğunda planlanan şekilde çalışır. Bununla birlikte, seçebileceğiniz yalnızca sekiz konum varsa, bir küme için yeterli iş olmadığı için bu hata iletisini alırsınız.

### <a name="issue-resolution"></a>Sorunun çözümü

Bu sorunu gidermek için küme profilini düzenleyin ve **Pozisyonları etkinleştir** seçeneğini *Hayır* olarak ayarlayın.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]