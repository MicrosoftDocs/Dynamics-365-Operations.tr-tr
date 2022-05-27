---
title: Dynamics 365 Talent - Attract ve Onboard uygulamalarının kullanımdan kaldırılması
description: Bu konuda, Dynamics 365 Talent - Attract ve Onboard uygulamalarının kullanımdan kaldırılması açıklanmaktadır.
author: twheeloc
ms.date: 01/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: e17b92621f05ad8483a7c578bfaece58a530df2d
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8692016"
---
# <a name="dynamics-365-talent-attract-and-onboard-apps-retirement"></a>Dynamics 365 Talent: Attract ve Onboard uygulamalarının kullanımdan kaldırılması


Aralık 2019'da, Dynamics 365 Talent - Attract ve Onboard uygulamalarının 1 Şubat 2022'de kullanımdan kaldırılacağını duyurarak müşterilerimize plan yapmaları için iki yıllık bir süre sunmuştuk.

Bu uygulamaların kullanımdan kaldırılmasıyla ilgili daha fazla bilgi için bkz:
 - [Dynamics 365 Talent - Attract ve Dynamics 365 Talent: Onboard Uygulamalarının Kullanımdan Kaldırılması](https://community.dynamics.com/365/humanresources/b/dynamics365forhumanresources/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)
 - [Dynamics 365 Human Resources ile daha başarılı bir iş gücü elde etme](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/12/06/building-a-more-successful-workforce-with-dynamics-365-human-resources)

Müşterilerimizin aşağıdakiler gibi birden fazla alanda veriye dayalı personel deneyimleri oluşturması için gereken iş gücü içgörülerini elde etmelerine yardımcı olacak Dynamics 365 Human Resources'ı desteklemeye devam edeceğiz:

- Maaş
- Yan haklar
- İzin ve devamsızlık
- Uyumluluk
- Bordro
- Performans geribildirimi
- Eğitim ve sertifika
- Self servis programları

## <a name="dynamics-365-talent-apps-retirement-faq"></a>Dynamics 365 Talent uygulamalarının kullanımdan kaldırılmasıyla ilgili SSS

### <a name="what-is-the-user-experience-for-both-dynamics-365-talent---attract-and-onboard-apps-starting-february-1-2022"></a>1 Şubat 2022'den itibaren Dynamics 365 Talent - Attract ve Onboard uygulamalar için kullanıcı deneyimi nasıl olacak?

Kullanıcılar uygulamaları kullanamayacak ve bir kullanımdan kaldırma sayfasına yeniden yönlendirilir.

### <a name="can-customers-continue-to-export-data-for-both-dynamics-365-talent---attract-and-onboard-apps-after-february-1-2022"></a>Müşteriler 1 Şubat 2022'den sonra Dynamics 365 Talent - Attract ve Onboard uygulamaları için veri dışarı aktarmaya devam edebilir mi?
  
Hayır, kullanımdan kaldırma duyurusu Aralık 2019'da yapıldı ve 1 Şubat 2022 tarihine kadar gerekli dışarı aktarma olanakları sağlandı. 

### <a name="will-the-customers-data-related-to-both-dynamics-365-talent---attract-and-onboard-apps-in-dataverse-be-deleted-after-february-1-2022"></a>Dataverse'teki Dynamics 365 Talent - Attract ve Onboard uygulamalarıyla ilgili müşteri verileri 1 Şubat 2022'den sonra silinecek mi?

Hayır, Human Capital Management Talent çözümü silinmediği veya kaldırılmadığı sürece, kullanımdan kaldırma işleminden sonra bile Dataverse varlıkları, müşterinin Microsoft Dataverse ortamında kalmaya devam edecek.

### <a name="i-know-the-name-of-the-talent-environment-how-can-i-see-the-attract-and-onboard-data-in-dataverse"></a>Talent ortamının adını biliyorum. Attract ve Onboard verilerini Dataverse'te nasıl görebilirim?

1.  Power Apps'te oturum açın: https://make.powerapps.com
2.  Attract ve Onboard verilerin igörmek istediğiniz ortamı seçin.
3.  **Dataverse > Tablolar**'a gidin. 
4.  **Arama** alanına "msdyn_" yazın. "msdyn_" + tablo adları ile başlayan tabloların listesini görürseniz (örneğin: msdyn_candidate), Attract ve Onboard verilerini içeren ortamı bulmuşsunuz demektir.

[![Power Apps](./media/Powerapps.png)](./media/Powerapps.png)

### <a name="i-dont-know-the-name-of-the-talent-environment-how-can-i-find-the-environment-that-has-the-data-for-the-dynamics-365-talent-attract-and-dynamics-365-talent-onboard-applications"></a>Talent ortamının adını bilmiyorum. Dynamics 365 Talent: Attract ve Dynamics 365 Talent: Onboard uygulamaları için verileri içeren ortamı nasıl bulabilirim?

1)  Power Platform yönetim merkezinde oturum açın: https://admin.powerplatform.microsoft.com/
2)  **Ortamlar**'ı seçin.
3)  Değerlendirilecek bir ortam seçin.
4)  **Kaynaklar > Dynamics 365 uygulamaları**'nı seçin.
5)  **HCM Talent** çözümü yüklü ise Attract ve Onboard verileri bu ortamda depolanıyor demektir. 

[![Power Platform](./media/HCMTalent.png)](./media/HCMTalent.png)

> [!NOTE] 
> **HCM Talent** çözümü Dynamics 365 Human Resources'da da kullanılır.
