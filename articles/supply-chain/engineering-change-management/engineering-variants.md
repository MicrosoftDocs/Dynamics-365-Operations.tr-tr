---
title: Mühendislik ürünleri için çeşitler oluşturma
description: Bu makalede, mühendislik ürünleri için çeşitlerin nasıl oluşturulacağı açıklanmaktadır
author: t-benebo
ms.date: 06/08/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-08
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 08feb66dedfa79f5a21a7723a22f3bef883431e6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870767"
---
# <a name="generate-variants-for-engineering-products"></a>Mühendislik ürünleri için çeşitler oluşturma

[!include [banner](../includes/banner.md)]

Bu makalede, mühendislik ürünleri için çeşitlerin nasıl oluşturulacağı açıklanmaktadır.

## <a name="turn-variant-generation-for-engineering-products-on-or-off"></a>Mühendislik ürünleri için varyant oluşturma özelliğini açma veya kapatma

Bu makalede açıklanan işlev, sisteminiz için hem *Mühendislik Değişiklik Yönetimi* hem de *Mühendislik ürünleri için varyant oluşturma* özelliğinin açık olmasını gerektirir. Bu özelliklerin nasıl açılacağı veya kapatılacağı hakkında ayrıntılar için bkz. [Mühendislik değişiklik yönetimine genel bakış](product-engineering-overview.md).

## <a name="generate-one-or-more-new-variants-of-an-engineering-product"></a>Mühendislik ürününün bir veya daha fazla yeni çeşidini oluşturma

Var olan bir üründen bilgi kopyalamadan bir ürünün bir veya daha fazla yeni çeşidini oluşturabilirsiniz. Bu, aynı anda birkaç ürün çeşidi oluşturmanız gerektiği durumlarda kullanışlıdır.

Aşağıdaki yordamda, renk boyutunu içeren birden çok çeşidin nasıl oluşturulacağına dair bir örnek sağlanmaktadır.

1. **Serbest bırakılan ürünler** sayfasını açın (örneğin, **Mühendislik değişim yönetimi \> Ortak \> Serbest bırakılan ürünler**'e gidin).
1. Eylem Bölmesi'nde **Ürün** sekmesini açın ve **Yeni** grubundan **Mühendislik ürünü**'nü seçin.
1. **Yeni ürün** iletişim kutusu açılır. Uygun **Mühendislik kategorisi**'ni seçin.
1. Seçtiğiniz mühendislik kategoriniz çeşit boyutları içeriyorsa bunların değerlerini şimdi ayarlayabilirsiniz. Bu örnek için kategorinin bir **Renk** boyutu varsa bunu *Mavi* olarak ayarlayabilirsiniz.
1. Diğer ayarları gerektiği gibi yapın. Ürünü oluşturmak için **Tamam**'ı seçin.
1. Ürün ve mavi V-1 çeşidi oluşturulur ve yeni ürün şimdi açılır.
1. Ürün reçetesi (BOM) ekleyin ve gerektiği şekilde çeşide yönlendirin.
1. Eylem Bölmesi'nde **Ürün** sekmesini açın ve **Ana ürün** grubundan **Ürün boyutları**'nı seçin.
1. **Ürün boyutları** sayfası açılır. Bu sayfa, var olan her boyut için bir sekme içerir. Her sekmede, her ilgili boyut için destekleyeceğiniz tüm değerlere bir satır ekleyin. (Bu örnekte, **Renk** sekmesinde *Beyaz*, *Sarı* ve *Yeşil* için satırlar ekleyebilirsiniz).
1. Sayfayı kapatın ve ardından **Serbest bırakılan ürün çeşitleri**'ni seçin. Oluşturduğunuz ilk çeşidin (mavi V-1) görüntülendiğine dikkat edin.
1. Eylem Bölmesi'ndeki **Ürün çeşidi** sekmesinde, **Çeşit önerileri**'ni seçin.
1. **Çeşit önerileri** iletişim kutusunda, şu adımlardan birini izleyin:

    - İletişim kutusunun üst kısmında, kullanılabilir her boyut için bir bölüm bulunur. Her boyut için çeşit önerisi oluşturmak istediğiniz her değerin onay kutusunu seçin ve ardından araç çubuğunda **Öner**'i seçin. İlgili öneriler, **Önerilen çeşitler** bölümüne eklenir.
    - Kullanılabilen tüm boyut değerleri birleşimleri için çeşit önerileri oluşturmak üzere araç çubuğunda **Tümünü öner**'i seçin. Öneriler, **Önerilen çeşitler** bölümüne eklenir.

1. **Önerilen çeşitler** bölümünde, oluşturmak istediğiniz her çeşit için onay kutusunu seçin. Ardından, seçilen çeşitleri oluşturmak ve mühendislik şirketine yayınlamak için **Oluştur**'u seçin. Aşağıdaki koşullar geçerlidir:

    - Oluşturulan çeşitlerin hiçbirinin bir ürün reçetesi veya rotası olmaz.
    - Bu çeşitlerin öznitelikleri mühendislik kategorisinden gelen bilgiye göre varsayılan olur ve önceki çeşitten kopyalanmaz.

## <a name="generate-a-variant-as-a-copy-of-another-product-variant"></a>Başka bir ürün çeşidinin kopyası olarak bir çeşit oluşturma

Başka bir ürün çeşidini temel alarak bir ürünün çeşidini oluşturabilirsiniz. Ürün reçetesi (BOM) ve rota, kaynak ürün çeşidinden yeni çeşide kopyalanır. Bu, bir başlangıç ürün reçetesini temel alan ürün reçetesi oluşturmanın ve önceki çeşitteki değişiklikleri takip etmenin yardımcı olabileceği parçalı üretim ürünleri için faydalı olabilir. İzlenebilirliği korumak üzere sistem, yeni kopya oluşturmak için hangi çeşidin kopyalandığını kaydeder.

Aşağıdaki yordam, var olan bir çeşidin bir kopyasını oluşturarak renk boyutunu içeren yeni bir çeşidin nasıl oluşturulacağına dair bir örnek sağlar

1. **Serbest bırakılan ürünler** sayfasını açın (örneğin, **Mühendislik değişim yönetimi \> Ortak \> Serbest bırakılan ürünler**'e gidin).
1. Eylem Bölmesi'nde **Ürün** sekmesini açın ve **Yeni** grubundan **Mühendislik ürünü**'nü seçin.
1. **Yeni ürün** iletişim kutusu açılır. Uygun **Mühendislik kategorisi**'ni seçin.
1. Seçtiğiniz mühendislik kategoriniz çeşit boyutları içeriyorsa bunların değerlerini şimdi ayarlayabilirsiniz. Bu örnek için kategorinin bir **Renk** boyutu varsa bunu *Mavi* olarak ayarlayabilirsiniz.)
1. Diğer ayarları gerektiği gibi yapın. Ürünü oluşturmak için **Tamam**'ı seçin.
1. Ürün ve mavi V-1 çeşidi oluşturulur ve yeni ürün şimdi açılır.
1. Ürün reçetesi ekleyin ve gerektiği şekilde çeşide yönlendirin.
1. Ürün çeşidine gerektiği şekilde öznitelikler ekleyin.
1. Mavi V-1 ürün çeşidini bir mühendislik değişiklik emrine ekleyin.
1. **Etki**'yi *Yeni çeşit* olarak ayarlayın.
1. Yeni renk değerini seçin (örneğin *Beyaz*). Aşağıdaki koşulların geçerli olacağını unutmayın: 
    - Yeni çeşit, önceki çeşitten kopyalanmış bir ürün reçetesine ve rotaya sahiptir.
    - Yeni çeşit, önceki çeşitten kopyalanan özniteliklere sahiptir.
1. Değişiklik emrini onaylayın.
1. Değişiklik emrini işleyin. Sipariş işlendikten sonra yeni V-1 çeşidi oluşturulur ve mühendislik şirketine yayımlanır.
