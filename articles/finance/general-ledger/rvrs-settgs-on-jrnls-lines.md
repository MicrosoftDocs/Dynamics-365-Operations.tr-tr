---
title: Günlükler ve satırlardaki ayarları tersine çevirme
description: Bu konuda, yevmiye defterindeki bir ters işlem girişinin deftere nakledilmiş işleme neden dahil edilemediği ele alınmaktadır.
author: kweekley
ms.date: 04/29/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 74020f6fc9b0fa8e05a1e2a09fd13dcd60490dc0
ms.sourcegitcommit: 817716c2e96f24af0ef1d7d5323afdeccdc602f3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/13/2021
ms.locfileid: "6028590"
---
# <a name="reverse-settings-on-journals-and-lines"></a>Günlükler ve satırlardaki ayarları tersine çevirme

[!include [banner](../includes/banner.md)]

Bu konuda, yevmiye defterindeki bir ters işlem girişinin deftere nakledilmiş işleme neden dahil edilemediği ele alınmaktadır.  

## <a name="symptom"></a>Belirti

Yevmiye defteri, günlükte bir ters işlem girişi ve ters işlem tarihi içerir. Günlüğü gönderdiğinizde fişlerin hiçbiri tersine çevrilmez. Bu neden gerçekleşir?

## <a name="resolution"></a>Çözüm

Günlük gönderildiğinde ters işlem yalnızca fişin **Satırlar** bölümündeki **Ters işlem girişi** ve **Ters işlem tarihi** ayarlarında görünür. Bu yaklaşım, günlüğün ters işlem için işaretlenmiş bazı fişlerin ve işaretlenmemiş diğer fişlerin dahil edilmesine olanak sağlar.

Günlükteki değerler yalnızca *yeni* satırlar eklenirken varsayılan olarak kullanılır. Günlükteki değerleri değiştirdiğinizde mevcut satırlar etkilenmez. Bu örnekte, ilk olarak fiş satırları girilmiştir. Günlüğü ters işlem olarak atamadan önce satır ayrıntısını girdiğinizde atama, ters işlem girişi ve tarihi olarak mevcut satırlara uygulanmaz.

Mevcut bir satırdaki ters işlem girişini veya ters işlem tarihini değiştirdiğinizde bu değişiklik aynı fişteki diğer satırlara yayılır. Performansı en iyi duruma getirmek için ızgara, değişiklikler diğer satırlara yayıldıktan sonra yenilenmez. Izgarayı yenileyerek güncelleştirilmiş değerleri görüntüleyebilirsiniz.


