---
title: Gelen ambar operasyonlarında sorun giderme
description: Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta gelen ambar işlemleriyle çalışırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 6d7fcb2ed32c57b8701bee5b90889a0a63e1f7061aa9014480ae8c543e1f229a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748679"
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

*Yük miktarlarını aşırı alma* adlı yeni bir özellikle bu sorunu düzeltilmiştir. Bu özelliği açmak için [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanına gidin ve aşağıdaki özellikleri (listelendikleri sırada) açın:

1. Satınalma siparişi stok hareketlerini yükle ilişkilendir
1. Yük miktarlarının fazlasını alma

Daha fazla bilgi için bkz. [Kayıtlı ürün miktarlarını satınalma siparişlerine göre deftere nakletme](inbound-load-handling.md#post-registered-quantities).

## <a name="when-i-register-inbound-orders-i-receive-the-following-error-message-the-quantity-is-not-valid"></a>Gelen siparişleri kaydettiğimde, şu hata iletisini alıyorum: "miktar geçerli değil."

### <a name="issue-description"></a>Sorun açıklaması

**Plaka gruplandırma ilkesi** alanı gelen siparişleri kaydetmek için kullanılan bir mobil aygıt menü öğesi için *Kullanıcı tanımlı* olarak ayarlanmışsa, bir hata iletisi alırsınız ("miktar geçerli değil") ve kaydı tamamlayamazsınız.

### <a name="issue-cause"></a>Sorun nedeni

*Kullanıcı tanımlı*, Plaka gruplama ilkesi olarak kullanıldığında sistem, gelen stoku birim sıra grubunda belirtildiği gibi ayrı plakalara böler. Alınmakta olan maddeyi izlemek için toplu iş veya seri numaraları kullanılıyorsa, her toplu iş veya seri miktarı kaydedilen her plaka için belirtilmelidir. Bir plaka için belirtilen miktar, geçerli boyutlar için hâlâ teslim alınması gereken miktarı aşarsa, hata iletisini alırsınız.

### <a name="issue-resolution"></a>Sorunun çözümü

**Plaka gruplandırma ilkesi** alanının *Kullanıcı tanımlı* olarak ayarlandığı bir mobil aygıt menü öğesini kullanarak bir öğeyi kaydettiğinizde, sistem plaka numaralarını, toplu iş numaralarını veya seri numaralarını onaylamanızı veya girmenizi gerektirebilir.

Plaka onayı sayfasında, sistem, geçerli plakaya ayrılan miktarı gösterir. Toplu iş veya seri onay sayfalarında, sistem geçerli plakanın üzerinde hâlâ alınması gereken miktarı gösterir. Ayrıca, bu plaka ve seri numarası birleşimi için kaydedilecek miktarı girebileceğiniz bir alan da içerir. Bu durumda, plaka için kaydedilen miktarın hâlâ teslim alınması gereken miktardan fazla olmadığından emin olun.

Alternatif olarak, gelen sipariş kaydında çok fazla plaka oluşturulursa, **Plaka gruplandırma ilkesi** alanının değeri *Plaka gruplandırma* ile değiştirilebilir, maddeye yeni bir birim dizi grubu atanabilir veya birim sıra grubu için **plaka gruplandırma** seçeneği devre dışı bırakılabilir.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
