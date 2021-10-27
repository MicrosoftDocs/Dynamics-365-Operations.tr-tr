---
title: Dynamics 365 Human Resources'taki yenilikler veya değişiklikler 5 Ekim 2021
description: Bu konuda, 5 Ekim 2021 için Microsoft Dynamics 365 Human Resources'taki yeni veya değişen özellikler açıklanmaktadır.
author: marcelbf
ms.date: 10/05/2021
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
ms.search.validFrom: 2021-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 206c7f590b495278b7899271db0e83b3a4da3edc
ms.sourcegitcommit: 42bd701179e664947b6eafcd1804c83a5e64abcb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2021
ms.locfileid: "7641442"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-october-5-2021"></a>Dynamics 365 Human Resources'taki yenilikler veya değişiklikler 5 Ekim 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konuda, Microsoft Dynamics 365 Human Resources uygulamasındaki yeni, değişen veya gelecek özellikler açıklanmaktadır.

Güncelleştirme işlemi ve planı hakkında daha fazla bilgi için bkz. [Güncelleştirme işlemi](hr-admin-setup-update-process.md).

Yeni özellikler ve bunların beklenen genel kullanılabilirlik tarihleri hakkında daha fazla bilgi için, [Dynamics 365 Human Resources 2021 sürümü 2. Dalga'ya bakın](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Bu sürümde

Bu sürüm aşağıdaki yeni özellikleri ve hata düzeltmelerini içerir. Değişiklikler derleme numarası 8.1.4485 uygulanır.

### <a name="new-features"></a>Yeni özellikler

Aşağıdaki özellikler genel olarak bu sürümde mevcuttur.

| Özellik | Sürüm planı | Belgeler |
|---|---|---|
| Platform güncelleştirmesi 10.0.21 (45) | -- | [Finance and Operations uygulamaların 10.0.21 sürümü için platform güncelleştirmeleri (Ekim 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21) |


### <a name="bug-fixes"></a>Hata düzeltmeleri

Bu sürümde aşağıdaki hata çözümleri bulunmaktadır.

> [!NOTE]
> Bizim hedefimiz size en kısa sürede bu bilgiyi sunmaktır. Bu konu ilk kez yayımlandıktan sonra derlemeye eklenen hata düzeltmelerini eklemek için bu konuya güncelleştirmeler uygulayabiliriz.

| Sorun numarası | Sorun | Tanım |
|---|---|---|
| 598896 | Çalışan tutarı, çalışanın kaydı tamamlanana kadar görüntülenmiyor | **Çalışan Self Servis** sayfasında, kazançla ilgili çalışan tutarı görüntülenmedi. **Kzanç self servis** artık çalışan miktarı görüntülenir.  |
| 613440 | **Veri yönetiminden** veriler dışa aktarılamıyor | **Veri yönetimi**'nde bir projeye ait verileri dışa aktarırken verme işlemi beklenmedik şekilde başarısız olur. |
| 618327 | Kapanan dönemler ve gelecek dönemler, kazanç beyanı için **Raporlar parametreleri** sayfasında görüntüleniyor | **Personel self servisi**'nde **Kazanç beyanı**'na giderken **Rapor parametreleri** sayfasında **Eklenecek kayıtlar** ve **Arka planda çalıştır** hızlı sekmeleri görüntüleniyor. Bu bölümler kaldırıldı.|
| 618326 | Kazanç beyanı için **Personel self servisi**'ndeki **Rapor parametreleri** sayfası yanlış görüntülenir| Kullanıcı, **Kazanç beyanı raporu** hedef sayfasına giderken kapalı durumda olan veya ileri tarihli kazanç planlarının dönemlerini seçebiliyor ve bu da boş bir sayfayla sonuçlanıyor. Listede yalnızca geçerli kazanç planı dönemi görüntülenmelidir. |

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
|Raporu, **GER raporu hedefi** kullanılarak e-postayla gönderirken hata | Kazanç beyanı, **GER Raporu hedefleri** sayfasındaki e-posta parametrelerini kullanacak şekilde ayarlanabilir. Kullanıcı, kurulumu tamamlayıp raporu yazdırırken bir biçimlendirme hatası alır ve kazanç beyanı gönderilmez.|

## <a name="feature-management-changes"></a>Özellik yönetimi değişiklikleri

| Özellik | Tanım |
|---|---|
|Performans günlükleri genişletilmiş raporlar görünümü | Bu özellik, bu sürümde varsayılan olarak etkinleştirilecektir. |

## <a name="coming-soon"></a>Çok yakında

Planlanan özelliklerin tam listesi ve bunların zamanlanmış sürümleri için, bkz. [Dynamics 365 Human Resources 2021 sürümü 2. Dalga'ya genel bakış](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

| Özellik | Ayrıntılar |
|---|---|
| Platform güncelleştirmesi 10.0.22 (46) | Platform güncelleştirmesi 10.0.22'in kullanıma sunulmasının, 1 Kasım 2021'deki hizmet sürümüyle başlaması planlanıyor. Daha fazla bilgi için bkz. [Finance and Operations uygulamalarının 10.0.22 sürümü için platform güncelleştirmeleri (Kasım 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-22). |



## <a name="see-also"></a>Ayrıca bkz.

[Human Resources'daki yenilikler veya değişiklikler](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 sürüm 2'ye genel bakış](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Güncelleştirme işlemi](hr-admin-setup-update-process.md)</br>
[Özellikleri yönetme](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
