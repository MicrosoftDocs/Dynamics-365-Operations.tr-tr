---
title: Otomatik navlun mutabakatını ayarlama
description: Bu yordam, otomatik navlun mutabakatı için verilerin nasıl ayarlanacağını gösterir.
author: ShylaThompson
manager: AnnBe
ms.date: 10/16/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSFreightBillType, TMSFreightBillTypeAssignment, TMSCarrierCodeLookup, DefaultDashboard, TMSAuditMaster
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7551805b7b942b042a0f0f8d2ce408d0bac19d06
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146293"
---
# <a name="set-up-automatic-freight-reconciliation"></a>Otomatik navlun mutabakatını ayarlama

[!include [banner](../../includes/banner.md)]

Bu yordam, otomatik navlun mutabakatı için verilerin nasıl ayarlanacağını gösterir. Bu, genellikle ambar yöneticisi tarafından yapılır. Bu yordamı USMF demo veri şirketinde kullanabilirsiniz.


## <a name="set-up-the-freight-bill-type"></a>Navlun fatura türünü ayarlama
1. Taşımacılık yönetimi > Kurulum > Navlun mutabakatı > Navlun faturası türü'ne gidin.
    * Navlun fatura kodu, navlun faturalarının ve taşıyıcı faturalarının nasıl eşleştirilmesi gerektiğini tanımlar.  
2. Yeni'ye tıklayın.
3. Navlun faturası türü alanına bir değer yazın.
4. Altyapı grubu alanına "Microsoft.Dynamics.Ax.Tms.dll" yazın.
    * Bu, altyapı kodu kitaplığını eşleştiren standart Taşıma yönetimidir.  
5. Altyapı sınıfı alanına "Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer" yazın.
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

