---
title: Şirketlerarası ticaret için satıcıları, müşterileri ve maddeleri ayarlama
description: Bu konuda, şirketlerarası ticaret için satıcıların, müşterilerin ve maddelerin nasıl ayarlanacağı açıklanmaktadır
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: CustTable, VendTable, EcoResProductListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 4c928435a4e66832b09dbc805664934cfb1236be
ms.sourcegitcommit: b666289f5113d0a3fa2220fe337d5aacf07cbd92
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/08/2022
ms.locfileid: "8945769"
---
# <a name="set-up-vendors-customers-and-items-for-intercompany-trade"></a>Şirketlerarası ticaret için satıcıları, müşterileri ve maddeleri ayarlama

[!include [banner](../../includes/banner.md)]

Kuruluşunuzu şirketlerarası ticarete hazırlamak için ticaret yapacağınız satıcıları ve müşterileri dahili olarak tanımlamanız gerekir. Daha sonra bu satıcıları ve müşterileri, satın alacağınız veya satacağınız ürünlerle ilişkilendirmeniz gerekir.

1. **Tedarik ve kaynak \> Satıcılar \> Tüm satıcılar**'a gidin.
1. Şirketlerarası satıcı olarak tanımlanacak satıcıyı seçin.
1. Eylem Bölmesi'ndeki **Genel** sekmesinde, **Şirketlerarası**'nı seçin.
1. Satıcı hesabı için şirketlerarası ayarlama parametrelerini belirtin. Bu parametreler, müşteri tüzel kişiliği ve hesabını, satış siparişi ilkelerini, satın alma siparişi ilkelerini, değer eşleme ve satın alma sözleşmesini ve satış sözleşmesi ilkelerini içerir. Ayrıca satış hesabındaki veya diğer tüzel kişilikte müşteri hesabındaki temel veri değerlerinin kullanılıp kullanılmayacağını da belirtirsiniz.
1. **Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.
1. **Serbest bırakılan ürünler** liste sayfasında, satıcıya atanacak maddeleri seçin; böylece maddeler şirketlerarası ticaret için kullanılabilir. Her madde için **Serbest bırakılan ürün ayrıntıları** sayfasını açın. **Satın alma** sekmesindeki **Satıcı** alanına satıcı numarasını yazın.
1. **Alacak hesapları \> Müşteriler \> Tüm müşteriler**'e gidin.
1. Şirketlerarası müşteri olarak tanımlanacak müşteriyi seçin.
1. Eylem Bölmesi'ndeki **Genel** sekmesinde, **Şirketlerarası**'nı seçin.
1. Müşteri hesabı için şirketlerarası ayarlama parametrelerini belirtin. Bu parametreler, satıcı tüzel kişiliği ve hesabı, satın alma siparişi ilkeleri, satış siparişi ilkeleri, değer eşleme ve satış sözleşmesi ve satın alma sözleşmesi ilkelerini içerir. Ayrıca müşteri hesabındaki veya diğer tüzel kişilikte satıcı hesabındaki temel veri değerlerinin kullanılıp kullanılmayacağını da belirtirsiniz.
1. Şirketlerarası parametreleri ayarlamayı bitirdiğinizde, seçilen müşteri ayrıntılarına dönmek için **Şirketlerarası** sayfasını kapatın.
1. **Çeşitli ayrıntılar** hızlı sekmesini genişletin ve **Şirketlerarası siparişleri oluştur**'u *Evet* olarak ayarlayın. Siparişlerin doğrudan müşterilere teslim edilmesini istiyorsanız **Doğrudan teslimat** onay kutusunu da *Evet* olarak ayarlayın.

    > [!NOTE]
    > Kuruluşunuzun stokladığı ve müşterilere teslim ettiği bazı maddeler varsa ürün stokta olsa bile şirketlerarası siparişleri otomatik olarak oluşturmak istemeyebilirsiniz. Bazen stokta bulunabilecek maddeler için otomatik sipariş oluşturmayı devre dışı bırakmak üzere **Şirketlerarası siparişler oluştur** onay kutusunun *Hayır* olarak ayarlayın.

1. Satış siparişinde dolaylı olarak fazladan satır oluşturulmasına izin vermek istiyorsanız **Dolaylı sipariş satırları oluştur** onay kutusunu *Evet* olarak ayarlayın. Kullanıcı daha sonra şirketlerarası satış siparişinden özgün satış siparişine satırlar ekleyebilir.

> [!WARNING]
> Sipariş satırlarının dolaylı olarak oluşturulmasına izin verirseniz şirketlerarası satış siparişinden özgün satış siparişine yapılan tüm eklemelere izin vermiş olursunuz. Her ekleme daha sonra müşteriye işlenir ve siparişe ve faturaya eklenir. Ayrıca, satışa dahil olan her belge otomatik olarak yazdırılır ve deftere nakledilir. Kullanıcılar, ekleme hakkında uyarılmaz.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
