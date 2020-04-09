---
title: Satıcı fatura ilkelerini ayarlama
description: Bu konuda, satıcı fatura ilkelerinin nasıl ayarlanacağını açıklanmaktadır.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 58518f5291b70c63506c20717034daff0268901b
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143373"
---
# <a name="set-up-vendor-invoice-policies"></a>Satıcı fatura ilkelerini ayarlama

[!include [banner](../../includes/banner.md)]

Bu konuda, satıcı fatura ilkelerinin nasıl ayarlanacağını açıklanmaktadır. Satıcı faturası sayfasından bir satıcı faturası naklettiğiniz zaman ve satıcı faturası İlke ihlalleri sayfasını açtığınız zaman satıcı faturası ilkeleri çalıştırılır. Ayrıca, satıcı faturası iş akışını yapılandırarak, iş akışına her fatura gönderişinizde satıcı faturası ilkelerinin çalıştırılmasını sağlayabilirsiniz. 

- Fatura kaydında veya fatura günlüğünde oluşturulmuş faturalara satıcı faturası ilkeleri uygulanmaz.  
- Fatura eşleştirme doğrulaması satıcı faturası ilkeleri kullanmaz, bunun yerine Borç hesapları parametreleri sayfasında ayarlanır.  
- Bu kayıtta USMF demo şirketi kullanılmaktadır. Bu adımları borç hesapları yöneticisi veya muhasebe müdürü rolü gerçekleştirir. Başlamadan önce Fatura eşleştirme yapılandırma anahtarının seçildiğinden emin olun.


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

