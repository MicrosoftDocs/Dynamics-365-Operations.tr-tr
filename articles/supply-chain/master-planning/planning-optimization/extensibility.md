---
title: Planlama Optimizasyonu genişletilebilirliği
description: Bu konu, Planlama Optimizasyonu sırasında desteklenen genişletilebilirlik senaryolarını açıklar.
author: t-benebo
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-07-07
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: d7e39c9ecd1dc1a101e219764e8f4457bb06ff7a
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/23/2022
ms.locfileid: "8468902"
---
# <a name="planning-optimization-extensibility"></a>Planlama Optimizasyonu genişletilebilirliği

[!include [banner](../../includes/banner.md)]

Bu konu, Planlama Optimizasyonu sırasında desteklenen, ana planlama ile ilgili olan ve genişletilebilirlik senaryolarını açıklar. Bu özellikler, Microsoft Dynamics 365 Supply Chain Management 10.0.13 sürümünden başlayarak kullanılabilir.

## <a name="custom-processing-when-master-planning-is-completed"></a>Ana planlama tamamlandığında özel işlem

En genel genişletilebilirlik senaryosunda Planlama Optimizasyonu sırasında, özel işlem planı güncelleştirildikten sonra yapılır. Örneğin, planlı siparişler tablosuna (`ReqPO`) bir sütun ekleyebilir veya oluşturulan plandaki bazı istatistiksel bilgileri türetmek isteyebilirsiniz. Bu senaryolara olanak tanıyan ana genişletilebilirlik noktası, `MpsMasterPlanningEvents` sınıfındaki `jobCompletedSuccessfully` yöntemidir.

```X++
public static void jobCompletedSuccessfully(MpsMasterPlanningJobCompletedSuccessfullyEventArgs _args)
```

Burada, planlı siparişte özel bir `CstmOrderPriority` alanında ayarlayan bir uzantı örneği verilmiştir.

```X++
[ExtensionOf(classStr(MpsMasterPlanningEvents))]
public static final class MpsMasterPlanningEvents_Cstm_Extension
{
    public static void jobCompletedSuccessfully(MpsMasterPlanningJobCompletedSuccessfullyEventArgs _args)
    {
        ttsbegin;

        var affectedPlannedOrdersQuery = _args.parmPostProcessingQueryBuilder().buildAffectedPlannedOrdersQuery();
        var affectedPlannedOrdersQueryRun = new QueryRun(affectedPlannedOrdersQuery);

        while (affectedPlannedOrdersQueryRun.next())
        {
            ReqPO reqPO = affectedPlannedOrdersQueryRun.get(tableNum(ReqPO));
            reqPO.selectForUpdate(true);
            reqPO.CstmOrderPriority = reqPO.ReqDate - systemDateGet() < 7 ? CstmPlannedOrderPriority::Urgent : CstmPlannedOrderPriority::Regular;
            reqPO.doUpdate();
        }

        ttscommit;

        next jobCompletedSuccessfully(_args);
    }

}
```

Özel mantık eklediğinizde, aşağıdaki kısıtlamalara ve en iyi uygulamaları göz önünde bulundurun:

- `jobCompletedSuccessfully` yöntemi, hareket kapsamı dışında çağrılır. Bu nedenle, özel mantık çalıştırılmaya başladığında plan zaten kullanıcı tarafından görülebilecektir. Özelleştirmeniz planlı siparişlerde ek alanlar ayarladıysa, bu alanların değerlerinin sonuçta tutarlı olacağını kullanıcılara bildirmeniz önemlidir (yani, bunlar planlanan iş tamamlandıktan hemen sonra güncelliklerini kaybedebilir).
- `jobCompletedSuccessfully` yöntemi çağrıldığında başka bir ana planlama işi başlayabilir. Yeni iş planın tam planını veya bir kısmını etkileyebilir. Yeni iş, `jobCompletedSuccessfully`'de işlenen planlama işinin bir parçası olarak oluşturulan veya güncelleştirilen aynı planlı siparişleri veya gereksinim hareketlerini güncelleştirebilir veya silebilir. Bu olay genişletildiğinde, güncelleştirme çakışması özel durumları işlenmelidir.
- Bu yöntemi genişlettiğinizde tek bir hareket kapsamı kullanmaktan kaçının. Tek bir ana planlama çalıştırması, milyonlarca gereksinim hareketi ve yüzlerce binlerce planlı sipariş oluşturabilir. Tüm bu hareketler ve planlı siparişler tek bir hareketin kapsamında işlenirse, birçok SQL kilidi gerçekleşir ve diğer planlama işlemleri engellenir. Ek olarak, hareket uzun süre tutulduğunda, SQL veritabanında "hayalet kayıtlar" oluşturulur. Hayalet kayıtlar sistemdeki her işlemi olumsuz etkiler.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]