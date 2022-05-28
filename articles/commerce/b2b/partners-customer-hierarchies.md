---
title: Müşteri hiyerarşileri kullanarak B2B iş ortaklarını yönetme
description: Bu konuda, Microsoft Dynamics 365 Commerce işletmeden işletmeye (B2B) e-ticaret web sitelerinde iş ortaklarını yönetmek için müşteri hiyerarşileri kullanma açıklanmaktadır.
author: josaw1
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 70acdf469be2fcddd9e2bf755e958c1b20ee2fcf
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686583"
---
# <a name="manage-b2b-business-partners-using-customer-hierarchies"></a>Müşteri hiyerarşileri kullanarak B2B iş ortaklarını yönetme

[!include [banner](../../includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce işletmeden işletmeye (B2B) e-ticaret web sitelerinde iş ortaklarını yönetmek için müşteri hiyerarşileri kullanma açıklanmaktadır.

Commerce Headquarters 'da, B2B e-ticaret sitenizi kullanacak iş ortağı kuruluşları temsil etmek için *müşteri hiyerarşisi* varlığı kullanılır. İş ortaklarını yönetmek amacıyla müşteri hiyerarşilerini kullanmaya başlamadan önce, Commerce Headquarters'da B2B e-ticaret özelliklerini etkinleştirmeniz ve sonra müşteri hiyerarşisi için bir numara sırası tanımlamanız gerekir.

## <a name="enable-the-b2b-e-commerce-feature-in-commerce-headquarters"></a>Commerce Headquarters'da B2B e-ticaret özelliğini etkinleştirme

B2B e-ticaret özelliklerini kullanmak için önce Commerce Headquarters'da **B2B eTicaret özellikleri kullanımını etkinleştir** özelliğinin etkinleştirilmesi gerekir.

1. **Çalışma alanları \> Özellik yönetimi**'ne gidin.
1. **Tümü** sekmesinde, **Modül: Retail ve Commerce**'i aramak için filtre kutusunu kullanın.
1. **B2B e-ticaret özelliklerinin kullanımını etkinleştir** özelliğini bulup seçin ve ardından sağ alt köşeden **Şimdi etkinleştir**'i seçin.

## <a name="define-a-number-sequence-for-the-customer-hierarchy"></a>Müşteri hiyerarşisi için numara sırası tanımlama

Numara serileri, ana veri kayıtları ve tanımlayıcı gerektiren işlem kayıtları için okunabilir ve benzersiz tanımlayıcılar oluşturmada kullanılır. Müşteri hiyerarşisi için kimlik oluşturmak üzere kullanılacak bir numara sırası tanımlamanız gerekir. Numara serileri hakkında daha fazla bilgi için bkz. [Numara serilerine genel bakış](/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview).

Commerce Headquarters'da müşterinin hiyerarşisi için numara sırası tanımlamak üzere şu adımları izleyin.

1. **Retail ve Commerce \> Headquarters kurulumu \> Numara sıraları \> Numara sıraları**'na gidin.
1. Yeni bir numara sırası oluşturun veya yeniden kullanmak üzere varolan bir numara sırasını seçin.
1. **Retail ve Commerce \> Headquarters ayarı \> Parametreler \> Paylaşılan Commerce parametreleri**'ne gidin.
1. **Numara sıraları** sekmesinde, önceden oluşturduğunuz veya daha önce seçtiğiniz numara sırasını **Müşteri hiyerarşi kodu** başvurusuna ekleyin.

![Müşteri hiyerarşisi kimliği başvurusuna eklenen numara serisi.](../media/NumberSequenceCustHierarchy.png)

## <a name="how-the-approval-process-works"></a>Onay işleminin çalışma şekli

Bir iş ortağı bir B2B e-ticaret sitesine katılmayı istediğinde, sistem isteği *aday müşteri* olarak kaydeder. Perakende operasyonlar yöneticisi gibi bir Commerce Headquarters kişisi iş ortağı isteklerini onaylayabilir veya reddedebilir. İş ortağı isteklerinin ve aday müşteri onaylarının nasıl yönetildiği hakkında daha fazla bilgi için [B2B e-ticaret web sitelerinde iş ortağı kullanıcılarını yönetme](manage-b2b-users.md) konusuna bakın.

Aday müşteri onaylandığında, sistem iki yeni müşteri kaydı oluşturur:

- **Kuruluş türünün** bir müşteri kaydı iş ortağı olmak isteyen kuruluşu temsil eder.
- **Kişi** türünde bir müşteri kaydı, isteği gönderen kişiyi temsil eder.

Ayrıca, **Retail ve Commerce \> Müşteriler \> Müşteri hiyerarşileri**'nde yeni bir müşteri hiyerarşisi kaydı oluşturulur. Bu müşteri hiyerarşisi kaydı aşağıdaki özelliklere sahiptir:

- **Müşteri hiyerarşisi kimliği** – Müşteri hiyerarşisi için benzersiz kimlik. Bu kimlik, Commerce paylaşılan parametrelerinde tanımladığınız numara sırasını kullanır.
- **Ad** - İş ortağının kuruluş adı ekleme isteğinde belirttiği kuruluş adı. Bu alan düzenlenebilir.
- **Amaç** – Bu özellik önceden tanımlanmış **B2B kuruluşu** değerine ayarlanır.
- **Kuruluş** - İş ortağı kuruluşunun müşteri kimliği.

Ekleme isteğini gönderen kişi **Hiyerarşi** hızlı sekmesine eklenir ve bunlara **Yönetici** rolü atanır. Yönetici, bir B2B sitesinde iş ortağı kuruluşuna daha fazla kullanıcı eklediğinde her bir kullanıcı için yeni bir müşteri kaydı oluşturulur. Müşteri kaydı aynı zamanda iş ortağı için ilgili müşteri hiyerarşisi kaydına eklenir ve buna bir **Kullanıcı** rolü atanır.

### <a name="examples"></a>Örnekler

Sam J adlı bir kişi, Microsoft kuruluşu adına ekleme isteği gönderir. İstek onaylandıktan sonra, iki yeni müşteri hesabı oluşturulur: Sam J için **Kişi** türünde bir hesap ve Microsoft için **Kuruluş** türünde bir hesap.

Aşağıda gösterilen örnekte olduğu gibi, yeni bir müşteri hiyerarşisi kaydı da oluşturulur. Bu kayıt kuruluşla aynı adı taşır (**Microsoft**) ve **Yönetici** rolü Sam J 'ye atanır. Yönetici olarak Sam J. B2B sitesinin diğer Microsoft kullanıcılarını bu hiyerarşiye ekler ve onlara **Kullanıcı** rolü atar. Bu örnekte, Sush R. bir kullanıcı olarak eklenmiştir.

![Müşteri hiyerarşisi kaydı örneği.](../media/CustomerHierarchy2.png)

Müşterinin bir müşteri hiyerarşisi ile ilişkili olup olmadığını belirlemek için müşteri kaydını açın. Aşağıdaki örnekte gösterildiği gibi, **Perakende** hızlı sekmesinin **B2B** bölümündeki **Müşteri hiyerarşisi kimliği** alanı, müşterinin bir müşteri hiyerarşisinin bir parçası olup olmadığını gösterir ve **B2B yöneticisi** seçeneği müşterinin o hiyerarşide bir yönetici olup olmadığını gösterir.

![Müşterinin bir hiyerarşi ile ilişkili olduğu ve yönetici olarak belirtildiği bir müşteri kaydının Retail hızlı sekmesinde bulunan B2B bölümü örneği.](../media/CustomerHierarchyMapping2.png)

Çoğu durumda, bir hiyerarşideki tüm müşteri kayıtlarının özellik değerleri eşleşmelidir. Örneğin, tüm iş ortağı kullanıcıların ürünlerle ilgili benzer fiyatları alması gerektiğinden, fiyat grubu ve ilişkili yapılandırmaların eşleşmesi gerekir. Ancak, sistem bu tutarlılığı zorunlu kılmaz. Bu nedenle, ilgili Commerce Headquarters kullanıcıları belirli bir hiyerarşideki tüm müşteriler için özellik değerlerinin ve yapılandırmaların eşleşmesini sağlamaya karşı sorumludur.

Commerce Headquarters kullanıcıları, hiyerarşideki tüm müşteri kayıtlarının özellik değerlerini yan yana görünümde inceleyebilir. Aşağıdaki örnekte gibi, **Hiyerarşi** hızlı sekmesindeki **Genel** seçeneğini kullanabilir ve sonra ilgili özellikleri göstermek için müşteri kaydının herhangi bir bölümünü seçebilirsiniz. Kullanıcılar bu görünümdeki özellik değerlerini doğrudan düzenleyebilir. Bir yönetici müşteri kaydındaki tüm değerleri tüm kullanıcılara kopyalamak için **Hiyerarşi** hızlı sekmesinde **Geçersiz kıl**'ı seçin.

![Geçersiz kıl düğmesini ve açılan listedeki seçeneği gösteren bir müşteri hiyerarşisi kaydı örneği.](../media/HierarchyDetails2.png)

[!include [footer-include](../../includes/footer-banner.md)]
