---
title: Servis siparişine adres ekleme
description: Bu konu bir servis siparişine nasıl müşteri adresi ekleneceğini açıklar.
author: ShylaThompson
ms.date: 05/02/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 55af2de689c70ca5041bb7bf5d0b7c199ae19384472ac96eb922df80f77150b3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6761008"
---
# <a name="add-an-address-to-a-service-order"></a>Servis siparişine adres ekleme    

[!include [banner](../includes/banner.md)]


Bu konu bir servis siparişine nasıl müşteri adresi ekleneceğini açıklar. Bir servis siparişi oluşturduğunuzda, adres bilgileri servis siparişinin iliştirildiği projeden transfer edilir. Ancak müşteriler, satıcılar, tesisler, ambarlar, servis siparişleri ve projeler için Microsoft Dynamics AX'e önceden girilmiş adreslerden alternatif bir konum seçebilirsiniz.

Yeni bir adres de oluşturabilirsiniz. Varsayılan olarak, yeni adres projeye transfer edilir. Ancak, yeni adresin yalnızca hizmetin bu örneği için geçerli olduğunu belirtebilirsiniz. Bunu yaparsanız, yeni adres projeye transfer edilmez.

## <a name="create-a-customer-address-for-a-service-order"></a>Servis siparişi için bir müşteri adresi oluşturma

Servis siparişine bir adres eklemek için bu adımları izleyin:

1.  **Servis yönetimi** \> **Ortak** \> **Servis siparişleri** \> **Servis siparişleri**'ne tıklayın.

2.  Bir adres oluşturmak istediğiniz servis siparişini açın.

3.  **Eylem Bölmesinde** **Düzenle**'ye ve ardından **Başlık görünümü**'ne tıklayın.

4.  **Adres** hızlı sekmesinde **Adres ekle**'ye tıklayın.

5.  **Yeni adres** formuna, adres için benzersiz bir ad girin ve kalan alanları doldurun. 
    

    > [!WARNING]
    > <P>Varolan bir adresle aynı adı girerseniz, kalan alanlara girdiğiniz bilgiler varolan adres bilgilerini geçersiz kılar.</P>


6.  Yeni adresi servis siparişine kopyalamak için **Tamam**'a tıklayın.

## <a name="specify-an-alternative-address-on-a-service-order"></a>Bir servis sipariş siparişinde alternatif bir adres belirtme

Servis siparişine alternatif bir adres eklemek için bu adımları izleyin:

1.  **Servis yönetimi** \> **Ortak** \> **Servis siparişleri** \> **Servis siparişleri**'ne tıklayın.

2.  Alternatif adres girmek istediğiniz servis siparişini açın.

3.  **Eylem Bölmesinde** **Düzenle**'ye ve ardından **Başlık görünümü**'ne tıklayın.

4.  **Adres** hızlı sekmesinde **Diğer adresler**'e tıklayın.

5.  **Adres seçimi** formunda **Kayıt türü** alanında **Servis siparişleri**'ni seçin.

6.  Bir adres seçin ve servis siparişine kopyalamak için **Tamam**'a tıklayın.


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]