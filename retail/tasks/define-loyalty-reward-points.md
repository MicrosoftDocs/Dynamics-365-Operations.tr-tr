--- 
title: " Bağlılık ödül puanlarını tanımlama"
description: "Bu yordam bağlılık ödül puanlarının nasıl belirleneceğini gösterir."
author: scott-tucker
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 56f11484d960ab22aefef359c18f71d54dc50071
ms.contentlocale: tr-tr
ms.lasthandoff: 07/28/2017

---
# <a name="define-loyalty-reward-points"></a> Bağlılık ödül puanlarını tanımlama

[!include[task guide banner](../includes/task-guide-banner.md)]

Bu yordam bağlılık ödül puanlarının nasıl belirleneceğini gösterir. Bir bağlılık programı ayarlamadan önce bağlılık ödül puanları ayarlamanız gerekir. Bu yordam, USRT demo veri şirketini kullanır.

1. Retail and commerce > Customers > Loyalty > Loyalty reward points (Perakende ve ticaret > Müşteriler > Bağlılık > Bağlılık programı ödül puanları) menüsüne gidin.
2. Yeni'ye tıklayın.
3. Ödül puanı kodu alanına bir değer girin.
4. Açıklama alanına bir değer girin.
5. Ödül puanı türü alanında bir seçenek belirleyin.
    * Ödül puanlarının en yakın tam sayıya yuvarlanmasını istiyorsanız Miktar seçeneğini seçin. Ödül puanlarının para birimi yuvarlama kurallarına göre yuvarlanmasını istiyorsanız Tutar seçeneğini seçin. Miktar'ı seçerseniz, bu yordamın bir sonraki adımına atlayın...  
6. Para birimi alanına bir değer yazın.
    * Tutar türü ödül puanları için, verilen tüm puanlar seçili para birimine sahip olacaktır. Miktar türü ödül puanları için bu alan kullanılmaz; bu adımı atlayın.  
7. Kullanılabilir onay kutusunu işaretleyin veya işaretini kaldırın.
8. Derecelendirme kullanma alanına bir sayı girin.
    * Derecelendirme kullanma, ürün ödemeleri için iki veya daha fazla kullanılabilir ödül puanı olduğunda kullanılır. İki ödül puanı aynı derecelendirme kullanma durumuna sahipse, daha düşük sayıda puana sahip olan kullanılır.  
9. Sonra erme süresi değer alanına bir sayı girin.
    * Ödül puanlarının süresi, puanlar verildikten sonra belirtilen sayıda gün, ay veya yıl geçtiğinde sonra erer. '0' değeri bağlılık ödül puanının süresiz olduğunu belirtir.  
10. Sona erme süresi birimi alanında bir seçenek seçin.
11. Kaydet'e tıklayın.


