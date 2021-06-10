---
title: Dynamics 365 Human Resources'daki yenilikler veya değişiklikler 19 Nisan 2021
description: Bu konuda, 19 Nisan 2021 için Microsoft Dynamics 365 Human Resources'taki yeni veya değişen özellikler açıklanmaktadır.
author: marcelbf
ms.date: 04/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-04-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b1371e453ae51dafe24b2105b1b9b7c38cdb4db4
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052373"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-19-2021"></a>Dynamics 365 Human Resources'daki yenilikler veya değişiklikler 19 Nisan 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konuda, Dynamics 365 Human Resources'daki yeni, değişen veya gelecek özellikler açıklanmaktadır.

Güncelleştirme işlemi ve planı hakkında daha fazla bilgi için bkz. [Güncelleştirme işlemi](hr-admin-setup-update-process.md).

Yeni özellikler ve bunların beklenen genel kullanılabilirlik tarihleri hakkında daha fazla bilgi için, [Dynamics 365 Human Resources 2021 sürümü 1. Dalga'ya bakın](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Bu sürümde

Bu sürüm aşağıdaki yeni özellikleri ve hata düzeltmelerini içerir. Değişiklikler derleme numarası 8.1.4113 uygulanır.

### <a name="new-features"></a>Yeni özellikler

Aşağıdaki özellikler genel olarak bu sürümde mevcuttur.

| Özellik | Sürüm planı | Belgeler |
| --- | --- | --- |
| Platform güncelleştirmesi 10.0.17 (41) | -- | [Finance and Operations uygulamaların 10.0.17 sürümü için platform güncelleştirmeleri (Nisan 2021)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-17.md) |
| Kazançlar Yönetim formlarında Özel Alanlar desteği | [Kazançlar yönetim formlarında özel alanlar desteği](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-benefits-management)| [Kazanç yönetimine genel bakış](hr-benefits-management-overview.md)|

### <a name="bug-fixes"></a>Hata düzeltmeleri

Bu sürümde aşağıdaki hata çözümleri bulunmaktadır.

> [!NOTE]
> Bizim hedefimiz size en kısa sürede bu bilgiyi sunmaktır. Bu konu ilk kez yayımlandıktan sonra derlemeye eklenen hata düzeltmelerini eklemek için bu konuya güncelleştirmeler uygulayabiliriz.

| Sorun numarası | Çıkış |  Tanım |
| --- | --- | --- |
| 552164 | **Çalışan self servis > Kursları aç**'ta **Kaydedilen görünüm**, ajandası olan kurslar için çalışmıyor | Açık kurslarda (ESS) Kaydedilmiş bir görünüm kullanılıyorsa ve kursların birine iliştirilmiş bir Ajanda varsa, görünüm artık o Kurs için birden çok satır göstermez |
| 560614 | **Kazançlar > Ömür olayı seçenekleri**, araç ipucu belgelerinde ve kod davranışlarında tutarsızlıkları gösterir. | Doğru davranışı göstermek için **Ömür olayı seçenekleri**'nde araç ipuçları güncelleştirildi. |
| 560616 | **Kazançlar > Ömür olayı seçenekleri**, çalışan kazanç planında düzenlenebilir ancak değişiklikler etkilenmez. | Araç ipucu belgelerine göre, bağlı seçeneklerine dayanarak Ömür olayı seçeneğinin etkinleştiği veya devre dışı kaldığı davranış güncelleştirildi. |
| 565054 | **Gelişmiş erişim** açık olduğunda, **İş kaydı olmayan çalışanlar** listesinin içeriği görüntülenemiyor. | Bu sürüm, **Gelişmiş erişim** açıldığında, **İş kaydı olmayan çalışanlar**  listesinin içeriğini yalnızca sistem yöneticilerin görüntüleyebildiği sorunu çözer. Bu düzeltme bir güvenlik değişikliği olduğundan, bunu Özellik yönetiminde etkinleştirmeniz gerekir. Özellik açıldıktan sonra, gelişmiş erişim açık olsa bile forma erişimi olan bu roller içeriği görürler. Daha fazla bilgi için bkz. [İş kaydı olmayan çalışanlar](hr-personnel-workers-without-employment.md). |
| 570586 | Çalışma, tüm izin planlarında ilgili çalışan için en son hareketten önce sona erdiğinde, izin talebi doğrulama başarısız olur. | Çalışma bittikten sonra, izin talebi doğrulama işlemi çalışanın izin hareketleri temelinde başarısız olmaz.|
| 570783 | Human Resources paylaşılan parametrelerde şirketler arası izni etkinleştirme ve devre dışı bırakma, tek bir şirkette çalışan çalışanların izin isteklerinde neler gördüğünü değiştirir. | Tek bir şirkette çalışan çalışanlar, parametre etkinleştirilse de devre dışı bırakılsa da izin isteklerinde hiçbir değişiklik görmez. |
| 572343 | Şirketler arası izin görüntüleme özelliği etkinleştirildiğinde gerekli neden kodu görüntülenmiyor. | Şirketler arası izin özelliği etkinleştirildiğinde, neden kodu artık beklendiği şekilde görüntülenir. |
| 573676 | **Kazançlar yönetimi > Bağlantılar > Kazanç planları**'na **Dönem** eklenemiyor. | Mevcut **Kazanç planı** formunda **Dönem** ekleme veya güncelleştirmenin yapılamadığı hatalar giderildi. |

## <a name="in-preview"></a>Ön izlemede

Aşağıdaki yeni özellikler önizlemededir. Özellikleri açma hakkında daha fazla bilgi için bkz. [Özellikleri yönetme](hr-admin-manage-features.md).

| Özellik | Sürüm planı | Belgeler |
| --- | --- | --- |
| Kazanç yönetimi çalışma alanı | [Kazanç yönetimi çalışma alanı (Önizleme)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Kazanç yönetimi çalışma alanı](hr-benefits-management-workspace.md) |
| İzin ve devamsızlık iş akışı deneyiminde geliştirmeler | [İzin ve devamsızlık iş akışı deneyiminde geliştirmeler](https://go.microsoft.com/fwlink/?linkid=2147528) | [İzin iste](hr-employee-self-service-request-time-off.md)|
| Basitleştirilmiş bordro tümleştirmesini (Bordro tümleştirme API'leri) etkinleştirme | [Bordro sağlayıcılarıyla basitleştirilmiş tümleştirmeleri etkinleştirme](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Bordro tümleştirme API'si](hr-admin-integration-payroll-api-introduction.md)|

## <a name="coming-soon"></a>Çok yakında

| Özellik | Ayrıntılı |
| --- | --- |
| Çalışanları için bir yönetici tarafından girilen yetenekler, bir iş akışı tarafından otomatik olarak onaylanabilir | Çok yakında sunulacak. |
| Platform güncelleştirmesi 10.0.18 (42) | Platform Update 10.0.18, 17 Mayıs 2021'deki hizmet sürümü ile kullanıma sunulmak üzere zamanlanmıştır. Daha fazla bilgi için bkz. [Finance and Operations uygulamalarının 10.0.18 sürümü için platform güncelleştirmeleri (Mayıs 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-18). |
| Kazançlar yönetimi uygunluğu kurallarında özel alanlar desteği  | [Uygunluk işleme için özel alan desteği](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |

Planlanan özelliklerin tam listesi ve bunların zamanlanmış sürümleri için, bkz. [Dynamics 365 Human Resources 2021 sürümü 1. Dalga'ya genel bakış](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Ayrıca bkz.

[Human Resources'daki yenilikler veya değişiklikler](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 sürüm 1'ye genel bakış](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Güncelleştirme işlemi](hr-admin-setup-update-process.md)</br>
[Özellikleri yönetme](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
