---
title: Toplu izlenen maddeler için geliştirilmiş işleme
description: Bu makalede, Microsoft Dynamics 365 Commerce'te ekstre deftere nakil işlemi sırasında toplu izlenen maddeler için geliştirilmiş işleme açıklanmaktadır.
author: josaw1
ms.date: 09/09/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: 10
ms.openlocfilehash: 736ab8dd21f04d7119cca6d53bfeb5e408b8cbd2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881892"
---
# <a name="improved-handling-of-batch-tracked-items"></a>Toplu izlenen maddeler için geliştirilmiş işleme

[!include [banner](includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce'te ekstre deftere nakil işlemi sırasında toplu izlenen maddeler için geliştirilmiş işleme açıklanmaktadır.

Dynamics 365 Commerce satış noktasında (POS), toplu iş numaraları toplu olarak izlenen maddeler için satış sırasında yakalanamaz. Ancak, belirli yapılandırmalarda satışlar Commerce Headquarters'ta müşteri siparişleri veya ekstre deftere nakil işlemi aracılığıyla deftere aktarıldığında, Commerce toplu izlenen maddeler için geçerli toplu iş numaraları olmasını bekler ve bu numaralar faturalama işlemi sırasında kullanılır.

Ürünler için geçerli toplu iş numaraları varsa, müşteri siparişi faturalama işlemi ve ekstre deftere nakil işleminden gerçekleştirilen satış siparişi faturalama işlemi bu numaraları kullanır. Ürünler için geçerli toplu iş numaraları yoksa müşteri siparişi faturalama işlemi deftere nakil gerçekleştiremez ve POS kullanıcısı hata iletisi alır. Ekstre deftere nakil işlemi, ürünler için negatif stok etkinleştirilmiş olsa bile, hata durumuna geçer.

Commerce'ta yapılan geliştirmeler, toplu işle izlenen maddeler için negatif stok etkinleştirildiğinde, stoğun 0 (sıfır) olması veya toplu iş numarasının kullanılabilir olmaması durumunda müşteri siparişi faturalama ve ekstre deftere nakil işlemi aracılığıyla satış siparişi faturalama işleminin engellenmemesini sağlamaya yardımcı olur. Geliştirilen işlev, toplu iş numaraları olmadığında satış satırları için varsayılan bir toplu iş kodu kullanır.

## <a name="define-the-default-batch-id-that-is-used-for-customer-orders"></a>Müşteri siparişleri için kullanılan varsayılan toplu iş kodunu tanımlama

Müşteri siparişleri için kullanılan varsayılan toplu iş kodunu tanımlamamak için aşağıdaki adımları izleyin.

1. Commerce Headquarters'ta **Retail ve Commerce \> Genel merkez kurulumu \> Parametreler \> Commerce parametreleri**'ne gidin.
1. **Müşteri siparişleri** sekmesinde, **Sipariş** hızlı sekmesinde, **Varsayılan toplu iş kodu** alanına bir değer girin.

## <a name="define-the-default-batch-id-that-is-used-for-sales-order-invoicing-through-statement-posting"></a>Ekstre deftere nakil işlemi aracılığıyla satış siparişi faturalama için kullanılan varsayılan toplu iş kodunu tanımlayın

Ekstre deftere nakil işlemi aracılığıyla satış siparişi faturalama için kullanılan varsayılan toplu iş kodunu tanımlamak için aşağıdaki adımları izleyin.

1. Commerce Headquarters'ta **Retail ve Commerce \> Genel merkez kurulumu \> Parametreler \> Commerce parametreleri**'ne gidin.
1. **Deftere nakil** sekmesinde, **Stok güncelleştirme** hızlı sekmesinde, **Varsayılan toplu iş kodu** alanına bir değer girin.

> [!NOTE]
> - Varsayılan toplu iş kodu işlevi yalnızca, belirli mağaza ambarı ve maddeleri için gelişmiş ambarlama etkin olduğunda kullanılabilir. Gelecekteki bir sürümde, varsayılan toplu iş kodu işlevi gelişmiş ambar yönetiminin etkinleştirilmediği senaryolar için de desteklenecektir.
> - Gelişmiş olmayan ambar yönetimi senaryoları için ekstre deftere nakledilirken, toplu işle izlenen maddelerin gelişmiş şekilde işlenmesine yönelik destek Commerce 10.0.5 sürümünde kullanıma sunuldu.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
