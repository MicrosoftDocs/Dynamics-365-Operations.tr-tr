---
title: Commerce'ta yeni ürün oluşturma
description: Bu makalede, Microsoft Dynamics 365 Commerce'te yeni bir ürünün nasıl oluşturulacağı açıklanmaktadır.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 654ba19b0bc96ab40c8c27106fd819faa85a4ce8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270194"
---
# <a name="create-a-new-product-in-commerce"></a>Commerce'ta yeni ürün oluşturma


[!include [banner](includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce'te yeni bir ürünün nasıl oluşturulacağı açıklanmaktadır.

## <a name="overview"></a>Genel Bakış

Ürün birincil olarak bir ürün numarası, adı ve açıklamasıyla tanımlanır. Bununla birlikte, bir ürünü veya hizmeti açıklamak için başka veriler de gereklidir:

## <a name="create-a-new-product"></a>Yeni ürün oluşturma

1. Gezinti bölmesinde, **Modüller \> Retail and commerce \> Ürünler ve kategoriler \> Kategoriye göre ürünler**'e gidin.
1. Eylem bölmesinde **Yeni**'yi seçin.
1. **Ürün türü** açılır listesinde, **Madde** veya **Servis**'i seçin.
1. **Ürün alt türü** açılır listesinde **Ürün**'ü (ürünün çeşitleri yoksa) veya **Ürün aslı**'nı (ürünün çeşitleri varsa) seçin.
1. **Ürün numarası** kutusuna, önceden doldurulmadıysa, bir ürün numarası girin.
1. **Ürün adı** kutusuna bir ürün adı girin.
1. **Arama adı** kutusuna bir arama adı girin.
1. **Perakende kategorisi** açılır listesinde uygun bir kategori seçin.
1. Ürün bir set ise **Ürün seti** için **Evet**'i seçin.
1. Ürün alt türü ürün aslı ise, **Ürün boyut grubunu** desteklenen çeşitleri içerecek şekilde ayarlayın. Seçenekler şunlardır: **Renk**, **Boyut**, **Stil** ve **Konfigürasyon**. Gerekirse ek ürün boyutu grupları oluşturabilirsiniz.
1. **Yapılandırma teknolojisi** açılır listesinde uygun bir seçenek belirtin.
1. **Tamam**'ı seçin.

Aşağıdaki resimde bir eklenen ürün örneği gösteriliyor.

![Ürün oluşturma.](media/create-new-product.png)

Ürün eklendikten sonra, **Ürün açıklaması**, **Çeşit grupları**, **Boyut grupları**, **Ürün öznitelikleri** ve **İlgili ürünler** gibi ek veriler ayarlayabilirsiniz.

Aşağıdaki resimde bir ürünün ek ayrıntıları gösterilmektedir.

![Ürün ayrıntıları.](media/create-new-product-2.png)

### <a name="create-product-variants"></a>Ürün çeşitleri oluştur

Ürün alt türü **Ürün aslı** ise, belirli çeşitler oluşturulması gerekecektir. 

Ürün çeşitleri oluşturmak için bu adımları izleyin.

1. Eylem bölmesinde **Ürün çeşitleri**'ni seçin.
1. Eylem bölmesinde çeşit grupları seçildiyse, **Çeşit önerileri*'ni seçin.
1. Ürün için desteklemek istediğiniz çeşitleri seçin.
1. **Oluştur**'u seçin.

## <a name="release-a-product"></a>Bir ürünü serbest bırakma

Bir ürünü satmak için önce tüzel bir kişiliğe serbest bırakılması gerekir.

1. Ürün sayfasından, **Ürünleri serbest bırak**'ı seçin.

    ![Ürünü serbest bırakma.](media/create-new-product-3.png)

1. Serbest bırakılacak ürünü ve ardından **İleri**'yi seçin.

    ![Serbest bırakılacak ürünü seçme.](media/create-new-product-4.png)

1. Serbest bırakılacak ürün çeşitleri kümesini ve ardından **İleri**'yi seçin.

    ![Serbest bırakılacak çeşitleri seçme.](media/create-new-product-5.png)

1. Tüzel kişiliği ve ardından **İleri**'yi seçin.

    ![Tüzel kişilik seçme.](media/create-new-product-6.png)

1. **Bitir**'i seçin.

    ![Ürün serbest bırakma işlemini bitirme.](media/create-new-product-7.png)

## <a name="configure-a-released-product"></a>Serbest bırakılmış bir ürünü yapılandırma

Ürün serbest bırakıldıktan sonra, ürün için fiyat eklemeyi içeren ek yapılandırma gerektirir.

1. Gezinti bölmesinde, **Modüller \> Retail and commerce \> Ürünler ve kategoriler \> Kategoriye göre serbest bırakılan ürünler**'e gidin.
1. Serbest bırakılan ürünle ilgili ürün kategorisi düğümünü ve ardından ürün listesinden ürünü seçin.
1. Eylem bölmesinde, **Düzenle**'yi seçin.
1. **Satınalma** bölümünde, **Birim**, **Fiyat** ve **Miktar**'ı içeren tüm gerekli özellikleri yapılandırın.
1. Eksik alanlar için herhangi bir hata raporlanmamasını sağlamak için, eylem bölmesinde, **Doğrula**'yı seçin.
1. Eylem bölmesinde, **Kaydet**'i seçin.

Aşağıdaki resimde, serbest bırakılmış bir ürün için yapılandırma örneği gösterilmektedir.

![Serbest bırakılmış ürünü yapılandırma.](media/create-new-product-8.png)

## <a name="additional-resources"></a>Ek kaynaklar

[Tüzel kişilik oluştur](channels-legal-entities.md)

[Çeşit grubu oluşturma](create-variant-group.md) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
