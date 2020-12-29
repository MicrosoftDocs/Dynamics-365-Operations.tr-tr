---
title: Özel durumları araştırma veya giderme
description: Satıcı faturası sayfasından bir satıcı faturası naklettiğiniz zaman ve satıcı faturası İlke ihlalleri sayfasını açtığınız zaman satıcı faturası ilkeleri çalıştırılır.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 995d68f6224b6dfbb1928c907ad991b86fc47668
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448757"
---
# <a name="research-or-resolve-exceptions"></a>Özel durumları araştırma veya giderme

[!include [banner](../../includes/banner.md)]

Satıcı faturası sayfasından bir satıcı faturası naklettiğiniz zaman ve satıcı faturası İlke ihlalleri sayfasını açtığınız zaman satıcı faturası ilkeleri çalıştırılır. Ayrıca, satıcı faturası iş akışını yapılandırarak, iş akışına her fatura gönderişinizde satıcı faturası ilkelerinin çalıştırılmasını sağlayabilirsiniz. 

Fatura kaydında veya fatura günlüğünde oluşturulmuş faturalara satıcı faturası ilkeleri uygulanmaz. 

Fatura eşleştirme doğrulaması satıcı faturası ilkeleri kullanmaz, bunun yerine Borç hesapları parametreleri sayfasında ayarlanır.

Bu kayıtta USMF demo şirketi kullanılmaktadır. Bu adımları borç hesapları yöneticisi veya muhasebe müdürü rolü gerçekleştirir. Başlamadan önce Fatura eşleştirme yapılandırma anahtarının seçildiğinden emin olun.


## <a name="prepare-to-create-vendor-invoice-policies"></a>Satıcı faturası ilkeleri oluşturmaya hazırlanın
1. Borç hesapları > Kurulum > Borç hesapları parametreleri'ne gidin.
2. Fatura doğrulama sekmesine tıklayın.
3. Fatura başlığı durumunu otomatik olarak güncelleştir onay kutusunu işaretleyin veya kutunun işaretini kaldırın.
4. Tamam'ı tıklatın.
5. Uyuşmazlıkları olan faturayı deftere naklet alanında bir seçenek belirtin.
6. Sayfayı kapatın.
7. Borç hesapları > İlke ayarı > Satıcı fatura ilkeleri'ne gidin.
8. Parametreler'e tıklayın.
9. Ekle'ye tıklayın.
10. Sayfayı kapatın.

## <a name="create-policy-rule-types-for-vendor-invoices"></a>Satıcı faturaları için ilke kuralı türleri oluşturun
1. Borç hesapları > İlke ayarı > Satıcı faturası ilke kuralı türleri'ne gidin.
2. Yeni'ye tıklayın.
3. Kural adı alanına bir değer girin.
4. Açıklama alanına bir değer girin.
5. Sorgu adı alanında, açılır menü düğmesine tıklayarak aramayı açın.
6. Listede, istenen kaydı bulun ve seçin.
7. Listede, seçili satırdaki bağlantıya tıklayın.
8. Kaydet'e tıklayın.
9. Sayfayı kapatın.

## <a name="define-a-vendor-invoice-policy"></a>Satıcı faturası ilkesi tanımlayın
1. Borç hesapları > İlke ayarı > Satıcı fatura ilkeleri'ne gidin.
2. Yeni'ye tıklayın.
3. İsim alanına bir değer yazın.
4. Açıklama alanına bir değer girin.
5. İlke organizasyonları bölümünü genişletin veya daraltın.
6. Ağaçta "Contoso Eğlence Sistemi Türkiye"yi (Contoso Entertainment System USA) seçin.
7. Ekle öğesini tıklatın.
8. İlke kuralları bölümünü genişletin veya daraltın.
9. İlke kuralı oluştur'a tıklayın.
10. İlke kuralı açıklaması alanına bir değer girin.
11. Filtre'ye tıklayın.
12. Ekle öğesini tıklatın.
13. Listede, seçili satırı işaretleyin.
14. Tablo alanında, açılır menü düğmesine tıklayarak aramayı açın.
15. Listede, seçili satırdaki bağlantıya tıklayın.
16. Türetilen tablo alanında, açılır menü düğmesine tıklayarak açılır menü düğmesine tıklayın.
17. Listede, seçili satırdaki bağlantıya tıklayın.
18. Alan alanında, açılır menü düğmesine tıklayarak aramayı açın.
19. Alan alanına bir değer yazın.
20. Sayfayı kapatın.
21. Ölçütler alanına bir değer yazın.
22. Tamam'a tıklayın.
23. Tamam'a tıklayın.
24. Sayfayı kapatın.
25. Sayfayı kapatın.

