---
title: E-posta bildirimi profili ayarlama
description: Bu konuda, Microsoft Dynamics 365 Commerce'ta bir e-posta bildirimi profilinin nasıl oluşturulacağı açıklanmaktadır.
author: bicyclingfool
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 7504b2b36f6869f90de196bf32c09e7bdd51e7b5
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792669"
---
# <a name="set-up-an-email-notification-profile"></a>E-posta bildirimi profili ayarlama

[!include [banner](includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce'ta bir e-posta bildirimi profilinin nasıl oluşturulacağı açıklanmaktadır.

Kanalları oluştururken, bir e-posta bildirim profili ayarlayabilirsiniz. Bu şekilde, sipariş oluşturma, sipariş Sevkiyat durumu ve ödeme hatası gibi çeşitli işlem olayları için müşterilere e-postalar gönderilebilir.

E-posta yapılandırma hakkında daha fazla bilgi için bkz. [E-posta yapılandırma ve gönderme](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).

## <a name="create-an-email-notification-profile"></a>E-posta bildirimi profili oluşturma

E-posta bildirim profili oluşturmak için bu adımları izleyin.

1. Gezinti bölmesinde **Modüller \> Retail and commerce \> Headquarters kurulumu \> Commerce E-posta bildirimi profili**'ne gidin.
1. Eylem bölmesinde **Yeni**'ye tıklayın.
1. **E-posta bildirimi profili** alanında, profili tanımlayacak bir ad girin.
1. **Açıklama** alanına ilgili bir açıklama girin.
1. **Etkin** anahtarını **Evet**'e çevirin.

### <a name="create-an-email-template"></a>Bir e-posta şablonu oluştur

Bir e-posta bildirim türünü etkinleştirmeden önce, Commerce genel merkezinde bir kuruluş e-posta şablonu oluşturmanız gerekir. Bu şablon, desteklemek istediğiniz her bir dil için e-posta konusu, gönderen, varsayılan dil ve e-posta gövdesini tanımlar.

Yeni bir e-posta şablonu oluşturmak için bu adımları izleyin.

1. Gezinti bölmesinde **Modüller \> Retail and commerce \> Headquarters kurulumu \> Parametreler \> Kuruluş e-posta şablonları**'na gidin.
1. Eylem bölmesinde **Yeni**'yi seçin.
1. **E-posta kodu** alanına, bu şablonu tanımaya yardımcı olacak bir kod girin.
1. **Gönderenin adı** alanına, gönderenin adını girin.
1. **E-posta Açıklaması** alanına, anlamlı bir açıklama girin.
1. **Gönderen e-postası** alanına, gönderenin e-posta adresini girin.
1. **Genel** bölümünde, e-posta şablonu için varsayılan dili seçin. Belirtilen dil için yerelleştirilmiş şablon yoksa, varsayılan dil kullanılır.
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
