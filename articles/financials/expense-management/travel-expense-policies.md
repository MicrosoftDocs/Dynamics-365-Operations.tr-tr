---
title: Gider ilkelerini tanımla
description: Microsoft Dynamics 365 for Finance and Operations içinde çalışanlarınızın gider raporlarını ve seyahat taleplerini girerken veya gönderirken izlemeleri gereken gider ilkeleri tanımlayabilirsiniz.
author: ryansandness
manager: AnnBe
ms.date: 04/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6923a4d5420cd768d1b0da24eab406033c17fd67
ms.sourcegitcommit: 06c8dc5bc4e1c41f68e1cda141d61529768be958
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/22/2019
ms.locfileid: "1594948"
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

## <a name="policy-tips"></a>İlke ipuçları
Burada, gider yönetimi için yeni ilkeler oluşturmanıza yardımcı olabilecek birkaç öneri verilmiştir. 
* İlkelerin geçerlilik tarihi vardır ve ilke giderin gerçekleştiği tarihten sonraki bir tarihle oluşturulduysa geçerli olmaz. Örneğin, en fazla $50 yemek gideri kullanmaya zorlamak için bugün yeni bir ilke oluşturuyorsanız, dün girilen tüm mevcut giderler bu ilkeye göre denetlenmez.
* Dökümü yapılabilecek bir gider kategorisi için ilke oluştururken, gider satırı türü için bir koşul eklemeyi düşünün. Makbuz gerektirme gibi bazı ilkeler, dökümü yapılan satırlar için anlamlı olmayabilir ve yalnızca başlık satırına veya dökümü oluşturulmamış bir satıra uygulanmalıdır. 

## <a name="when-to-evaluate-policies"></a>İlkeler ne zaman değerlendirilir

Gider yönetimi parametrelerinde, bir satır kaydedildiğinde veya gider raporu gönderildiğinde gider yönetim ilkelerini değerlendirmek için bir seçenek vardır. Bir satır kaydedildiğinde değerlendirmeyi seçerseniz bu, kullanıcıların gider raporlarını bir kerede tamamlamak için yapmaları gerekenler hakkında daha önceden görünürlüğe sahip olmasını sağlar. Aksi takdirde, iş akışına gönderim sırasında doğrulamanın sonda gerçekleşmesi durumunda ilke değerlendirmesini erteleyebilir ve zamandan tasarruf edebilirsiniz.
