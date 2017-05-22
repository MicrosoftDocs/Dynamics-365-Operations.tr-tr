---
title: "Bir kazançlar programı tanımlama ve yönetme"
description: "İnsan kaynakları bir organizasyonun sunduğu veya çalışanları için yürürlüğe koyduğu kazançları, kesintileri ve çalışanların tazminat planlarını oluşturmak ve bunları yönetmek için kullanılabilecek bir takım araçlar sağlar. Bu makalede bir kazanç yönetiminin nasıl kurulacağı hakkında bilgiler verilmiştir."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmBenefitEligibilityDetail, HcmBenefitSelection, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: aa28ece8b18fba11bfa4af2fe785fbe5047965e3
ms.contentlocale: tr-tr
ms.lasthandoff: 04/25/2017


---

# <a name="define-and-manage-a-benefits-program"></a>Bir kazançlar programı tanımlama ve yönetme

[!include[banner](includes/banner.md)]


İnsan kaynakları bir organizasyonun sunduğu veya çalışanları için yürürlüğe koyduğu kazançları, kesintileri ve çalışanların tazminat planlarını oluşturmak ve bunları yönetmek için kullanılabilecek bir takım araçlar sağlar. Bu konuda bir kazanç yönetiminin nasıl kurulacağı hakkında bilgiler verilmiştir.

<a name="benefit-setup"></a>Kazanç kurulumu
-------------

Çalışanları bir kazanca kaydetmeden önce her bir kazanç için öğeler oluşturmanız gerekir. Bu öğeler benzer kazanç planlarını birleştirir ve indirim oranları ve muhasebe ayrıntıları vb. gibi varsayılan ayarları tanımlar. Bu ayarların birçoğu, çalışanlar daha sonra kazanda kaydedildiklerinde ayarlanabilir. Bir organizasyon, her bir kazanç planı için birden fazla kayıt seçeneği sunabilir veya bir çalışan, plana kaydolmaktan feragat edebilir. 

[![Kazanç süreç akışı](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)

## <a name="benefit-elements"></a>Kazanç öğeleri
Kazançlar oluşturmadan ve çalışanları bu kazançlara kaydetmeden önce, kazancı meydana getirecek öğeleri tanımlamanız gerekir: tür, plan ve seçenekler.

-   **Tür** – Örneğin tıbbi veya otopark vb. gibi belirli bir kazanç için bir planlar topluluğudur.
-   **Plan** – Bir sağlayıcıdan sözleşme yapılarak alınan, özel bir kazançtır.
-   **Seçenek** – Sadece çalışanlar veya çalışanlar ve eşleri/partnerleri gibi kapsam düzeyi.

Bir organizasyon göz tedavileri veya diş tedavileri vb. gibi her bir kazanç türü için çalışanlarına bir veya birden fazla plan sunabilir. Her bir plan için organizasyon farklı seçenekler sunabilir. Örneğin, çalışanlar yıllık kazançlarının bir, iki veya üç katına kadar ilave hayat sigortası kapsamı satın alabilirler. Her bir plan kombinasyonu ve seçenekler, çalışanların kaydolabileceği bir kazanç haline gelir. 

[![kazanç fotoğrafı](./media/benefit-pic.png)](./media/benefit-pic.png)

## <a name="eligibility"></a>Uygunluk
Bir işverenin sunduğu çeşitli kazanç türleri için çalışanın uygunluğunu belirleyen çok sayıda faktör bulunmaktadır. Microsoft Dynamics 365 for Operations'ta bir kazanç oluşturduğunuzda, bu kazanç için geçerli uygunluk türünü ayarlayabilirsiniz. 

Kazançları tüm çalışanlar için kullanılabilir kılabilirsiniz. Örneğin, bazı şirketler park izinlerini tüm çalışanlara bir yan kazanç olarak sunar. Bu kazancı oluşturduğunuzda uygunluğu **Tüm çalışanlar uygundur** olarak ayarlarsınız. 

Maaş haczi ve vergi koyma gibi diğer kazançlar için, uygunluk uygulanmaz. Bu tür kazançlar oluşturduğunuzda, uygunluğu **Uygunluk işlemini atla** olarak ayarlarsınız. 

Son olarak, kazanç uygunluğu kural tabanlı olabilir. Örneğin, şirket çalışanları için iki türde hayat sigortası kazancı sunar. Yönetici personel bir hayat sigortası planında hak sahibiyken, diğer tüm tam zamanlı personel diğer hayat sigortası planına hak sahibidir. Dynamics 365 for Operations içerisinde, tüm yönetici personeli bulmak için bir kural ve diğer tüm tam zamanlı personeli bulmak için başka bir kural oluşturabilirsiniz ve bunları daha sonra uygun kazanca uygulayabilirsiniz.

## <a name="enrollment"></a>Kayıt
Organizasyonunuzun sunduğu kazançları oluşturduktan ve uygunluğu belirledikten sonra çalışanları bu kazançlara kaydedebilirsiniz. Kazançları tek bir çalışanı kaydedebileceğiniz gibi, tek bir süreçle çok sayıda çalışanı bir veya daha fazla sayıdaki kazanca da kaydedebilirsiniz. 

Bazı durumlarda bir organizasyon belirli kazançları durdurur. Bu durumda, kazancı ve katılım gösteren çalışanları güncelleştirmeniz gerekir. Toplu yarar sona erdirme, hem kazancın hem de bu kazanç için çalışan katılımlarının bitiş tarihini aynı zamanda değiştirmenize olanak tanır. Ayrıca, bir kazanca kayıtlı birden fazla çalışanı seçebilir ve kapsamlarının bitiş tarihini değiştirebilirsiniz. 

Benzer şekilde, toplu kazanç uzatma özelliği, bir kazancı başlangıçta planladığınızdan daha uzun süre sunmaya karar verdiğinizde hem bu kazancın hem de bu kazanca kayıtlı çalışanların geçerlilik bitiş tarihini uzatmanıza izin verir.

<a name="see-also"></a>Ayrıca bkz.
--------

[Kazanca uygunluk ilkeleri](benefit-eligibility-policies.md)



