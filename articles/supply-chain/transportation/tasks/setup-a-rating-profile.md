---
title: Değerlendirme profilleri
description: Bu makalede, değerlendirme profilleri için veri ayarlama yöntemi açıklanmaktadır.
author: Weijiesa
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: weijiesa
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1f7408574187ddb099181bd2566c46c52307f603
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850495"
---
# <a name="rating-profiles"></a>Değerlendirme profilleri

[!include [banner](../../includes/banner.md)]

Değerlendirme profili, lojistik sözleşmesine (ancak yasal sözleşmeye değil) benzer. Bunlar, yükler için taşıma tarifelerini belirlemek amacıyla kullanılır. 

Her değerlendirme profili bir sevkiyat taşıyıcısı için benzersizdir. Profilde, sevkiyat taşıyıcısını bir ana oranla ilişkilendirirsiniz. Ana oran, oran tabanı atamasını ve oran tabanını tanımlar. Oran tabanı, taşıyıcının oranını belirler.

Var olan tüm değerlendirme profillerinin özetini gösteren bir genel sayfa kullanarak bir değerlendirme profili ayarlayabilirsiniz. Alternatif olarak, doğrudan sevkiyat taşıyıcısından bir değerlendirme profili ayarlayabilirsiniz. Her iki durumda da, değerlendirme profili için ayarladığınız bilgiler aynıdır.

## <a name="create-or-edit-a-rating-profile-on-the-rating-profiles-page"></a>Değerlendirme profilleri sayfasında bir değerlendirme profili oluşturun veya düzenleyin.

**Değerlendirme profilleri** sayfasında, kullanılabilir tüm değerlendirme profillerini gözden geçirebilirsiniz. Ayrıca, var olan profilleri düzenleyebilir ve yeni profiller oluşturabilirsiniz.

1. **Taşıma Yönetimi \> Kurulum \> Değerlendirme \> Değerlendirme profili**'ne gidin.
1. Eylem bölmesinde, kılavuza yeni değerlendirme profili eklemek için **Yeni**'yi veya var olan bir profili düzenlemek için **Düzenle**'yi seçin.
1. Yeni veya var olan değerlendirme profili satırında, aşağıdaki alanları ayarlayın:

    - **Değerlendirme profili**: Değerlendirme profili için benzersiz bir tanımlayıcı (kod) girin.
    - **Ad**: Değerlendirme profili için tanımlayıcı bir ad girin.
    - **Sevkiyat taşıyıcısı**: Sevkiyat taşıyıcısı seçin. Ayarlamakta olduğunuz değerlendirme profili, seçilen taşıyıcı için **Sevkiyat taşıyıcıları** sayfasında da gösterilir.
    - **Tesis** ve **Ambar**: Tesis ve ambar seçin.
    - **Değerlendirme Altyapısı** Değerlendirme profili için değerlendirme altyapısını seçin.
    - **Ana değerlendirme** Değerlendirme profili için ana değerlendirmeyi seçin. Ana oranı oran tabanı türü ve oran tabanı tanımlamak için kullanabilirsiniz. Daha fazla bilgi için bkz. [Ana oranları ayarlama](set-up-rate-masters.md).
    - **Yoldaki süre altyapısı**: Değerlendirme profili için yoldaki süresi altyapısını seçin.
    - **Taşıyıcı yakıt dizini**: Değerlendirme profili için taşıyıcı yakıt dizinini seçin.
    - **Geçerlilik başlangıç tarihi ve saati** ve **Geçerlilik bitiş tarihi ve saati**: Değerlendirme profilinin etkin olması gereken dönemi tanımlayın.

1. Eylem bölmesinde, **Kaydet**'i seçin.

## <a name="create-a-rating-profile-directly-on-the-shipping-carriers-page"></a>Sevkiyat taşıyıcıları sayfasında değerlendirme profili oluşturma

1. **Taşımacılık yönetimi \> Kurulum \> Taşıyıcılar \> Sevkiyat taşıyıcıları** seçeneğine gidin.
1. Listeden sevkiyat taşıyıcısı seçin.
1. Değerlendirme profili oluşturmak için **Değerlendirme profilleri** hızlı sekmesinde, **Yeni**'yi seçin.
1. Yeni değerlendirme profili için alanları ayarlayın. Bu alanlar, bu makalenin önceki bölümünde açıklandığı gibi, **Değerlendirme profilleri** sayfasındaki alanlara karşılık gelir.

> [!NOTE]
> **Sevkiyat taşıyıcıları** sayfasında oluşturulan profiller, **Değerlendirme profilleri** sayfasında da gösterilir.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]