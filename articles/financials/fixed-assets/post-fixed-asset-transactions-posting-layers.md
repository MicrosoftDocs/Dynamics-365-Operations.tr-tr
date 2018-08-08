---
title: "Sabit kıymet hareketlerini deftere nakil katmanlarında deftere nakletme"
description: "Bu makalede sabit kıymet hareketleri için katman işlevlerinin deftere nakline genel bir bakış sunulmuştur."
author: ShylaThompson
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3001
ms.assetid: 7dabde57-0843-47c3-85ef-f36b6f472e30
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b210bddf640dff2d65e2aec63a18c27acebdc5a8
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="post-fixed-asset-transactions-to-posting-layers"></a>Sabit kıymet hareketlerini deftere nakil katmanlarında deftere nakletme

[!include [banner](../includes/banner.md)]

Bu makalede sabit kıymet hareketleri için katman işlevlerinin deftere nakline genel bir bakış sunulmuştur.

Bir sabit kıymet genellikle farklı amaçlarla ve farklı şekillerde amortize edilir. Vergi nedeniyle yapılan amortisman, vergiler için mümkün olan en yüksek amortismanı oluşturmak amacıyla geçerli vergi kuralları kullanılarak hesaplanır, ancak raporlama amacıyla yapılan amortismanlar muhasebe kanun ve standartlarına göre hesaplanır. Çeşitli amortisman türleri ayrı ayrı hesaplanır ve nakil katmanlarına ayrı ayrı kaydedilir.

Sabit bir değere bağlı her defter genel amortisman amacını içeren belirli bir nakil katmanı için ayarlanır. On tür deftere nakil katmanı vardır: Cari, İşlemler, Vergi ve yedi Özel Katman. Ayrıca Defter için genel muhasebeye nakil işlemini, Genel muhasebeye naklet alanını Hayır olarak ayarlayarak devre dışı bırakabilirsiniz. Ardından Deftere nakil katmanı alanı otomatik olarak Hiçbiri olarak ayarlanır. Normalde, genel muhasebeye nakledilmeyen defterler vergi raporlama amacıyla kullanılır. Bu yaklaşım, genel muhasebeye taahhütte bulunulmadığından kıymet defterine ait geçmiş hareketleri silmek için ek esneklik sağlar.

Sabit kıymet günlükleri Genel muhasebe > Günlük ayarı > Günlük adları konumunda Günlük adları sayfası kullanılarak tanımlanır. Amortisman nakledebileceğiniz her günlük, yalnızca bir nakil katmanı için günlük adı ile tanımlanır. Günlükte deftere nakil katmanı değiştirilemez. Bu kısıtlama her deftere nakil katmanı için hareketlerin ayrı tutulmasını garantiye almaya yardımcı olur. Her nakil katmanı için en az bir günlük adı oluşturulmalıdır. Genel muhasebeye nakledilmeyen defterler kullanıyorsanız ayrıca deftere nakil katmanı Hiçbiri olarak ayarlanan bir günlük de oluşturmanız gerekir.

Sabit kıymet hareketleri için Sabit kıymet nakil profilleri sayfasında genel muhasebe hesapları atayabilirsiniz. Her deftere nakil profili için ilgili hareket tipini ve defteri seçmeli ve ardından genel muhasebe kayıtlarını belirlemelisiniz. Her defter için genel muhasebeye nakleden bir deftere nakil profili kaydı ayarlayın.

> [!NOTE] 
> Türetilmiş defterleri kullanarak hareketleri aynı anda farklı nakil katmanlarında deftere nakledebilirsiniz. Birincil defterin hareketlerini bir günlükte oluşturabilirsiniz. Burada nakil katmanı deftere nakil katmanına karşılık gelir. Deftere nakil sırasında türetilmiş defter hareketleri ilgili deftere nakil katmanlarına nakledilir.

Daha fazla bilgi için bkz. [Türetilmiş defterler](derived-books.md) ve [Türetilmiş defterlerle deftere nakil](post-derived-value-models.md).




