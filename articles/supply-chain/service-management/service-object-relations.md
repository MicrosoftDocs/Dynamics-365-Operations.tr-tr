---
title: Servis nesnesi ilişkileri
description: Servis nesnesi ve servis sözleşmesi veya servis siparişi arasında servis nesnesi ilişkileri oluşturabilirsiniz.
author: ShylaThompson
manager: tfehr
ms.date: 02/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectRelation
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 913b3c30bf972de7cc3dde73280e4f2f2be38507
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974347"
---
# <a name="service-object-relations"></a>Servis nesnesi ilişkileri 

[!include [banner](../includes/banner.md)]

Servis nesnesi ve servis sözleşmesi veya servis siparişi arasında servis nesnesi ilişkileri oluşturabilirsiniz. Bir ilişki oluşturduğunuzda servis nesnesini servis sözleşmesine veya servis siparişine iliştirirsiniz.

İlişki oluşturulduktan sonra, servis nesnesini servis sözleşmesine veya servis siparişindeki herhangi bir satıra iliştirebilirsiniz.

## <a name="template-boms"></a>Şablon Ürün Reçeteleri

Parça ilişkisi için bir şablon ürün reçetesi de belirtebilirsiniz. Şablon ürün reçetesi, servis uyguladığınız ürün reçetesidir. Servis ziyareti sırasında servis nenesinin bileşen parçasını değiştirirseniz bu değişikliği Servis nesneleri formunu kullanarak servis ürün reçetesinde kaydedebilirsiniz.

## <a name="example"></a>Örnek

Müşteri sitesinde iki asansör hizmeti için bir servis sözleşmesi oluşturuyorsunuz.
Servis sözleşmesi, SAL-001 kimlik tanımlayıcı koduna sahiptir.

Asansörler, Servis nesneleri formunda EL-S/1000 ve EL-L/1000 nesneleri olarak ayarlanır.

Servis nesnelerini (EL-S/1000 ve EL-L/1000) servis sözleşmesine iliştiriyorsunuz.

Parçanın bileşen parçalarını değiştirdikçe servis kapsamındaki parça için ürün reçetesindeki değişiklikleri kaydetmek, böylece aşağıdaki tabloda açıklandığı gibi servis ürün reçetesini servis kapsamındaki parçaya iliştirmek isteyebilirsiniz.

| Servis nesnesi | İlişki – Servis sözleşmesi | Servis ürün reçetesi   |
|----------------|------------------------------|---------------|
| EL-S/1000      | ID SAL-001                   | BOM-EL-S/1000 |
| EL-L/1000      | ID SAL-001                   | BOM-EL-L/1000 |

Bunlar sözleşme için servis nesnesi ilişkileri olduğundan, artık aşağıdaki tabloda gösterildiği gibi bu nesnelere servis sözleşmesi satırları oluşturabilirsiniz.

| Hareket türü | Kategori           | Servis nesnesi |
|------------------|--------------------|----------------|
| Saat             | Denetleme         | EL-S/1000      |
| Saat             | Vites kutusu temizliği  | EL-S/1000      |
| Madde             | Temizlik malzemeleri | EL-S/1000      |
| Saat             | Denetleme         | EL-L/1000      |
| Saat             | Vites kutusu temizliği   | EL-L/1000      |
| Madde             | Temizlik malzemeleri | EL-L/1000      |

Bir servis ziyaretinde, EL-S/1000 asansörünün vitesi kutusunu temizlemeniz gerekiyor. Nesnenin bileşen parçasını değiştirmek için, geçerli servis sözleşmesinde ayarladığınız servis nesnesi ilişkisini kullanarak Ürün Reçetesi Tasarımcısı'na ulaşabilirsiniz.

Servis kapsamındaki parça ilişkisini kullanarak Ürün Reçetesi Tasarımcısı'na erişme

1. Servis sözleşmeleri
2. Servis sözleşmesi oluşturmak için servis sözleşmesine çift tıklayın veya Servis sözleşmesine tıklayın.
3. Kurulum sekmesine tıklayın.
4. Servis sözleşmesine bir şablon ürün reçetesi iliştirmek için Servis nesnelerine tıklayın.
5. Şablon ürün reçetesini değiştirmek için Servis nesneleri formunda Tasarımcı'ya tıklayarak Tasarımcı'yı açın.

## <a name="automatically-created-service-orders"></a>Otomatik olarak oluşturulan servis siparişleri

Servis sözleşmesi için otomatik olarak servis siparişleri oluşturursanız sözleşmedeki servis nesnesi ilişkileri de servis siparişlerinde oluşturulur.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]