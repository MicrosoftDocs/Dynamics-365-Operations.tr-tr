---
title: Güncelleştirme işlemi
description: Microsoft Dynamics 365 Human Resources uygulama ve platform değişiklikleri için sürekli, temassız servis güncelleştirmeleri sağlayan gerçek bir hizmet olarak yazılımdır (SaaS).
author: andreabichsel
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2466c53885340991aeeb0a07af83517473b332b6
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053647"
---
# <a name="update-process"></a>Güncelleştirme işlemi

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Microsoft Dynamics 365 Human Resources, sürekli, temassız servis güncelleştirmeleri sağlayan gerçek bir hizmet olarak yazılımdır (SaaS). Bu güncelleştirmeler, yasal güncelleştirmeler de dahil olmak üzere hizmette kritik geliştirmeler sağlayan uygulama ve platform değişikliklerini içerir.

## <a name="update-policy"></a>Güncelleştirme ilkesi

Güncelleştirmeler düzenli aralıklarla yayımlanır ve tüm ortamlar için yapılır. İnsan Kaynakları, ürün destek kullanılabilirliği hakkında düzenli ve öngörülebilir kılavuzlar sunan [Microsoft Lifecycle ilkesi](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy) ile uygun olarak desteklenir.

## <a name="release-cadence"></a>Sürüm temposu 

İnsan Kaynakları güncelleştirmeler otomatik olarak tüm ortamlara uygulanır. İnsan Kaynakları iki tür sürüm sağlar:

- **Hizmet güncelleştirmeleri**: Güncellemeler, hata düzeltmeleri ve yeni özellikler içererek iki haftada bir yapılır. Hizmet güncelleştirmeleri, serbest bıraktıklarında uygun platform güncelleştirmelerini de içerir. Platform güncelleştirmelerinin ne zaman yayınlanacaklarını öğrenmek için [Tablo 3: Platform yayımları](../fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy.md#table-3-platform-releases)'na bakın. İki Haftalık Güncelleştirmeler, bölgeler arasında aşamalı genel bir piyasaya sahiptir. İki Haftalık güncellemeler hakkında daha fazla bilgi için bkz. [Dynamics 365 Human Resources'ta yenilikler veya değişiklikler](hr-admin-whats-new.md).

    Aksi belirtilmedikçe, tüm desteklenen veri merkezleri iki haftalık olarak güncelleştirilir. ABD, Avustralya, Avrupa, Birleşik Krallık, Asya ve Kanada bölgeleri iki haftalık güncelleştirmelere dahil edilmiştir. 

- **Dataverse çözüm güncelleştirmeleri**: Bu güncelleştirmeler gerektiğinde yaklaşık altı haftada bir gerçekleşir. Bunlar yeni varlıkları ve Dataverse'deki varolan varlıklara yapılan değişiklikleri içerir. Bu güncelleştirmeler iki haftalık güncelleştirmelerle aynı bölgeler için serbest çalışırlar ve tüm veri merkezleri arasında yineleme yapmak için altı hafta sürer. Çözüm güncelleştirmeleri iki haftalık hizmet güncelleştirmelerine göre hizalanmayabilir veya bunları hizalamayabilir.

> [!NOTE]
> Çözüm güncelleştirmeleri, serbest bırakıldıktan sonra tüm veri merkezlerinde kullanılabilir. Güncelleştirmelerin otomatik olarak çoğaltılmasını beklemek istemezseniz, bu güncelleştirmeleri herhangi bir veri merkezindeki herhangi bir ortama el ile uygulayabilirsiniz.

Gerektiğinde, İnsan Kaynakları aşağıdaki düzeltme türlerini de sağlar:

- **Düzeltme (düzeltme)**: İki haftada bir hizmet güncelleştirme sürümü ile veya bu sürümden ayrı olarak oluşabilecek hata düzeltmeleri

- **Acil durum düzeltmesi**: tek başına yapıdaki proaktif ve reaktif düzeltmeler, canlı site sorunlarını gidermek için yalnızca konfigürasyon veya kod değişikliklerini içerebilir ve iki haftalık bir Servis Güncelleştirmesi sürümünden ayrı olarak oluşabilir

Sürümler bir iç ortam üzerinde gözden geçirilip test edildiğini ve doğrulanmaktadır. Yapılar imzalandıktan sonra üretime dağıtılır.

## <a name="release-cadence-exceptions-in-2021"></a>2021 içinde sürüm temposu özel durumları

Tatilleri hesaba eklemek için, Kasım ve Aralık 2021 için sürüm planı aşağıdaki gibidir:

- Kasım sürümü: 1 Kasım - 14 Kasım
- Aralık sürümü: 29 Kasım - 12 Aralık
 
İki haftalık sürüm temposu 10 Ocak 2022'de her zamanki gibi devam ettirilecektir.

## <a name="communications"></a>İletişim

İnsan Kaynaklarıyla ilgili neler olduğunu ve aşağıdaki konumlarda yayımladığımız neleri öğrenebilirsiniz:

- [Dynamics 365 Human Resources Yol haritası](https://dynamics.microsoft.com/roadmap/human-resources/)

- [Dynamics 365 sürüm planları](/dynamics365/release-plans/)

- [Dynamics 365 Human Resources'teki yenilikler veya değişiklikler](hr-admin-whats-new.md)

- [Lifecycle Services'de (LCS) Sorun arama](../fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs.md) (yalnızca platform ile ilgili hatalar için)

- [İnsan kaynakları blogu](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [İnsan Kaynakları Yammer topluluğu](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a>Korumalı alan ortamındaki Önizleme özellikleri

Bir korumalı alan ortamındaki Önizleme özelliklerini, üretim ortamınızda etkinleştirmeden önce doğrulayabilirsiniz. Yeni özellikleri etkinleştirme hakkında daha fazla bilgi için [Özellik yönetimine genel bakış](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)'a bakın.

Tüm yeni özellikler en az 30 gün boyunca ve genellikle 30-60 gün önizlemede kalır. Önemli özellikler genellikle önizleme dönemini izleyen her yılın Ekim ve Nisan ayında kullanılabilir. Özellik yönetimi çalışma alanında yeni yetenekleri gördüğünüz anda bunları açabilirsiniz. Bazı özellikler varsayılan olarak açık olabilir.

Bazen bir tümleştirme özelliği varsayılan olarak açıktır ve kapatılamaz (örneğin, Özellik yönetimi çalışma alanı).

Bir özellik genel olarak kullanılabilir olduğunda üretim ortamlarında açılıp kapatılamayabilir. Özellik yönetimi çalışma alanı bir önizleme özelliğinin zorunlu hale gelme zamanını belirtir. Bu tarih genellikle yarıyıllık sürüm planlarına uygun olacak şekilde 1 Ekim veya 1 Nisandır. Zorunlu özellikleri kapatamazsınız. Bir özelliği zorunlu olana kadar tüm ortamlarda kapatıp açabilirsiniz.

Korumalı alan veya deneme ortamındaki özelliklerin önizlenmesini önemle öneririz. Verileriniz ile yeni özelliklerin eksiksiz deneyimini elde edebilmeniz için, geçerli üretim ortamınızın veya veritabanınızın bir kopyasını bir sandbox ortamına oluşturmak en iyisidir.

Korumalı alan ortamının sağlanması hakkında daha fazla bilgi için, bkz. [İnsan Kaynakları projesi hazırlama](hr-admin-setup-provision.md). Test ortamını kaldırmak için, bkz. [Örnek kaldırma](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment). 

## <a name="report-bugs"></a>Hataları raporla

Önizleme özellikleri test edilirken veya yeni yetenekler denerken, beklendiği gibi çalışmayan maddeler bulunabilir. Lütfen [Microsoft Dynamics 365 desteğiyle](https://dynamics.microsoft.com/support/) tüm hataları bildirin.

## <a name="see-also"></a>Ayrıca bkz.

[Dynamics 365 ve Power Platform sürüm planları](/dynamics365/release-plans)</br>
[Dynamics 365 Human Resources'daki yenilikler veya değişiklikler](hr-admin-whats-new.md)</br>
[Yazılım yaşam döngüsü ilkesi](../fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]