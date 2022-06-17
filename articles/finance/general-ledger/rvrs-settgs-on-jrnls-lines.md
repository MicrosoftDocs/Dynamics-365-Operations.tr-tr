---
title: Yevmiye defterleri ve satırlardaki tersine çevirme ayarları
description: Bu makalede, yevmiye defterindeki bir ters işlem girişinin deftere nakledilmiş işleme neden dahil edilemediği ele alınmaktadır.
author: kweekley
ms.date: 04/29/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e36a3ea1736e4d7f60a5a6ce588ad3e66c950c14
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899856"
---
# <a name="reverse-settings-on-journals-and-lines"></a>Yevmiye defterleri ve satırlardaki tersine çevirme ayarları

[!include [banner](../includes/banner.md)]

Bu makalede, yevmiye defterindeki bir ters işlem girişinin deftere nakledilmiş işleme neden dahil edilemediği ele alınmaktadır.  

## <a name="symptom"></a>Belirti

Yevmiye defteri, günlükte bir ters işlem girişi ve ters işlem tarihi içerir. Günlüğü gönderdiğinizde fişlerin hiçbiri tersine çevrilmez. Bu neden gerçekleşir?

## <a name="resolution"></a>Çözüm

Günlük gönderildiğinde ters işlem yalnızca fişin **Satırlar** bölümündeki **Ters işlem girişi** ve **Ters işlem tarihi** ayarlarında görünür. Bu yaklaşım, günlüğün ters işlem için işaretlenmiş bazı fişlerin ve işaretlenmemiş diğer fişlerin dahil edilmesine olanak sağlar.

Günlükteki değerler yalnızca *yeni* satırlar eklenirken varsayılan olarak kullanılır. Günlükteki değerleri değiştirdiğinizde mevcut satırlar etkilenmez. Bu örnekte, ilk olarak fiş satırları girilmiştir. Günlüğü ters işlem olarak atamadan önce satır ayrıntısını girdiğinizde atama, ters işlem girişi ve tarihi olarak mevcut satırlara uygulanmaz.

Mevcut bir satırdaki ters işlem girişini veya ters işlem tarihini değiştirdiğinizde bu değişiklik aynı fişteki diğer satırlara yayılır. Performansı en iyi duruma getirmek için ızgara, değişiklikler diğer satırlara yayıldıktan sonra yenilenmez. Izgarayı yenileyerek güncelleştirilmiş değerleri görüntüleyebilirsiniz.


