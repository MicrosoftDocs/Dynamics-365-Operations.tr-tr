---
title: Sabit kıymet hareketlerini deftere nakil katmanlarında deftere nakletme
description: Bu makalede sabit kıymet hareketleri için katman işlevlerinin deftere nakline genel bir bakış sunulmuştur.
author: moaamer
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: kfend
ms.custom: 3001
ms.assetid: 7dabde57-0843-47c3-85ef-f36b6f472e30
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e6361a3bef58bcc06ff01d0aada9ba309f283a83
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/06/2022
ms.locfileid: "8722366"
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





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
