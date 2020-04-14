---
title: " Bağlılık ödül puanlarını tanımlama"
description: Bu yordam bağlılık ödül puanlarının nasıl belirleneceğini gösterir.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailLoyaltyRewardPoints
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e40ebcbf3ab1befc641ae34571a8b974bd0425a
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140888"
---
# <a name="define-loyalty-reward-points"></a> Bağlılık ödül puanlarını tanımlama

[!include [banner](../includes/banner.md)]

Bu yordam bağlılık ödül puanlarının nasıl belirleneceğini gösterir. Bir bağlılık programı ayarlamadan önce bağlılık ödül puanları ayarlamanız gerekir. Bu yordam, USRT demo veri şirketini kullanır.

1. Retail and Commerce >Müşteriler > Bağlılık > Bağlılık programı ödül puanları'na gidin.
2. Yeni'yi tıklatın.
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

