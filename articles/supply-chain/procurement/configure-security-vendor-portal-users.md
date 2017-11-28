---
title: "Satıcı portal kullanıcı güvenliği"
description: "Bu makale, Satıcı portalını kullanan dış satıcılar için güvenliğin nasıl ayarlanacağını açıklamaktadır. Bu bilgiler, Dynamics AX'in yalnızca Şubat 2016 &amp; Mayıs 2016 sürümleri için geçerlidir."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserManagement
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 30231
ms.assetid: 3574db17-81c7-4c5a-999b-0098aa0b9cda
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f79f686720d615da6996f854a9e4cc18f840337f
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="vendor-portal-user-security"></a>Satıcı portal kullanıcı güvenliği

[!include[banner](../includes/banner.md)]


Bu makale, Satıcı portalını kullanan dış satıcılar için güvenliğin nasıl ayarlanacağını açıklamaktadır. Bu bilgiler, Dynamics AX'in yalnızca Şubat 2016 &amp; Mayıs 2016 sürümleri için geçerlidir.

Satıcı portal işlevi, Dynamics 365 for Operations sürüm 1611'de genişletilmiş satıcı işbirliği işlevleri ile değiştirilmiştir. Satıcı iş birliğini için satıcıların güvenliğinin yapılandırması hakkında daha fazla bilgi için bkz. [Satıcı işbirliğini kurulumu ve bakımı](set-up-maintain-vendor-collaboration.md). Satıcı portal dış satıcı için satın alma siparişleri (PO'lar) hakkında sınırlı bir bilgi kümesini sunar. Satıcılar Dynamics AX yüklemenizdeki ek bilgilere erişimi olmasın diye, Microsoft Dynamics AX'te satıcı portalı için kullanıcı izinlerini doğru ayarlamanız önemlidir. **Önemli:** diğer kullanıcılardan farklı olarak, harici satıcılarda **SystemUser** rolü olmamalıdır. **SystemUser** rolü dış kullanıcılar için uygun olmayan ayrıcalıklar kümesine erişim verir.

## <a name="setting-up-a-vendor-portal-user"></a>Bir tedarikçi portalı kullanıcısı kurma
Tedarikçi portalı kullanan birisi için bir kullanıcı hesabı oluşturmadan önce satıcıyı satıcı portal işbirliği için izin verecek şekilde ayarlamanız gerekir. **satıcılar** sayfasında **genel** sekmesinde **satın alma siparişi işbirliği** alanını seçin. Tedarikçi portalı kullanan harici satıcılarda aşağıdaki Kurulum olması gerekir:

-   Microsoft Azure Active Directory (AAD) kullanıcı hesabı Dynamics AX'de **kullanıcı** sayfasında satıcı üzerinde kayıtlı olması gerekir.
-   Satıcı **(Dış) satıcı** güvenlik rolüne sahip olması gerekir, **SystemUser** rolü değil. **Not:** **SystemUser** rolü Dynamics AX uygulamasında yeni bir kullanıcı hesabı oluşturduğunuzda otomatik olarak verilir. Bu nedenle, bu rolü kaldırmanız ve aldığınız uyarı iletisini kabul etmeniz gerekir.
-   Satıcı kullanıcıya kendi PO görünümüne PO tablolardan ek alanlar eklemek için izni verilmemelidir. **kişiselleştirme** sekmesinde, **kullanıcılar** sekmesinde, kullanıcı için **açık kişiselleştirme izinli** seçeneğini **Hayır** olarak ayarlayın.
-   Kullanıcı hesabı kayıtlı bir ilgili kişi ile ilişkilendirilmiş olması gerekir. **kullanıcı** sayfasında, **Ad** alanında bir kişiyi seçin. Seçtiğiniz kişinin ilgili satıcı için **kişi** rolüne sahip olması gerekir.

Aynı kişi için birden çok satıcı hesapları satıcı portal erişimi gerektiriyorsa (farklı tüzel kişilikler için belki de), o kişinin kullanıcı hesaplarının her birini aynı kayıtlı ilgili kişi ile ilişkilendirilmiş olması gerekir. **(Dış) satıcı** rolü satıcı Portal'da kullanılabilir işlevleri kullanmak için gerekli olan temel özellikleri içerir. Bu kurulum yalnızca amaçlanan senaryoda dış kullanıcının gördüğü kullanıcı arayüzüne odaklanmasına garantilemeye yarar.

<a name="see-also"></a>Ayrıca bkz.
--------

[Satıcı işbirliği](collaborate-vendors-vendor-portal.md)




