---
title: "Deftere nakil katmanı için sabit kıymet hareketlerini nakletme"
description: "Bu makalede sabit kıymet hareketleri için katman işlevlerinin deftere nakline genel bir bakış sunulmuştur."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3001
ms.assetid: 7dabde57-0843-47c3-85ef-f36b6f472e30
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 4b112eee303604149c7609972a60c2014d4be423
ms.lasthandoff: 03/31/2017


---

# <a name="post-fixed-asset-transactions-to-posting-layers"></a>Deftere nakil katmanı için sabit kıymet hareketlerini nakletme

Bu makalede sabit kıymet hareketleri için katman işlevlerinin deftere nakline genel bir bakış sunulmuştur.

Bir sabit kıymet genellikle farklı amaçlarla ve farklı şekillerde amortize edilir. Vergi nedeniyle yapılan amortisman, vergiler için mümkün olan en yüksek amortismanı oluşturmak amacıyla geçerli vergi kuralları kullanılarak hesaplanır, ancak raporlama amacıyla yapılan amortismanlar muhasebe kanun ve standartlarına göre hesaplanır. Çeşitli amortisman türleri ayrı ayrı hesaplanır ve nakil katmanlarına ayrı ayrı kaydedilir.

Sabit bir değere bağlı her defter genel amortisman amacını içeren belirli bir nakil katmanı için ayarlanır. On tür deftere nakil katmanı vardır: Cari, İşlemler, Vergi ve yedi Özel Katman. Ayrıca Defter için genel muhasebeye nakil işlemini, Genel muhasebeye naklet alanını Hayır olarak ayarlayarak devre dışı bırakabilirsiniz. Ardından Deftere nakil katmanı alanı otomatik olarak Hiçbiri olarak ayarlanır. Genellikle, genel muhasebeye nakletmek gerekmez defterleri vergi raporlama amaçları için kullanılır. Bu yaklaşım genel muhasebeye işlenmeden önce henüz çünkü kıymet defterine ait geçmiş hareketlerini silmek için ek bir esneklik sağlar.

Sabit kıymet günlükleri Genel muhasebe > Günlük ayarı > Günlük adları konumunda Günlük adları sayfası kullanılarak tanımlanır. Amortisman nakledebileceğiniz her günlük, yalnızca bir nakil katmanı için günlük adı ile tanımlanır. Günlüğü deftere nakil katmanı değiştirilemez. Bu kısıtlama her deftere nakil katmanı için hareketlerin ayrı tutulmasını garantiye almaya yardımcı olur. Her nakil katmanı için en az bir günlük adı oluşturulmalıdır. Genel muhasebeye nakletmek gerekmez defterleri kullanıyorsanız, bir günlüğü deftere nakil katmanı yok olarak belirlendiği de oluşturmanız gerekir.

Sabit kıymet hareketleri için Sabit kıymet nakil profilleri sayfasında genel muhasebe hesapları atayabilirsiniz. Her deftere nakil profili için ilgili hareket tipini ve defteri seçmeli ve ardından genel muhasebe kayıtlarını belirlemelisiniz. Her defter için genel muhasebeye nakleden bir deftere nakil profili kaydı ayarlayın.

> [!NOTE] 
> Türetilmiş kitapları kullanarak aynı anda farklı nakil katmanlarına hareketleri deftere nakledebilirsiniz. Birincil defterin hareketlerini bir günlükte oluşturabilirsiniz. Burada nakil katmanı deftere nakil katmanına karşılık gelir. Deftere nakil sırasında türetilmiş defter hareketleri ilgili deftere nakil katmanlarına nakledilir.

Daha fazla bilgi için [kitaplar türetilmiş](derived-books.md) ve [türetilmiş Defterleriyle deftere nakil](post-derived-value-models.md).


