---
title: Şirketlerarası ticareti ayarlama
description: Bu makalede, şirketlerarası ticaretin nasıl ayarlanacağı açıklanmaktadır
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: CustTable, VendTable, EcoResProductListPage, InterCompanyTradingRelationSetupCustomer
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 8d956c60db9f3acf2f1759dc3e1922da40d8a514
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905645"
---
# <a name="set-up-intercompany-trade"></a>Şirketlerarası ticareti ayarlama

[!include [banner](../../includes/banner.md)]

Şirketlerarası ticareti çalıştırmak için Microsoft Dynamics 365 Supply Chain Management'ı etkinleştirmek üzere müşterileri ve satıcıları ayarlamanız gerekir. Ayrıca Borç hesapları, Alacak hesapları, Tedarik ve kaynak atama ve Satış ve pazarlama'yı da ayarlamanız gerekir.

## <a name="before-you-set-up-intercompany-trade"></a>Şirketlerarası ticareti ayarlamadan önce

Şirketlerarası ticareti ayarlamadan önce hangi müşterilerin şirketlerarası müşteri ve hangi satıcıların şirketlerarası satıcı olduğunu belirlemeniz gerekir. Microsoft Dynamics 365 Supply Chain Management'ta her tüzel kişilik için, belirli şirketlerarası müşteri veya satıcı ile şirketlerarası ticaret ilişkisine hangi ticaret politikasının uygulanacağına karar vermeniz gerekir.

Özellikle, sizin ve kuruluşunuzun şirketlerarası parametreler hakkında bilgi sahibi olmanızı öneririz.

- Her tüzel kişilikte şirketlerarası ticaretten sorumlu yöneticilerle ayarların etkilerini tartışın.
- Her tüzel kişilik için uygun değerleri ayarlayın.

## <a name="set-up-trading-relations"></a>Ticaret ilişkilerini ayarlama

Müşteriler ve satıcılar için şirketlerarası ticareti ayarlamak üzere aşağıdaki adımları izleyin.

1. **Alacak hesapları \> Müşteriler \> Tüm müşteriler**'e gidin.
1. Bir müşteri hesabı seçin.
1. Eylem Bölmesi'ndeki **Genel** sekmesinde, **Şirketlerarası**'nı seçin.
1. Müşteri hesabı için şirketlerarası ayarlama parametrelerini belirtin. Bu parametreler, karşılık gelen satıcının ve satıcı hesabının bulunduğu tüzel kişiliği içerir. Parametreler ayrıca satınalma siparişi politikalarını, satış siparişi politikalarını, değer eşlemesini ve satış sözleşmeleri ve satınalma sözleşmeleri politikalarını içerir. Ayrıca müşteri hesabındaki veya diğer tüzel kişilikte satıcı hesabındaki temel veri değerlerinin kullanılıp kullanılmayacağını da belirtirsiniz.
1. Tüzel kişilikteki kalan şirketlerarası müşteriler için 1'den 4'e kadar adımları yineleyin.
1. **Borç hesapları \> Satıcılar \> Tüm satıcılar**'a gidin.
1. Satıcı hesabı seçin.
1. Eylem Bölmesi'ndeki **Genel** sekmesinde, **Şirketlerarası**'nı seçin.
1. Satıcı hesabı için şirketlerarası ayarlama parametrelerini belirtin. Bu parametreler, karşılık gelen müşterinin ve müşteri hesabının bulunduğu tüzel kişiliği içerir. Parametreler ayrıca satış siparişi politikalarını, satınalma siparişi politikalarını, değer eşlemesini ve satınalma sözleşmeleri ve satış sözleşmeleri politikalarını içerir. Ayrıca satış hesabındaki veya diğer tüzel kişilikte müşteri hesabındaki temel veri değerlerinin kullanılıp kullanılmayacağını da belirtirsiniz.
1. Tüzel kişilikteki kalan şirketlerarası satıcılar için 6'dan 9'a kadar adımları yineleyin.

## <a name="set-up-products"></a>Ürünleri ayarlama

Müşteriler ve satıcılar için şirketlerarası ticareti ayarlamak üzere aşağıdaki adımları izleyin.

1. **Ürün bilgileri yönetimi \> Ürünler \> Tüm ürünler ve ana ürünler**'e gidin.
1. Şirketlerarası ticaret yapmak istediğiniz tüzel kişiliklere serbest bırakılan ürünleri tanımlayın.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
