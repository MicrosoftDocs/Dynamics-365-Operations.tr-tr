---
title: Sabit kıymete bir ek girme
description: Bu prosedür, mevcut bir sabit kıymeti eklemenin nasıl yapılacağını gösterir.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetAddition
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fe1a1d4db696ac013afee05b697b301383232134
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839965"
---
# <a name="enter-an-addition-to-a-fixed-asset"></a>Sabit kıymete bir ek girme

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu prosedür, mevcut bir sabit kıymeti eklemenin nasıl yapılacağını gösterir. Sabit kıymet eklerinin amacı, yalnızca, bir kıymetin madde eklemelerini, bakımını veya iyileştirmelerini izleme ve bilgi amaçlıdır. Sabit kıymet değerindeki veya servis ömründeki değişikliklerin ayrı ayrı yapılması gerekir.   

Prosedürde Muhasebeci rolü ve USMF adlı tüzel kişilik için demo verileri kullanılmaktadır.

1. Gezinti bölmesinde **Modüller > Sabit kıymetler > Sabit kıymetler > Sabit kıymetler günlüğü**'ne gidin.
2. Listede, eklemede kullanılacak sabit kıymeti bulup seçin.
3. Listede, seçili satırdaki bağlantıya tıklayın.
4. Eylem Bölmesinde, **Sabit kıymet**'e tıklayın.
5. **Sabit kıymet ekleri**'ne tıklayın.
6. **Yeni**'ye tıklayın.
7. **Ad** alanına bir değer yazın.
8. **Alım tarihi** alanında, ek satınalma veya servisin tarihini ayarlayın.
9. **Birim maliyeti** alanına madde bakım veya diğer geliştirmelerin maliyetini girin.
10. **Miktar** alanına bir sayı girin. Toplam maliyetin sabit kıymet değeri üzerinde hiçbir etkisi yoktur; yalnızca izleme ve bilgi amaçlıdır. Maliyet büyük harfle yazılırsa, ayrıca bir değer artırma düzeltmesi hareketinin nakledilmesi gerekir.  
11. **Genel** sekmesine tıklayın.

    * Ekleme kıymetin servis ömrünü artırıyorsa, **Servis ömrünü artırır**'ı **Evet** olarak ayarlayın.  
    * Bu alan yalnızca bilgi amaçlıdır. Servis ömrünü uzatmak için, kıymetin Değer modellerindeki ve/veya Amortisman defterlerindeki Servis ömrünü değiştirin.  

