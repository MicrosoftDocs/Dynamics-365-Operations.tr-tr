---
title: Sipariş durumu, faturalandırıldıktan sonra Kısmi serbest bırakıldı olarak kalıyor
description: Bazı durumlarda, satış siparişinin durumu, sipariş faturalandırıldıktan sonra bile Kısmi serbest bırakıldı olarak kalır. Bu sayfada, bunun nedeni ve olası bir geçici çözüm açıklanmaktadır.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 8bfe7ecfd4beb6e77e8dd1e23ccd896d067bdb51
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477858"
---
# <a name="order-status-remains-partially-released-even-after-the-sales-order-is-invoiced"></a>Satış siparişi faturalandırıldıktan sonra bile sipariş durumu Kısmen serbest bırakıldı olarak kalıyor

## <a name="symptoms"></a>Belirtiler

Satış siparişi bir teslimat siparişi ancak üzerindeki bir veya daha fazla madde farklı teslimat moduna sahip. Sipariş faturalandıktan sonra, serbest bırakma durumu *Kısmi serbest bırakıldı* şeklindedir.

Örneğin, bir satış siparişinde iki madde vardır: biri teslimat için, diğeri ise malzeme çekme içindir. Teslimat ve malzeme çekme tamamlanmıştır. Bu nedenle, her iki satır da faturalanmıştır. Ancak, serbest bırakma durumu hala *Kısmi serbest bırakıldı* olarak gösterilir ve bu yanıltıcı olabilir.

## <a name="workaround"></a>Geçici çözüm

Serbest bırakma durumu, yalnızca maddelerin ambar yönetimi için etkinleştirildiği sipariş satırları için geçerlidir. Bu nedenle, serbest bırakma durumu, bu senaryoda *Kısmi serbest bırakıldı* olarak kalır. Microsoft bu sorunu değerlendirmiş ve bir özellik sınırlaması olduğunu tespit etmiştir. Serbest bırakma durumunu güncelleştirmek için sevk irsaliyesi ve faturalama işleminin bir parçası olarak bir uzantı eklenebilir.
