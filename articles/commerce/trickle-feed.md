---
title: Perakende mağaza hareketleri için kademeli akış tabanlı sipariş oluşturma
description: Bu makalede, Microsoft Dynamics 365 Commerce'te mağaza hareketleri için kademeli akış tabanlı sipariş oluşturma işlemi açıklanmaktadır.
author: analpert
ms.date: 01/11/2021
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
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0f0ee361df8c565761e79f5b0ecf519c149f2ec0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873264"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions"></a>Perakende mağaza hareketleri için kademeli akış tabanlı sipariş oluşturma

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Commerce sürüm 10.0.5 ve sonraki sürümlerde, tüm ekstre deftere nakil işlemlerini, kademeli akış tabanlı ekstre deftere nakil işlemlerine geçirmenizi öneririz. Önemli performans ve iş avantajları, kademeli akış işlevini kullanmayla ilişkilidir. Satış hareketleri gün içinde işlenir. Ödeme ve nakit yönetimi hareketleri gün sonunda mali tablolara işlenir. Kademeli akış işlevi; satış siparişlerinin, faturaların ve ödemelerin sürekli işlenmesini sağlar. Bu nedenle stok, gelir ve ödemeler gerçek zamanlıya yakın olarak güncelleştirilip kabul edilir.

## <a name="use-trickle-feed-based-posting"></a>Kademeli akış tabanlı deftere nakil özelliğini kullanma

> [!IMPORTANT]
> Kademeli akış tabanlı deftere nakil özelliğini etkinleştirmeden önce, hesaplanmış ve deftere nakledilmemiş ekstreler bulunmadığından emin olmanız gerekir. Bu özelliği etkinleştirmeden önce tüm ekstreleri deftere nakledin. **Mağaza mali öğeleri** çalışma alanında, açık ekstreleri denetleyebilirsiniz.

Perakende hareketlerinin akış tabanlı deftere nakil özelliğini etkinleştirmek için **Özellik yönetimi** çalışma alanında, **Perakende ekstreleri - Kademeli akış** özelliğini etkinleştirin. Ekstreler iki türe ayrılır: hareket ekstreleri ve mali tablolar.

### <a name="transactional-statements"></a>Hareket ekstreleri

Hareket ekstresi işlemenin gün içinde yüksek bir sıklıkta çalıştırılması amaçlanır, böylece hareketler Commerce genel merkezine yüklendiğinde belgeler oluşturulur. **P İşi**'ni çalıştırdığınızda hareketler mağazalardan Commerce genel merkezine yüklenir. Ayrıca hareket ekstresi tarafından alınmaları için hareketleri doğrulamak üzere **Mağaza hareketlerini doğrula** işini çalıştırmanız gerekir.

Aşağıdaki işleri yüksek sıklıkta çalıştırılacak şekilde zamanlayın:

- Hareket ekstresini hesaplamak için **Hareket ekstrelerini toplu işle hesapla** işini çalıştırın (**Retail ve Commerce \> Retail ve Commerce BT \> POS Deftere nakli \> Hareket ekstrelerini toplu işle hesapla**). Bu iş, deftere nakledilmemiş ve doğrulanmış tüm hareketleri alır ve bunları yeni bir hareket ekstresine ekler.
- Hareket ekstrelerini toplu işle deftere nakletmek için **Hareket ekstrelerini toplu işle deftere naklet** işini çalıştırın (**Retail ve Commerce \> Retail ve Commerce BT \> POS Deftere nakli \> Hareket ekstrelerini toplu işle deftere naklet**). Bu iş, deftere nakil işlemini çalıştırır ve herhangi bir hata içermeyen deftere nakledilmemiş ekstreler için satış siparişleri, satış faturaları, ödeme günlükleri, iskonto günlükleri ve gelir-gider hareketleri oluşturur. 

### <a name="financial-statements"></a>Mali tablolar

Mali tablo işleme, gün sonu işlemi olacak şekilde tasarlanmıştır. Bu tür ekstre işleme yalnızca **Vardiya** kapatma yöntemini destekler ve yalnızca kapalı vardiyaları alır. Ekstreler, mali mutabakatla sınırlıdır. Yalnızca ödemeler için sayılan tutar ile hareket tutarı arasındaki tutar farklarına yönelik günlükleri ve diğer nakit yönetimi hareketlerine ilişkin günlükleri oluşturur.

Mali tablolar ayrıca şu hareketlerin incelenmesine de olanak tanır: kasa sayımı hareketleri, ödeme hareketleri, bankaya nakledilen ödeme hareketleri ve kasa ödemesi hareketleri. Ödeme ayrıntıları sayfası yalnızca bir mali tablo seçildiğinde görünür.

![Yalnızca bir mali tablo seçildiğinde, deftere nakledilen ekstrelerin ödeme ayrıntıları bölümünü gösteren resim.](./media/Trickle-feed-posted-statements-transaction-view.png)

Aşağıdaki mali tablo işlerinin başlangıç ve bitiş zamanlarını, beklenen gün sonuna göre zamanlayın:

- Mali tabloyu hesaplamak için **Mali tabloları toplu işle hesapla** işini çalıştırın (**Retail ve Commerce \> Retail ve Commerce BT \> POS Deftere nakli \> Mali tabloları toplu işle hesapla**). Bu iş, deftere nakledilmemiş tüm mali hareketleri toplar ve bunları yeni bir mali tabloya ekler.
- Mali tabloları toplu işle deftere nakletmek için **Mali tabloları toplu işle deftere naklet** işini çalıştırın (**Retail ve Commerce \> Retail ve Commerce BT \> POS Deftere nakli \> Mali tabloları toplu işle deftere naklet**).

### <a name="manually-create-statements"></a>El ile ekstre oluşturma

Hareket ekstresi ve mali tablo türleri el ile de oluşturulabilir. 

1. **Retail ve Commerce \> Kanallar \> Mağazalar**'a gidin ve **Ekstreler**'i seçin. 
2. **Yeni**'yi ve ardından oluşturulacak ekstre türünü seçin. **Ekstreler** sayfasındaki alanlar, seçili ekstre türüyle ilgili verileri gösterir ve **Ekstre grubu** altındaki eylemler, ilgili eylemleri gösterir.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
