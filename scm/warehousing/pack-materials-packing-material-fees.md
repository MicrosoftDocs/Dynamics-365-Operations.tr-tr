---
title: "Ambalaj malzemeleri ve ücretler"
description: "Ambalaj malzemesi masrafları, belirli aralıklarla bir geri dönüştürme şirketine ödenmektedir. Bir ambalaj birimini meydana getiren her malzeme için ağırlık birimi başına bir tutar ödenir. Ambalaj malzemesi masrafları hesaplanır ve raporlanır, fakat masraflar bir kuruma ödenecek vergiler olarak görülmediğinden, genel muhasebeye hareket nakledilmez."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventPackagingGroup, InventPackagingMaterialCode, InventPackagingMaterialFee, InventPackagingMaterialTrans, InventPackagingMaterialTransPurch, InventPackagingUnit
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2194
ms.assetid: 040b65dc-43c9-4256-b69f-b2d6e736fbe9
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 7c0bc5b5d86956336012096c11d0d7621abab1f9
ms.lasthandoff: 03/31/2017


---

# <a name="packing-materials-and-fees"></a>Ambalaj malzemeleri ve ücretler

[!include[banner](../includes/banner.md)]


Ambalaj malzemesi masrafları, belirli aralıklarla bir geri dönüştürme şirketine ödenmektedir. Bir ambalaj birimini meydana getiren her malzeme için ağırlık birimi başına bir tutar ödenir. Ambalaj malzemesi masrafları hesaplanır ve raporlanır, fakat masraflar bir kuruma ödenecek vergiler olarak görülmediğinden, genel muhasebeye hareket nakledilmez.

Ambalaj malzemesi ağırlıkları ve masrafları satış sipariş satırları ve satınalma siparişi satırları için hesaplanır.

Madde, madde ambalaj grubu veya tüm maddeler bazında bir veya birden fazla ambalaj birimi tanımlayabilirsiniz. Bir ambalaj birimi, ambalaj biriminde bulunan madde sayısı ve , ambalaj malzemeleri ve ağırlıklarını da içerir. Tanımlanan her tür ambalaj malzemesi için ambalaj malzemesi kodu atanır. Ambalaj malzemesi koduna göre belirli bir dönem için bir fiyat belirleyebilirsiniz. Ambalaj malzemesi masrafını bu bilgiler temel alınarak hesaplanır.

| **Not **                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Şirketiniz ambalaj malzemesi masrafı ödemiyorsa dahi, bu işlevi ambalaj malzemesi ağırlıkları istatistiklerini hesaplamak amacıyla kullanabilirsiniz. |

## <a name="setup-requirements-for-packing-material-fees"></a>Ambalaj malzemesi ücretleri için kurulum gereklilikleri
Ambalaj malzemesi ağırlıklarını veya masraflarını veya her ikisini birden hesaplamadan önce, aşağıdaki temel veriler oluşturmalısınız:

-   Ambalaj grupları - Maddelere atamak için ambalaj grupları oluşturun.
-   Ambalaj malzemesi kodları - Ambalaj malzemesi tanımlanan her türü için ambalaj malzemesi kodları oluşturun.
-   Ambalaj birimleri - Bir madde, bir ambalaj grubu veya tüm maddeler için bir ambalaj birimi belirtin. Her ambalaj birimi için hangi ambalaj malzemelerinin dahil edileceğini tanımlayın, ağırlıkları atayın ve ambalaj birimi faktörü alanında, dönüştürme faktörünü stok biriminden girin.
-   Ambalaj malzeme ücretleri - Ambalaj malzemesi kodu bazında ambalaj malzemesi masraflarını belirtin. Her malzeme tipi için geçerlilik süresini, malzeme başına fiyatı, para birimini ve birimi tanımlayın.

## <a name="packing-units-on-sales-order-lines"></a>Satış siparişi satırlarındaki ambalaj birimleri
Bir satış sipariş satırı oluşturduğunuzda, ambalaj birimlerinin madde için belirtip belirtilmediğini görmek amacıyla sistem bir kontrol gerçekleştirilir. Eğer ambalaj birimleri belirlendiyse, satış sipariş satırı, belirtilen ambalaj birimi ve ambalaj birim miktarı ile sistem tarafından güncelleştirilir. Ambalaj birim miktarı, sipariş miktarının seçili ambalaj birimindeki madde sayısına bölünmesine dayanır. Bir ambalaj birimi belirtilmemişse, satış sipariş satırına el ile bir ambalaj birimi ve bir ambalaj birim miktarı girebilirsiniz. Ayrıca, satış sipariş satırını naklettiğinizde ambalaj biriminin ve ambalaj birim miktarının değiştirebilirsiniz. Ancak sadece satış sipariş satırı kısmen teslim edilmiş veya kısmen faturalanmışsa mantıklı olur. Satış siparişini faturaladığınızda, ambalaj malzemesi hareketleri oluşturulur. Ambalaj malzemesi hareketleri, satış satırı için ambalaj malzemelerinin ağırlıklarını içerir. Hareketleri de bunları faturaladıktan ve sonra yeni hareketleri oluşturduktan sonra değiştirebilirsiniz.

## <a name="packing-units-on-purchase-order-lines"></a>Satınalma siparişi satırlarındaki ambalaj birimleri
Sistem tarafından bir satınalma siparişi satırı için ambalaj malzemesi hareketleri oluşturulmaz. Faturalanmış sipariş satırları için hareketleri **Ambalaj malzemesi hareketleri** sayfasında el ile oluşturabilirsiniz.

## <a name="set-up-customer-packagingmaterialfee-license-numbers"></a>Müşteri ambalaj malzemesi ücreti lisans numaralarını ayarlama
Müşteriler ambalaj malzemesi ücretlerini ödüyorsa, müşterilerin ambalaj malzemesi ücreti lisans numaralarını **Müşteriler** sayfasında belirtin. Müşteriye lisans numarası atandığında, satış siparişleri faturalandığında ambalaj malzemesi ücretleri otomatik olarak hesaplanacaktır. Faturalamadan sonra **Ambalaj malzemesi hareketleri** sayfasındaki **Ücreti hesapla** onay kutusu temizlenir çünkü hesaplamanıza ve bir rapor yazdırmanıza gerek kalmamıştır. Ambalaj malzemesi ağırlıklarını faturaya yazdırmayı ve müşterileri ücretleri ödemeleri konusunda bilgilendirebilirsiniz. 

Şirketinizin ambalaj malzemesi ücretlerini ödemesi durumunda, müşteri lisans numaralarını belirtmeyin. Faturalama sonra **Ambalaj malzemesi hareketleri** sayfasında **Ücreti hesapla** onay kutusu seçilidir. Bu da rapor oluşturulduğunda ücretlerin hesaplandığını gösterir. Ağırlıkları faturaya yazdırmayı ve şirketinizin ücretleri ödediğini belirtebilirsiniz.

## <a name="print-packaging-material-weights-on-invoices"></a>Faturalarda ambalaj malzemesi ağırlıklarını yazdırma
Ambalaj malzemesi ağırlıklarını yazdırmayı ve faturadaki ambalaj malzemesi ücretlerini kimin ödeyeceğini belirtebilirsiniz. Ambalaj koduna göre ağırlıklar özetlenmiştir.
 





