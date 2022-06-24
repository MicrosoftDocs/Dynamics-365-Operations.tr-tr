---
title: Bağlantılı ödemeler ayarlama ve işleme
description: Bu makale, bağlantılı müşteri ödemelerinin nasıl ayarlanacağını ve işleneceğini açıklar. Bir bağlantılı ödeme, iki adımda genel muhasebeye nakledilen bir ödemedir.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPaymMode, VendPaymMode, LedgerJournalTable, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, LedgerJournalTransDaily
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4f0609e333fb16ba189b6a971f88fbb5bf900fec
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887991"
---
# <a name="set-up-and-process-bridged-payments"></a>Bağlantılı ödemeler ayarlama ve işleme

[!include [banner](../includes/banner.md)]

Bir bağlantılı ödeme, iki adımda genel muhasebeye nakledilen bir ödemedir. Genellikle, ödeme yöntemi **Banka** olarak ayarlandığında bu yaklaşım kullanılır. Hareketleri yalnızca hareket bankada onaylandıktan sonra banka hesabına nakletmelisiniz. Ancak, bunu bir genel muhasebe hesabı için de kullanabilirsiniz. Bu durumda, bağlantı deftere nakli işlendiğinde sistem bu tutarı bir ana hesaptan başka bir ana hesaba taşır.

Borç hesaplarından veya Alacak hesaplarından bağlantılı ödemeler oluşturabilirsiniz. Bu makale, Alacak hesapları için bağlantı deftere naklini yapılandırma işlemini açıklar ancak Borç hesapları hareketleri için adımlar benzerdir.

## <a name="set-up-bridging-posting"></a>Bağlantı deftere naklini ayarlama

Bağlantı deftere naklini kullanmak için, **Bağlantı deftere nakil** yöntemini kullanacak şekilde bir veya daha fazla ödeme yöntemi ayarlamanız gerekir. Bir bağlantı hesabı seçmelisiniz.

1. **Alacak hesapları &gt; Ödeme kurulumu &gt; Ödeme yöntemi** seçeneğine gidin.
2. Bağlantı deftere nakletmeyi etkinleştirmek için mevcut bir ödeme yöntemi seçin. Alternatif olarak yeni bir ödeme yöntemi oluşturabilirsiniz.
3. **Bağlantılı deftere nakletme** onay kutusunu seçin.
4. **Bağlantı hesabı** alanında, ödemelerin banka hesabında temizlenmeleri için deftere nakledileceği ana hesabı seçin.
5. Sayfayı kapatın.

## <a name="process-and-transfer-bridging-posting"></a>Bağlantı deftere naklini işleme ve transfer etme

Bağlantı deftere nakli oluşturmak ve işlemek için aşağıdaki adımları izleyin.

1. **Alacak hesapları &gt; Ödemeler &gt; Müşteri ödeme günlüğü** seçeneğine gidin.
2. Bir günlük oluşturmak için **Yeni**'yi seçin.
3. **Ad** alanına, bir ad seçin.
4. Müşteri ödeme günlüğüne satırlar ekleyin ve bağlantı nakli için konfigüre edilen ödeme yöntemini seçin.
5. Günlüğü deftere nakledin. Hareketler, önceki yordamdaki **Bağlantı hesabı** alanında seçtiğiniz ana hesaba nakledilir.

Hareketler bankada onaylandığında ve bağlantı hesabından ödeme yöntemi için belirtilen ödeme hesabına transfer edilmek istendiğinde, aşağıdaki adımları izleyin.

1. **Genel muhasebe &gt; Günlük girişleri &gt; Genel günlükler**.
2. Bir günlük oluşturmak için **Yeni**'yi seçin.
3. **Ad** alanına, bir ad seçin.
4. Günlük ayrıntılarını açmak için **Satırları** seçin.
5. **İşlevler &gt; Bağlantı hareketlerini seçin**'i belirleyin.
6. Temizlenen her ödemeyi işaretleyin ve **Kabul et**'i seçin.
7. Günlüğü deftere nakledin.
