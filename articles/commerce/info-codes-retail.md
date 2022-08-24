---
title: Bilgi kodları ve bilgi kodu grupları
description: Bu makalede bilgi kodları, bilgi kodu grupları ve bunların nasıl kullanılacağı hakkında genel bir bakış sunulmuştur.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 22761
ms.assetid: 99877dba-a6e3-4d88-ba0a-ee5913aea17e
ms.search.industry: Retail
ms.search.form: RetailInfocodeTable
ms.openlocfilehash: a6fc84db368c602f74778eb0a44ac52798dc5161
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273516"
---
# <a name="info-codes-and-info-code-groups"></a>Bilgi kodları ve bilgi kodu grupları

[!include [banner](includes/banner.md)]

Bu makalede bilgi kodları, bilgi kodu grupları ve bunların nasıl kullanılacağı hakkında genel bir bakış sunulmuştur.

Bilgi kodları, satış noktası (POS) kasasındaki verileri yakalamanın bir yolunu sunar. Bilgi kodlarını ürün satışları, ürün iadeleri veya müşterileri seçme gibi çeşitli POS işlemleri sırasında kasiyerden bilgileri girmesinin istenmesi için kullanabilirsiniz. Kasiyerler listeden bir giriş seçebilir ya da bilgiyi bir kod, sayı, tarih veya metin olarak girebilir. Bilgi kodlarını, önceden tanımlanmış mağaza eylemlerine, perakende ürünlerine, ödeme yöntemlerine, müşterilere veya belirli satış noktası etkinliklerine atayabilirsiniz. Bilgi kodlarını, aşağıdakileri yapmak için kullanabilirsiniz:

- Uçuş numarası veya iade nedeni gibi işlemler gerektiğinde ek bilgileri görebilmek.
- Kasiyerden belirli ürünler için bir fiyat listesi seçmesini istemek.
- Kasiyerden belirli bir eylem gerçekleştirirken giriş yapmasını istemek için bir alt kodu bir bilgi koduna bağlamak. Örneğin, bir müşteri bir ürünü iade ettiğinde kasiyerden ürün iadesinin nedenini sormasını isteyebilirsiniz. Sonra, kasiyerin aralarından seçim yapabileceği bir neden listesi göstermek için bir alt kodları kullanabilirsiniz.
- Biri ürünü normal satış, indirimli satış veya ücretsiz ürün şeklinde satmak.
- Bir satış işlemi gerçekleştirilmeden kasa çekmecesi açıldığında kasiyerin bir değer girmesini veya bir alt kodlar listesinden seçim yapmasını istemek.

## <a name="info-codes-group"></a>Bilgi kodları grubu

Commerce'de bilgi kodu grupları oluşturabilirsiniz. Bilgi kodları grupları, daha az bilgi kodu tanımlamanızı ve bunları çok yönlü şekilde kullanmanızı sağlayan esneklik kazandırır. Bilgi kodu gruplarını aşağıdaki yollarla kullanabilirsiniz:

- Daha az bilgi kodu tanımlamak ve bunları kolayca yeniden kullanmak. Bilgi kodu gruplarına dahil edilen bilgi kodlarının diğer bilgi kodlarında önceden tanımlanmış bir bağımlılığı yoktur. Aynı bilgi kodlarını birden çok bilgi kodu grubuna ekleyebilir ve sonra aynı bilgi kodlarını belirli bir duruma uygun sırada sunmak için öncelik belirlemeyi kullanabilirsiniz.
- Her senaryo için bağlantılı bilgi kodu veya ayrı bilgi kodu tanımlamanız gerekmeden bir ürün veya hareket hakkında bilgi toplamak için bilgi kodlarını diğer bilgi kodlarına veya bilgi kodu gruplarına bağlayın.

## <a name="info-code-examples"></a>Bilgi kodu örnekleri

**Örnek 1: Bilgi kodlarını yeniden kullanmak**

Bir bilgi kodu tetiklendiğinde başka bir bilgi kodunun hemen ardından tetiklenmesi için bilgi kodlarını bağlayabilirsiniz. Örneğin, belirli ürünler için kasiyerin müşteriye batarya ve ürün garantisi satın almak isteyip istemediğini sormasını isteyebilirsiniz. Diğer ürünler için, kasiyerin müşteriye batarya satın almak isteyip istemediğini sormasını ve posta kodlarını almalarını isteyebilirsiniz. Bu senaryolar için bağlantılı bilgi kodları oluşturursanız, kasiyerin doğru bilgileri sormasını isteyebilmek için bilgi kodunun her bir varyasyonunu ayarlamanız gerekir. Bilgi kodu grupları kullanırsanız, batarya isteği gibi genel bilgi kodları bir defada ayarlanabilir ve sonra birden çok bilgi kodu grubunda yeniden kullanılabilir. İstemlerin görüntüleneceği sırayı belirlemek için bilgi kodu gruplarında öncelik belirlemeyi de kullanabilirsiniz.

**Örnek 2: Bilgi kodlarını bilgi kodu gruplarına bağlantılamak**

Mobil cihaz gibi belirli ürünler satarken her zaman telefon numarası, mobil cihaz ekipmanı tanımlayıcısı (MEID) ve seri numarası gibi bir dizi bilgiyi toplamak isteyebilirsiniz. Ancak, aynı zamanda cep telefonunun yanı sıra bir tablete ilişkin farklı bilgiler de toplamak istersiniz. Telefon numarası, MEID ve seri numarası istemlerini içeren bir bilgi kodu grubu ayarlayabilir ve sonra bilgi kodu grubunu bağımsız bir bilgi koduna bağlayabilirsiniz. Ürüne özgü bilgi kodları tetiklendiğinde her cihaz için birden çok bağlı bilgi kodu grubunu tanımlamanız gerekmeden genel verileri toplayabilmeniz için ardından bilgi kodu grubu tetiklenebilir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
