---
title: Değerlendirme profilleri
description: Bu konuda, değerlendirme profilleri için veri ayarlama yöntemi açıklanmaktadır.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3c54e7457813774027debd301d9a0bf8ce1b6d47
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646443"
---
# <a name="rating-profiles"></a>Değerlendirme profilleri

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
1. Yeni değerlendirme profili için alanları ayarlayın. Bu alanlar, bu konunun önceki bölümünde açıklandığı gibi, **Değerlendirme profilleri** sayfasındaki alanlara karşılık gelir.

> [!NOTE]
> **Sevkiyat taşıyıcıları** sayfasında oluşturulan profiller, **Değerlendirme profilleri** sayfasında da gösterilir.
