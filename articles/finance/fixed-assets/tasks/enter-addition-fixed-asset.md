---
title: Sabit kıymete bir ek girme
description: Bu prosedür, mevcut bir sabit kıymeti eklemenin nasıl yapılacağını gösterir.
author: moaamer
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetAddition
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2d23f60963466249b332b759ee72ebc8387aee4b
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/05/2022
ms.locfileid: "8713063"
---
# <a name="enter-an-addition-to-a-fixed-asset"></a>Sabit kıymete bir ek girme

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
