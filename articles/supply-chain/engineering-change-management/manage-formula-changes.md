---
title: Formüllerdeki ve içeriklerindeki değişiklikleri yönetme
description: Bu makalede, formül yönetiminin nasıl yapılması ve üretim ana verilerinin işlenmesine yapılan değişikliklerin nasıl yönetileceği açıklanmaktadır.
author: t-benebo
ms.date: 05/19/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-05-19
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 8105ebc7f3698a6baaa04b6548dac18a7bf81a47
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904086"
---
# <a name="manage-changes-in-formulas-and-their-ingredients"></a>Formüllerdeki ve içeriklerindeki değişiklikleri yönetme

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management'un işlem üretme yeteneklerini kullanıyorsanız, aşağıdaki değişiklikleri yönetmek için ilgili formül yönetimi yeteneklerini de kullanabilirsiniz:

- **Formül ve planlama öğeleri:** Formüllerdeki bileşenlerdeki ve bunların ortak ürünlerinde ve yan ürünlerinde yapılan değişiklikleri yönetin.
- **Ortak ürünler ve yan ürünler:** Ortak ürünlerin ve yan ürünlerin miktarlarını ve diğer bilgilerini bir formülde düzenleyin.
- **Ağırlık öğeleri:** Fiili ağırlık öğelerine yapılan değişiklikleri yönetin.

## <a name="turn-this-feature-on-or-off"></a>Bu özelliği açma veya kapatma

Bu makalede açıklanan işlev, sisteminiz için hem *Mühendislik Değişiklik Yönetimi* hem de *Formüllerdeki ve formül içeriklerindeki değişiklikleri yönet* özelliğinin açık olmasını gerektirir. Bu özelliklerin nasıl açılacağı veya kapatılacağı hakkında ayrıntılar için bkz. [Mühendislik değişiklik yönetimine genel bakış](product-engineering-overview.md).

## <a name="feature-naming-conventions"></a>Özellik adlandırma kuralları

Supply Chain Management kullanıcı arabiriminde (UI) ve belgelerinde, değişiklik yönetimi işlevselliği genellikle *mühendislik değişim yönetimi* olarak adlandırılır ve yönetilebilir ürünler genellikle *mühendislik ürünleri* olarak adlandırılır. Bu terminoloji genellikle proses üretimi için formüllerin yönetimiyle ilişkili olmasa da, mühendislik değişim yönetimini basit bir değişiklik yönetimi olarak düşünmeli ve mühendislik ürünlerini sürümlü ürünler olarak düşünmelisiniz.

## <a name="work-with-formula-change-management-features"></a>Formül değişikliği yönetimi özellikleriyle çalışma

Aşağıdaki listede, mühendislik değişikliği yönetimi özelliklerinin formül yönetimi için nasıl uygulandığı özetlenmektedir. Ayrıca daha fazla bilgiye bağlantılar sağlar. Formül değişikliği yönetimi mühendislik değişikliği yönetimi özelliklerinden yararlandığı için, mühendislik değişim yönetiminin genel olarak nasıl çalıştığını öğrenmelisiniz, böylece formüllerinizi ve bileşenlerini yönetmek için kullanabilirsiniz.

- **Merkezi ürün veri yönetimi** – Yönetilen bir sürüm süreciyle, doğru ve alakalı ürün verilerinin kuruluş genelindeki kullanıcılar tarafından kullanılabilmesini sağlayan bir kuruluş kurun. Daha fazla bilgi için bkz. [Mühendislik şirketleri ve veri sahipliği kuralları](engineering-org-data-ownership-rules.md).
- **Ürün sürüm oluşturma** – Ürün sürümleri aracılığıyla ürünlerdeki değişiklikleri izleyin ve tedarik zincirinin tüm aşamalarında ürünü kontrol edin. Bu şekilde, formülasyonlarınızdaki değişiklikleri izleyebilirsiniz. Daha fazla bilgi için bkz. [Mühendislik sürümleri ve mühendislik ürünü kategorileri](engineering-versions-product-category.md).
- **Ürün yaşam döngüsü yönetimi** – Kuruluş genelinde ürün verilerinin görünürlüğünü yönetin ve tedarik zincirinin her aşamasında ürün sürümlerinin kullanılabilirliğini kontrol edin. Ürün sürümü belirli iş süreçlerinde kullanılabilecekse ayrıntılı denetiminiz vardır ve iş gereksinimlerinize uygun kendi yaşam döngüsü eyaletlerinizi oluşturabilirsiniz. Daha fazla bilgi için bkz. [Ürün yaşam döngüsü durumları ve hareketler](product-lifecycle-state-transactions.md).
- **Formül değişiklik Yönetimi** – Kuruluşunuzdaki kullanıcılar formüllerde değişiklik isteyebilir. Önerilen değişikliklerin etkisini değerlendirmek ve belgelemek için değişiklik emirlerini kullanın. Değişiklik sürecini ve ürünün yeni sürümlerinin ve formülünün serbest bırakılması için iş akışları ekleyin. Daha fazla bilgi için bkz. [Mühendislik ürünlerindeki değişiklikleri yönetme](engineering-change-management.md).
- **Hazır olma denetimi** – Tüm gerekli ürün verilerinin ürün bırakılmadan önce tam olarak girildiğinden emin olmak için sistem denetimlerini ve kullanıcı kılavuzunu (soru formları ve denetim listeleri) kullanın. Daha fazla bilgi için bkz. [Ürün hazırlığı](product-readiness.md).
- **Geliştirilmiş ürün sürüm işlevselliği** – Bir ürünün tam olarak tanımlanan sürümlerini ve bir kuruluştan (yasal tüzel kişiliği) diğer hukuk varlıklarına yayınlayın. Ürün bilgilerinin yayınlanmadan önce incelenmesi veya düzenlenmesi gerekip gerekmediğine bile karar verebilirsiniz. Daha fazla bilgi için bkz. [Ürün yapılarını serbest bırakma](release-product-structure.md).

Önceki listede bağlanan makalelerin çoğunun ürün reçetelerini (BOM) temel alan örnekler sağlamasını unutmayın. Ancak, formüller benzer şekilde çalışır. Formülleri ve ürün reçetelerini yönetmek için değişiklik yönetimini (veya yalnızca formül değişikliği yönetimi) kullandığınızda bilmeniz faydalı olan bazı ek kavramlar şunlardır:

- Her bir [ürün mühendisliği kategorisi](engineering-versions-product-category.md) için, üretim tipini (ürün reçetesi, formül veya planlama maddesi) belirtebilirsiniz. Ayrıca, bu kategoriyi kullanan ürünler için fiili ağırlık desteğinin gerekli olup olmadığını da belirtebilirsiniz.
- Ortak ürünler ve yan ürünler, mühendislik ürünleri değildir. Bu nedenle, bunlar sürümlenmiş değildir. Bunları değiştirmeniz gerekiyorsa, yeni bir ürün oluşturmanız yeterlidir. Bu yaklaşım bakımın daha kolay olmasını sağlar.
- Ürün reçeteleri olan ve alt formül maddeleri olan son maddeleri yönetebilirsiniz. İşlevler, ürün reçeteleri içeren formüller ve/veya formüller içeren ürün reçeteleri birleşimleri için çalışacaktır.
