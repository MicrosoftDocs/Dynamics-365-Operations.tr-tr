---
title: Dynamics 365 Human Resources'taki yenilikler veya değişiklikler 26 Eylül 2020
description: Bu makalede, 26 Eylül 2020 için Microsoft Dynamics 365 Human Resources'daki yeni veya değişen özellikler açıklanmaktadır.
author: jcart1106
ms.date: 09/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2f78201585101e2848eded69e03d5eb4c22d7e9a
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066777"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-26-2020"></a>Dynamics 365 Human Resources'taki yenilikler veya değişiklikler 26 Eylül 2020

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Bu makalede, Dynamics 365 Human Resources'da yeni, değişen veya yakında sunulacak özellikler açıklanmaktadır. Güncelleştirme işlemi ve planı hakkında daha fazla bilgi için bkz. [Güncelleştirme işlemi](hr-admin-setup-update-process.md).

Yeni özellikler ve bunların beklenen genel kullanılabilirlik tarihleri hakkında daha fazla bilgi için, [Dynamics 365 Human Resources 2020 sürümü 2. Dalga'ya bakın](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Bu sürümde

Bu sürüm aşağıdaki yeni özellikleri ve hata düzeltmelerini içerir. Değişiklikler derleme numarası 8.1.3589-hf.3 için geçerlidir.

### <a name="new-features"></a>Yeni özellikler

Aşağıdaki özellik genellikle bu sürümde mevcuttur:

- **Platform güncelleştirmesi 10.0.13 kullanıma sunuldu**: Güncelleştirme hakkında daha fazla bilgi için bkz. [Finans ve operasyon uygulamalarının 10.0.13 sürümü için platform güncelleştirmeleri (2020 Ekim)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-13.md).

### <a name="bug-fixes"></a>Hata düzeltmeleri

Bu sürümde aşağıdaki hata çözümleri bulunmaktadır.

> [!NOTE]
> Bizim hedefimiz size en kısa sürede bu bilgiyi sunmaktır. Bu makale, ilk kez yayımlandıktan sonra derlemeye eklenen hata düzeltmeleri eklenerek güncelleştirilebilir.

| Sorun numarası | Sorun | Açıklama |
| --- | --- | --- |
| 469495 | Varsayılan mali boyutlar kılavuz ve iletişim kutusunu Güncelleştir | Human Resources uygulamasının tamamında mali boyutlar kılavuz ve iletişim kutusu güncelleştirildi. |
| 474887 | İstek bırak iş öğesi, el ile yapılan bir kararda yanlış bağlantı açıyor | Bir iş akışı konfigürasyonu el ile girilen bir karar içerdiğinde, **Bana atanan çalışma öğelerinden** çıkış isteğine gitmek yanlış bağlantıyı açar ve boş bir form gösterir veya el ile karar vermek üzere kendisine atanan çıkış isteği yerine geçerli kullanıcının oluşturduğu çıkış isteği gösterilir. |
| 474962 | İzin ve devamsızlık parametreleri varlığı, belirsiz etiketleri olan alanlara sahip | İzin ve devamsızlık parametreleri varlık etiketleri daha anlaşılır olacak şekilde güncelleştirildi. |
| 481401 | Tahakkuk tarihi temeli, tahakkuk başlangıç tarihinden sonra ve ay sonunda olduğunda tahakkuk işlemleri askıda kalır | Tahakkuk tarihi temeli, tahakkuk başlangıç tarihinden sonra ve ayın sonunda olduğunda tahakkuk işlemleri gecikmemesi için güncelleştirilir. |
| 447167 | Süresi dolmak üzere olan kayıtlar listeleri etkin olmayan çalışanlar içeriyor | **Personel yönetiminde** **Süresi dolmak üzere olan kayıtlar** sekmesi etkin olmayan çalışanları içeriyordu. Artık yalnızca etkin çalışanları içerir. |
| 486840 | **Bana atanan iş öğelerinden** yanlış izin isteği açılıyor | **Bana atanan iş öğelerinden** izin isteği seçildiğinde artık geçerli kullanıcıya atanmış en son izin isteği açılmıyor. |
| 506868 | Dataverse **Unvan** alanı **İş pozisyonu** varlığı için ayarlanmadı | **İş** ve **İş pozisyonu** varlıklarındaki **başlık** alanı belirtilmemiş olarak görüntüleniyor. **Başlık** alanı artık görüntüleniyor. |
| 430359 | Yönetici ve çalışan rolleri atandığında çıkarma denetim listesi görevlerine erişilemiyor | Gelecekteki bir sonlandırma tarihine sahip çalışanlar, bir çalışan veya yönetici rolüne sahipse denetim listeleri görevlerine erişemiyor. Artık yalnızca bir çalışan veya yönetici rolüne sahip olan kullanıcılar gelecekteki bir sonlandırma tarihi olan çıkarma görevlerine erişebilir. |
| 458102 | Oluşturulduğunda, yeni çalışan **Çalışan Bordro bilgileri** varlığında görünmüyor | Yeni çalışanlar, varlığı dışa aktarmadan önce çalışanın bordro bilgilerini açmak zorunda kalmadan çalışan Bordro bilgileri varlığına dahil ediliyor. |

## <a name="in-preview"></a>Ön izlemede

Aşağıdaki yeni özellikler önizlemededir. Özellikleri açma hakkında daha fazla bilgi için bkz. [Özellikleri yönetme](hr-admin-manage-features.md).

| Özellik | Sürüm planı | Belgeler |
| --- | --- | --- |
| Microsoft Teams'de Human Resources uygulaması | [Microsoft Teams'de çalışan izin ve devamsızlık deneyimi](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Teams'de Human Resources uygulaması](./hr-admin-teams-leave-app.md)<br>[Teams'de izin isteklerini yönetme](hr-teams-leave-app.md) |
| Geliştirilmiş iş akışı istekleri ve onaylar | [Kuruluş ve personel yönetimi iş akışı deneyimi geliştirmeleri](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Bana atanan iş öğeleri listesini konumlandırmak için yapılandırma seçeneği](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |

## <a name="coming-soon"></a>Çok yakında

Aşağıdaki yeni özellik gelecekteki bir sürüm için planlanmıştır:

- [Yönetici self servisindeki özel bağlantılar](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service)

Planlanan özelliklerin tam listesi ve bunların zamanlanmış sürümleri için bkz. [Dynamics 365 Human Resources 2019 sürümü 2. Dalga'ya genel bakış](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/).

## <a name="additional-resources"></a>Ek kaynaklar

[Human Resources'da yeni olan veya değiştirilen özellikler](hr-admin-whats-new.md)
[Dynamics 365 Human Resources 2020 sürümü 2. Dalga'ya genel bakış](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)
[Güncelleştirme işlemi](hr-admin-setup-update-process.md)
[Özellikleri Yönetme](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
