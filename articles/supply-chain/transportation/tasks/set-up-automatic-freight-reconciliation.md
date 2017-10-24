--- 
title: "Otomatik navlun mutabakatını ayarlama"
description: "Bu yordam, otomatik navlun mutabakatı için verilerin nasıl ayarlanacağını gösterir."
author: BibiSp
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 97f0c4d8fe06ab2fc252b9543cb688306214c79f
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-automatic-freight-reconciliation"></a>Otomatik navlun mutabakatını ayarlama

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, otomatik navlun mutabakatı için verilerin nasıl ayarlanacağını gösterir. Bu, genellikle ambar yöneticisi tarafından yapılır. Bu yordamı USMF demo veri şirketinde kullanabilirsiniz.


## <a name="set-up-the-freight-bill-type"></a>Navlun fatura türünü ayarlama
1. Taşımacılık yönetimi > Kurulum > Navlun mutabakatı > Navlun faturası türü'ne gidin.
    * Navlun fatura kodu, navlun faturalarının ve taşıyıcı faturalarının nasıl eşleştirilmesi gerektiğini tanımlar.  
2. Yeni'ye tıklayın.
3. Navlun faturası türü alanına bir değer yazın.
4. Altyapı derlemesi alanına "Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer" yazın.
    * Bu, altyapı kodu kitaplığını eşleştiren standart Taşıma yönetimidir.  
5. Altyapı sınıfı alanına "Microsoft.Dynamics.Ax.Tms.dll" yazın.
    * Bu, altyapı sınıfını eşleştiren standart Taşıma yönetimidir.  
6. Yeni'ye tıklayın.
7. Açıklama alanında, navlun faturası ve taşıyıcı faturasında eşleşmesi gereken değeri seçin.  
8. Eşleşme gerekli alanında Evet'i seçin.
    * Bu alanı Evet olarak ayarlarsanız bu, Tanımlama alanında seçilen değerin, navlun faturası ve taşıyıcı fatura ile eşleşmesi gerektiği anlamına gelir. Hayır olarak ayarlarsanız alan bunların birinde boş kalabilir.  
9. Kaydet'e tıklayın.

## <a name="set-up-the-freight-bill-type-assignment"></a>Navlun fatura türü atamasını ayarlama
1. Sayfayı kapatın.
2. Taşımacılık yönetimi > Kurulum > Navlun mutabakatı > Navlun fatura türü atamaları öğesine gidin.
    * Navlun fatura türü atamaları, belirli bir taşıyıcı için hangi navlun faturası türünün kullanıldığını tanımlamak için kullanılır.   
3. Yeni'ye tıklayın.
4. Mod alanına bir değer girin veya seçin.
5. Sevkiyat taşıyıcısı alanına bir değer girin veya seçin.
6. Navlun fatura türü alanında daha önce oluşturduğunuz navlun fatura türünü seçin.
7. Sayfayı kapatın.

## <a name="set-up-the-audit-master"></a>Ana denetimi ayarlama
1. Taşımacılık yönetimi > Kurulum > Navlun mutabakatı > Ana denetim'e gidin.
    * Ana denetim, otomatik navlun mutabakatı için tolerans sınırlarını tanımlar. Navlun faturası ve taşıyıcı faturasında parasal tutarların ne kadar değiştiğini belirtir ve yine de mutabakatın gerçekleşmesine izin verir. Ayrıca tutarsızlıkların nasıl ele alınacağını da tanımlar.  
2. Yeni'ye tıklayın.
3. Ana denetim kodu alanına bir değer girin.
4. Sevkiyat taşıyıcısı alanında önceden seçtiğiniz gibi sevkiyat taşıyıcısını seçin.
5. Navlun fatura türü alanında daha önce oluşturduğunuz navlun fatura türünü seçin.
6. Tolerans bölümünü genişletin.
7. Minimum tolerans düzeyi alanına bir sayı girin.
8. Maksimum tolerans düzeyi alanına bir sayı girin.
9. Sonuç bölümünü genişletin.
10. Fazla ödeme neden kodu alanına bir değer girin veya seçin.
    * Parasal tutarlar navlun faturasında ve taşıyıcı faturasında farklılık gösterirse fazla ödeme ve eksik ödeme neden kodları, farklılıklar tolerans düzeyleri içinde kaldığı sürece farklılıkların kaydedilmesinin gerekli olduğu hesapları belirtir.  
11. Eksik ödeme neden kodu alanına bir değer girin veya seçin.
12. Sayfayı kapatın.


