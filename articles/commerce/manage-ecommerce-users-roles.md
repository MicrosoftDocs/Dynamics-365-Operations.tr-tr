---
title: e-Ticaret kullanıcıları ve rolleri yönetme
description: Bu konu, Microsoft Dynamics 365 Commerce sitenizin geliştirme ortamına kullanıcıların erişmelerine nasıl izin verileceğini açıklamaktadır.
author: bicyclingfool
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ff0d3e607eb905eb9264bbb9ba151fbd527a81a2c72252252f2a45edc201e1b4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6715418"
---
# <a name="manage-e-commerce-users-and-roles"></a>e-Ticaret kullanıcıları ve rolleri yönetme


[!include [banner](includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce sitenizin geliştirme ortamına kullanıcıların erişmelerine nasıl izin verileceğini açıklamaktadır.

Kullanıcı erişiminin denetimine yardımcı olmak ve belirli görevleri gerçekleştirmek için kullanıcılara izin vermek istiyorsanız, site geliştirme ortamı, Microsoft Azure Active Directory (Azure AD) uygulamasında oluşturduğunuz güvenlik gruplarını kullanır. İlk olarak, geliştirme ortamındaki her role Azure AD'den yeni veya varolan bir güvenlik grubu atarsınız. Daha sonra, bu kullanıcıları uygun bir güvenlik grubuna ekleyerek veya bir güvenlik grubundan kaldırarak bireysel kullanıcılar için izinleri verirsiniz veya iptal edebilirsiniz.

## <a name="overview-of-roles-in-the-authoring-environment"></a>Geliştirme ortamındaki rollere genel bakış

Dynamics 365 for Commerce düzenleme ortamı aşağıdaki rolleri destekler.

| Rol                 | Tanım |
|----------------------|-------------|
| Sistem Yöneticisi | Bu role sahip kullanıcıların tüm araçlar ve tüm derecelendirmeler ve incelemeler için tüm öncelikleri vardır. Siteler de oluşturabilirler. |
| Yönetici   | Bu role sahip kullanıcıların, belirli bir site yapısındaki tüm araçlar ve RnR ayrıcalıklarına sahip olması gerekir. |
| Web üreticisi         | Bu role sahip kullanıcılar, sayfalar, parçalar ve şablonlar oluşturabilir, varlıkları karşıya yükleyebilir ve yönetebilir, zengin ürün ve kategorileri oluşturabilirsiniz. |
| Okuyucu               | Bu role sahip kullanıcılar sayfaları, şablonları, varlıkları, parçaları, düzenleri ve ayarları görüntüleyebilir, ancak değişiklik yapamaz. |
| RnR Moderatörü        | Bu role sahip kullanıcılar, ürün incelemelerinin orta olmasını içerebilir. |

## <a name="system-administrator-role"></a>Sistem Yöneticisi rolü

Microsoft Dynamics Lifecycle Services (LCS) ortamında Dynamics 365 Commerce sağladığınızda, **Sistem Yöneticisi** rolü için bir güvenlik grubu sağlamanız istenir. Bu rol, konfigüre ettiğiniz ortamda oluşturduğunuz tüm sitelere otomatik olarak uygulanır. Bu rolün güvenlik grubu yalnızca LCS'de güncelleştirilebilir. Tüm sitelerin **site yönetim** sayfasında salt okunur olarak görünür ve yalnızca bilgilendirme amaçlıdır.

## <a name="administrator-role"></a>Yönetici rolü

Commerce'ta yeni bir site oluşturduğunuzda, **yönetici** rolü için bir güvenlik grubu sağlamanız istenir. Bu rolün verdiği izinlere genel bakış için bu konunun yukarısındaki tabloya bakın.

## <a name="add-or-update-security-groups"></a>Güvenlik grupları Ekle veya güncelleştir

Siteniz oluşturulduktan sonra, yalnızca **Sistem Yöneticisi** ve **Yönetici** rolleriyle ilişkilendirilmiş güvenlik gruplarında olan kullanıcılar o sitenin geliştirme ortamına erişebilir. **Web Üreticisi**, **RNR moderatör** ve **Okuyucu** rollerine Kullanıcı atamak için, bu rollere güvenlik grupları atamanız gerekir. Bir role güvenlik grubu eklemek veya bir role atanmış olan bir güvenlik grubunu güncelleştirmek için, aşağıdaki adımları izleyin.

1. Güncelleştirmek istediğiniz siteye gidin.
1. **Site Yönetimi**'nde, **güvenlik** sayfasını açın.
1. Değiştirilecek rolü seçin.
1. Rollere güvenlik grupları ekleyin veya rollerden güvenlik gruplarını kaldırın.

## <a name="additional-resources"></a>Ek kaynaklar

[Telemetriyi desteklemek için site sayfalarına komut dosyası kodu ekleme](add-telemetry.md)

[Siteniz için arama motoru optimizasyonu (SEO) konuları](search-engine-optimization-considerations.md)

[İçerik Güvenliği İlkesini (CSP) yönetme](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]