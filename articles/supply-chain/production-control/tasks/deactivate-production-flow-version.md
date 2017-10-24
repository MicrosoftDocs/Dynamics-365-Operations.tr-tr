--- 
title: "Üretim akışı sürümünü devre dışı bırakma"
description: "Etkin bir üretim akışı sürümüne artık ihtiyaç duyulmuyorsa devre dışı bırakılabilir."
author: cvocph
manager: AnnBe
ms.date: 10/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 4a7eee6617e12d59a3d06207f5f6b58c93e28240
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="deactivate-a-production-flow-version"></a>Üretim akışı sürümünü devre dışı bırakma

[!include[task guide banner](../../includes/task-guide-banner.md)]

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


