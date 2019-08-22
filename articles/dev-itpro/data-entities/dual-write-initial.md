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
ms.openlocfilehash: b74bc2d3133af7e87663a4e6bafb8780e0a6a66f
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797310"
---
# <a name="execution-order-for-initial-sychronization-of-finance-and-operations-and-common-data-service"></a>Finance and Operations ve Common Data Service'ın ilk eşzamanlı yürütülmesi için yürütme emri.

Veri tümleştirmesini kullanmadan önce, müşteriler, satıcılar ve kişiler için gereken ilk verileri oluşturmanız gerekir. Örneğin yeni bir **Satıcı grubu** öğesi oluşturmak ve **Ödeme koşulları**'nı **Net30**olarak ayarlamak istiyorsanız **Satıcı grubu** öğesini oluşturmaya çalışmadan önce **Net30**'un hem Finance and Operations'ta hem de Common Data Service'te mevcut olduğundan emin olmalısınız. (Gelecekte **İlk Eşitleme** denilen bir çift yazma platformu işlevselliği yayımlayacağız. Finance and Operations ve Common Data Service arasında tek seferlik veri eşitlemesi ve çift yazma kurulumunun bir parçası olacak.)

İpuçları: **Ödeme Şartları** (Ödeme Koşulları) dahil olmak üzere tüm referans verileri için bir çift yazma haritası yayınlamaktadır. Bir sistemde ilk veri zaten varsa bir kayıtta küçük bir güncelleştirme işlemi bu kayıtta çift yazmayı tetikleyebilir. 

Aşağıdaki öncelik sırasını izlemeniz ve başlangıç verilerinin hem Finance and Operations'ta hem de Common Data Service'te kullanılabilir olduğundan emin olmanız gerekir .   

## <a name="vendor"></a>Satıcı

Satıcı için yürütme sırası şudur:

```
Vendor Group
    Terms of payment
        Payment day & lines
        Payment schedule
Vendor payment method
```

## <a name="customer-organization"></a>Müşteri (Kuruluş)

Müşteri için yürütme sırası şudur:

```
Customer Group
    Terms of payment
        Payment day & lines
        Payment 
Customer payment method
```

## <a name="contact-person"></a>İlgili Kişi (Kişi)

İlgili kişi için yürütme sırası şudur:

```
Customer
Vendor               
```
