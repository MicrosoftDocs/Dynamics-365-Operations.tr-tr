---
title: Dynamics 365 Talent'taki yenilikler veya değişiklikler (29 Ekim 2019)
description: Bu konuda, Microsoft Dynamics 365 Talent'taki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 10/29/2019
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
ms.search.validFrom: 2019-10-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 83b4734190163ebd2dc29096632642bd45c61e8f
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773889"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-29-2019"></a>Dynamics 365 Talent'taki yenilikler veya değişiklikler (29 Ekim 2019)

[!include [banner](includes/banner.md)]

Bu konuda, Dynamics 365 Talent'daki yeni veya değişen özellikler açıklanmaktadır.

## <a name="changes-in-attract"></a>Attract'te değişiklikler

Bu sürüm, Dynamics 365 Talent: Attract için küçük hata düzeltmeleri içeriyor.

## <a name="changes-in-onboard"></a>Onboard'taki değişiklikler

Bu sürüm, Dynamics 365 Talent: Onboard için küçük hata düzeltmeleri içeriyor.

## <a name="changes-in-core-hr"></a>Core HR içindeki değişiklikler

Bu bölümde açıklanan değişiklikler sürüm numarası 8.1.2586 için geçerlidir. Bazı başlıklardaki parantez içindeki numaralar Microsoft Dynamics Lifecycle Services (LCS) destek numaralarına referans verir.

### <a name="delete-parties-with-no-roles-should-be-on-by-default-371233"></a>Rolü olmayan tarafları sil varsayılan olarak açık olmalı (371233)

Talent'te yeni bir ortam hazırladığınızda **Rol yoksa tarafları sil** varsayılan olarak açıktır. Bir çalışanı sildiğinizde çalışanla ilişkili taraf bu ayar açık olmadıkça kaldırılmaz. Bu değişiklik, çalışanları içe aktarmanız, değiştirmeniz veya yeniden içe aktarmanız gerektiğinde genel adres defterindeki tekrarlanan kayıtları sınırlar.

### <a name="draft-and-cancelled-leave-requests-should-be-allowed-to-be-deleted-in-common-data-service-376999"></a>Taslak ve iptal edilmiş izin isteklerinin Common Data Service'te silinmesine izin verilmelidir (376999)

Bu değişiklikle artık **Taslak** veya **İptal edildi** durumundaki izin istekleri Common Data Service'te silinebilir.

### <a name="additional-list-values-in-custom-fields-arent-reflected-in-common-data-service-after-clicking-apply-on-the-custom-fields-form-379599"></a>Özel alanlar formunda Uygula'ya tıkladıktan sonra özel alanlardaki ek liste değerleri Common Data Service'te yansıtılmıyor (379599)

Common Data Service ile önceden eşitlenen mevcut özel alana yeni liste değerleri eklediğinizde değişikliklerinizi **Özel alanlar** formunda uyguladıktan sonra bunlar artık Common Data Service'te kullanılabilir.

### <a name="apply-onboarding-checklists-across-legal-entities-when-more-than-one-employment-exists-371270"></a>Birden fazla çalışan varken tüzel kişilikler arasında işe alım yapılacaklar listeleri uygulama (371270)

Bu haftanın sürümünde, **Çalışan formu > Yapılacaklar listeleri**'nde birden fazla çalışana yapılacaklar listeleri uygulayabilirsiniz.

### <a name="benefits-open-enrollment-preview-feature-has-been-removed"></a>Kazançlar açık kayıt önizlemesi özelliği kaldırıldı

Microsoft, [Core HR operasyonel mükemmellik sağlama konusunda stratejik yatırımlar](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence) blog gönderisindeki duyurumuzla birlikte genel önizlemedeki kazançlar açık kayıt özelliğini kaldırdı. Gelecekte yeni işlevler yayımlanacaktır. Kazançlar açık kayıt özelliğinin üretim kullanımı desteklenmez.

## <a name="coming-soon"></a>Çok yakında

### <a name="print-performance-reviews"></a>Performans incelemelerini yazdırma

Dynamics 365: 2019 sürüm dalgası 2 planındaki [Performans incelemelerini yazdır](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) konusuna bakın.

### <a name="feature-management-workspace"></a>Özellik yönetimi çalışma alanı

Özellikler, her sürümüne eklenir ve güncelleştirilir. Özellik yönetimi deneyimi, her sürümde teslim edilen özelliklerin listesini görüntüleyebileceğiniz bir çalışma alanı sağlar. Varsayılan olarak, bu özellikler kapalıdır. Çalışma alanını, bu özellikleri açıp ilgili belgelere bakmak için kullanabilirsiniz.

Özellik yönetimiyle gelen değişiklikler hakkında daha fazla bilgi edinmek için bkz. [Özellik yönetimine genel bakış](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).
