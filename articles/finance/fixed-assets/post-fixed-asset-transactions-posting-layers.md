---
title: Sabit kıymet hareketlerini deftere nakil katmanlarında deftere nakletme
description: Bu makalede sabit kıymet hareketleri için katman işlevlerinin deftere nakline genel bir bakış sunulmuştur.
author: moaamer
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.custom: 3001
ms.assetid: 7dabde57-0843-47c3-85ef-f36b6f472e30
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cf35194badfa3c09758ad4dd9927af172a4ffdab
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990552"
---
# <a name="post-fixed-asset-transactions-to-posting-layers"></a>Sabit kıymet hareketlerini deftere nakil katmanlarında deftere nakletme

[!include [banner](../includes/banner.md)]

Bu makalede sabit kıymet hareketleri için katman işlevlerinin deftere nakline genel bir bakış sunulmuştur.

Bir sabit kıymet genellikle farklı amaçlarla ve farklı şekillerde amortize edilir. Vergi nedeniyle yapılan amortisman, vergiler için mümkün olan en yüksek amortismanı oluşturmak amacıyla geçerli vergi kuralları kullanılarak hesaplanır, ancak raporlama amacıyla yapılan amortismanlar muhasebe kanun ve standartlarına göre hesaplanır. Çeşitli amortisman türleri ayrı ayrı hesaplanır ve nakil katmanlarına ayrı ayrı kaydedilir.

Sabit bir değere bağlı her defter genel amortisman amacını içeren belirli bir nakil katmanı için ayarlanır. On tür deftere nakil katmanı vardır: Cari, İşlemler, Vergi ve yedi Özel Katman. Ayrıca Defter için genel muhasebeye nakil işlemini, Genel muhasebeye naklet alanını Hayır olarak ayarlayarak devre dışı bırakabilirsiniz. Ardından Deftere nakil katmanı alanı otomatik olarak Hiçbiri olarak ayarlanır. Normalde, genel muhasebeye nakledilmeyen defterler vergi raporlama amacıyla kullanılır. Bu yaklaşım, genel muhasebeye taahhütte bulunulmadığından kıymet defterine ait geçmiş hareketleri silmek için ek esneklik sağlar.

Sabit kıymet günlükleri Genel muhasebe > Günlük ayarı > Günlük adları konumunda Günlük adları sayfası kullanılarak tanımlanır. Amortisman nakledebileceğiniz her günlük, yalnızca bir nakil katmanı için günlük adı ile tanımlanır. Günlükte deftere nakil katmanı değiştirilemez. Bu kısıtlama her deftere nakil katmanı için hareketlerin ayrı tutulmasını garantiye almaya yardımcı olur. Her nakil katmanı için en az bir günlük adı oluşturulmalıdır. Genel muhasebeye nakledilmeyen defterler kullanıyorsanız ayrıca deftere nakil katmanı Hiçbiri olarak ayarlanan bir günlük de oluşturmanız gerekir.

Sabit kıymet hareketleri için Sabit kıymet nakil profilleri sayfasında genel muhasebe hesapları atayabilirsiniz. Her deftere nakil profili için ilgili hareket tipini ve defteri seçmeli ve ardından genel muhasebe kayıtlarını belirlemelisiniz. Her defter için genel muhasebeye nakleden bir deftere nakil profili kaydı ayarlayın.

Sabit varlık yalnızca **Geçerli** deftere nakit katmanını destekleyen belgelere girilir (ör. **Satın alma siparişi**, **Bekleyen satıcı faturası**, **Satış siparişi** veya **Serbest metinli fatura**). Bu belgelerden herhangi birinde sabit varlık kimliğini seçerken varlık defteri **Geçerli** deftere nakil katmanına sahip defterle filtrelenir ve sistem, sabit varlık deftere nakil katmanının **Geçerli** olduğunu doğruladığında bu kimlik deftere nakil sırasında otomatik olarak doldurulur. Bu doğrulama tamamlanamazsa deftere nakil işlemi durdurulur. 

> [!NOTE] 
> Türetilmiş defterleri kullanarak hareketleri aynı anda farklı nakil katmanlarında deftere nakledebilirsiniz. Birincil defterin hareketleri bir günlükte veya nakil katmanı deftere nakil katmanına karşılık gelen bir kaynak belgede oluşturulur. Deftere nakil sırasında türetilmiş defter hareketleri uygun deftere nakil katmanlarına nakledilecektir. 


Daha fazla bilgi için bkz. [Türetilmiş defterler](derived-books.md) ve [Türetilen defterlerle deftere nakletme](post-derived-value-models.md).



