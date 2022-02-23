---
title: E-posta bildirimi profili ayarlama
description: Bu konuda, Microsoft Dynamics 365 Commerce'ta bir e-posta bildirimi profilinin nasıl oluşturulacağı açıklanmaktadır.
author: samjarawan
manager: annbe
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: c0ab56c15a37313d0a88b1174d5bcf51d391dcec
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416339"
---
# <a name="set-up-an-email-notification-profile"></a>E-posta bildirimi profili ayarlama


[!include [banner](includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce'ta bir e-posta bildirimi profilinin nasıl oluşturulacağı açıklanmaktadır.

## <a name="overview"></a>Genel Bakış

Kanalları oluşturmadan önce, sipariş oluşturma, sipariş sevkiyat durumu ve ödeme hatası gibi çeşitli olaylar için e-posta bildirimleri gönderilebilmesini sağlamak amacıyla bir profil ayarlamanız iyi olacaktır.

E-posta yapılandırma hakkında daha fazla bilgi için bkz. [E-posta yapılandırma ve gönderme](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).

## <a name="create-an-email-notification-profile"></a>E-posta bildirimi profili oluşturma

E-posta bildirim profili oluşturmak için bu adımları izleyin.

1. Gezinti bölmesinde **Modüller \> Retail and commerce \> Headquarters kurulumu \> Commerce E-posta bildirimi profili**'ne gidin.
1. Eylem bölmesinde **Yeni**'ye tıklayın.
1. **E-posta bildirimi profili** alanında, profili tanımlayacak bir ad girin.
1. **Açıklama** alanına ilgili bir açıklama girin.
1. **Etkin** anahtarını **Evet**'e çevirin.

### <a name="create-an-email-template"></a>Bir e-posta şablonu oluştur

Bir e-posta bildirimi oluşturulmadan önce, gönderen e-posta bilgilerini ve e-posta şablonunu içeren bir kuruluş e-postası şablonu oluşturmanız gerekir.

Yeni bir e-posta şablonu oluşturmak için bu adımları izleyin.

1. Gezinti bölmesinde **Modüller \> Retail and commerce \> Headquarters kurulumu \> Parametreler \> Kuruluş e-posta şablonları**'na gidin.
1. Eylem bölmesinde **Yeni**'yi seçin.
1. **E-posta kodu** alanına, bu şablonu tanımaya yardımcı olacak bir kod girin.
1. **Gönderenin adı** alanına, gönderenin adını girin.
1. **E-posta Açıklaması** alanına, anlamlı bir açıklama girin.
1. **Gönderen e-postası** alanına, gönderenin e-posta adresini girin.
1. **Genel** bölümünde, gerekli olan isteğe bağlı bilgileri (örneğin e-posta önceliği) doldurun.
1. **E-posta iletisi içeriği** bölümünü genişletin ve şablon içeriğini oluşturmak için **Yeni**'yi seçin. Her bir içerik öğesi için, dili seçin ve e-posta konu satırını belirtin. E-postanın gövde metni varsa, **Gövde metni var** kutusunun işaretlendiğinden emin olun.
1. Eylem bölmesinde, e-posta gövde şablonu sağlamak için **E-posta iletisi**'ni seçin.

Aşağıdaki resimde bazı örnek e-posta şablonu ayarları gösteriliyor.

![E-posta şablonu ayarları](media/email-template.png)

### <a name="create-an-email-event"></a>Bir e-posta olayı oluşturma

Bir e-posta olayı oluşturmak için bu adımları izleyin.

1. Gezinti bölmesinde **Modüller \> Retail and commerce \> Headquarters kurulumu \> Commerce E-posta bildirimi profili**'ne gidin.
1. Listede, istenen kaydı bulun ve seçin. 
1. **E-posta kodu** açılır listesinden e-posta şablonunu seçin.
1. Açılır listeden uygun **E-posta bildirimi türünü** seçin.
1. **Etkin** onay kutusunu işaretleyin.
1. Eylem bölmesinde, **Kaydet**'i seçin.

Aşağıdaki resimde bazı örnek olay bildirimi ayarları gösteriliyor.

![Olay bildirim ayarları](media/email-notification-profile.png)

### <a name="next-steps"></a>Sonraki adımlar

Posta gönderebilmek için önce giden posta hizmetinizi yapılandırmanız ve bir toplu iş ayarlamanız gerekir. Daha fazla bilgi için bkz. [E-posta yapılandırma ve gönderme](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).


## <a name="additional-resources"></a>Ek kaynaklar

[E-posta yapılandırma ve gönderme](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[Kanallara genel bakış](channels-overview.md)

[Kanal kurulum önkoşulları](channels-prerequisites.md)

[Kuruluşlar ve kuruluş hiyerarşilerine genel bakış](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
