---
title: Satıcı portal kullanıcı güvenliği
description: Bu makale, Satıcı portalını kullanan dış satıcılar için güvenliğin nasıl ayarlanacağını açıklamaktadır. Bu bilgiler, Dynamics AX'in yalnızca Şubat 2016 &amp; Mayıs 2016 sürümleri için geçerlidir.
author: mkirknel
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 30231
ms.assetid: 3574db17-81c7-4c5a-999b-0098aa0b9cda
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 72f353448f3b5d1f816bb240a230e26529c9cec3
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207138"
---
# <a name="vendor-portal-user-security"></a>Satıcı portalı kullanıcı güvenliği

[!include [banner](../includes/banner.md)]

Bu makale, Satıcı portalını kullanan dış satıcılar için güvenliğin nasıl ayarlanacağını açıklamaktadır. Bu bilgiler, Dynamics AX'in yalnızca Şubat 2016 &amp; Mayıs 2016 sürümleri için geçerlidir.

Satıcı portal işlevi, Dynamics 365 for Operations sürüm 1611'de genişletilmiş satıcı iş birliği işlevleri ile değiştirilmiştir. Satıcı iş birliğini için satıcıların güvenliğinin yapılandırması hakkında daha fazla bilgi için bkz. [Satıcı iş birliğini kurulumu ve bakımı](set-up-maintain-vendor-collaboration.md). Satıcı portal dış satıcı için satın alma siparişleri (PO'lar) hakkında sınırlı bir bilgi kümesini sunar. Satıcılar Dynamics AX yüklemenizdeki ek bilgilere erişimi olmasın diye, Microsoft Dynamics AX'te satıcı portalı için kullanıcı izinlerini doğru ayarlamanız önemlidir. **Önemli:** diğer kullanıcılardan farklı olarak, harici satıcılarda **SystemUser** rolü olmamalıdır. **SystemUser** rolü dış kullanıcılar için uygun olmayan ayrıcalıklar kümesine erişim verir.

## <a name="setting-up-a-vendor-portal-user"></a>Bir tedarikçi portalı kullanıcısı kurma
Tedarikçi portalı kullanan birisi için bir kullanıcı hesabı oluşturmadan önce satıcıyı satıcı portal iş birliği için izin verecek şekilde ayarlamanız gerekir. **satıcılar** sayfasında **genel** sekmesinde **satın alma siparişi iş birliği** alanını seçin. Tedarikçi portalı kullanan harici satıcılarda aşağıdaki Kurulum olması gerekir:

-   Microsoft Azure Active Directory (AAD) kullanıcı hesabı Dynamics AX'de **Kullanıcılar** sayfasında satıcı üzerinde kayıtlı olması gerekir.
-   Satıcı **(Dış) satıcı** güvenlik rolüne sahip olması gerekir, **SystemUser** rolü değil. **Not:** **SystemUser** rolü Dynamics AX uygulamasında yeni bir kullanıcı hesabı oluşturduğunuzda otomatik olarak verilir. Bu nedenle, bu rolü kaldırmanız ve aldığınız uyarı iletisini kabul etmeniz gerekir.
-   Satıcı kullanıcıya kendi PO görünümüne PO tablolardan ek alanlar eklemek için izni verilmemelidir. **kişiselleştirme** sekmesinde, **kullanıcılar** sekmesinde, kullanıcı için **açık kişiselleştirme izinli** seçeneğini **Hayır** olarak ayarlayın.
-   Kullanıcı hesabı kayıtlı bir ilgili kişi ile ilişkilendirilmiş olması gerekir. **kullanıcı** sayfasında, **Ad** alanında bir kişiyi seçin. Seçtiğiniz kişinin ilgili satıcı için **kişi** rolüne sahip olması gerekir.

Aynı kişi için birden çok satıcı hesapları satıcı portal erişimi gerektiriyorsa (farklı tüzel kişilikler için belki de), o kişinin kullanıcı hesaplarının her birini aynı kayıtlı ilgili kişi ile ilişkilendirilmiş olması gerekir. **(Dış) satıcı** rolü satıcı Portal'da kullanılabilir işlevleri kullanmak için gerekli olan temel özellikleri içerir. Bu kurulum yalnızca amaçlanan senaryoda dış kullanıcının gördüğü kullanıcı arayüzüne odaklanmasına garantilemeye yarar.

<a name="additional-resources"></a>Ek kaynaklar
--------

[Satıcılarla Satıcı portalını kullanarak iş birliği yapın](collaborate-vendors-vendor-portal.md)



