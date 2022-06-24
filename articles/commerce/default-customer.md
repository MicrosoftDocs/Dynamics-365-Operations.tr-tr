---
title: Varsayılan müşteri oluşturma
description: Bu makalede, Microsoft Dynamics 365 Commerce'te bir kanal oluşturulurken kullanılacak bir varsayılan müşterinin nasıl oluşturulacağı açıklanmaktadır.
author: samjarawan
ms.date: 01/27/2020
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
ms.openlocfilehash: b4658356e268d045fcb7065b397411ffc5161864
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894541"
---
# <a name="create-a-default-customer"></a>Varsayılan müşteri oluşturma

[!include [banner](includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce'te bir kanal oluşturulurken kullanılacak bir varsayılan müşterinin nasıl oluşturulacağı açıklanmaktadır.

Bir kanal oluştururken varsayılan bir müşteri sağlamanız gerekir. Müşteri grubu ve müşteri adres defteri oluşturulduktan sonra, varsayılan bir müşteri kolayca oluşturulabilir.

## <a name="create-a-customer-group"></a>Müşteri grubu oluşturma

Henüz müşteri grupları yoksa bir müşteri grubu oluşturabilirsiniz. Bunlar, örneğin, toptan satış, perakende, Internet, Çalışanlar gibi farklı müşteri gruplarını temsil eden gruplar olabilir.

Müşteri grubu oluşturmak için bu adımları izleyin.

1. Gezinti bölmesinde **Modüller \> Perakende ve ticaret \> Müşteriler \> Müşteri grupları**'na gidin.
1. Eylem bölmesinde **Yeni**'yi seçin.
1. **Müşteri grubu** alanına bir müşteri grubu kodu girin.
1. **Açıklama** kutusuna, uygun bir açıklama girin.
1. **Ödeme koşulları** kutusuna, uygun bir değer girin.
1. **Fatura vade tarihi ile ödeme tarihi arasındaki süre** kutusuna, uygun değer girin.
1. **Varsayılan vergi grubu** kutusuna, varsa bir vergi grubu girin.
1. **Fiyatlara satış vergisi dahildir** onay kutusunu (uygunsa) işaretleyin.
1. **Varsayılan silme nedeni** kutusuna, varsa uygun bir değer girin.

Aşağıdaki resimde, yapılandırılmış birkaç müşteri grubu gösteriliyor.

![Müşteri grupları.](media/customer-groups.png)

## <a name="create-a-customer-address-book"></a>Müşteri adres defteri oluşturma

Müşterinin bir adres defteriyle ilişkilendirilmesi gerekir. Henüz oluşturulmadıysa, bir tane oluşturmanız gerekir.

Bir müşteri adres defteri oluşturmak için bu adımları izleyin.

1. Gezinti bölmesinde **Modüller \> Perakende ve ticaret \> Kanal kurulumu \> Adres Defterleri**'ne gidin.
1. Eylem bölmesinde **Yeni**'yi seçin.
1. **Ad** kutusuna bir ad girin.
1. **Açıklama** kutusuna bir açıklama girin.
1. Eylem bölmesinde, **Kaydet**'i seçin.

Aşağıdaki resimde örnek bir adres defteri gösterilmektedir.

![Adres defteri.](media/address-book.png)

## <a name="create-a-default-customer"></a>Varsayılan müşteri oluşturma

Bir varsayılan müşteri oluşturmak için bu adımları izleyin.

1. Gezinti bölmesinde **Modüller \> Perakende ve ticaret \> Müşteriler \> Tüm müşteriler**'e gidin.
1. Eylem bölmesinde **Yeni**'yi seçin.
1. **Tür** açılır listesinde "Kişi"yi seçin.
1. **Müşteri hesabı** açılır listesinde bir hesap numarası seçin veya girin (örneğin "100001").
1. **Ad** açılır listesinde, bir ad seçin veya girin (örneğin "Varsayılan").
1. **İkinci ad** açılır listesinde, bir ad seçin veya girin (örneğin "Perakende").
1. **Soyadı** açılır listesinde, bir ad seçin veya girin (örneğin "Müşteri").
1. **Para birimi** açılır listesinde, bir para birimi seçin veya girin (örneğin "USD").
1. **Para birimi** açılır listesinde, önceden oluşturulan müşteri grubunu seçin.
1. **Adres defterleri** açılır listesinde, varolan bir müşteri adres defterini seçin.
1. Kaydetmek ve yeni müşterinin müşteri ayrıntıları ekranına dönmek için **Kaydet**'i seçin.

> [!NOTE]
> Varsayılan müşteri için bir adres eklemek gerekmez.

Aşağıdaki resimde bir müşteri oluşturma örneği gösteriliyor.

![Varsayılan müşteri oluşturma.](media/default-customer-creation.png)

Aşağıdaki resimde, bir varsayılan müşteri yapılandırması gösteriliyor.

![Örnek müşteri yapılandırması.](media/default-customer-configuration1.png)

Müşteri ayrıntıları ekranındaki varsayılan değerlerin çoğu kalabilir ancak iki değer değiştirilmelidir.

1. Müşteri ayrıntıları ekranında **Satış siparişi varsayılanları**'nı genişletin.
1. **Site** açılır listesinde, önceden yapılandırılmış bir siteyi seçin veya girin.
1. **Ambar** açılır listesinde, önceden yapılandırılmış bir ambarı seçin veya girin.

Aşağıdaki resimde bir müşteri yapılandırma örneği gösteriliyor.

![Örnek müşteri yapılandırması.](media/default-customer-configuration2.png)

## <a name="additional-resources"></a>Ek kaynaklar

[Kanallara genel bakış](channels-overview.md)

[Kanal kurulum önkoşulları](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
