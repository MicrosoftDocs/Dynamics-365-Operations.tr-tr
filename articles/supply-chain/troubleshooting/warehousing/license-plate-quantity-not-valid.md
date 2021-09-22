---
title: Gelen siparişleri kaydederken miktar geçerli değil
description: 'Bir plaka için tahsis edilen miktar, alınması gereken miktarı aşarsa şu hatayı alırsınız: "Miktar geçerli değil."'
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 5099b320447bf59c72f5017564ea660f19c690a5
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477888"
---
# <a name="license-plate-quantity-is-not-valid-when-registering-inbound-orders"></a>Gelen siparişleri kaydederken plaka miktarı geçerli değil

## <a name="symptoms"></a>Belirtiler

Gelen siparişleri kaydederken aşağıdaki hata iletisini alabilirsiniz:

> Miktar geçersiz.

**Plaka gruplandırma ilkesi** alanı gelen siparişleri kaydetmek için kullanılan bir mobil aygıt menü öğesi için *Kullanıcı tanımlı* olarak ayarlanmışsa bu hatayı alırsınız ve kaydı tamamlayamazsınız.

## <a name="cause"></a>Nedeni

*Kullanıcı tanımlı*, Plaka gruplama ilkesi olarak kullanıldığında sistem, gelen stoku birim sıra grubunda belirtildiği gibi ayrı plakalara böler. Alınan maddeyi izlemek için toplu iş veya seri numaraları kullanılıyorsa her toplu işin ya da serinin miktarları, kayıtlı olan plaka başına belirtilmelidir. Bir plaka için belirtilen miktar, geçerli boyutlar için hala alınması gereken miktarı aşarsa bu hata iletisini alırsınız.

## <a name="resolution"></a>Çözüm

**Plaka gruplandırma ilkesi** alanının *Kullanıcı tanımlı* olarak ayarlandığı bir mobil aygıt menü öğesini kullanarak bir öğeyi kaydettiğinizde, sistem plaka numaralarını, toplu iş numaralarını veya seri numaralarını onaylamanızı veya girmenizi gerektirebilir.

Plaka onayı sayfasında sistem, geçerli plaka için tahsis edilen miktarı gösterir. Toplu iş veya seri onay sayfalarında, sistem geçerli plakanın üzerinde hâlâ alınması gereken miktarı gösterir. Ayrıca, bu plaka ve seri numarası birleşimi için kaydedilecek miktarı girebileceğiniz bir alan da içerir. Bu durumda, plaka için kaydedilen miktarın hala teslim alınması gereken miktardan fazla olmadığından emin olun.

Alternatif olarak, gelen sipariş kaydında çok fazla plaka oluşturulursa, **Plaka gruplandırma ilkesi** alanının değeri *Plaka gruplandırma* ile değiştirilebilir, maddeye yeni bir birim dizi grubu atanabilir veya birim sıra grubu için **plaka gruplandırma** seçeneği devre dışı bırakılabilir.
