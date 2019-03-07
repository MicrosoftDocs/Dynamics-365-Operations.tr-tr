---
title: Üretim akışı sürümünü devre dışı bırakma
description: Etkin bir üretim akışı sürümüne artık ihtiyaç duyulmuyorsa devre dışı bırakılabilir.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 091cafd02bd568323e586373fc8b0f983afee343
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "340764"
---
# <a name="deactivate-a-production-flow-version"></a>Üretim akışı sürümünü devre dışı bırakma

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

