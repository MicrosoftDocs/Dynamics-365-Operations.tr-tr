--- 
title: "Kaynak yeteneklerini tanımlama"
description: "Kaynak yetenekleri, kaynağın hangi işlemleri yapabileceğini açıklar."
author: sorenva
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 4a7d342eeb16fd76f2dde58151bfc7973de76e2d
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---
# <a name="define-resource-capabilities"></a>Kaynak yeteneklerini tanımlama

[!include[task guide banner](../../includes/task-guide-banner.md)]

Kaynak yetenekleri, kaynağın hangi işlemleri yapabileceğini açıklar. Planlama sırasında, her iş ve operasyonun gereklilikleri kullanılabilir kaynakların yetenekleriyle eşleştirilir. Bu görev kılavuzu, bir kaynak yeteneği oluşturup bunu bir kaynağa atamanıza yardımcı olur. Bu görevi oluşturmak için kullanılan demo veri şirketi USMF'dir.


## <a name="create-a-resource-capability"></a>Kaynak yeteneği oluşturma
1. Kaynak yetenekleri'ne gidin
2. Yeni'yi tıklatın.
3. Yetenek alanına, kaynak yeteneği kodunu yazın.
    * Belirli bir işlem için, kaynakların operasyonu gerçekleştirmek üzere sahip olması gereken yeteneği belirtmek için yetenek kodunu kullanın.  
4. Açıklama alanına yetenek açıklamasını girin.

## <a name="assign-capability-to-a-resource"></a>Bir kaynağa yetenek atama
1. Ekle öğesini tıklatın.
2. Kaynak alanına, kaynak kodunu yazın.
    * Kaynak yeteneği bir veya daha fazla kaynağa atanabilir.  
3. Bitiş alanına bir tarih girin.
    * Bu alanı, bir kaynağın yeteneğe sınırlı süre sahip olduğunu belirtmek için kullanabilirsiniz.  
4. Öncelik alanına bir sayı girin.
    * İşleri ve operasyonları planlarken, kaynakların öncelik sırasına göre seçilip seçilmeyeceğini belirtebilirsiniz. Bunu yapmayı seçtiğinizde, istenen tarih için işi veya operasyonu gerçekleştirebilecek birden fazla kaynak varsa, istenen yetenekle ilgili en düşük önceliğe sahip kaynak seçilir.  
5. Düzey alanına bir sayı girin.
    * Bir iş veya operasyonun belirli bir yetenek gerektirdiğini belirttiğinizde, gerekli olan en düşük düzeyi de belirtebilirsiniz. Aynı işi farklı hızda, güçte ve boyutta yapabilecek kaynakları birbirinden ayırmak için yetenek düzeyini kullanın.  


