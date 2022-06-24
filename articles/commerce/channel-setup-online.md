---
title: Çevrimiçi kanal ayarlama
description: Bu makalede, Microsoft Dynamics 365 Commerce'te yeni bir çevrimiçi kanalın nasıl oluşturulacağı açıklanmaktadır.
author: samjarawan
ms.date: 02/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: fe137fe0c69a5b9613086c66366b064194b9b6c4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864941"
---
# <a name="set-up-an-online-channel"></a>Çevrimiçi kanal ayarlama

[!include [banner](includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce'te yeni bir çevrimiçi kanalın nasıl oluşturulacağı açıklanmaktadır.

Dynamics 365 Commerce birden fazla perakende kanalı destekler. Bu perakende kanalları çevrimiçi mağazaları, çağrı merkezlerini ve perakende mağazalarını (tuğla dibek mağazalar olarak da bilinir) içerir. Çevrimiçi mağazalar müşterilere perakendecinin perakende mağazalarının yanı sıra çevrimiçi mağazasından da ürün satın alma seçeneği verir.

Commerce'te bir çevrimiçi mağaza oluşturmak için önce bir çevrimiçi kanal oluşturmanız gerekir. Yeni bir çevrimiçi kanal oluşturmadan önce [Kanal kurulumu önkoşullarını](channels-prerequisites.md) tamamladığınızdan emin olun.

Yeni bir site oluşturabilmeniz için, Commerce'te en az bir çevrimiçi mağazanın oluşturulması gereklidir. Daha fazla bilgi için, bkz [e-ticaret sitesi oluşturma](create-ecommerce-site.md).

## <a name="create-and-configure-a-new-online-channel"></a>Yeni bir çevrimiçi kanal oluşturma ve yapılandırma

Yeni bir çevrimiçi kanal oluşturmak ve yapılandırmak için bu adımları izleyin.

1. Gezinti bölmesinde **Modüller \> Kanallar \> Çevrimiçi Mağazalar**'a gidin.
1. Eylem bölmesinde **Yeni**'yi seçin.
1. **Ad** alanına yeni kanal için bir ad girin.
1. **Tüzel kişilik** açılır listesinde, uygun tüzel kişiliği girin.
1. **Ambar** açılır listesinde, ilgili ambarı girin.
1. **Mağaza saati dilimi** alanında, ilgili saat dilimini seçin.
1. **Para birimi** alanında uygun para birimini seçin.
1. **Varsayılan müşteri** alanında, geçerli bir varsayılan müşteri girin.
1. **Müşteri adres defteri** alanında, geçerli bir adres defteri girin.
1. **İşlevsellik profili** alanında, varsa bir işlevsellik profili seçin.
1. **E-posta bildirimi profili** alanında, geçerli bir e-posta bildirimi profili girin.
1. Eylem bölmesinde, **Kaydet**'i seçin.

Aşağıdaki resimde yeni bir çevrimiçi kanalın oluşturulması gösteriliyor.

![Yeni çevrimiçi kanal.](media/channel-setup-online-1.png)

Aşağıdaki resimde örnek bir çevrimiçi kanal gösteriliyor.

![Örnek çevrimiçi kanal.](media/channel-setup-online-2.png)

## <a name="assign-the-channel-to-a-commerce-scale-unit"></a>Kanalı Commerce Scale Unit'e atama

Yeni kanalınızın bir Commerce Scale Unit'e atanmış olması gerekir. Talimatlar için bkz. [Commerce Scale Unit'i kullanacak kanalları yapılandırma](../fin-ops-core/dev-itpro/deployment/initialize-retail-channels.md#configure-channels-to-use-commerce-scale-unit).

## <a name="set-up-languages"></a>Dilleri ayarlama

E-ticaret siteniz birden çok dili destekleyecekse **Diller** bölümünü genişletin ve gereken dilleri ekleyin.

## <a name="set-up-payment-account"></a>Ödeme hesabını ayarlama

**Ödeme hesabı** bölümünün içinden, üçüncü taraf ödeme sağlayıcı ekleyebilirsiniz. Adyen ödeme bağlayıcısı ayarlama hakkında bilgi için bkz. [Adyen için Dynamics 365 Ödeme Bağlayıcı](./dev-itpro/adyen-connector.md).

## <a name="additional-channel-setup"></a>Ek kanal ayarları

Çevrimiçi kanal kurulumu için gereken ek görevler ödeme yöntemleri, teslimat şekilleri ve karşılama grubu ataması ayarlamayı içerir.

Aşağıdaki resimde, **Ayarla** sekmesindeki **Teslimat şekilleri**, **Ödeme yöntemleri** ve **Karşılama grubu ataması** ayarlama seçenekleri gösteriliyor.

![Ek çevrimiçi kanal kurulumu eylemleri.](media/channel-setup-online-3.png)

### <a name="set-up-payment-methods"></a>Ödeme yöntemlerini ayarlama

Ödeme yöntemlerini ayarlamak için, bu kanalda desteklenen her ödeme türü için bu adımları izleyin.

1. Eylem bölmesinde, **Ayarla** sekmesini ve ardından **Ödeme yöntemleri**'ni seçin.
1. Eylem bölmesinde **Yeni**'yi seçin.
1. Gezinti bölmesinde, istediğiniz bir ödeme yöntemini seçin.
1. **Genel** bölümünde bir **İşlem adı** belirtin ve istediğiniz diğer ayarları yapılandırın.
1. Ödeme türü için gereken ek ayarları yapılandırın.
1. Eylem bölmesinde, **Kaydet**'i seçin.

Aşağıdaki resimde bir nakit ödeme yöntemi örneği gösteriliyor.

![Örnek ödeme yöntemleri.](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a>Teslimat şekillerini ayarla

Yapılandırılan teslimat şekillerini, **Eylem bölmesindeki** **Ayarla** sekmesinden **Teslimat şekilleri**'ni seçerek görebilirsiniz.  

Bir teslimat şekli eklemek veya değiştirmek için bu adımları izleyin.

1. Gezinti bölmesinde **Modüller \> Stok yönetimi \> Teslimat şekilleri**'ne gidin.
1. Eylem bölmesinde, yeni bir teslimat şekli oluşturmak için **Yeni**'yi seçin veya varolan bir şekli seçin.
1. **Perakende kanalları** bölümünde, kanalı eklemek için **Satır ekle**'yi seçin. Kanalları tek tek eklemek yerine kuruluş düğümleri kullanarak eklemek, kanal eklemeyi kolaylaştırabilir.

Aşağıdaki resimde bir teslimat şekli örneği gösteriliyor.

![Teslimat şekillerini ayarla.](media/channel-setup-retail-7.png)

### <a name="set-up-a-fulfillment-group-assignment"></a>Karşılama grubu atamasını ayarlama

Bir karşılama grubu ataması ayarlamak için bu adımları izleyin.

1. Eylem bölmesinde, **Ayarla** sekmesini ve ardından **Karşılama grubu ataması**'nı seçin.
1. Eylem bölmesinde **Yeni**'yi seçin.
1. **Karşılama grubu** açılır listesinde bir karşılama grubu seçin.
1. **Açıklama** açılır listesinde bir açıklama girin.
1. Eylem bölmesinde, **Kaydet**'i seçin.

Aşağıdaki resimde, bir karşılama grubu ataması kurulum örneği gösterilmektedir.

![Karşılama grubu atamasını ayarlama.](media/channel-setup-retail-9.png)

## <a name="additional-resources"></a>Ek kaynaklar

[Kanallara genel bakış](channels-overview.md)

[Kanal kurulum önkoşulları](channels-prerequisites.md)

[Perakende kanalını ayarlama](channel-setup-retail.md)

[Çağrı merkezi kanalını ayarlama](channel-setup-callcenter.md)

[Adyen için Dynamics 365 Ödeme Bağlayıcısı](./dev-itpro/adyen-connector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
