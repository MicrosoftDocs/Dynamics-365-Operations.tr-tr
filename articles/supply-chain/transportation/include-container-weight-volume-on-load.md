---
title: Konteyner ağırlığını ve hacmini yüke dahil etme
description: Bu konu, yüklerdeki konteyner ağırlığı ve hacmi dahil etmek için işlevi ayarlamayı ve uygulamayı açıklar.
author: Henrikan
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRateRouteWorkbench, TMSDriverLogListPage, TMSTransportationTender
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9196e9c4ce1a8aa629400b8bf379e7164a797b85
ms.sourcegitcommit: 0cc89dd42c1924ca0ec735c6566bc56b39cc5f7d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/26/2021
ms.locfileid: "6102651"
---
# <a name="include-container-weight-and-volume-on-load"></a>Konteyner ağırlığını ve hacmini yüke dahil etme

[!include [banner](../includes/banner.md)]

Konteyner ağırlığı ve hacmini bir yükte ekleme işlevi, bir yükte giden konteynerlerin ve maddelerin toplam ağırlığı ve hacmi hakkında net bir görünüm verir.

Bir yük, tek bir sevkiyat veya birden fazla sevkiyat içerir ve bu sevkiyatlar, tek bir satış siparişine veya birden fazla satış siparişine ait farklı öğeler içerir. Maddeler bir konteyner içerisinde depolanır ve konteyner bir yüke yüklenir. Bir konteyner dışındaki maddeler de yükün parçası olabilir. Bu koşullara dayalı olarak, sistem yükteki ağırlık ve hacmin değerlerini, hem konteynerlerin hem de maddelerin yükünü ve hacmini dikkate alarak hesaplar.

Hesaplanan değerler hassas değilse, yük üzerindeki gerçek ağırlık ve hacimleri girerek bunları ayarlayabilirsiniz. Ağırlık ve hacim için değerler taşıma yönetimi işleminde kullanılır. Örneğin, değerler rota oranı workbenchinde kullanılır, burada yükler için rota ve oranı belirlemeye yardımcı olurlar ve ayrıca taşıma ödemesi ve sürücü girişi için de kullanılırlar.

## <a name="where-it-applies"></a>Uygulandığı yerler

Bir yükteki konteyner ağırlığını ve hacmini dahil etmek, taşıma yönetimi işlemine uygulanır; örneğin rota oranı workbench'i, taşıma ödemeleri veya sürücü girişi gibi.

## <a name="how-it-is-set-up"></a>Nasıl ayarlanır

Bir yük için dikkate alınacak konteynerlerin sayısı, konteynerin ağırlığı ve hacmine ve kullanılan konteynerin yüzdesine dayanarak hesaplanır.

-   Bir konteyner için ağırlık ve hacmi ayarlamak için **Ambar yönetimi** \> **Kurulum** \> **Konteynerler** \> **Konteyner türleri** üzerine tıklayın.

-   Konteyner kullanım yüzdesini ayarlamak için **Ambar yönetimi** \> **Kurulum** \> **Konteynerler** \> **Konteyner grupları** üzerine tıklayın ve **Konteyner kullanım yüzdesi** alanına bir değer girin.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]