---
title: Mali boyut kümeleri
description: Bu konu, finansal boyut kümelerini açıklar ve kullanımlarını en iyi duruma getirmek için bazı ipuçları sağlar.
author: yukonpeegs
ms.date: 03/07/2022
ms.topic: article
ems.prod: ''
ms.technology: ''
ms.search.form: DimensionFocus, LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom: 25871
ms.search.region: Global
ms.author: epegors
ms.search.validFrom: 2021-03-23
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: c583a2a89b45b59ea76ffd8e38b6206c9ca9ed41
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/06/2022
ms.locfileid: "8722590"
---
# <a name="financial-dimension-sets"></a>Mali boyut kümeleri

[!include [banner](../includes/banner.md)]

Bu konu, finansal boyut kümelerini açıklar ve kullanımlarını en iyi duruma getirmek için bazı ipuçları sağlar.

Boyut kümesi, kullanıcı tanımlı bir şekilde Genel muhasebe verilerini özetlemek için kullanılabilen finansal boyutların sıralı bir listesidir. Boyut kümelerinin birincil kullanımı mizan tanımlamaktır.

Tek standart boyut kümesi yalnızca ana hesabı içeren boyut kümesidir.

**Mali boyut kümeleri** sayfası, finansal boyut kümeleri oluşturmak ve bunları yönetmek için kullanılır.

## <a name="dimension-set-balances"></a>Boyut kümesi bakiyeleri

Boyut kümesinde, mali boyutlarına dayalı bakiyeler olabilir. Bakiyeler Genel muhasebede bulunur ve boyut kümesi tanımını temel alır. Bakiyeler, alındıklarında (örneğin, bir mizan oluşturulduğunda) performansı artırmaya yardımcı olmak için Genel muhasebe verilerinden özetlenir.

## <a name="create-balances"></a>Bakiyeleri oluştur

Henüz bakiyesi olmayan bir boyut kümesinin bakiyelerini başlatmak için **Bakiyeleri oluştur** düğmesini kullanın.

> [!NOTE]
> Bakiye güncelleştirmeleri tüm Genel muhasebe deftere nakil faaliyetlerini etkilediğinden, bakiyeleri olan boyut kümeleri sayısını sınırlandırmanızı öneririz.

## <a name="update-balances"></a>Bakiyeleri güncelleştir

Bakiyelere en son Genel muhasebe deftere nakil faaliyetini dahil etmek için **Bakiyeleri güncelleştir** düğmesini kullanın. Bakiye güncelleştirmeleri hafif işlemlerdir. Bunlar yalnızca son güncelleştirmeden bu yana gerçekleşen Genel muhasebe deftere nakil etkinliğini işlemelidir.

> [!NOTE]
> Mizan görüntüleme gösterilen bakiyelerin güncel olmasını sağlamak üzere güncelleştirme yapmaya zorlar. En sık kullanılan boyut kümelerinde yapılan güncelleştirmelerin hızlı olması için, tekrarlayan bir toplu iş kullanmayı düşünebilirsiniz. Bu şekilde, kullanıcıların deneme mizanı için beklemesi gereken zamanı en aza indirmeye yardımcı olursunuz.

## <a name="rebuild-balances"></a>Bakiyeleri yeniden yapılandır

Bakiyeleri sıfırdan oluşturmak için **Bakiyeleri yeniden oluştur** düğmesini kullanın. Bu şekilde, bunların Genel muhasebedeki verilerle eşleşmesini sağlamaya yardımcı olursunuz. Bakiyeleri yeniden oluşturma işlemi birçok işlem gerektirir ve genellikle gerekli olmamalıdır.

> [!NOTE]
> Bakiyeleri düzenli olarak yeniden oluşturmaya gerek duyan bir senaryonuz varsa, müşteri desteğine başvurmanızı öneririz. Müşteri desteği, bakiyelerin Genel muhasebedeki verilerle neden eşleşmediğini belirlemenize yardımcı olabilir.

## <a name="clear-balances"></a>Bakiyeleri temizle

Bakiyeleri kaldırmak ve diğer güncelleştirmeleri durdurmak için **Bakiyeleri temizle** düğmesini kullanın. Boyut kümesinin artık Genel muhasebe deftere nakil faaliyetleri üzerinde bir etkisi olmayacaktır.

## <a name="delete-a-dimension-set"></a>Bir boyut kümesini silme

Belirli bir boyut kümesi için olan bakiye verileriyle ilgili olası sorunları çözmek üzere herhangi bir geçici çözüm formu olarak boyut kümelerini **silmeyin ve yeniden oluşturmayın**. Bir boyut kümesini yeniden oluşturmak maliyetlidir. Sorunlarla ilgili daha fazla yardım için müşteri desteğe başvurun. 


Daha fazla bilgi için bkz. [Mali boyutlar](financial-dimensions.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
