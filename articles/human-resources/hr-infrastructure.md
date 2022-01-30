---
title: Dynamics 365 Human Resources altyapı birleştirme - Yayın 10.0.25 güncelleştirmesi
description: Bu konu, altyapı birleştirmesindeki ilk özellikler dalgasını getiren Microsoft Dynamics 365 Human Resources sürüm 10.0.25 hakkında bilgi sağlar.
author: twheeloc
ms.date: 01/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ec6d47c44136f7a105a702358370dd676d9339c1
ms.sourcegitcommit: 96f936267d3f314f06da6ce6f809eba2ec3b205f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2022
ms.locfileid: "8018360"
---
# <a name="dynamics-365-human-resources-infrastructure-merge---release-10025-update"></a>Dynamics 365 Human Resources altyapı birleştirme - Yayın 10.0.25 güncelleştirmesi

10.0.25 sürümü, altyapı birleştirmedeki birinci yetenekler dalgasını getirir. Altyapı birleştirme sırasında, Microsoft Dynamics 365 Human Resources, Finance ve Operations alt yapısı ile birleştirilir. Ancak, Dynamics 365 Finance ve Dynamics 365 Supply Chain Management gibi bağımsız bir uygulama olarak lisanslandırılmaya devam eder. Altyapı birleştirme hakkında daha fazla bilgi için, bkz. [Dynamics 365 Human Resources altyapı birleştirmesi SSS](../human-resources/hr-infrastructure-merge-faq.md).

Birleştirme işlemi, İnsan Kaynakları kullanıcılarına aşağıdaki yollarla tutarlılık sağlar:

- [Ortam yönetimi ve tümleştirme, İnsan Kaynakları ile Finance ve Operations uygulamaları arasında tutarlıdır.](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/consistent-environment-management-integrations-between-human-resources-finance-operations-apps)

    - Microsoft Dynamics Lifecycle Services hizmetlerindeki ortamları yönetin, sorun arayın ve Regression Suite Automation Tool.
    - İnsan Kaynakları yeni işlevlerinin, normal bir sürüm güncelleştirme işleminin parçası olarak serbest bırakıldığı tek bir kod tabanı vardır.
    - Yükseltmelerin, güncelleştirmelerin ve düzeltmelerin ortamlara uygulanma biçimi tutarlıdır.

- [Genişletilebilirlik seçenekleri geliştirildi.](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/improve-extensibility-options.md)

    - Gerektiğinde genişletmek için Microsoft Power Platform tools kullanmaya devam edebilirsiniz.
    - İşlevleri formlar, tablolar, yöntemler ve uygulama programlama arabirimleri (API) ile genişletebilirsiniz.
    - Varlıklar oluşturabilir ve genişletebilirsiniz.

    Mevcut uzantı seçenekleri hakkında daha fazla bilgi için bkz. [Dynamics 365'te genişletilebilirlik genel bakışı](../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md).

- [Dynamics 365'te bir insan kaynakları kümesi özelliği oluşturun.](/dynamics365-release-plan/2021wave2/human-resources/create-one-set-human-resources-capabilities-within-dynamics-365.md)

    10.0.25 sürümünde, yalnızca İnsan Kaynaklarında bulunan işlevsel yetenekler Finance ve Operations altyapısında kullanılabilir yapılmıştır. Müşterilerin bir Finance ve Operations ortamında bu yeteneklerden yararlanabilmeleri için, özellik yönetiminde aşağıdaki İnsan Kaynakları özelliklerinin etkinleştirilmesi gerekir.

    | Özellik adı | Genel Bakış | Serbest bırakılma durumu | 
    |--------------|----------|----------------| 
    | Hizmet yılları hesaplaması | Kurulum seçeneği, **Hizmet yılları** hesaplaması için kullanılan tarihi seçmenizi sağlar. | Genel kullanılabilir | 
    | İş akışı deneyimi geliştirmeleri | Bu özellik, iş akışı gönderimleri ve onayları için gelişmiş bir kullanıcı deneyimi sağlar. | Genel kullanılabilir | 
    | Performans incelemelerini yazdır | Performans incelemelerini PDF formatında yazdırabilirsiniz. | Genel kullanılabilir | 
    | **Yönetici self servisi** ndeki özel bağlantılar | **Yönetici self servisi**'nin **İlgili bağlantılar** bölümünde görünen özel bağlantılar oluşturabilirsiniz. | Genel kullanılabilir | 
    | Şirketler arası ücret görünümü | Kullanıcılar , şirketler arasında geçiş yapmak zorunda kalmadan tüm tüzel kişiliklerde **Yönetici self servisi** içindeki maaş planlarını görüntüleyebilirler. | Genel kullanılabilir | 
    | İşe göre çoklu ücret düzeylerini yapılandırma\*&dagger; | İşlerde artık çoklu ücret düzeyleri desteklenir. | Genel kullanılabilir | 
    | Görev Yönetimi\* | Ekleme, çıkarma ve geçiş işlemi için denetim listeleri ve görevler oluşturabilirsiniz. | Önizleme | 
    | Kolaylaştırılmış personel girişi | Bu özellik, varolan **Çalışan** sayfasında güncelleştirilmiş bir kullanıcı deneyimi sağlar. | Önizleme | 
    | İnsan kaynakları kullanıcı deneyimi geliştirmeleri | Sonraki bölümdeki tabloya bakın.  | Önizleme | 

\* **İnsan kaynakları kullanıcı deneyimi geliştirmeleri** özelliği öncesinde bu özelliğin açık olması gerekir.

&dagger;Bu özellik, etkinleştirildikten sonra devre dışı bırakılamaz.

## <a name="human-resource-user-experience-enhancements"></a>İnsan kaynakları kullanıcı deneyimi geliştirmeleri

| Özellik adı | Genel Bakış | 
|--------------|----------| 
| İstihdamı sil | Bir çalışanın bir çalışanlığını silebilirsiniz. | 
| İş aileleri | Benzer bir iş içeren ve benzer eğitim, beceriler, bilgi ve uzmanlığa gereksinim duyan bir iş grubunu takip edebilirsiniz. | 
| Ek istihdam alanları | Şu alanlar eklendi: **İstihdam kategorisi**, **Çalışma türü** ve **Çalışma durumu**. | 
| **İstihdamı bulunmayan çalışanlar** sayfası | Bir sayfa, istihdam kaydı olmayan çalışanların listesini gösterir. | 
| Konum boyutu kullanıcı deneyimi güncelleştirmesi | Tüzel kişilik başına pozisyon boyutu atamak için geliştirilmiş bir kullanıcı deneyimi vardır. | 
| **Personel yönetimi** çalışma alanındaki adres değişiklikleri | Bu özellik, **İnsan Kaynakları parametreleri** sayfasında belirtilen gün sayısı boyunca gerçekleşen tüm adres değişikliklerinin sayısını sağlar. | 
| **Personel yönetimi** çalışma alanındaki süresi dolan kayıtlar | Bu özellik, zaman aşımına uğramış veya uğrayacak sertifikalar, kimlikler, denemeler, taramalar veya testler için bir liste sağlar. | 
| **Konum hiyerarşisi doğrulama** sayfası | Pozisyon satırı hiyerarşisinde döngüsel referanslar için bir kontrol yapılır. | 
| Ülkeye özel bordro bilgileri | Çalışanların çalıştığı tüzel kişiliğin ülkesine veya bölgesine bağlı olarak, **Çalışan istihdam** sayfasında ek bordro alanları kullanılabilir. | 
| Uyumluluk raporlama geliştirmeleri | EEO-1, Vets 4212 ve OSHA300a için ek raporlama seçenekleri kullanılabilir. | 
| **Personel yönetimi** çalışma alanında güncelleştirmeler | Adres değişikliklerinin ve sona eren kayıtların izlenmesi için güncelleştirmeler yapıldı. Ek olarak, yeni sekmeler çalışan ve pozisyon eylemlerini listeler. | 
