---
title: Finance and Operations ve Common Data Service'ın ilk eşzamanlı yürütülmesi için yürütme emri.
description: Bu konu, ilk verileri oluşturmak için izlemeniz gereken eşitleme sırasını belirtir.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 1473c3bad55734d5f83ee3e4c1654921b872f3bb
ms.sourcegitcommit: 3f05ede8b8acdf0550240a83a013e093b4ad043d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2019
ms.locfileid: "1873140"
---
# <a name="execution-order-for-initial-synchronization-of-finance-and-operations-and-common-data-service"></a>Finance and Operations ve Common Data Service'ın ilk eşzamanlı yürütülmesi için yürütme emri.

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Veri tümleştirmesini kullanmadan önce, müşteriler, satıcılar ve kişiler için gereken ilk verileri oluşturmanız gerekir. Örneğin, yeni bir **Satıcı grubu** maddesi oluşturmak ve **Ödeme şartları** değerini **Net30**olarak ayarlamak istiyorsunuz. Bu durumda, **Satıcı grup** maddesini oluşturmaya çalışmadan önce **Net30**'un Microsoft Dynamics 365 for Finance and Operations ve Common Data Service'in her ikisinde de bulunduğundan emin olmalısınız. (Gelecekte Microsoft İlk Eşitleme denilen bir çift yazma platformu işlevselliği yayımlayacak. Finance and Operations ve Common Data Service arasında tek seferlik veri eşitlemesi ve çift yazma kurulumunun bir parçası olacak.)

> [!TIP]
> Microsoft **Ödeme Şartları** (Ödeme Koşulları) dahil olmak üzere tüm referans verileri için bir çift yazma haritası yayımlamaktadır. Bir sistemde ilk veri zaten varsa bir kayıtta küçük bir güncelleştirme işlemi bu kayıtta çift yazmayı tetikleyebilir.

Aşağıdaki öncelik sırasını izlemeniz ve başlangıç verilerinin hem Finance and Operations'ta hem de Common Data Service'te kullanılabilir olduğundan emin olmanız gerekir .

## <a name="vendor"></a>Satıcı

İşte **Satıcı** varlığı için yürütme sırası:

1. Satıcı grubu

    1. Ödeme koşulları

        1. Ödeme günü ve satırlar
        2. Ödeme planı

2. Satıcı ödeme yöntemi

## <a name="customer-organization"></a>Müşteri (Kuruluş)

İşte **Müşteri** varlığı için yürütme sırası:

1. Müşteri grubu

    1. Ödeme koşulları

        1. Ödeme günü ve satırlar
        2. Ödeme 

2. Müşteri ödeme yöntemi

## <a name="contact-person"></a>İlgili Kişi (Kişi)

İşte **İlgili kişi** varlığı için yürütme sırası:

1. Müşteri
2. Satıcı
