---
title: Satıcı fatura ilkelerini ayarla
description: Bu makalede, satıcı faturası ilkelerinin nasıl ayarlanacağı açıklanmaktadır.
author: ShivamPandey-msft
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 049b38b6feba5f4369d79b89b4c81a8195dd7758
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904744"
---
# <a name="set-up-vendor-invoice-policies"></a>Satıcı fatura ilkelerini ayarla

[!include [banner](../../includes/banner.md)]

Bu makalede, satıcı faturası ilkelerinin nasıl ayarlanacağı açıklanmaktadır. **Satıcı faturası** sayfasından bir satıcı faturası naklettiğiniz zaman ve satıcı faturası **İlke ihlalleri** sayfasını açtığınız zaman satıcı faturası ilkeleri çalıştırılır. Ayrıca, satıcı faturası iş akışını yapılandırarak, iş akışına her fatura gönderişinizde satıcı faturası ilkelerinin çalıştırılmasını sağlayabilirsiniz. 

- Fatura kaydında veya fatura günlüğünde oluşturulmuş faturalara satıcı faturası ilkeleri uygulanmaz.  
- Fatura eşleştirme doğrulaması satıcı faturası ilkeleri kullanmaz, bunun yerine **Borç hesapları parametreleri** sayfasında ayarlanır.  
- Bu kayıtta USMF demo şirketi kullanılmaktadır. Bu adımları borç hesapları yöneticisi veya muhasebe müdürü rolü gerçekleştirir. Başlamadan önce **Fatura eşleştirme** yapılandırması anahtarının seçildiğinden emin olun.


## <a name="prepare-to-create-vendor-invoice-policies"></a>Satıcı faturası ilkeleri oluşturmaya hazırlanın
1. **Gezinti bölmesi > Modüller > Borç hesapları > Kurulum > Borç hesapları parametreleri**'ne gidin.
2. **Fatura doğrulama** sekmesine tıklayın.
3. **Fatura başlığı durumunu otomatik olarak güncelleştir** onay kutusunu işaretleyin veya kutunun işaretini kaldırın.
4. **Tamam**'ı seçin.
5. **Uyuşmazlıkları olan faturayı deftere naklet** alanında bir seçenek belirtin.
6. Sayfayı kapatın.
7. **Gezinti bölmesi > Modüller > Borç hesapları > Politika ayarı > Satıcı faturası politikaları**'na gidin.
8. **Parametreler**'i seçin.
9. **Ekle**'yi seçin.
10. Ana sayfaya dönmek için sayfayı kapatın.

## <a name="create-policy-rule-types-for-vendor-invoices"></a>Satıcı faturaları için ilke kuralı türleri oluşturun
1. **Gezinti bölmesi > Modüller > Borç hesapları > Politika ayarı > Satıcı faturası politika kural türleri**'ne gidin.
2. **Yeni**'yi seçin.
3. **Kural adı** ve **Açıklama** alanlarına değer girin.
4. **Sorgu adı** alanında, açılır menü düğmesini seçerek aramayı açın, ardından istenen kaydı seçin.
5. **Kaydet**'i seçin.
6. Ana sayfaya dönmek için sayfayı kapatın.

## <a name="define-a-vendor-invoice-policy"></a>Satıcı faturası ilkesi tanımlayın
1. **Gezinti bölmesi > Modüller > Borç hesapları > Politika ayarı > Satıcı faturası politikaları**'na gidin.
2. **Yeni**'yi seçin.
3. **Ad** ve **Açıklama** alanlarına değer girin.
4. **İlke organizasyonları** bölümünü genişletin veya daraltın.
5. Ağaçta **Contoso Eğlence Sistemi Türkiye** (Contoso Entertainment System USA) seçeneğini seçin.
6. **Ekle**'yi seçin.
7. **İlke kuralları** bölümünü genişletin veya daraltın.
8. **İlke kuralı oluştur**'u seçin.
9. **İlke kuralı açıklaması** alanına bir değer girin.
10. **Filtre**'yi seç.
11. **Ekle**'yi seçin. İstenen kaydı seçin.
12. **Tablo** , **Türetilmiştablo** ve **Alan** alanlarında, açılır menülerden seçenekler seçin veya girin.
13. Sayfayı kapatın.
14. **Ölçütler** alanına bir değer yazın.
15. **Tamam**'ı seçin.
16. **Tamam**'ı seçin.
17. Ana sayfaya dönmek için sayfaları kapatın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
