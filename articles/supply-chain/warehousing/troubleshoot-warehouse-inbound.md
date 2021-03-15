---
title: Gelen ambar operasyonlarında sorun giderme
description: Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta gelen ambar işlemleriyle çalışırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 71f590ec01b757de298bd2692fdbdb0324843376
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970268"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a>Gelen ambar operasyonlarında sorun giderme

[!include [banner](../includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta gelen ambar işlemleriyle çalışırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a>Şu hata iletisini alıyorum: "%1 kalite emri oluşturuldu. Küme profili bulunamadı. Lütfen yapılandırmanızı denetleyin."

### <a name="issue-description"></a>Sorun açıklaması

Bu hata iletisi, kalite yönetiminin (QMS) açık olduğu bir alma işlemiyle ilgilidir. Ortamınızdaki yapılandırmalara bağlı olarak, hata iletisini üreten hareketle ilgili ek ayrıntılar sorunu gidermeye yardımcı olabilir.

### <a name="issue-resolution"></a>Sorunun çözümü

Önce, [küme malzeme çekme](set-up-cluster-picking.md) kurulumunu gözden geçirin ve küme profillerinizin doğru ayarlandığından emin olun. Küme profilleri ayarlanmadıkça, küme malzeme çekme için bir mobil cihaz menü öğesi kullanamazsınız. Ortamınıza bağlı olarak, diğer ilgili yapılandırmaları da gözden geçirmeniz gerekebilir.

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a>Karma plaka alma işlemi, Alacak dışındaki herhangi bir değerlendirme kodu için çalışmaz.

### <a name="issue-description"></a>Sorun açıklaması

Değerlendirme kodunun **Eylem** alanı *Alacak* veya *Hurda* olarak ayarlandığında , iade edilen maddeleri işlemek için yalnızca [Karma plaka alma işlemi](mixed-license-plate-receiving.md) menü öğesini kullanabilirsiniz.

### <a name="issue-resolution"></a>Sorunun çözümü

Microsoft bu sorunu değerlendirmiş ve bir özellik sınırlaması olduğunu tespit etmiştir. Şu anda, karma plaka alma işlemi için yalnızca **Eylem** alanı *Alacak* veya *Hurda* olarak ayarlanan [değerlendirme kodları](../service-management/set-up-disposition-codes.md) desteklenmektedir.

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a>Ürün girişlerini güncelleştir periyodik görevini çalıştırdığımda, onaylanmamış satın alma siparişleri onaylanıyor.

### <a name="issue-description"></a>Sorun açıklaması

*Ürün girişlerini güncelleştir* periyodik görevini çalıştırdıktan sonra, sistem, stok hareket durumu *Kayıtlı* olan onaylanmamış satın alma siparişlerini otomatik olarak onaylar.

### <a name="issue-resolution"></a>Sorunun çözümü

*Yük miktarlarını aşırı alma* adlı yeni bir özellikle bu sorunu düzeltilmiştir. Bu özelliği açmak için [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)'ne gidin ve aşağıdaki özellikleri (listelendikleri sırada) açın:

1. Satınalma siparişi stok hareketlerini yükle ilişkilendir
1. Yük miktarlarının fazlasını alma

Daha fazla bilgi için bkz. [Kayıtlı ürün miktarlarını satınalma siparişlerine göre deftere nakletme](inbound-load-handling.md#post-registered-quantities).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]