---
title: "Gider ilkelerini tanımla"
description: "Microsoft Dynamics 365 for Finance and Operations içerisinde gider raporları ve seyahat talepleri girerken ve gönderirken çalışanlarınızın izlemesi gereken gider ilkelerini tanımlayabilirsiniz."
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 3b2a28fe6acf03e52c292048a797ce997f58bcce
ms.contentlocale: tr-tr
ms.lasthandoff: 03/26/2018

---

# <a name="expense-policies"></a>Gider ilkeleri

[!include [banner](../includes/banner.md)]

Çalışanlarınızın gider raporlarını ve seyahat taleplerini girerken veya gönderirken izlemeleri gereken ilkeleri tanımlayabilirsiniz.         
Gider ilkelerinin uygulanması giderleri etkili bir şekilde yönetmenize yardımcı olabilir.         

Örneğin, New York City için bir gecelik otel giderlerinin 250 ABD dolarını aşamayacağını belirten bir ilke ayarlayabilirsiniz.       
Bir çalışan oda ücretinin bu tutarı aştığı bir seyahat talebi veya gider raporu gönderirse, sistem çalışanı        
gider için ilke tutarının aşıldığı konusunda bilgilendirir. İlkeyi tanımlarken çalışanın alacağı iletiyi        
yapılandırabilirsiniz.      
        
Üç farklı ilke türü tanımlayabilirsiniz:         
        
- Uyarı – Çalışanın bir gider raporu veya seyahat talebi göndermesine izin verir ancak gider sonra raporlanmak üzere tüm        
  onaylayıcılar için işaretlenir.        

- Hata – Çalışanın gider raporu veya seyahat talebini göndermeden önce ilke ile uyum sağlar hale getirmesini gerektirir.       
 
  - Mazeret – Çalışanın veya bir yöneticini, gider raporunu veya seyahat talebini girmeden önce ilke tutarını aşmasına dair bir mazeret girmesini gerektirir.        
 
  Ayrıca, gider ilkelerinin yürürlükte olacağı bir tarih aralığı da ayarlayabilirsiniz. Örneğin Danimarka ile New York City arasındaki      
  uçuşlar için bilet ücreti tatil dönemlerinde pahalı olabilir. New York City'ye yapılacak uçuşlar için maliyeti      
  5000 DKK ile sınırlayacak bir gider kuralı oluşturabilir ve bu kuralın 15 Mart ile      
  15 Eylül arasında geçerli olacağını belirtebilirsiniz.

