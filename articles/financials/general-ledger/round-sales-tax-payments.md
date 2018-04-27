---
title: "Satış vergisi ödemeleri ve yuvarlama kuralları"
description: "Bu makalede, Satış vergisi makamlarında yuvarlama kuralı ayarlarının nasıl çalıştığı ve Satış vergilerini kapatma ve deftere nakletme işi sırasında satış vergisi bilançosunun yuvarlanması açıklanmaktadır."
author: twheeloc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 13470282efc6b9135e86355cf8071b841aad3071
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="sales-tax-payments-and-rounding-rules"></a>Satış vergisi ödemeleri ve yuvarlama kuralları

[!INCLUDE [banner](../includes/banner.md)]

Bu makalede, Satış vergisi makamlarında yuvarlama kuralı ayarlarının nasıl çalıştığı ve Satış vergilerini kapatma ve deftere nakletme işi sırasında satış vergisi bilançosunun yuvarlanması açıklanmaktadır.

Satış vergilerinin düzenli olarak vergi dairelerine bildirilmesi ve ödenmesi gerekir. Bu, Satış vergisi sayfasındaki satış vergisi kapatma ve nakletme işlemi çalıştırılarak yapılabilir. Bir döneme ait satış vergisi, satış vergisi hesaplarına karşı kapatılır ve satış vergisi bakiyesi Satış vergisi kapatma hesabına nakledilir. Satış verghisi kapatma hesabına nakledilen satış vergisi bakiyesi, Satş vergisi sayfasında bir yuvarlama kuralı ayarlanarak vergi kurumlarının gerektirdiği şekilde yuvarlanabilir. 

Yuvarlama farkı, Genel muhasebenin Otomatik hareketler için hesaplar alanında seçilen Satış vergisi yuvarlama hesabına nakledilir.

Aşağıdaki örnekte, Satış vergisi dairesinde yuvarlama kuralının nasıl işlediği gösterilmektedir.

### <a name="example"></a>Örnek:

Bir döneme ilişkin toplam satış vergisi alacak bakiyesi -98.765,43 olarak görünmektedir. Tüzel kişilik ödediğinden daha fazla satış vergisi tahsil etmiştir. Bu nedenle, tüzel kişiliğin vergi dairesine ödeme yapması gerekir. 

Tüzel kişilik bakiyeyi en yakın 1,00 değerine yuvarlayan bir yuvarlama yöntemi kullanmak istemektedir. Satış vergisi muhasebesinden sorumlu kullanıcı aşağıdaki adımlardan birini gerçekleştirmelidir:

1.  Vergi &gt; Dolaylı vergiler &gt; Satış vergisi &gt; Satış vergisi dairesi öğelerine tıklayın
2.  Genel hızlı sekmesinde, Yuvarlama formu alanından Normal seçeneğini seçin.
3.  Yuvarlama alanına 1,00 girin.
4.  Satış vergisini vergi dairesine ödeme zamanı geldiğinde, Satış vergisini kapat ve naklet sayfasını açın. (Vergi &gt; Beyannameler &gt; Satış vergisi &gt; Satış vergisini kapat ve naklet'e tıklayın.)
5.  Satış vergisi kapatma hesabındaki 98.765,43 tutarındaki vergi borcu 98.765'e yuvarlanır.

Aşağıdaki tabloda, 98.765,43 tutarının Satış vergisi dairesi sayfasındaki Yuvarlama formu alanında bulunan her yuvarlama yöntemi kullanılarak nasıl yuvarlandığı gösterilmektedir.

| Yuvarlama formu seçeneği                | Yuvarlama değeri = 0,01 | Yuvarlama değeri = 0,10 | Yuvarlama değeri = 1,00 | Yuvarlama değeri = 100,00 |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|
| Normal                              | 98.765,43              | 98.765,40              | 98.765,00              | 98.800,00                |
| Aşağı yuvarlama                            | 98.765,43              | 98.765,40              | 98.765,00              | 98.700,00                |
| Yukarı yuvarlama                         | 98.765,43              | 98.765,50              | 98.766,00              | 98.800,00                |
| Kendi avantajı, alacak bakiyesi için | 98.765,43              | 98.765,40              | 98.765,00              | 98.700,00                |
| Kendi avantajı, borç bakiyesi için  | 98,765.43              | 98,765.50              | 98,766.00              | 98,800.00                |

> [!NOTE]                                                                                  
> Kendi avantajı seçeneğini seçerseniz, yuvarlama daima tüzel kişiliğin yararına yapılır. 

Daha fazla bilgi için aşağıdaki konulara bakın:
- [Satış vergisine genel bakış](indirect-taxes-overview.md)
- [Satış vergisi ödemesi oluşturma](tasks/create-sales-tax-payment.md)
- [Belgelerde satış hareketleri oluşturma](tasks/create-sales-tax-transactions-documents.md)
- [Deftere nakledilen satış vergisi hareketlerini görüntüleme](tasks/view-posted-sales-tax-transactions.md)



