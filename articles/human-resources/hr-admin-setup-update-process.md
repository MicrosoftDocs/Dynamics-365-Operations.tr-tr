---
title: Güncelleştirme işlemi
description: Microsoft Dynamics 365 Human Resources uygulama ve platform değişiklikleri için sürekli, temassız servis güncelleştirmeleri sağlayan gerçek bir hizmet olarak yazılımdır (SaaS).
author: twheeloc
ms.date: 12/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 197b3c5717494ab3c80a57cda337a9021293bf73
ms.sourcegitcommit: 68efa7b89273d04484566cbe14d3533a8fd4ee53
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/02/2022
ms.locfileid: "9819309"
---
# <a name="update-process"></a>Güncelleştirme işlemi

_**Uygulandığı Öğe** tek başına çalışan altyapıda İnsan Kaynakları_ 

> [!NOTE]
> Temmuz 2022 tarihinden başlayarak tek başına İnsan Kaynakları altyapısında yeni İnsan Kaynakları ortamları sağlanamaz ve burada yeni Microsoft Dynamics Lifecycle Services (LCS) projeleri oluşturulamaz. Müşteriler, İnsan Kaynakları ortamları yalnızca finans ve operasyon altyapısı üzerinden dağıtılabilir. Daha fazla bilgi için bkz. [Finans ve operasyon altyapısında İnsan Kaynakları sağlama](hr-admin-setup-provision-fo.md).

> [!IMPORTANT]
> Finans ve operasyon uygulama altyapısındaki güncelleştirme ve düzeltme işlemi süreci İnsan Kaynakları bağımsız güncelleştirme ve düzeltme sürecinden farklıdır. Güncelleştirme süreci hakkında daha fazla bilgi için bkz. [Finans ve operasyonu en son güncelleştirmeye taşıma işlemi](../fin-ops-core/dev-itpro/migration-upgrade/upgrade-latest-update.md). Düzeltmeler hakkında daha fazla bilgi için bkz. [Lifecycle Services'den (LCS) güncelleştirme indirme](/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs.md). 

Microsoft Dynamics 365 Human Resources, sürekli, temassız servis güncelleştirmeleri sağlayan gerçek bir hizmet olarak yazılımdır (SaaS). Bu güncelleştirmeler, yasal güncelleştirmeler de dahil olmak üzere hizmette kritik geliştirmeler sağlayan uygulama ve platform değişikliklerini içerir.

## <a name="update-policy"></a>Güncelleştirme ilkesi

Güncelleştirmeler düzenli aralıklarla yayımlanır ve tüm ortamlar için yapılır. İnsan Kaynakları, ürün destek kullanılabilirliği hakkında düzenli ve öngörülebilir kılavuzlar sunan [Microsoft Lifecycle ilkesi](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy) ile uygun olarak desteklenir.

## <a name="release-cadence"></a>Sürüm temposu 

İnsan Kaynakları güncelleştirmeler otomatik olarak tüm ortamlara uygulanır. İnsan Kaynakları iki tür sürüm sağlar:

- **Hizmet güncelleştirmeleri**: Hizmet güncelleştirmeleri, yayınlandıklarında uygun platform güncelleştirmelerini de içerir. Özel durum tabanlı güncelleştirmelere ek olarak, Dynamics 365 Finance platformu güncelleştirmelerinin Genel Kullanıma (GA) sunulması ardından düzenli servis güncelleştirmeleri gerçekleştirilir. Platform güncelleştirmeleri hakkında daha fazla bilgi için bkz. [Platform güncelleştirmelerindeki yenilikler veya değişiklikler](../fin-ops-core/dev-itpro/get-started/whats-new-home-page.md). Güncelleştirmeler, bölgeler arasında aşamalı genel bir piyasaya sahiptir. Güncelleştirmeler hakkında daha fazla bilgi için bkz. [Dynamics 365 Human Resources'ta yenilikler veya değişiklikler](hr-admin-whats-new.md).

- **Dataverse çözüm güncelleştirmeleri**: Bu güncelleştirmeler gerektiğinde yaklaşık altı haftada bir gerçekleşir. Bunlar yeni varlıkları ve Dataverse'deki varolan varlıklara yapılan değişiklikleri içerir. Bu güncelleştirmeler iki haftalık güncelleştirmelerle aynı bölgelerde yayınlanır ve tüm veri merkezlerinde çoğaltılmaları altı hafta sürer. Çözüm güncelleştirmeleri iki haftalık hizmet güncelleştirmelerine göre hizalanmayabilir veya bunları hizalamayabilir.

> [!NOTE]
> Çözüm güncelleştirmeleri, serbest bırakıldıktan sonra tüm veri merkezlerinde kullanılabilir. Güncelleştirmelerin otomatik olarak çoğaltılmasını beklemek istemezseniz, bu güncelleştirmeleri herhangi bir veri merkezindeki herhangi bir ortama el ile uygulayabilirsiniz.

Gerektiğinde, İnsan Kaynakları aşağıdaki düzeltme türlerini sağlar:

- **Düzeltme (düzeltme)**: İki haftada bir hizmet güncelleştirme sürümü ile veya bu sürümden ayrı olarak oluşabilecek hata düzeltmeleri

- **Acil durum düzeltmesi**: tek başına yapıdaki proaktif ve reaktif düzeltmeler, canlı site sorunlarını gidermek için yalnızca konfigürasyon veya kod değişikliklerini içerebilir ve iki haftalık bir Servis Güncelleştirmesi sürümünden ayrı olarak oluşabilir

Sürümler bir iç ortam üzerinde gözden geçirilip test edildiğini ve doğrulanmaktadır. Yapılar imzalandıktan sonra üretime dağıtılır.

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

Tüm yeni özellikler en az 30 gün boyunca ve genellikle 30-60 gün önizlemede kalır. Önemli özellikler genellikle önizleme dönemini izleyen her yılın Ekim ve Nisan ayında kullanılabilir. **Özellik yönetimi** çalışma alanında yeni yetenekleri gördüğünüz anda bunları açabilirsiniz. Bazı özellikler varsayılan olarak açık olabilir.

Bazen bir tümleştirme özelliği varsayılan olarak açıktır ve kapatılamaz (örneğin, Özellik yönetimi çalışma alanı).

Bir özellik genel olarak kullanılabilir olduğunda üretim ortamlarında açılıp kapatılamayabilir. **Özellik yönetimi** çalışma alanı bir önizleme özelliğinin zorunlu hale gelme zamanını belirtir. Bu tarih genellikle yarıyıllık sürüm planlarına uygun olacak şekilde 1 Ekim veya 1 Nisandır. Zorunlu özellikleri kapatamazsınız. Bir özelliği zorunlu olana kadar tüm ortamlarda kapatıp açabilirsiniz.

Korumalı alan veya deneme ortamındaki özelliklerin önizlenmesini önemle öneririz. Verileriniz ile yeni özelliklerin eksiksiz deneyimini elde edebilmeniz için, geçerli üretim ortamınızın veya veritabanınızın bir kopyasını bir sandbox ortamına oluşturmak en iyisidir.

Korumalı alan ortamının sağlanması hakkında daha fazla bilgi için bkz. [İnsan Kaynakları projesi hazırlama](hr-admin-setup-provision.md). Test ortamını kaldırmak için bkz. [Örnek kaldırma](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment). 

## <a name="report-bugs"></a>Hataları raporla

Önizleme özellikleri test edilirken veya yeni yetenekler denerken, beklendiği gibi çalışmayan maddeler bulunabilir. Lütfen [Microsoft Dynamics 365 desteğiyle](https://dynamics.microsoft.com/support/) tüm hataları bildirin.

## <a name="see-also"></a>Ayrıca bkz.

[Dynamics 365 ve Power Platform sürüm planları](/dynamics365/release-plans)</br>
[Dynamics 365 Human Resources'daki yenilikler veya değişiklikler](hr-admin-whats-new.md)</br>
[Yazılım yaşam döngüsü ilkesi](../fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
