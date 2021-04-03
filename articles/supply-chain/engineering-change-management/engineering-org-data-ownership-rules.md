---
title: Mühendislik şirketleri ve veri sahipliği kuralları
description: Bu konu, ürünlerin ana verilerinin merkezi olarak oluşturulduğundan ve korunduğundan emin olmak için bir veya daha fazla mühendislik şirketini nasıl kullanabileceğinizi açıklamaktadır. Mühendislik şirketi, mühendislik ürünlerine ve mühendislik ile ilgili verilerin sahibi olan şirketi temsil eder.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgEngineeringOrganization
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 837960a628ef03df4d73909e96713e256d0f5e60
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5262321"
---
# <a name="engineering-companies-and-data-ownership-rules"></a>Mühendislik şirketleri ve veri sahipliği kuralları

[!include [banner](../includes/banner.md)]

## <a name="engineering-companies-and-operational-companies"></a>Mühendislik şirketleri ve operasyonel şirketler

Ürünlerin ana verilerinin merkezi olarak oluşturulduğundan ve korunduğundan emin olmak için bir veya daha fazla *mühendislik şirketi* kullanabilirsiniz. Mühendislik şirketi, mühendislik ürünleri ve mühendislik ile ilgili verilerin sahibidir. Bu, aynı zamanda bir şirket olan mevcut *tüzel kişiliğe* (temel alarak) daima bağlıdır. Bu bağlantıyla, sistem, mühendislik şirketinde mühendislik ürünleri ile ilgili tüm veriler için merkezi bir giriş noktası oluşturur. Bu merkezi giriş noktasında, mühendislik ürünleri oluşturulur ve mühendislik ile ilgili veriler korunur. Mühendislik ürünleri ve mühendislik ile ilgili veriler, diğer tüzel kişilikler olan *operasyonel şirketler* tarafından serbest bırakılacaktır. (Serbest bırakımı yönetimi hakkında daha fazla bilgi için bkz. [Ürün yapılarını serbest bırakma](release-product-structure.md).) Bu operasyonel şirketler, mühendislik şirketi tarafından tasarlanan için mühendislik verilerini kullanır. Tüm lojistik verileri, her mühendislik şirketi ve operasyonel şirket tarafından yerel olarak tutulur.

Bir mühendislik şirketi oluşturmak için **Mühendislik değişikliği yönetimi \> Kurulum \> Mühendislik kuruluşları**'na gidin. **Yeni**'yi seçin, mühendislik şirketi için bir ad girin ve temel aldığı şirketi (tüzel kişiliği) seçin.

Harici ürün yaşam döngüsü yönetimi (PLM) sistemleriyle tümleştirme yapıyorsanız harici bir şirket olacak bir departman (şirket türü) oluşturmanız gerekir.

## <a name="engineering-product-categories-and-engineering-companies"></a>Mühendislik ürünü kategorileri ve mühendislik şirketleri

*Mühendislik ürünü kategorileri*, mühendislik ürünlerinin şirketinizin iş kurallarına göre oluşturulmasını ve gerektiği şekilde davranmasını sağlamaya yardımcı olur. Mühendislik ürünü kategorileri hakkında daha fazla bilgi için bkz. [Mühendislik sürümleri ve mühendislik ürünü kategorileri](engineering-versions-product-category.md).

Her mühendislik ürünü kategorisi belirli bir mühendislik şirketine aittir ve yalnızca o şirkete ait ürünler oluşturabilir. Benzer şekilde, bir mühendislik ürününü koruma hakkı, o ürünün mühendislik ürünü kategorisiyle ilişkilendirilmiş olan şirkete aittir.

## <a name="data-that-is-owned-by-the-engineering-company"></a>Mühendislik şirketinin sahip olduğu veriler

Mühendislik şirketi, mühendislik ile ilgili verilerin sahibi olduğundan, aşağıdaki süreçleri kontrol eder:

- **Mühendislik ürünleri oluşturma:** Her mühendislik şirketi yalnızca sahip olduğu mühendislik ürünü kategorisine göre yeni mühendislik ürünleri oluşturabilir. Bazı durumlarda, operasyonel şirketler bu ürünlerle ilgili kendi yerel verilerini korur.
- **Mühendislik sürümleri oluşturma:** Bir şirket yeni bir mühendislik ürünü oluşturduğunda, sistem otomatik olarak ürün için bir ilk mühendislik sürümünü oluşturur. Yalnızca sahibi olan mühendislik şirketi ürünün yeni sürümlerini oluşturabilir.
- **Mühendislik öznitelikleri oluşturma ve bakımını yapma:** Bir şirket yeni bir mühendislik ürünü oluşturduğunda, sistem otomatik olarak ürüne mühendislik öznitelikleri ekler. Yalnızca sahibi olan mühendislik şirketi bu özniteliklerin değerlerini oluşturabilir ve bakımını yapabilir. Mühendislik öznitelikleri hakkında daha fazla bilgi için bkz. [Mühendislik öznitelikleri ve mühendislik özniteliği araması](engineering-attributes-and-search.md).
- **Mühendislik sürümlerine bağlı ürün reçetelerinin oluşturulması ve bakımı:** Sahibi olan mühendislik şirketi, bir ürün reçetesini bir mühendislik ürün sürümüne doğrudan bağlayabilir. Bu ürün reçeteleri diğer tüzel kişiliklere serbest bırakıldığında, ürün reçetelerindeki mühendislik verilerinde yapılan değişiklikler aşağıdaki yollarla sınırlıdır:

    - Operasyonel şirket, serbest bırakılmış ürün reçetesi satırlarını kaldıramaz.
    - Ürün reçetesi satırlarındaki mühendislik alanları operasyonel şirket için salt okunur özelliklidir. Diğer tüm alanlar lojistik uygulama alanlarıdır ve operasyonel şirket tarafından düzenlenebilir.
    - Operasyonel şirket aynı ürün reçetesine ürün reçetesi satırı ekleyebilir. Bu şekilde, ambalaj malzemeleri veya yağlama sıvıları gibi yerel eklemeler yapabilir.
    - Operasyonel şirket tümüyle yeni, yerel bir ürün reçetesi ekleyebilir. Bu değişiklik, örneğin serbest bırakma sırasında herhangi bir ürün reçetesi sağlanamadığı durumlarda gerekli olabilir. Operasyonel şirket bu yerel ürün reçetelerinin sahibi olur ve onlara bakım yapar. Serbest bırakma yönetimi hakkında daha fazla bilgi için bkz. [Ürün yapılarını serbest bırakma](release-product-structure.md).
    - Mühendislik şirketi ürün reçetesini güncelleştirdiğinde, tüm yerel ürün reçeteleri ve ürün reçetesi satırları korunur.

- **Mühendislik sürümlerine bağlı rotaların oluşturulması ve bakımı:** Sahibi olan mühendislik şirketi, bir rotayı her mühendislik sürümüne doğrudan bağlayabilir. Bu rotalar diğer tüzel kişiliklere serbest bırakıldığında, rotalardaki mühendislik verilerinde yapılan değişiklikler aşağıdaki yollarla sınırlıdır:

    - Diğer tüzel kişilikler rotalardaki mühendislik verilerini kaldıramaz.
    - Diğer tüzel kişilikler rotaya işlem ekleyebilir. Böylece, yerel rota adımları ekleyebilirler.
    - Operasyonel şirketler tümüyle yeni, yerel bir rotalar ekleyebilir. Bu değişiklik, örneğin serbest bırakma sırasında rotaları dahil etmediğiniz durumlarda gerekli olabilir. Operasyonel şirketler bu yerel rotaların sahibi olur ve onlara bakım yapar. Serbest bırakma yönetimi hakkında daha fazla bilgi için bkz. [Ürün yapılarını serbest bırakma](release-product-structure.md).
    - Mühendislik şirketinden güncelleştirmeler tekrar rotalarda yeniden serbest bırakıldığında yerel olarak yapılan tüm değişiklikler korunur.

- **Mühendislik belgelerinin oluşturulması ve bakımı:** Mühendislik şirketi, her bir mühendislik sürümüne mühendislik belgeleri ekleyebilir.

    - Bu belgeler diğer tüzel kişiliklere serbest bırakıldığında, belgelerin operasyonel şirket tarafından kaldırılmaya karşı korunur.
    - Diğer tüzel kişilikler tamamen yeni yerel belgeler ekleyebilirler. Operasyonel şirket bu yerel belgelerin sahibi olur ve onlara bakım yapar.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]