---
title: Mağaza seçicisi modülü
description: Bu konu mağaza seçici modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 03/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 460d05ca29d5b8da70a971a649d9edd786f7260d
ms.sourcegitcommit: 15c5ec742d648c5f3506d031a2ab6150dcbae348
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2020
ms.locfileid: "3378220"
---
# <a name="store-selector-module"></a>Mağaza seçicisi modülü

[!include [banner](includes/banner.md)]

Bu konu mağaza seçici modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.

## <a name="overview"></a>Özet

"Çevrimiçi satın al, mağazadan al" "(BOPIS) müşteri senaryosu için bir depolama Seçicisi modülü kullanılır. Bir ürünün malzeme çekme için uygun olduğu mağazaların listesini ve her mağazanın depolama saatlerini ve ürün envanterini gösterir.

Mağaza Seçicisi modülü, mağazaları bulmak için bir ürün bağlamı ve bir arama konumu gerektirir. Arama konumu olmadığında, müşteri izin vermek koşuluyla müşterinin tarayıcı yerleşimi varsayılan olur. Modül, müşterinin yakındaki mağazaları bulmak için bir konum (posta kodu veya şehir ve il) girmesine olanak sağlayan bir giriş kutusu içerir.

Mağaza seçici modülü Bing Haritalar Coğrafi kodlama uygulama programlama arayüzü (API) ile tümleştirilmiştir ve bu sayede konumu bir enlem ve boylama dönüştürür. Bir Bing Haritalar API anahtarı gereklidir ve Dynamics 365 Commerce içinde Commerce paylaşılan parametreler sayfasına eklenmelidir.

Ürün Ayrıntıları sayfasındaki (PDP) bir ürünün malzeme çekme için uygun olduğu mağazaları görüntülemek için, bir satın alma kutusu modülüne Mağaza Seçici modülü eklenebilir. Bir sepet modülüne da eklenebilir. Bir sepet modülüne eklendiğinde, mağaza seçici modülü her bir sepet çizgisi öğesi için toplama seçeneklerini görüntüler. Ek olarak, özel kodlamaya sahip bu modül Uzantılar ve özelleştirmeler aracılığıyla diğer sayfalara veya modüllere eklenebilir.

BOPIS senaryosunun çalışması için, ürünlerin "müşteri malzeme çekme" teslim moduyla konfigüre edilmesi gerekir. Aksi durumda, modül ilgili sayfalarda gösterilmez. Teslimat modunun konfigüre edilmesine ilişkin ayrıntılar için bkz. [Teslimat modları ayarla](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Aşağıdaki resimde, PDP üzerinde kullanılan bir Mağaza Seçicisi modülü örneği gösterilmektedir.

![Mağaza seçici modülü örneği](./media/BOPIS.PNG)

## <a name="store-selector-module-usage-in-e-commerce"></a>e-Ticarette mağaza seçici modül kullanımı

- Ürün Ayrıntıları sayfasındaki (PDP) bir ürünün malzeme çekme için uygun olduğu mağazaları görüntülemek için, bir satın alma kutusu modülüne Mağaza Seçici modülü eklenebilir.
- Sepet sayfasındaki (PDP) bir ürünün malzeme çekme için uygun olduğu mağazaları görüntülemek için, bir satın alma kutusu modülüne Mağaza Seçici modülü eklenebilir.

## <a name="store-selector-module-properties"></a>Mağaza seçicisi modülü özellikleri

| Özellik adı             | Değer                 | Tanım |
|---------------------------|-----------------------|-------------|
| Arama yarıçapı | Sayı | Mağazalar için, mil cinsinden, arama yarıçapını tanımlar. Herhangi bir değer belirtilmezse, varsayılan arama yarıçapı olan 50 mil değeri kullanılır.|
|Hizmet Koşulları | URL    |  Bing Haritalar hizmeti için bir hizmet koşulları URL'si gereklidir. |

## <a name="add-a-store-selector-module-to-a-page"></a>Bir sayfaya mağaza seçici modülü ekleme

Bir mağaza seçici modülü bir ürünün bağlamını gerektiriyor, bu nedenle yalnızca satın alma kutusu ve sepet modülleri içinde kullanılabilir. Mağaza seçici modülleri bu modüllerin dışında çalışmıyor.

- Satın alma kutusu modülüne bir mağaza Seçicisi modülü ekleme hakkında bilgi için bkz. [Satın alma kutusu modülü](add-buy-box.md). 
- Sepet kutusu modülüne bir mağaza Seçicisi modülü ekleme hakkında bilgi için bkz. [Sepet modülü](add-cart-module.md).

## <a name="additional-resources"></a>Ek kaynaklar

[Başlangıç paketine genel bakış](starter-kit-overview.md)

[Satınalma kutusu modülü](add-buy-box.md)

[Sepet modülü](add-cart-module.md)

[PDP'ye hızlı gezinti](quick-tour-pdp.md)

[Sepet ve ödemede hızlı tur](quick-tour-cart-checkout.md)

[Teslimat şekillerini ayarla](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[Kuruluşunuz için Bing Haritalar'ı yönetme](dev-itpro/manage-bing-maps.md)
