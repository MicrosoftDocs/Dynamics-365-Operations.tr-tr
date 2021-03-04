---
title: Kısmi serbest bırakma ve kısmi sevkiyatlarla ilgili sorunları giderme
description: Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta kısmi serbest bırakma ve kısmi sevkiyatlarla çalışırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e89a430f90374733b23fadaf53f5bab598d67d62
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645960"
---
# <a name="troubleshoot-partial-releases-and-partial-shipments"></a>Kısmi serbest bırakma ve kısmi sevkiyatlarla ilgili sorunları giderme

[!include [banner](../includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta kısmi serbest bırakma ve kısmi sevkiyatlarla çalışırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.

## <a name="the-release-status-of-a-sales-order-remains-partially-released-even-after-the-sales-order-is-invoiced"></a>Satış siparişi faturalandıktan sonra bile bir satış siparişinin serbest bırakma durumu Kısmi serbest bırakıldı olarak kalır.

### <a name="issue-description"></a>Sorun açıklaması

Satış siparişi bir teslimat siparişi ancak üzerindeki bir veya daha fazla madde farklı teslimat moduna sahip. Sipariş faturalandıktan sonra, serbest bırakma durumu *Kısmi serbest bırakıldı* şeklindedir.

Örneğin, bir satış siparişinde iki madde vardır: biri teslimat için, diğeri ise malzeme çekme içindir. Teslimat ve malzeme çekme tamamlanmıştır. Bu nedenle, her iki satır da faturalanmıştır. Ancak, serbest bırakma durumu hala *Kısmi serbest bırakıldı* olarak gösterilir ve bu yanıltıcı olabilir.

### <a name="issue-resolution"></a>Sorunun çözümü

Serbest bırakma durumu, yalnızca maddelerin ambar yönetimi için etkinleştirildiği sipariş satırları için geçerlidir. Bu nedenle, serbest bırakma durumu, bu senaryoda *Kısmi serbest bırakıldı* olarak kalır. Microsoft bu sorunu değerlendirmiş ve bir özellik sınırlaması olduğunu tespit etmiştir. Serbest bırakma durumunu güncelleştirmek için sevk irsaliyesi ve faturalama işleminin bir parçası olarak bir uzantı eklenebilir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]