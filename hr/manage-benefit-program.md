---
title: "Tanımlamak ve yararları program yönetmek"
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
translationtype: Human Translation
ms.sourcegitcommit: 81b5c9056001b26c33b2b42a95711ff5b50243e6
ms.openlocfilehash: 9d00d8f6dfa075f53473af31c257deb57c9efa86
ms.lasthandoff: 03/31/2017


---

# <a name="define-and-manage-a-benefits-program"></a>Tanımlamak ve yararları program yönetmek

İnsan kaynakları bir organizasyonun sunduğu veya çalışanları için yürürlüğe koyduğu kazançları, kesintileri ve çalışanların tazminat planlarını oluşturmak ve bunları yönetmek için kullanılabilecek bir takım araçlar sağlar. Bu konu bir yönetme yararları hakkında bilgi sağlar.

<a name="benefit-setup"></a>Kazanç ayarı
-------------

Çalışanları bir kazanca kaydetmeden önce her bir kazanç için öğeler oluşturmanız gerekir. Bu öğeler benzer kazanç planlarını birleştirir ve indirim oranları ve muhasebe ayrıntıları vb. gibi varsayılan ayarları tanımlar. Bu ayarların birçoğu, çalışanlar daha sonra kazanda kaydedildiklerinde ayarlanabilir. Bir organizasyon, her bir kazanç planı için birden fazla kayıt seçeneği sunabilir veya bir çalışan, plana kaydolmaktan feragat edebilir. 

[![Avantaj işlem akışı](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)

## <a name="benefit-elements"></a>Kazanç öğeleri
Kazançlar oluşturmadan ve çalışanları bu kazançlara kaydetmeden önce, kazancı meydana getirecek öğeleri tanımlamanız gerekir: tür, plan ve seçenekler.

-   **Tür** – Örneğin tıbbi veya otopark vb. gibi belirli bir kazanç için bir planlar topluluğudur.
-   **Plan** – Bir sağlayıcıdan sözleşme yapılarak alınan, özel bir kazançtır.
-   **Seçenek** – Sadece çalışanlar veya çalışanlar ve eşleri/partnerleri gibi kapsam düzeyi.

Bir organizasyon göz tedavileri veya diş tedavileri vb. gibi her bir kazanç türü için çalışanlarına bir veya birden fazla plan sunabilir. Her bir plan için organizasyon farklı seçenekler sunabilir. Örneğin, çalışanlar yıllık kazançlarının bir, iki veya üç katına kadar ilave hayat sigortası kapsamı satın alabilirler. Her bir plan kombinasyonu ve seçenekler, çalışanların kaydolabileceği bir kazanç haline gelir. 

[![PIC fayda](./media/benefit-pic.png)](./media/benefit-pic.png)

## <a name="eligibility"></a>Uygunluk
Bir işverenin sunduğu çeşitli kazanç türleri için çalışanın uygunluğunu belirleyen çok sayıda faktör bulunmaktadır. Microsoft Dynamics 365 işlemleri için bir faydası oluşturduğunuzda, bu kazanç için uygulanan uygunluk türünü ayarlayabilirsiniz. 

Size bir yararı tüm çalışanlar için erişilebilir kılabilirsiniz. Örneğin, bazı şirketler, park geçişleri tüm çalışanlara kazançlar sunar. Bu kazancı oluşturduğunuzda uygunluğu **Tüm çalışanlar uygundur** olarak ayarlarsınız. 

Garnishments ve vergi tutucusuna, gibi diğer yararları için uygunluk uygulanmaz. Whey bu faydaları türlerini oluşturun, uygunluk ayarlamak **uygunluk işlemini atlamak**. 

Son olarak, kural tabanlı uygunluk yararı olabilir. Örneğin, şirket çalışanları için hayat Sigortası yararı iki tür sunar. Tüm tam zamanlı çalışanların hayat Sigortası planı uygun ise üst düzey çalışanlar bir hayat Sigortası planı için uygundur. İşlemleri için Dynamics 365 executive tüm çalışanları bulmak amacıyla bir yararı uygunluk kural ve tüm tam zamanlı çalışanların bulmak için başka bir kural oluşturmak ve bu kurallara uygun bir kazançla uygulayın.

## <a name="enrollment"></a>Kayıt
Organizasyonunuzun sunduğu kazançları oluşturduktan ve uygunluğu belirledikten sonra çalışanları bu kazançlara kaydedebilirsiniz. Kazançları tek bir çalışanı kaydedebileceğiniz gibi, tek bir süreçle çok sayıda çalışanı bir veya daha fazla sayıdaki kazanca da kaydedebilirsiniz. 

Bazı durumlarda bir organizasyon belirli kazançları durdurur. Bu durumda, kazancın ve kaydolmadığınız çalışanları güncelleştirmeniz gerekir. Toplu yararı sona erme bu yararı, aynı anda hem bir yararı, hem de çalışan kayıtlarına sona erme tarihini değiştirmenize olanak tanır. Ayrıca, bir kazanca kayıtlı birden fazla çalışanı seçebilir ve kapsamlarının bitiş tarihini değiştirebilirsiniz. 

Benzer şekilde, toplu kazanç uzatma özelliği, bir kazancı başlangıçta planladığınızdan daha uzun süre sunmaya karar verdiğinizde hem bu kazancın hem de bu kazanca kayıtlı çalışanların geçerlilik bitiş tarihini uzatmanıza izin verir.

<a name="see-also"></a>Ayrıca bkz.
--------

[Benefit eligibility policies](benefit-eligibility-policies.md)


