---
title: Dynamics 365 Human Resources uygulamasındaki yenilikler veya değişiklikler (23 Ağustos 2021)
description: Bu konuda, 23 Ağustos 2021 için Microsoft Dynamics 365 Human Resources'taki yeni veya değişen özellikler açıklanmaktadır.
author: marcelbf
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-08-23
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 21c3448c373600ffebca82be41fb5849b952dfe1
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686841"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-23-2021"></a>Dynamics 365 Human Resources uygulamasındaki yenilikler veya değişiklikler (23 Ağustos 2021)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konuda, Microsoft Dynamics 365 Human Resources uygulamasındaki yeni, değişen veya gelecek özellikler açıklanmaktadır.

Güncelleştirme işlemi ve planı hakkında daha fazla bilgi için bkz. [Güncelleştirme işlemi](hr-admin-setup-update-process.md).

Yeni özellikler ve bunların beklenen genel kullanılabilirlik tarihleri hakkında daha fazla bilgi için, [Dynamics 365 Human Resources 2021 sürümü 2. Dalga'ya bakın](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Bu sürümde

Bu sürüm aşağıdaki yeni özellikleri ve hata düzeltmelerini içerir. Değişiklikler derleme numarası 8.1.4419 uygulanır.

### <a name="bug-fixes"></a>Hata düzeltmeleri

Bu sürümde aşağıdaki hata çözümleri bulunmaktadır.

> [!NOTE]
> Bizim hedefimiz size en kısa sürede bu bilgiyi sunmaktır. Bu konu ilk kez yayımlandıktan sonra derlemeye eklenen hata düzeltmelerini eklemek için bu konuya güncelleştirmeler uygulayabiliriz.

| Sorun numarası | Sorun | Tanım |
| --- | --- | --- |
| 594066 | İlgili Kişi Bilgileri silinemiyor | Çalışan için İlgili Kişi bilgileri kaydı silinmek üzere seçildiğinde, bunun yerine seçilen kayıttan farklı bir ilgili kişi bilgileri kaydı silinir. |
| 611339 | Kişiselleştirme eklemek, banka hesabının filtreyi yoksaymasına neden oluyor ve ilk kaydı getiriyor | Kişiselleştirme eklemek, veri kaynağı sorgusu çalıştırıldıktan sonra banka hesabı listesinin bir kişiselleştirme sorgusu çalıştırmasına neden olur ve bu da ayrıntıları görüntülenen çalışandan bağımsız olarak sorguda en üst kaydın getirilmesiyle sonuçlanır. |
| 591806 | İşe alım süreci son tarih görevleri yanlış hesaplanıyor | Şu koşullarda son tarihler yanlış hesaplanır: Oluşturulan denetim listelerinde, genişletilmiş tarih aralığı kullanan bir takvim kullanılır (örn. 2005'ten 2050'ye) ve kullanıcı tercihlerinde Merkezi Standart Saat'ten farklı bir saat dilimi kullanılır. |   
| 592749 | **Personel self servisi**'nde izin bakiyesi yanlış | Personelin birden fazla tüzel kişilikte işe sahip olması ve şirketler arası izin görünümünün etkin olması durumunda izin bakiyesi yanlış olabilir. |
| 603133 | İzin istenirken oluşan beklenmeyen uyarı | İzin istenirken **Miktar** alanından önce **Yarım gün** alanını doldurmak, beklenmeyen bir uyarıya neden olur. |
| 606546 | Onaylanan izinde Alan seç görünmüyor | Birden fazla onaylanan izin isteğini seçmek için onay kutusu görünmüyor. |
| 597059 | **İzin ve Devamsızlık şirket takvimi**'nde çalışan görünmüyor | Uygulanan tarih aralığının izin isteğinin reddedildiği günleri içermesi durumunda çalışan, **İzin ve devamsızlık şirket takvimi**'nde görünmez. |


## <a name="in-preview"></a>Ön izlemede

Aşağıdaki yeni özellikler önizlemededir. Özelliklerin nasıl açılıp kapatılacağı hakkında daha fazla bilgi için bkz. [Özellikleri yönetme](hr-admin-manage-features.md).

| Özellik | Sürüm planı | Belgeler |
| --- | --- | --- |
| Kazanç yönetimi çalışma alanı | [Kazanç yönetimi çalışma alanı (Önizleme)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Kazanç yönetimi çalışma alanı](hr-benefits-management-workspace.md) |
| Basitleştirilmiş bordro tümleştirmesini (Bordro tümleştirme API'leri) etkinleştirme | [Bordro sağlayıcılarıyla basitleştirilmiş tümleştirmeleri etkinleştirme](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Bordro tümleştirme API'si](hr-admin-integration-payroll-api-introduction.md)|
| Devamsızlık Yöneticisi'nin izni yönetmesini etkinleştirme | [Devamsızlık Yöneticisi'nin izni yönetmesini etkinleştirme](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | Bu sürümde, devamsızlık yöneticisi çalışma alanı görünümünü güncelleştiriyoruz. Daha fazla bilgi için bkz. [Devamsızlık yöneticisi rolünü yapılandırma](https://go.microsoft.com/fwlink/?linkid=2168107). |
| İzin türü başına ek gereksinimini yapılandırma | [İzin türü başına ek gereksinimini yapılandırma](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) |[İzin ve devamsızlık türlerini yapılandırma](https://go.microsoft.com/fwlink/?linkid=2168108)|
| İzin birimlerini izin türüne göre yapılandır | [İzin birimlerini izin türüne göre yapılandır](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) |[İzin ve devamsızlık türlerini yapılandırma](https://go.microsoft.com/fwlink/?linkid=2168215)|
| Çalışanların ödenmeye hazır olarak işaretlenmelerine olanak sağlama | [Çalışanların ödenmeye hazır olarak işaretlenmelerine olanak sağlama](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Ödemeye hazır](/dynamics365/human-resources/hr-compensation-payroll) |

## <a name="coming-soon"></a>Çok yakında

Planlanan özelliklerin tam listesi ve bunların zamanlanmış sürümleri için, bkz. [Dynamics 365 Human Resources 2021 sürümü 2. Dalga'ya genel bakış](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

| Özellik | Ayrıntılı |
| --- | --- |
| Platform güncelleştirmesi 10.0.21 (45) | Platform güncelleştirmesi 10.0.21'in kullanıma sunulmasının, 4 Ekim 2021'deki hizmet sürümüyle başlaması planlanıyor. Daha fazla bilgi için bkz. [Finans ve Operasyon uygulamalarının 10.0.21 sürümü için platform güncelleştirmeleri (Ekim 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21). |

## <a name="see-also"></a>Ayrıca bkz.

[Human Resources'daki yenilikler veya değişiklikler](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 sürüm 2'ye genel bakış](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Güncelleştirme işlemi](hr-admin-setup-update-process.md)</br>
[Özellikleri yönetme](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
