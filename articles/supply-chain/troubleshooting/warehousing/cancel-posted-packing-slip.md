---
title: Siparişten deftere nakledildikten sonra sevk irsaliyesi iptal edilemiyor
description: Malzeme çekme ve sevkiyat işlemleri WMS için etkinleştirildiğinde, bir satış siparişinden deftere nakledildikten sonra sevk irsaliyesini iptal edemezsiniz. Bu sayfada bir geçici çözüm sunulmaktadır.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d20e66e2721560b8409eb63c3546a79adc188c7c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477901"
---
# <a name="cant-cancel-a-packing-slip-after-its-posted-from-a-sales-order"></a>Satış siparişinden deftere nakledildikten sonra sevk irsaliyesi iptal edilemiyor

## <a name="symptoms"></a>Belirtiler

Malzeme çekme ve sevkiyat işlemleri gelişmiş ambar yönetimi (WMS) için etkinleştirildiğinde, bir satış siparişinden deftere nakledildikten sonra sevk irsaliyesini iptal edemezsiniz.

## <a name="resolution"></a>Çözüm

WMS için etkinleştirilen maddelere ait deftere nakledilen sevk irsaliyelerini düzeltmek için deftere nakletme işlemi siparişten değil, yükten oluşturulmalıdır. Microsoft bu sorunu değerlendirmiş ve bir özellik sınırlaması olduğunu tespit etmiştir.  

Genel olarak, ambar yönetimi işlemleri üzerinden malzemesi çekilen ve sevk edilen bir satış siparişi sevk irsaliyesi yük veya sevkiyattan ve satış siparişi belgesinden güncelleştirilen bir sevk irsaliyesi olabilir. Ancak satış siparişini satış siparişi belgesinden güncelleştiren sevk irsaliyesi durumunda sevk irsaliyesi tersine çevirme işlemi yükten veya satış siparişinden yapılamaz. Bu nedenle, sevk irsaliyesini yükten deftere nakletme işlemini kullanmanızı öneririz. Bu durumda, yükten gerçekleştirilmesi gereken ters işlem etkinleştirilir.
