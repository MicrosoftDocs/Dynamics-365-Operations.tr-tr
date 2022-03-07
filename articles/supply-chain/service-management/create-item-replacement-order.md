---
title: Madde değiştirme emri oluşturma
description: Madde değiştirme siparişleri genellikle bir ürün iade edildikten ve incelendikten sonra oluşturulur.
author: josaw1
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReturnTableListPage, ReturnReplaceItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 57bbb8eb638b990914dc00f9700ff0c1925c48852862b02e09f3f26415d3e347
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6745514"
---
# <a name="create-an-item-replacement-order"></a>Madde değiştirme emri oluşturma 

[!include [banner](../includes/banner.md)]


Madde değiştirme siparişleri genellikle bir ürün iade edildikten ve incelendikten sonra oluşturulur. Ancak bir maddenin iade edilmeden önce değiştirilmesi gerekiyorsa veya orijinal madde iade edilmeyecekse iade siparişini oluşturduktan hemen sonra bir madde değiştirme siparişi oluşturabilirsiniz.

## <a name="create-a-replacement-order-after-you-receive-an-item-that-is-returned"></a>İade edilen bir maddeyi aldığınızda değiştirme siparişi oluşturma

1.  **Satış ve pazarlama** \> **Genel** \> **İade siparişleri** \> **Tüm iade siparişleri**'ne tıklayın.

2.  Yeni bir iade siparişi oluşturun veya **İade emri - RMA numarası: %1, %2** formunu açmak için listeden bir iade siparişi seçin.

3.  **İade satırı**'na tıklayın ve **Yerine koyulacak madde**'yi seçin.

4.  İade edilen maddenin yerine konulacak maddeyi seçin. Madde belirtimlerini girin ve ardından **Uygula**'ya tıklayın.

5.  İade sipariş için sevk irsaliyesi oluşturmak üzere **Sevk irsaliyesi**'ne tıklayın. Seçtiğiniz yerine konulan madde için bir satış siparişi oluşturulur.
    
    Yerine konulan madde için için satış siparişi oluşturulduktan sonra otomatik olarak satış sözleşmeleri aranır ve uygulanan bir satış sözleşmesini varsa satış siparişine uygulanır.

## <a name="create-a-replacement-order-before-you-receive-an-item-that-will-be-returned"></a>İade edilecek bir maddeyi almadan önce değiştirme siparişi oluşturma

1.  **Satış ve pazarlama** \> **Genel** \> **İade siparişleri** \> **Tüm iade siparişleri**'ne tıklayın.

2.  Yeni bir iade siparişi oluşturun veya **İade emri - RMA numarası: %1, %2** formunu açmak için listeden bir iade siparişi seçin.

3.  İade edilen madde için satış siparişi tanımlamak isterseniz **Satış siparişini bul**'a tıklayın. **Satış siparişi bul** formunu doldurun ve formu kapatmak için **Tamam**'a tıklayın, **İade siparişi - RMA numarası: %1, %2** formuna geri dönün. İade edilen maddeyle ilişkili satış siparişi satırı iade siparişine kopyalanır.

4.  **Satış siparişi oluştur** formunu açmak için **Değiştirme siparişi**'ne tıklayın.

5.  **İade siparişi - RMA numarası %1, %2** formunda seçtiğiniz iade siparişindeki ayrıntıları bu satış siparişine transfer etmek için **İade siparişi satırlarını kopyala** onay kutusunu seçin.

6.  Ayrıntıları gerektiği gibi girin veya değiştirin.
    
    Satış siparişini adım 3'te tanımladıysanız ve iade edilen madde için satış sipariş satırı bir satış sözleşmesine bağlıysa, uygun satış sözleşmesinin madde değiştirme siparişi tanımlayıcısı otomatik olarak **Satış sözleşmesi kodu** alanında görüntülenir.

7.  **Satış siparişi oluştur** formunu kapatmak için **Tamam**'a tıklayın, yeni satış siparişi için bilgileri girmeye devam edebileceğiniz **Satış siparişi** formunu açın. Geçerli iade sipariş satırları yeni satış siparişine kopyalanır. 
    
    Satış sözleşmesi tanımlayıcısı otomatik olarak **Satış sözleşmesi kodu** alanında görüntülenirse, satış sözleşmesi madde değiştirme siparişiyle ilgili satış siparişi başlığına bağlanır. Satış sözleşmesinde henüz karşılanmamış geçerli bir taahhüt varsa ve satış siparişi satış sözleşmesi sona ermeden önce oluşturulursa, satış sözleşmesi ile satış siparişi satırı arasında bir bağlantı oluşturulur. Bu nedenle, satış sözleşmesinden alınan madde fiyatı gibi bilgiler yeni satış sipariş satırına kopyalanır. 
  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]