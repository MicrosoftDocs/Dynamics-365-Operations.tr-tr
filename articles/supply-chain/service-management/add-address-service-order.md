---
title: Servis siparişine adres ekleme
description: Bu makale bir servis siparişine nasıl müşteri adresi ekleneceğini açıklar.
author: sorenva
ms.date: 06/15/2020
ms.topic: article
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c485c50bab7c2e945aa0f0fc0601008dcebd3328
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015739"
---
# <a name="add-an-address-to-a-service-order"></a>Servis siparişine adres ekleme

[!include [banner](../includes/banner.md)]

Bu makale bir servis siparişine nasıl müşteri adresi ekleneceğini açıklar. Bir servis siparişi oluşturduğunuzda, adres bilgileri servis siparişinin iliştirildiği projeden transfer edilir. Ancak müşteriler, satıcılar, tesisler, ambarlar, servis siparişleri ve projeler için Microsoft Dynamics AX'e önceden girilmiş adreslerden alternatif bir konum seçebilirsiniz.

Yeni bir adres de oluşturabilirsiniz. Varsayılan olarak, yeni adres projeye transfer edilir. Ancak, yeni adresin yalnızca hizmetin bu örneği için geçerli olduğunu belirtebilirsiniz. Bunu yaparsanız, yeni adres projeye transfer edilmez.

## <a name="create-a-customer-address-for-a-service-order"></a>Servis siparişi için bir müşteri adresi oluşturma

Servis siparişine bir adres eklemek için bu adımları izleyin:

1. **Servis yönetimi** \> **Servis siparişleri** \> **Servis siparişleri**'ne gidin.

1. Bir adres oluşturmak istediğiniz servis siparişini açın.

1. **Üst bilgi** sekmesini açın.

1. **Adres** hızlı sekmesini genişletin ve sonra hızlı sekme araç çubuğundan **Adres ekle**'yi seçin.

1. **Yeni adres** iletişim kutusuna adres için benzersiz bir ad girin ve kalan alanları doldurun. 

    > [!WARNING]
    > Varolan bir adresle aynı adı girerseniz, kalan alanlara girdiğiniz bilgiler varolan adres bilgilerini geçersiz kılar.

1. Yeni adresi servis siparişine kopyalamak için **Tamam**'ı seçin.

## <a name="specify-an-alternative-address-on-a-service-order"></a>Bir servis sipariş siparişinde alternatif bir adres belirtme

Servis siparişine alternatif bir adres eklemek için bu adımları izleyin:

1. **Servis yönetimi** \> **Servis siparişleri** \> **Servis siparişleri**'ne gidin.

1. Alternatif adres girmek istediğiniz servis siparişini açın.

1. **Üst bilgi** sekmesini açın.

1. **Adres** hızlı sekmesini genişletin ve sonra hızlı sekme araç çubuğundan **Diğer adres**'i seçin.

1. **Adres seçimi** iletişim kutusunda, ızgaranın üstündeki açılan listeden **Servis siparişleri**'ni seçin.

1. Bir adres seçin ve bu adresi servis siparişinize kopyalamak için **Tamam**'ı seçin.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]