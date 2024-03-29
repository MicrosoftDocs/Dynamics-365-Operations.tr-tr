---
title: E-posta bildirimi profili ayarlama
description: Bu makalede, Microsoft Dynamics 365 Commerce'ta bir e-posta bildirimi profilinin nasıl oluşturulacağı açıklanmaktadır.
author: bicyclingfool
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: db6c46d471e3b54982132df3e4819236833cf4a8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292148"
---
# <a name="set-up-an-email-notification-profile"></a>E-posta bildirimi profili ayarlama

[!include [banner](includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce'ta bir e-posta bildirimi profilinin nasıl oluşturulacağı açıklanmaktadır.

Kanalları oluştururken, bir e-posta bildirim profili ayarlayabilirsiniz. E-posta bildirim profili, müşterilerinize bildirim göndereceğiniz satış hareketini (sipariş oluşturuldu, sipariş hazırlandı ve sipariş faturalandı gibi etkinlikler) tanımlar. 

E-posta yapılandırma hakkında daha fazla bilgi için bkz. [E-posta yapılandırma ve gönderme](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).



## <a name="create-an-email-template"></a>Bir e-posta şablonu oluştur

Desteklemek istediğiniz her bildirim türü için bir e-posta bildirim türünü etkinleştirmeden önce, Commerce genel merkezinde bir kuruluş e-posta şablonu oluşturmanız gerekir. Bu şablon, desteklenen her bir dil için e-posta konusu, gönderen, varsayılan dil ve e-posta gövdesini tanımlar.

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

![E-posta şablonu ayarları.](media/email-template.png)

E-posta şablonlarının nasıl oluşturulacağı hakkında bilgi için bkz. [İşlem olayları için e-posta şablonları oluşturma](email-templates-transactions.md). 

## <a name="create-an-email-notification-profile"></a>E-posta bildirimi profili oluşturma

Headquarters'da e-posta bildirim profili oluşturmak için bu adımları izleyin.

1. Gezinti bölmesinde **Modüller \> Retail and commerce \> Headquarters kurulumu \> Commerce E-posta bildirimi profili**'ne gidin.
1. Eylem bölmesinde **Yeni**'yi seçin.
1. **E-posta bildirimi profili** alanında, profili tanımlayacak bir ad girin.
1. **Açıklama** alanına ilgili bir açıklama girin.
1. **Etkin** anahtarını **Evet**'e çevirin.

## <a name="add-a-notification-type"></a>Bildirim türü ekleme

Bir e-posta olayı oluşturmak için bu adımları izleyin.

1. Gezinti bölmesinde **Modüller \> Retail and commerce \> Headquarters kurulumu \> Commerce E-posta bildirimi profili**'ne gidin.
1. **Perakende e-posta bildirim ayarları** altında **Yeni**'yi seçin.
1. Açılır listeden uygun **E-posta bildirimi türünü** seçin.
1. Yukarıda **E-posta Kimliği** açılır listesinden oluşturduğunuz e-posta şablonunu seçin.
1. **Etkin** onay kutusunu işaretleyin.
1. Eylem bölmesinde, **Kaydet**'i seçin.

Aşağıdaki resimde bazı örnek olay bildirimi ayarları gösteriliyor.

![Olay bildirim ayarları.](media/email-notification-profile.png)


## <a name="schedule-a-recurring-email-notification-process-job"></a>Yinelenen e-posta bildirim işlemi işi zamanla

E-posta bildirimleri göndermek için **Perakende sipariş e-posta bildirimini işle** işinin çalışıyor olması gerekir.

İşlem tabanlı e-postaları göndermek üzere Headquarters'da bir toplu iş ayarlamak için aşağıdaki adımları izleyin.

1. **Retail ve Commerce \> Retail ve Commerce BT \> E-posta ve bildirimler \> E-posta bildirimi gönder**'e gidin.
1. **Perakende sipariş e-posta bildirimini işle** iletişim kutusunda **Yineleme**'yi seçin.
1. **Yinelemeyi tanımla** iletişim kutusunda **Bitiş tarihi yok**'u seçin.
1. **Yinelenme düzeni** altında **Dakika**'yı seçin ve sonra **Sayı** alanını **1** olarak ayarlayın. Bu ayarlar, e-posta bildirimlerinin olabildiğince çabuk şekilde işlenmesini sağlar.
1. **Perakende sipariş e-posta bildirimini işle** iletişim kutusuna dönmek için **Tamam**'ı seçin.
1. İş kurulumunu tamamlamak için **Tamam**'ı seçin.

## <a name="next-steps"></a>Sonraki adımlar

E-posta gönderebilmek için önce giden posta hizmetinizi yapılandırmanız gerekir. Daha fazla bilgi için bkz. [E-posta yapılandırma ve gönderme](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).

## <a name="additional-resources"></a>Ek kaynaklar

[E-posta yapılandırma ve gönderme](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[Kanallara genel bakış](channels-overview.md)

[Kanal kurulum önkoşulları](channels-prerequisites.md)

[Kuruluşlar ve kuruluş hiyerarşilerine genel bakış](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
