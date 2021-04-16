---
title: Dynamics 365 Human Resources'daki yenilikler veya değişiklikler (8 Mart 2021)
description: Bu konuda, 08 Mart 2021 için Microsoft Dynamics 365 Human Resources'taki yeni veya değişen özellikler açıklanmaktadır.
author: marcelbf
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7029f1dab1f10c2b237fafb7b5d8eeff9fa7a543
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5790296"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-08-2021"></a>Dynamics 365 Human Resources'daki yenilikler veya değişiklikler (8 Mart 2021)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konuda, Dynamics 365 Human Resources'daki yeni, değişen veya gelecek özellikler açıklanmaktadır.

Güncelleştirme işlemi ve planı hakkında daha fazla bilgi için bkz. [Güncelleştirme işlemi](hr-admin-setup-update-process.md).

Yeni özellikler ve bunların beklenen genel kullanılabilirlik tarihleri hakkında daha fazla bilgi için, [Dynamics 365 Human Resources 2021 sürümü 1. Dalga'ya bakın](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Bu sürümde

Bu sürüm aşağıdaki yeni özellikleri ve hata düzeltmelerini içerir. Değişiklikler derleme numarası 8.1.4017 uygulanır.

### <a name="new-features"></a>Yeni özellikler

Aşağıdaki özellikler genel olarak bu sürümde mevcuttur.

| Özellik | Sürüm planı | Belgeler |
| --- | --- | --- |
| Şirketler arası Yöneticiler şirket içi görünümü | [Şirketler arası Yöneticiler şirket içi çalışan izni görünümü](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [İzin ve devamsızlık parametrelerini yapılandırma](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-parameters) |

### <a name="bug-fixes"></a>Hata düzeltmeleri

Bu sürümde aşağıdaki hata çözümleri bulunmaktadır.

> [!NOTE]
> Bizim hedefimiz size en kısa sürede bu bilgiyi sunmaktır. Bu konu ilk kez yayımlandıktan sonra derlemeye eklenen hata düzeltmelerini eklemek için bu konuya güncelleştirmeler uygulayabiliriz.

| Sorun numarası | Çıkış |  Tanım |
| --- | --- | --- |
| 486611 | **Tüm takvimlerde izni devre dışı bırak** etkinleştirildiğinde izin takviminde izin gösterilir | **Tüm takvimlerde izni devre dışı bırak** etkinleştirilmişse İzin ve devamsızlık takvimi geliştirmeleri özelliği etkinleştirildiğinde, artık bilgiler görüntülenmez.|
| 508972 | İzin ve Devamsızlık Banka Hareketi varlığının kayıt doğrulaması eksik | İzin ve Devamsızlık Bankası Hareketi varlığını kullanırken, bir plana kayıtlı olmayan çalışanlar artık içeri aktarılamaz. |
| 554854 | Kullanıcı seçeneklerindeki varsayılan Tüzel kişilik farklıysa İşe Alım varlığı hatalarında takvimi güncelleştirme | Kullanıcı seçeneklerindeki varsayılan tüzel kişilik farklıysa bir çalışanın takvimini güncelleştirmek için İşe Alım varlığını kullanmak artık hata vermez. |
| 558347 | Başlangıç sayfası yüklenirken "Form yapılandırmalarında kayıt oluşturulamıyor (FormRunConfiguration)" görüntüleniyor. | Kişiselleştirmeler, başlangıç sayfası yüklenirken "Form yapılandırmalarında kayıt oluşturulamıyor (FormRunConfiguration)" hatasının görünmesine neden oluyor. |
| 557327 | Kazanç yönetimi çalışma alanı: Kılavuzun üstünde boşluk görünür. | Kazanç çalışma alanında tablo kılavuzu kenarlıklarında istenmeyen bir boşluk görünmesiyle ilgili kullanıcı deneyimi sorunu düzeltildi. |
| 557334 | Kazanç yönetimi çalışma alanı: **Dönem** seçimi açılan kutusu yalnızca **Özet** sekmesinde görünmelidir | Kazanç **Dönem** seçimi açılır menüsü artık yalnızca **Özet** sekmesi **İşleme sonuçları** ve **Bağlantılar** bölümlerinde değil, Kazançlar çalışma alanında etkin olduğunda görünür. |
| 557336 | Kazanç yönetimi çalışma alanı: Kutucuk görünümünde **Kullanıma alınmış planların olduğu açık kayıt** metni kesilmiş | Kutucuk görünümündeki metin, gerekli bağlamın kesilmesini önlemek için **Açık kayıttaki...planlar kullanıma alındı** olarak değiştirildi. |

## <a name="in-preview"></a>Ön izlemede

Aşağıdaki yeni özellikler önizlemededir. Özellikleri açma hakkında daha fazla bilgi için bkz. [Özellikleri yönetme](hr-admin-manage-features.md).

| Özellik | Sürüm planı | Belgeler |
| --- | --- | --- |
| Kazanç yönetimi çalışma alanı | [Kazanç yönetimi çalışma alanı (Önizleme)](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Kazanç yönetimi çalışma alanı](hr-benefits-management-workspace.md) |
| Çalışanların ilgili kişi bilgilerini düzenlemelerini kısıtlama | [Çalışanların ilgili kişi bilgilerini düzenlemesini kısıtlama](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [Kişisel bilgilerin düzenlenmesini kısıtlama](hr-employee-self-service-restrict-editing.md)|

## <a name="coming-soon"></a>Çok yakında

| Özellik | Ayrıntılı |
| --- | --- |
| Çalışanları için bir yönetici tarafından girilen yetenekler, bir iş akışı tarafından otomatik olarak onaylanabilir | Çok yakında sunulacak. |

Planlanan özelliklerin tam listesi ve bunların zamanlanmış sürümleri için, bkz. [Dynamics 365 Human Resources 2021 sürümü 1. Dalga'ya genel bakış](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Ayrıca bkz.

[Human Resources'daki yenilikler veya değişiklikler](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 sürüm 1'ye genel bakış](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Güncelleştirme işlemi](hr-admin-setup-update-process.md)</br>
[Özellikleri yönetme](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
