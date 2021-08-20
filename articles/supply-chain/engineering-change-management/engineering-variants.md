---
title: Mühendislik ürünleri için çeşitler oluşturma
description: Bu konuda, mühendislik ürünleri için çeşitlerin nasıl oluşturulacağı açıklanmaktadır
author: t-benebo
ms.date: 06/08/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-08
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 57eda6a833df6ff8e91c006bbc5096554eff6c503a8b7ba2bd0b13e2f8e98f56
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766175"
---
# <a name="generate-variants-for-engineering-products"></a>Mühendislik ürünleri için çeşitler oluşturma

[!include [banner](../includes/banner.md)]

Bu konuda, mühendislik ürünleri için çeşitlerin nasıl oluşturulacağı açıklanmaktadır.

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
1. Sayfayı kapatın ve **Serbest bırakılan ürün çeşitleri**'ni seçin. İlk oluşturulan çeşidin (beyaz V-1) görüntülendiğini unutmayın.
1. **Çeşit önerileri**'ni seçin.
1. Sistem, oluşturulan renk değerlerine sahip çeşitleri önerir (örneğin, beyaz V-1, sarı V-1 ve yeşil V-1).
1. Önerilen çeşitleri seçin ve mühendislik şirketi için çeşitleri serbest bırakmak üzere **Tamam**'ı seçin. Aşağıdaki koşulların geçerli olacağını unutmayın: 
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
