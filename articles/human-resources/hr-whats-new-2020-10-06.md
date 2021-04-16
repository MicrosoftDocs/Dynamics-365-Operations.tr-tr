---
title: Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (6 Ekim 2020)
description: Bu konuda, 6 Ekim 2020 için Microsoft Dynamics 365 Human Resources'taki yeni veya değişen özellikler açıklanmaktadır.
author: jcart1106
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 132d91c2a17fa5116d7aa6650e4ee807a03030bb
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802299"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-october-6-2020"></a>Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (6 Ekim 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Bu konuda, Dynamics 365 Human Resources'daki yeni, değişen veya gelecek özellikler açıklanmaktadır. Güncelleştirme işlemi ve planı hakkında daha fazla bilgi için bkz. [Güncelleştirme işlemi](hr-admin-setup-update-process.md).

Yeni özellikler ve bunların beklenen genel kullanılabilirlik tarihleri hakkında daha fazla bilgi için, [Dynamics 365 Human Resources 2020 sürümü 2. Dalga'ya bakın](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Bu sürümde

Bu sürüm aşağıdaki yeni özellikleri ve hata düzeltmelerini içerir. Değişiklikler derleme numarası 8.1.3636 uygulanır.

### <a name="new-features"></a>Yeni özellikler

Aşağıdaki özellik genel olarak bu sürümde mevcuttur.

| Özellik | Sürüm planı | Belgeler |
| --- | --- | --- |
| İzin takvimleri konusunda ek bilgiler | [İzin takvimleri görünümü konusunda ek bilgiler sunma](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-leave-calendar-views) | [Takım ve şirket takvimini görüntüleme](hr-employee-self-service-calendar.md) |

### <a name="bug-fixes"></a>Hata düzeltmeleri

Bu sürümde aşağıdaki hata çözümleri bulunmaktadır.

>[!NOTE]
> Bizim hedefimiz size en kısa sürede bu bilgiyi sunmaktır. Bu konu ilk kez yayımlandıktan sonra derlemeye eklenen hata düzeltmelerini eklemek için bu konuya güncelleştirmeler uygulanabilir.

| Sorun numarası | Çıkış | Tanım |
| --- | --- | --- |
| 448806 | **Varsayılan tanımlama türü**, HCM parametrelerine **RecId** olarak dışa aktarılır | Human Resources parameteleri varlığındaki bu değişiklik, **varsayılan tanımlama türünü** görüntüleyen ek bir sütun ekler. |
| 492923 | Görev kayıtları Lifecycle Services'de (LCS) kaydedilmiyor | Görev kayıtları artık LCS'ye kaydedilebilir. |
| 429950 | Konum değiştirilirken sabit ücret zaman aşımına uğramaz | Bir çalışanın konumunu **Çalışanı aktar** sayfasında değiştirirken, bitiş ücreti pozisyonun son tarihinden bir gün önceye ayarlandı. Ücret bitiş tarihi pozisyonun bitiş tarihiyle aynıdır. |
| 467214 | **Maaşlı analizleri**, yalnızca **ödeme oranı dönüştürme adı** **Yıllık** olarak ayarlandığında görüntülenir | **Yıllık** dışında bir adı olan maaşlı ödeme oranları Ücret Analizi içinde gösterilmedi. Bu güncelleştirmeyle, Ücret Analizi tüm ödeme oranı dönüştürmelerini artık kullanır. Raporları **saatlik** veya **maaş** ile çalıştırdığınızda, saatlikten farklı bir dönem kullanan herhangi bir ödeme oranı dönüştürmesi **maaş** filtresine dahil edilir. Yalnızca **Saatlik** bir dönemi olan ödeme oranları **Saatlik** filtresine dahil edilir. |
| 482464 | **İncelemeler** görüntülenirken, filtre uygulandıktan sonra **Ayrıntılar** görünümü kılavuz görünümüne değişmez | Bir filtre uygulandıktan sonra, incelemeler Kılavuzu beklendiği gibi görüntülenir. |
| 483184 | **Ayrılma kaydı** kaydında **ayarlanmış başlangıç tarihi** olarak **Katman tabanı**'nı seçtiğinizde Human Resources izin tahakkukları oluşturmaz |**Ayarlanmış başlangıç tarihi** izin tahakkukları oluşturulurken doldurulur ve kullanılır.  |
| 509731 | Gelecekteki işten ayrılacak çalışan için izin talebi, işten ayrılma tarihinden sonrası için geçerliyse sorun yaratır | İzin istekleri işten ayrılma tarihinden önce olduğu sürece, artık gelecekteki bir işten çıkarma tarihi olan çalışanlar için gönderilebilir. |
| 510716 | Ücret analizi, **erkek ortalama saatlik ücreti** için hem erkek hem de kadın çalışanları içeriyor | Ücret analizinde **Ücret demografik analizindeki** **erkek ortalama saatlik ücreti** kadın ortalama ücretini de içeriyordu. Artık yalnızca erkekleri içermektedir. |
| 511348 | Kazançlar self servisi yalnızca bugünden itibaren geçerlilik süresinin sonuna kadar olan kazanç planlarını göstermelidir | **Kazançlar kayıt** sayfasında çalışanlara süresi dolan kazanç planları gösteriliyordu. Bu düzeltme, bu planları kaldırır. |
| 512706 | Aşağıdaki alanları salt okunur olarak ayarla:<ul><li>BenefitPlanEmployeeEntity</li><li>EnrollmentConfirmed</li><li>EnrollmentConfirmedBy</li><li>EnrollmentConfirmedDateTime | Boyut ayrıntıları için **Ekle** ve **Kaldır** düğmeleri eylem tamamlandıktan sonra yanlış şekilde etkinleştirildi. **Pozisyon eylemi ayrıntı** sayfası güncelleştirmesi, alanları eylem tamamlandıktan sonra düzenlenemez hale getirir. |

## <a name="in-preview"></a>Ön izlemede

Aşağıdaki yeni özellikler önizlemededir. Özellikleri açma hakkında daha fazla bilgi için bkz. [Özellikleri yönetme](hr-admin-manage-features.md).

| Özellik | Sürüm planı | Belgeler |
| --- | --- | --- |
| Microsoft Teams'de Human Resources uygulaması | [Microsoft Teams'de çalışan izin ve devamsızlık deneyimi](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Teams'de Human Resources uygulaması](https://go.microsoft.com/fwlink/?linkid=2127841)<br>[Teams'de izin isteklerini yönetme](hr-teams-leave-app.md) |
| Geliştirilmiş iş akışı istekleri ve onaylar | [Kuruluş ve personel yönetimi iş akışı deneyimi geliştirmeleri](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Bana atanan iş öğeleri listesini konumlandırmak için yapılandırma seçeneği](https://docs.microsoft.com/dynamics365/human-resources/hr-whats-new-2020-09-03#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| Human Resources için Dataverse'te sanal varlıklar | [Dataverse'te Dynamics 365 Human Resources temel verilerini genişletme](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/expand-dynamics-365-human-resources-core-data-common-data-service) | [Dataverse sanal varlıklarını yapılandırma](hr-admin-integration-common-data-service-virtual-entities.md) |

## <a name="coming-soon"></a>Çok yakında

Aşağıdaki yeni özellikler gelecekteki bir sürüm için planlanmıştır:

- **Dataverse'e dahil edilen denetim listesi varlıkları**: Ekleme, çıkarma, transferler ve iş süreçleri için denetim listesi varlıkları yakında Dataverse'te kullanılabilir olacaktır.

- **Yan haklar yönetimi neden kodları**: Yan haklar yönetimi neden kodları Human Resources içinde var olan neden kodlarıyla yakında birleştirilecektir. Yan haklar yönetiminde 15 karakterden uzun neden kodları oluşturduysanız, Yan haklar yönetimi **Neden kodları** formunda neden kodunun adını 15 karakter veya daha az olacak şekilde değiştirmeniz gerekir. Adı güncelleştirdiğinizde, neden kodu, Personel yönetimi'nde var olan neden kodu formunun altında görüntülenir. Bu değişiklik gelecekte kullanılabilir olacaktır ve var olan işlevleri etkilemeyecek.

- **Yönetici self servisindeki özel bağlantılar**: Yöneticileri desteklemek için, Yönetici Self Servisindeki yetenekleri genişletiyoruz. **Ekibim** sekmesinde özel bağlantılar ekleme özelliği ekliyoruz. Bu özellik, Çalışan Self Servisindeki **bilgilerim sekmesinde** bulunan özel bağlantılar özelliğine benzer. Daha fazla bilgi için bkz [Yönetici self servisinde özel bağlantılar](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service).

Planlanan özelliklerin tam listesi ve bunların zamanlanmış sürümleri için, bkz. [Dynamics 365 Human Resources 2019 sürümü 2. Dalga'ya genel bakış](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/).

## <a name="additional-resources"></a>Ek kaynaklar

[Human Resources'daki yenilikler veya değişiklikler](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2020 sürüm 2'ye genel bakış](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Güncelleştirme işlemi](hr-admin-setup-update-process.md)</br>
[Özellikleri yönetme](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]