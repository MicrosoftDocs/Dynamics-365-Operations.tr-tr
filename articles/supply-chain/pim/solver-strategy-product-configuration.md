---
title: Ürün yapılandırması için Çözücü stratejisi
description: Bu konu çözücü stratejisini ürün yapılandırmasının performansını artırmak üzere nasıl kullanabileceğinizi açıklar.
author: cvocph
manager: AnnBe
ms.date: 02/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCCreateProductConfigurationModel, PCProductConfigurationModelListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 16a11c5030f5641abb87830f5221ded5bb7ac038
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560313"
---
# <a name="solver-strategy-for-product-configuration"></a>Ürün yapılandırması için Çözücü stratejisi

[!include [banner](../includes/banner.md)]

Bu konu çözücü stratejisini ürün yapılandırmasının performansını artırmak üzere nasıl kullanabileceğinizi açıklar.

Çözücü stratejileri kavramı ilk olarak Microsoft Dynamics AX 2012 R2 için Toplu güncelleştirme 7'de (CU7) kullanılmıştır. Microsoft Dynamics AX 2012 R3 ve Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 için kümülatif güncelleştirme 8 (CU8) içinde genişletildi.

Çözücü stratejisi kavramı şu anda aşağıdaki stratejileri içermektedir:

- Varsayılan
- Önce minimal etki alanları
- Yukarıdan aşağıya
- Z3

## <a name="solver-strategy"></a>Çözüm stratejisi 

Ürün yapılandırma modeli [kısıtlama memnuniyet sorunu (CSP)](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf) olarak formüle edilebilir. Microsoft Solver Foundation (MSF), ürün yapılandırma modellerinden kullanılabilen CSP'leri çözmek için iki tür çözücü stratejisi sağlar. Bu çözücü stratejileri, sorun çözüldüğünde CSP'lerin değişkenlerinin dikkate alındığı sırayı belirlemek üzere kullanılan [buluşsal yöntemlere](https://techterms.com/definition/heuristic) dayanır. Buluşsal yöntemler, bir sorun veya sorunlar sınıfı çözüldüğünde performansı belirgin şekilde etkileyebilir.

Finance and Operations'ta, ürün yapılandırma modellerine yönelik çözücü stratejisi buluşsal yöntemlerle hangi çözücünün kullanıldığını belirler. **Varsayılan**, **En az etki alanları önce** ve **Yukarıdan aşağıya** stratejileri MSF'den iki çözücüyü kullanırken, **Z3** stratejisi Z3 çözücüsü kullanır. 

Gerçek müşteri uygulaması çalışmaları, bir ürün yapılandırma modeline yönelik çözücü stratejisindeki bir değişikliğin, yanıt sürelerini dakikalardan mili saniyelere düşürebildiğini göstermiştir. Bu nedenle, ürün yapılandırma modeliniz için en etkili stratejisi bulmak için farklı çözücü stratejileri denemek faydalıdır.

## <a name="change-the-settings-for-the-solver-strategy"></a>Çözücü stratejisi ayarlarını değiştirme

Çözücü stratejisini değiştirmek için, Eylem Bölmesindeki **Ürün yapılandırma modeli** sayfasında **Model özellikleri**'ni seçin. Sonra, **Model ayrıntılarını düzenle** iletişim kutusunda, bir çözücü stratejisi seçin.

[![Çözüm stratejisini değiştirme](./media/solver-strategy.png)](./media/solver-strategy.png)

Şu anda, sınırlama tabanlı ürün yapılandırması için en etkili olacak çözücü stratejisini otomatik olarak algılayan bir mantık yoktur. Bu nedenle, çözücü stratejilerini tek tek denemeniz gerekir.

Aşağıdaki tablo çeşitli senaryolarda kullanılacak çözücü stratejisi hakkında öneriler sağlar.

| Çözüm stratejisi      | Stratejiyi bu senaryoda kullan |
|----------------------|-----------------------------------|
| Varsayılan              | **Varsayılan** strateji tablo sınırlamalarına dayanan modelleri çözmek üzere en iyi duruma getirilmiştir. Müşteri uygulaması çalışmaları, bu stratejinin tablo sınırlamalarının yoğun şekilde kullanıldığı senaryolarda en etkili strateji olduğunu göstermiştir. |
| Önce minimal etki alanları | **Önce minimal etki alanları** ve **Yukarıdan aşağıya** stratejileri yakından ilişkilidir. Müşteri uygulama çalışmaları, **Yukarıdan aşağıya** stratejisinin **Önce minimal etki alanları** stratejisinden daha iyi performans gösterdiğini ortaya koymuştur. Ancak, **Önce minimal etki alanları** stratejisi, geriye doğru uyumluluk açısından üründe tutulmuştur. Bu iki çözücü stratejisinin de tablo sınırlamalarının kullanılmadığı çeşitli aritmetik ifadeler içeren çözüm modellerinde daha etkili olduğu görülmüştür. Ancak, bazı durumlarda, **Varsayılan** strateji bu iki stratejiden daha iyi performans gösterir. Bu nedenle, her bir strateji denemeyi unutmayın. |
| Yukarıdan aşağıya             | **Önce minimal etki alanları** ve **Yukarıdan aşağıya** stratejileri yakından ilişkilidir. Müşteri uygulama çalışmaları, **Yukarıdan aşağıya** stratejisinin **Önce minimal etki alanları** stratejisinden daha iyi performans gösterdiğini ortaya koymuştur. Ancak, **Önce minimal etki alanları** stratejisi, geriye doğru uyumluluk açısından üründe tutulmuştur. Bu iki çözücü stratejisinin de tablo sınırlamalarının kullanılmadığı çeşitli aritmetik ifadeler içeren çözüm modellerinde daha etkili olduğu görülmüştür. Ancak, bazı durumlarda, **Varsayılan** strateji bu iki stratejiden daha iyi performans gösterir. Bu nedenle, her bir strateji denemeyi unutmayın. |
| Z3                   | Varsayılan çözücü stratejisi olarak **Z3** stratejisini kullanmanızı öneririz. Performans ve ölçeklenebilirlik hakkında endişeleriniz olması durumunda, diğer stratejileri değerlendirebilirsiniz. |

## <a name="additional-resources"></a>Ek kaynaklar

[Ürün yapılandırma modeli oluşturma](build-product-configuration-model.md)

[Buluşsal yöntemler](https://techterms.com/definition/heuristic)

[Sınırlama Memnuniyet Sorunu](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf)
