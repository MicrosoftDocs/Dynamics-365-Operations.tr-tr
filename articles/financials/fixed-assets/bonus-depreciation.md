---
title: Bonus amortisman
description: "Bu makalede, bonus amortisman işlevselliğine bir genel bakış verilmektedir."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBonus
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3621
ms.assetid: 835ec594-744e-461c-a676-1b9abc094173
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 48d50cbba648beb9831e186cd160853abe79c4e4
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="bonus-depreciation"></a>Bonus amortisman

[!include[banner](../includes/banner.md)]


Bu makalede, bonus amortisman işlevselliğine bir genel bakış verilmektedir.

Ek amortisman için, kıymetin hizmete girdiği ve amortisman uygulandığı ilk yıl boyunca ek amortisman tutarları alabilirsiniz. Ek amortismanın, diğer her türlü amortisman hesaplamasından önce alınması gerekir. Bu nedenle, genel muhasebe işlemlerine nakil devre dışı olduğunda defterlerle ek amortismanı kullanmak en iyisidir. Genel muhasebeye nakledilmeyen defterler için geçmiş hareketleri silmek için **Genel muhasebe defterine nakledilmeyen hareketleri sil** seçeneğini kullanabilirsiniz. Daha önceden nakledilen amortisman hareketlerini silerek kıymet yaşam döngüsünde ek amortismanı barındırabilirsiniz. 

Ek amortismanı, teklif işlemini kullanarak hesaplayabilir veya el ile ek amortisman hareketleri oluşturabilirsiniz. Kıymet defteri için amortisman hareketleri veya amortisman düzeltme hareketleri varsa, ek amortisman hareketleri oluşturamazsınız.

Ek amortismanı hesaplamak için teklif işlemini kullandığınızda, varolan tüm ek hareketler temel hesaplamasına dahil. Bu hesaplama, kıymet için el ile girdiğiniz önceki ek amortismanları da içerir. 

Kıymet için alınacak birden fazla ek amortisman varsa öncelik dikkate alınır. Her ek, bir sonraki ekin kıymet temelini düşürür. Hurda değeri, ek amortisman hesaplamaları için kıymet temelinde hesaba katılmaz ve ek amortisman için amortisman yöntemi uygulanmaz. 

Şu anda Amerika Birleşik Devletleri'nde bazı mülkiyetler, Bölüm 179 mülkiyeti olarak görülür. Bölüm 179 kesintisini kullanarak, bazı mülkiyetlerin maliyetinin bir bölümünü veya tümünü (bir sınıra kadar) kurtarabilirsiniz. Mülkiyeti servise koyduğunuz yıl indirim yaparak maliyet kurtarabilirsiniz.

## <a name="example"></a>Örnek
Aşağıdaki ek amortismanlar bir kıymet defteriyle ilişkilidir:

-   **Bölüm 179:** 1000,00, Öncelik 1
-   **Serbest Bölge:** Yüzde 30, Öncelik 2

Kıymetin alım maliyeti 5.000,00'dir. Ek amortisman hesaplandığında ilk ek amortisman tutarı Bölüm 179 amortismanı için 1000,00'dir. 

Serbest Bölge amortismanı için sonraki ek amortisman tutarı şu şekilde hesaplanır: 

Alım maliyeti – 1000 (Bölüm 179 amortismanı) × yüzde 30 = 1.200 

Ek amortisman tutarı, kalan alım maliyetinden daha fazlaysa ek amortisman tutarı, ek amortisman hesaplaması sonucu veya kalan amortisman alım maliyetidir (hangisi düşük ise). 

Kalan alım maliyeti 0 (sıfır) veya sıfırdan düşükse ek amortisman hareketleri oluşturulmaz. 

Ek amortisman, teklif işlemi kullanılarak hesaplandığında kıymet defteriyle ilişkili uygun tüm ek amortisman kayıtları için bir ek amortisman hareketi oluşturulur. 

Sınırsız sayıda bonus amortisman kaydı oluşturabilirsiniz. Bu kayıtlar, kıymet grubu defterine atandıktan sonra kıymet defterine uygulanır. 

Bonus amortisman bir yüzde veya sabit bir tutar olarak girilir. Amortisman tekliflerini deftere naklettiğinizde, ek amortisman hareketleri amortisman defterine amortisman hareketlerinden ayrı hareketler olarak nakledilir.




