---
title: Dynamics 365 Human Resources'taki yenilikler veya değişiklikler 20 Eylül 2021
description: Bu konuda, 20 Eylül 2021 için Microsoft Dynamics 365 Human Resources'taki yeni veya değişen özellikler açıklanmaktadır.
author: marcelbf
ms.date: 09/20/2021
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
ms.search.validFrom: 2021-09-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3f4fc4768f8c96678b216709f78af6d3ddfd4132
ms.sourcegitcommit: ba8ca42e43e1a5251cbbd6ddb292566164d735dd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2021
ms.locfileid: "7556945"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-20-2021"></a>Dynamics 365 Human Resources'taki yenilikler veya değişiklikler 20 Eylül 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konuda, Microsoft Dynamics 365 Human Resources uygulamasındaki yeni, değişen veya gelecek özellikler açıklanmaktadır.

Güncelleştirme işlemi ve planı hakkında daha fazla bilgi için bkz. [Güncelleştirme işlemi](hr-admin-setup-update-process.md).

Yeni özellikler ve bunların beklenen genel kullanılabilirlik tarihleri hakkında daha fazla bilgi için, [Dynamics 365 Human Resources 2021 sürümü 2. Dalga'ya bakın](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Bu sürümde

Bu sürüm aşağıdaki yeni özellikleri ve hata düzeltmelerini içerir. Değişiklikler derleme numarası 8.1.4464 uygulanır.

### <a name="new-features"></a>Yeni özellikler

Aşağıdaki özellikler genel olarak bu sürümde mevcuttur.

| Özellik | Sürüm planı | Belgeler |
|---|---|---|
| Basitleştirilmiş bordro tümleştirmesini (Bordro tümleştirme API'leri) etkinleştirme | [Bordro sağlayıcılarıyla basitleştirilmiş tümleştirmeleri etkinleştirme](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Bordro tümleştirme API'si](hr-admin-integration-payroll-api-introduction.md) |
| Çalışanların ödenmeye hazır olarak işaretlenmelerine olanak sağlama | [Çalışanların ödenmeye hazır olarak işaretlenmelerine olanak sağlama](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Ödemeye hazır](/dynamics365/human-resources/hr-compensation-payroll) |

### <a name="bug-fixes"></a>Hata düzeltmeleri

Bu sürümde aşağıdaki hata çözümleri bulunmaktadır.

> [!NOTE]
> Bizim hedefimiz size en kısa sürede bu bilgiyi sunmaktır. Bu konu ilk kez yayımlandıktan sonra derlemeye eklenen hata düzeltmelerini eklemek için bu konuya güncelleştirmeler uygulayabiliriz.

| Sorun numarası | Sorun | Tanım |
|---|---|---|
| 619774 | Adres açıklamasının düzenlenmesi, gerçek zamanlı olarak Dataverse ile eşitlenmez. | Çalışan adresi için açıklamayı düzenlerken güncelleştirilmiş açıklama gerçek zamanlı olarak Dataverse ile eşitlenmez. **Lojistik Konum** tablosundaki abonelik, güncelleştirme göndermek üzere güncelleştirildi. |
| 614603| **Çalışan personel eylemleri** parametresi seçilmediğinde **Çalışan** sayfasında hata. | Yeni bir çalışan işe alırken veya **Çalışan** sayfasına giderken **Personel eylemleri** kapatılmış olsa bile "**Personel eylem türü** alanı doldurulmalıdır" hatası görüntüleniyor. |
| 615367 | **Onaylanan izin** sekmesi bir uyarı görüntülüyor ve uyarıyı yanlış görüntülüyor. | İzin birimi, **İzin birimlerini izin türüne göre yapılandır** özelliği etkinleştirilmeden önce **Günler** olarak ayarlanırsa **Onaylanan izin** sekmesi geçersiz bir uyarı ve yanlış sütunlar görüntüler. |


## <a name="in-preview"></a>Ön izlemede

Aşağıdaki yeni özellikler önizlemededir. Özelliklerin nasıl açılıp kapatılacağı hakkında daha fazla bilgi için bkz. [Özellikleri yönetme](hr-admin-manage-features.md).

| Özellik | Sürüm planı | Belgeler |
|---|---|---|
| Kazanç yönetimi çalışma alanı | [Kazanç yönetimi çalışma alanı (Önizleme)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Kazanç yönetimi çalışma alanı](hr-benefits-management-workspace.md) |
| Uygunluk'taki özel alanlar |[Uygunluk işlemede özel alanlar desteği](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-benefits-management) | [Uygunluk işlemede özel alanları kullanma](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules#using-custom-fields-in-eligibility-rules) |
| Kazanç beyanı |[Kazanç Beyanı](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/benefits-summary-statement) | [Kazanç beyanı](hr-benefits-statement.md) |

### <a name="benefits-statement-known-issues"></a>Kazanç beyanıyla ilgili bilinen sorunlar

| Sorun | Tanım |
|---|---|
| Kazanç beyanı için **Personel self servisi**'ndeki **Rapor parametreleri** sayfası yanlış. | **Personel self servisi**'nde **Kazanç beyanı**'na giderken **Rapor parametreleri** sayfasında **Eklenecek kayıtlar** ve **Arka planda çalıştır** hızlı sekmeleri görüntüleniyor.  Bunların kaldırılması gerekir. |
| Kapanan dönemler ve gelecek dönemler, kazanç beyanı için **Raporlar parametresi** sayfasında görüntüleniyor. | Kullanıcı, **Kazanç beyanı raporu** hedef sayfasına giderken kapalı durumda olan veya ileri tarihli kazanç planlarının dönemlerini seçebiliyor ve bu da boş bir sayfayla sonuçlanıyor. Listede yalnızca geçerli kazanç planı dönemi görüntülenmelidir. |
|Raporu, GER raporu hedefi kullanılarak e-postayla gönderirken hata. | Kazanç beyanı, **GER Raporu hedefleri** sayfasındaki e-posta parametrelerini kullanacak şekilde ayarlanabilir. Kullanıcı, kurulumu tamamlayıp raporu yazdırırken bir biçimlendirme hatası alır ve kazanç beyanı gönderilmez.|


## <a name="coming-soon"></a>Çok yakında

Planlanan özelliklerin tam listesi ve bunların zamanlanmış sürümleri için, bkz. [Dynamics 365 Human Resources 2021 sürümü 2. Dalga'ya genel bakış](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

| Özellik | Ayrıntılı |
|---|---|
| Platform güncelleştirmesi 10.0.21 (45) | Platform güncelleştirmesi 10.0.21'in kullanıma sunulmasının, 4 Ekim 2021'deki hizmet sürümüyle başlaması planlanıyor. Daha fazla bilgi için bkz. [Finance and Operations uygulamalarının 10.0.21 sürümü için platform güncelleştirmeleri (Ekim 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21). |
|Performans günlükleri genişletilmiş raporlar görünümü | Bu özellik, bir sonraki güncelleştirmede varsayılan olarak etkinleştirilecektir. |


## <a name="see-also"></a>Ayrıca bkz.

[Human Resources'daki yenilikler veya değişiklikler](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 sürüm 2'ye genel bakış](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Güncelleştirme işlemi](hr-admin-setup-update-process.md)</br>
[Özellikleri yönetme](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
