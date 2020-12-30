---
title: Dynamics 365 Talent'taki yenilikler veya değişiklikler (8 Ekim 2019)
description: Bu konuda, Microsoft Dynamics 365 Talent'taki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 10/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-10-08
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 40898ca7f54089337180def964b8942e8653663b
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529492"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-8-2019"></a>Dynamics 365 Talent'taki yenilikler veya değişiklikler (8 Ekim 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Bu konuda, Microsoft Dynamics 365 Talent'taki yeni veya değişen özellikler açıklanmaktadır.

## <a name="changes-in-attract"></a>Attract'te değişiklikler

Bu sürüm, Dynamics 365 Talent: Attract için küçük hata düzeltmeleri içeriyor.

## <a name="changes-in-onboard"></a>Onboard'taki değişiklikler

Bu sürüm, Dynamics 365 Talent: Onboard için küçük hata düzeltmeleri içeriyor.

## <a name="changes-in-core-hr"></a>Core HR içindeki değişiklikler

Bu bölümde açıklanan değişiklikler sürüm numarası 8.1.2542 için geçerlidir. Bazı başlıklardaki parantez içindeki numaralar Microsoft Dynamics Lifecycle Services (LCS) destek numaralarına referans verir.

### <a name="removal-of-benefits-open-enrollment-from-public-preview"></a>Kazançlar açık kaydının genel önizlemeden kaldırılması

[Core HR operasyonel mükemmellik sağlama konusunda stratejik yatırımlar](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence/) blog gönderisindeki duyurumuzla birlikte Microsoft 18 Ekim 2019 tarihinde genel önizlemedeki kazançlar açık kayıt özelliğini kaldırdı. Bunun yerine, gelecekte yeni işlevler yayımlanacaktır. Kazançlar açık kayıt özelliğinin şu anda önizlemede olan üretim kullanımı desteklenmeyecektir. 

### <a name="common-data-service-integration-is-now-turned-off-by-default-on-new-provisions-343675"></a>Common Data Service tümleştirmesi artık yeni sağlamalarda varsayılan olarak kapalı olacak (343675)
 
Yeni ortamlar sağlandığında, Common Data Service tümleştirmesi kapalı olacaktır. Daha fazla bilgi için bkz. [Common Data Service tümleştirmesini yapılandırma](hr-common-data-service-integration.md).

### <a name="streamlined-employee-entry-and-navigation"></a>Kolaylaştırılmış çalışan girişi ve gezintisi

Personel girişi ve gezinme işlevleri artık tüm ortamlarda kullanılabilir. Bu özelliği etkinleştirmek için, **Sistem yönetimi \> Bağlantılar \> Kurulum \> Sistem parametreleri \> Önizleme özellikleri**'ne gidin ve **Gelişmiş çalışan formu ve gezinme**'yi seçin. Özellik tüm kullanıcılar için açılır. Bu seçeneği istediğiniz zaman kapatabilirsiniz.

Daha fazla bilgi için Dynamics 365: 2019 sürümü dalga 2 planındaki [Kolaylaştırılmış çalışan girişi ve gezintisi](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/streamlined-employee-data-entry) konusuna bakın.

### <a name="attract-and-onboard-create-inactive-workers-in-core-hr-380517"></a>Attract ve Onboard, Core HR'de etkin olmayan çalışanlar oluşturuyor (380517)

Bu haftanın sürümü, Attract ve Onboard'un Core HR'de etkin olmayan çalışanlar oluşturma sorununu düzeltiyor.

### <a name="the-workflow-fails-when-the-manager-is-signed-in-to-another-company-while-terminating-an-employee-346852"></a>Yönetici bir personelin işini sonlandırırken başka bir şirkette oturum açtığında iş akışı başarısız oluyor (346852)

İş akışı artık yöneticinin oturum açtığı yasal varlığa göre başarısız olmuyor.

### <a name="missing-information-on-hcmonboardingworkerchecklisttaskentity-349591"></a>HcmOnboardingWorkerChecklistTaskEntity varlığında eksik bilgi (349591)

Bu sürüm, **HcmOnboardingWorkerChecklistTaskEntity** hakkında ek bilgiler içerir. Burada bazı örnekler verilmiştir:

- Atanan tür **grup** olduğunda **Grup adı** 
- Atanan tür **personel** olduğunda **Personel adı** 
- Atanan tür **yönetici** olduğunda **Yönetici adı**

### <a name="entities-arent-listed-in-alphabetical-order-in-common-data-service-administration-377414"></a>Varlıklar Common Data Service Yönetiminde alfabetik sırada listelenmiyor (377414)

Varlıklar artık **CDS Yönetimi** sayfasında alfabetik sırada listeleniyor.

### <a name="changing-the-employment-type-with-a-future-date-doesnt-allow-a-position-assignment-339958"></a>Gelecekteki bir tarihe sahip istihdam türünü değiştirme işlemi pozisyon atamasına izin vermiyor (339958)

Bu değişiklik, çalışan türleri değiştirildiğinde (örneğin, personelden yükleniciye) pozisyon atamalarına olanak sağlar.

### <a name="updating-the-common-data-service-leave-bank-transaction-entity-creates-a-new-record-in-talent-352938"></a>Common Data Service İzin bankası hareketi varlığının güncelleştirilmesi Talent'ta yeni bir kayıt oluşturuyor (352938)

İzin hareketleri artık izin bankası hareketleri için Common Data Service'ta güncelleştirme yapıldığında güncelleştiriliyor.

### <a name="the-title-of-attachments-for-feedback-items-shows-the-feedback-description-343765"></a>Geri bildirim öğeleriyle ilgili eklerin başlığı geribildirim açıklamasını gösteriyor (343765)

Geri bildirim açıklaması artık ek başlığında görünmüyor.

### <a name="compensation-workflow-comments-field-shows-incorrect-content-339297"></a>Ücret iş akışı Açıklamaları alanı yanlış içerik gösteriyor (339297)

Bu değişiklik, **%HcmActionState.HcmWorkerActionComment.Comments%** alanının içeriğini gösterir.

### <a name="workcalendarentity-and-workcalendardayentity-arent-exposed-through-odata-376329"></a>WorkCalendarEntity ve WorkCalendarDayEntity, OData aracılığıyla sunulamıyor (376329)

Bu sürümde, **WorkCalendarEntity** ve **WorkCalendarDayEntity** artık Open Data Protokolü (OData) üzerinden kullanılabilir.

### <a name="hcmworkerentity-is-slow-when-odata-is-used-375221"></a>HCMWorkerEntity OData kullanıldığında yavaş (375221)

Değişiklikler, Microsoft Excel çalışma kitabı tasarımcısı kullanıldığında **HCMWorkerEntity** varlığının performansını artırdı.

### <a name="manager-performance-journal-entry-shows-an-error-after-deleting-a-performance-journal-and-creating-a-new-one-336061"></a>Yönetici performans günlüğü girişi, bir performans günlüğünü sildikten ve yeni bir günlük oluşturduktan sonra hata gösteriyor (336061)

Bu sürüm, bir performans günlüğü silindikten ve ardından hemen bir yenisi oluşturulduğunda oluşan sorunu gideriyor. Bu düzeltme, yönetici self servis'deki davranışı değiştirir.

## <a name="coming-soon"></a>Çok yakında

### <a name="print-performance-reviews"></a>Performans incelemelerini yazdırma

Dynamics 365: 2019 sürüm dalgası 2 planındaki [Performans incelemelerini yazdır](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) konusuna bakın.
