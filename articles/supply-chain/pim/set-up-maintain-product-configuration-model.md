---
title: Ürün yapılandırma modelini ayarlama
description: Bu makalede, bir ürün yapılandırma modelinin ayarlanmasına ve oluşturulmasına yönelik adımlar açıklanmaktadır.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCProductConfigurationModelListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 4051
ms.assetid: 00df5537-b148-4e32-a248-3e35876ad4e1
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e6562353a96c2a69c255d20c3f2084c9c3f99bd3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011309"
---
# <a name="set-up-a-product-configuration-model"></a>Ürün yapılandırma modelini ayarlama

[!include [banner](../includes/banner.md)]

Bu makalede, bir ürün yapılandırma modelinin ayarlanmasına ve oluşturulmasına yönelik adımlar açıklanmaktadır.

| Görev                                                        | Açıklama                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bir ana ürün oluşturun.                                    | **Ana ürün** listesinden bir ana ürün oluşturun. Ana ürünü ilgili tüm şirketlere serbest bırakın. Bir ürün yapılandırma modeli sürümü veya bir alt bileşen olarak kullanılan bir ana ürün için yapılandırma teknolojisi olarak **Kısıtlama tabanlı yapılandırma** seçilmeli ve yapılandırma boyutu yalnızca bir ürün boyutu grubu için seçilmelidir. |
| Bileşenleri oluşturun.                                          | **Bileşenleri** sayfasında bileşenleri oluşturun. Bileşenler ürün yapılandırma modelinin yapı taşlarıdır ve birden fazla ürün yapılandırma modelinde yeniden kullanılabilir.                                                                                                                                                                                                                      |
| Öznitelik türleri oluşturun.                                     | **Öznitelik türleri** sayfasında öznitelik türleri oluşturun. Öznitelik türleri, ürün yapılandırma modellerinde kullanılan tüm özniteliklere ilişkin veri türleri kümesini belirler. **Boole**, sabit listeyle **Metin** ve aralığa sahip **Tamsayı** öznitelikleri, ürün yapılandırma modelini temel alan bir ürün varyantı yapılandırırken kullanabileceğiniz değer kümesini listeler.       |
| Bir ürün yapılandırma modeli oluşturun.                       | **Yeni ürün yapılandırma modeli** sayfasında bir ürün yapılandırma modeli oluşturun.                                                                                                                                                                                                                                                                                                              |
| Ürün yapılandırma modeline öznitelikler ekleyin.            | **Kısıtlama tabanlı ürün yapılandırma modeli ayrıntıları** sayfasındaki **Öznitelikler** hızlı sekmesinde bir öznitelik oluşturun. Öznitelikler, ürün yapılandırma modelinin özelliklerini açıklar.                                                                                                                                                                                                       |
| Ürün yapılandırma modeline kısıtlamalar ekleyin.           | **Kısıtlama tabanlı ürün yapılandırma modeli ayrıntıları** sayfasındaki **Kısıtlamalar** hızlı sekmesinde kısıtlamalar oluşturun. Kısıtlamalar, bir ürün yapılandırmasının uyması gereken sınırlardır. Kısıtlamalar ifade kısıtlamaları ya da tablo kısıtlamaları olabilir.                                                                                                                                 |
| Bir ürün yapılandırma modeline alt bileşenler ekleyin.         | **Kısıtlama tabanlı ürün yapılandırma modeli ayrıntıları** sayfasındaki **Alt bileşenler** hızlı sekmesinde alt bileşenler oluşturun. Alt bileşenler bileşenlerle ilgilidir ve alt bileşeni temsil eden maddelere bağlıdır.                                                                                                                                                                       |
| Bir ürün yapılandırma modeline kullanıcı gereksinimleri ekleyin.     | Kullanıcı gereksinimleri alt bileşenlere benzer, ancak bir maddeye başvuruda bulunmaz. Kullanıcı gereksinimlerini, hayali ürün reçetesi olarak düşünebilirsiniz. Doğrudan kullanıcı gereksinimi altına yerleştirilen ürün reçetesi satırları veya rota operasyonları, ana bileşen içinde daraltılır.                                                                                                                       |
| Ürün yapılandırma modeline ürün reçetesi satırları ekleyin.             | **Kısıtlama tabanlı ürün yapılandırma modeli ayrıntıları** sayfasındaki **Ürün reçetesi satırları** hızlı sekmesinde ürün reçetesi satırları oluşturun. Ürün reçetesi satırları, bir ürün varyantı oluşturmak için gerekli olan bölümü temsil eder.                                                                                                                                                                                                 |
| Bir ürün yapılandırma modeline rota operasyonları ekleyin.      | **Kısıtlama tabanlı ürün yapılandırma modeli ayrıntıları** sayfasındaki **Rota operasyonları** hızlı sekmesinde rota operasyonları oluşturun. Rota operasyonları, bir ürün varyantı yapmak için uygulanan adım dizesindeki bir adımı temsil eder.                                                                                                                                                    |
| Ürün yapılandırma modeli için etkin bir sürüm oluşturun. | **Sürümler** sayfasındaki ürün yapılandırma modelinin etkin bir sürümünü oluşturun. Sürüm, bir ürün yapılandırma modeli ile ana ürün arasındaki ilişkidir. Etkin sürümü olan bir ürün yapılandırma modeli satış siparişinden, satış teklifinden, satınalma siparişinden veya üretim emrinden yapılandırılabilir.                                                               |
| Bir ürün yapılandırma modelini test edin.                         | Ürün yapılandırma modeli **Kısıtlama tabanlı ürün yapılandırma modeli ayrıntıları** sayfasından veya **Ürün yapılandırma modelleri listesi** sayfasından test edin. Ürün yapılandırma modelleri testi, sipariş işleme sırasında oluşan ürün modeli yapılandırma işlemi benzetimi yapar.                                                                                                |
| Ürün yapılandırma modeli şablonu oluşturun.                | **Yapılandırma şablonları** sayfasında bir ürün yapılandırma modeli şablonu oluşturun. Ürün yapılandırma şablonu, ürün yapılandırma modelindeki özniteliklere ilişkin değerleri içerir. **Satırı yapılandırma** sayfasındaki öznitelik değerlerini seçin. Ürün modeli yapılandırma sırasında bir ürün modeli yapılandırma şablonu yüklemeyi seçebilirsiniz.                                                   |
| Bir maddeyi yapılandırın.                                          | Ürün yapılandırma modelleri satış siparişinden, satış teklifinden, satınalma siparişinden veya üretim emrinden yapılandırılabilir.                                                                                                                                                                                                                                                                           |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]