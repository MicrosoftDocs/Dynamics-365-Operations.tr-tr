---
title: Üretim akışı sürümünü devre dışı bırakma
description: Etkin bir üretim akışı sürümüne artık ihtiyaç duyulmuyorsa devre dışı bırakılabilir.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1691dc644e2e191a9e74980784d6dcf741dcd598
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7576772"
---
# <a name="deactivate-a-production-flow-version"></a>Üretim akışı sürümünü devre dışı bırakma

[!include [banner](../../includes/banner.md)]

Etkin bir üretim akışı sürümüne artık ihtiyaç duyulmuyorsa devre dışı bırakılabilir. Bu seçeneği yalnızca tüm kanban kuralları ve etkinlikler sonlandırmışsa ve yeniden etkinleştirilmeyecekse kullanmalısınız. Bu üretim akışı sürümüyle ilgili tüm kanban kurallarının bitiş tarihinin geçerli tarih ve saat ile güncelleştirileceğini unutmayın. 

Etkin bir üretim akışı sürümünü değiştirmek için etkin sürümün bitiş tarihini ayarlamayı düşünün ve yeni bir sürüm oluşturun. Bu, yeni sürümü ve ilgili kanban kurallarını hazırlarken üretim operasyonlarınıza devam etmenizi sağlar. 

Etkin bir üretim akışı sürümünün geçerliliğini sona erdirmek için bitiş tarihini ayarlamanız gerekir. Bu anlamda devre dışı bırakma bir kuraldan çok bir istisnadır. 

Bu yordam için devre dışı bırakılabilir bir sürüme sahip bir üretim akışı gereklidir. Sürümün tamamen geçersiz olduğundan %100 emin olmadan bunu üretim ortamında denemeyin.


## <a name="deactivate-a-production-flow-version"></a>Üretim akışı sürümünü devre dışı bırakma
1. Üretim kontrolü > Kurulum > Yalın üretim akışı > Üretim akışları seçeneğine gidin.
2. Listede, istenen kaydı bulun ve seçin.
3. Listede, seçili satırdaki bağlantıya tıklayın.
4. Listede, istenen kaydı bulun ve seçin.
5. Devre Dışı Bırak'a tıklayın.
    * Bu üretim akışı sürümünün geçersiz olduğundan %100 emin değilseniz devam etmeyin. Tamam'a tıklamak tüm kanban kurallarını sona erdirir ve bu üretim akışı sürümünün tüm üretim ve stok yenileme faaliyetlerini anında durdurur.  
6. Tamam'a tıklayın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]