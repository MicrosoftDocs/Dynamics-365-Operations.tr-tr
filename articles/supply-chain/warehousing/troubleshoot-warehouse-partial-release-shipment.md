---
title: Kısmi serbest bırakma ve kısmi sevkiyatlarla ilgili sorunları giderme
description: Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta kısmi serbest bırakma ve kısmi sevkiyatlarla çalışırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7b8cb887a4acd6fc1a691614dc666bbdbe4a34b1ff874c5d80cf492f2984d299
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742572"
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