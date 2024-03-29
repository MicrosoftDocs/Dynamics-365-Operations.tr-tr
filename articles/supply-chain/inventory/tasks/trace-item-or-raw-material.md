---
title: Maddeyi veya hammaddeyi izleme
description: Bu yordam, ürünlerin veya hammaddelerin kullanılmış veya kullanılmakta olduğunu belirlemek amacıyla ürün izleme işlevinin nasıl kullanılacağını gösterir.
author: yufeihuang
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventTrackingDimTracing, InventTrackingDimTracingCriteria, InventTrackingItemIdLookup, InventBatchIdLookup, CustTable, SalesLine
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c01cabf32542798f70720ab0db7d055fc54cf345
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7575836"
---
# <a name="trace-an-item-or-raw-material"></a>Maddeyi veya hammaddeyi izleme

[!include [banner](../../includes/banner.md)]

Bu yordam, ürünlerin veya hammaddelerin kullanılmış veya kullanılmakta olduğunu belirlemek amacıyla ürün izleme işlevinin nasıl kullanılacağını gösterir. Bu yordamı kullanarak, bir ürünü belirleyebilir, kaynağına kadar izleyebilir ve sonra ürünün üretiminden satışına kadar olan ileriye yönelik izleme işlemleri görebilirsiniz. Bu işlem, ilişkili müşterileri, satış siparişlerini ve daha fazlasını araştırmak için kullanılabilir. Bu yordam, USP2 demo verisi şirketini kullanır.


## <a name="trace-an-item-backwards-using-a-known-batch-number"></a>Bilinen bir toplu iş numarası kullanarak bir ürünü geriye doğru izleme
1. **Gezinti panosu**'nda, **Modüller > Stok yönetimi > Sorgular ve raporlar > İzleme boyutları > Madde izleme**'ye gidin.
2. **Madde numarası** alanında 'P9100' seçin.
3. Listede, seçili satırdaki bağlantıya tıklayın.
4. **İleriye doğru veya Geriye doğru** alanında 'Geriye doğru'yu seçin.
5. **Toplu iş numarası** alanında '12-344-01' olarak seçin.
6. Listede, seçili satırdaki bağlantıya tıklayın.
7. **Tamam**'a tıklayın.

## <a name="identify-an-item-trace-it-forward-and-make-an-analysis"></a>Bir ürünü tanımlama, ileriye doğru izleme ve analizini yapma

Ağacının en üst düğümü seçilen ürün ve toplu işe yönelik eldeki ürün miktarını gösterir. İleriye doğru iz üzerinde yürütülmesi gereken maddeyi bulmak için ağaç düğümlerini genişletmeniz gerekir.   
1. Ağaçta 'Aşağıda açıklanan düğümler ve son düğümü seç' seçeneğini genişletin.
    
    Genişletin: ' P9100 / 1 / 10 / olarak-12-344-01 2 ● ● 7.00 gal  \P9100 Çekildi satış siparişi 000072 ● ● 22/12/2015 ● ●-1 keg ● ●-4.00 gal keg Site = 1, ambar = 10, toplu iş numarası olarak-12-344-01  \P9100 ● B-000050 ● üretim 12/9/2015● 7 keg ● ● 27.00 gal = Site = 1, ambar = 10, toplu iş numarası olarak-12-344-01 ● yan ürünler =: P9101' ve bu düğümü seçin.     
2. Ağaçta 'Aşağıda açıklanan düğüm ve bu düğümü seç' seçeneğini genişletin.
    
    Yalnızca seçtiğiniz düğümünden başlayan genişletin ' M9103 ● B-000050 ● 9/12/2015 ● üretim satırı-160.00 lb ● boyutu = 70, renk Tamam, Site = = 1, ambar = 10, toplu iş numarası App01 =' ve bu düğümü seçin.  
3. **İzleme başlangıç düğümü**'nü tıklatın.
4. **İleri**'ye tıklayın.
5. **Eylem Bölmesi**'nde **İzleme** öğesini tıklatın.
    
    İzlemekte olduğunuz madde tarafından etkilenen müşteriler ve gönderilmiş ve gönderilmemiş bu maddeyle ilgili satış siparişleri hakkında bilgi veren birkaç izleme seçeneği vardır.   
6. **Müşteriler**'i tıklatın.
7. Sayfayı kapatın.
8. **Eylem Bölmesi**'nde **İzleme** öğesini tıklatın.
9. **Sevk edilmiş satış siparişleri**'ni tıklatın.
10. Sayfayı kapatın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]