---
title: POS oturum açma için Azure Active Directory kimlik doğrulamasını etkinleştirme
description: Bu konu, Microsoft Dynamics 365 Commerce satış noktası (POS) için oturum açma deneyiminin Azure Active Directory kimlik doğrulaması kullanacak şekilde nasıl ayarlanacağını açıklar.
author: boycezhu
manager: annbe
ms.date: 03/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycezhu
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: f030e8382627191dd32d855e15432fc85dca4bbd
ms.sourcegitcommit: 1789a78de1cbeac19d96767812df653a191c67e9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/05/2020
ms.locfileid: "3100392"
---
# <a name="enable-azure-active-directory-authentication-for-pos-sign-in"></a>POS oturum açma için Azure Active Directory kimlik doğrulamasını etkinleştirme
[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Microsoft Dynamics 365 Commerce kullanan çoğu müşteri diğer Microsoft bulut hizmetlerini de kullanır ve bu hizmetler için kullanıcı kimlik bilgilerini yönetmek üzere Azure Active Directory (Azure AD) kullanabilir. Bu gibi durumlarda, müşteriler uygulamalarda aynı Azure AD hesabını kullanmak isteyebilir. Bu konu, Microsoft Commerce satış noktası (POS) oturum açma deneyiminin Azure AD kimlik doğrulaması kullanmak üzere nasıl ayarlanacağını açıklar.

## <a name="configure-azure-ad-authentication"></a>Azure AD kimlik doğrulamasını yapılandırma

Mağaza için POS oturum açma için Azure AD'yi kimlik doğrulama yöntemi olarak kullanılabilir hale getirmek amacıyla, mağazanın işlevsel profilinin ayarlarını yapılandırmanız ve sonra bu ayarı POS istemcisine uygulamanız gerekir.

İşlev profili yapılandırmak için aşağıdaki adımları izleyin.

1. **Perakende ve ticaret** \> **Kanal kurulumu** \> **POS kurulumu** \> **POS profilleri** \> **İşlevsellik profilleri** öğesine tıklayın.
1. Değiştirilecek işlev profilini seçin.
1. **İşlevler** hızlı sekmesinde **POS personeli oturum açma** bölümünde, **Oturum Açma Kimlik Doğrulama Yöntemi** alanının değerini **Personel Kimliği ve Parola** yerine **Azure Active Directory** olarak değiştirin.

Varsayılan olarak, tüm işlev profilleri POS kimlik doğrulama yöntemi olarak **Personel Kimliği ve Parola** kullanır. Bu nedenle, Azure AD kullanmak istiyorsanız **Oturum Açma Kimlik Doğrulama Yöntemi** alanının değerini değiştirmeniz gerekir. Seçilen işlev profiline bağlı her perakende mağazası bu değişiklikten etkilenir.

Ayarları POS istemcilerine uygulamak için, aşağıdaki adımları izleyin.

1. **Retail ve Commerce** \> **Retail ve Commerce BT** \> **Dağıtım planı**'na gidin.
1. **1070** (**Kanal yapılandırması**) dağıtım planını çalıştırın.

> [!NOTE]
> Azure AD kimlik doğrulaması internet bağlantısı gerektirir. POS çevrimdışı moddayken çalışmaz.

## <a name="associate-an-azure-ad-account-with-a-worker"></a>Azure AD hesabını bir çalışanla ilişkilendirme

Bir mağaza çalışanının POS uygulamasında oturum açmak Azure AD hesabını kullanabilmesi için, Azure AD hesabının o çalışanla ilişkilendirilmesi gerekir.

Azure AD hesabını bir çalışanla ilişkilendirmek için, aşağıdaki adımları izleyin.

1. **Retail ve Commerce** \> **Personel** \> **Çalışanlar**'a gidin.
1. Çalışanın ayrıntılar sayfasını açın.
1. Eylem Bölmesinde, **Commerce** sekmesindeki **Harici kimlik** gurubunda **Mevcut kimliği ilişkilendir**'i seçin.
1. **Mevcut harici kimliği kullan** iletişim kutusunda, **E-posta kullanarak ara**'yı seçin, bir Azure AD e-posta adresi girin ve sonra **Ara**'yı seçin.
1. Döndürülen Azure AD hesabını seçin ve ardından **Tamam**'ı seçin.

Çalışanın ayrıntılar sayfasındaki **Commerce** sekmesinde bulunan **Diğer ad**, **UPN** ve **Harici alt kimlik tanımlayıcı** alanları doldurulacaktır.

## <a name="additional-resources"></a>Ek kaynaklar

[MPOS ve Bulut POS için genişletilmiş oturum açma işlevini ayarlama](extended-logon.md)

[Perakende işlevselliği profili oluşturma](retail-functionality-profile.md)

[ Çalışanı yapılandırma](https://docs.microsoft.com/dynamics365/commerce/tasks/worker)
