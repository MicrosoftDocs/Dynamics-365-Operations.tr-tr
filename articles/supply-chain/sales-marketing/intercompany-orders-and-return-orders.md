---
title: Şirketlerarası siparişler ve sipariş iadeleri
description: Bu konuda, şirketlerarası siparişler ve sipariş iadeleri açıklanmaktadır
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 1c22c021adce5f892ccb6c2ff8735f9e647e8b81
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/03/2022
ms.locfileid: "8671856"
---
# <a name="intercompany-orders-and-return-orders"></a>Şirketlerarası siparişler ve sipariş iadeleri

[!include [banner](../../includes/banner.md)]

Bu konuda, şirketlerarası satınalma siparişleri, satış siparişleri, sipariş iadeleri, satınalma sözleşmeleri ve satış sözleşmelerinin nasıl oluşturulduğu ve güncelleştirildiği açıklanmaktadır.

## <a name="about-intercompany-orders"></a>Şirketlerarası siparişler hakkında

Şirketlerarası satış siparişi oluşturduğunuzda Microsoft Dynamics 365 Supply Chain Management otomatik olarak buna karşılık gelen bir satınalma siparişi oluşturur. Benzer şekilde, şirketlerarası bir satınalma siparişi oluşturulduğunda buna karşılık gelen bir şirketlerarası satış siparişi otomatik olarak oluşturulur.

Bu, iki taraflı siparişler (iki ilişkili şirket arasındaki hareketler) ve çoğu üç taraflı şirketler (şirketlerarası bir hareketin kaynağı, harici bir müşteriye yönelik satış siparişi olduğunda) için geçerlidir.

## <a name="intercompany-order-example"></a>Şirketlerarası sipariş örneği

Birbiriyle ilişkili iki şirketi ele alalım. A Şirketi bir satış yan kuruluşudur ve B Şirketi bir dağıtım birimidir. Şirketlerarası satış siparişleri ve satınalma siparişleri aşağıdaki senaryolarda otomatik olarak oluşturulur:

- A Şirketi bir satınalma siparişi oluşturduğunda ve B şirketi satıcı olduğunda B Şirketinde otomatik olarak bir şirketlerarası satış siparişi oluşturulur. İki taraflı sipariş zinciri, A Şirketindeki bir satınalma siparişinden ve B Şirketindeki bir şirketlerarası satış siparişinden oluşur.
- B Şirketi bir satış siparişi oluşturduğunda ve müşteri A şirketi olduğunda A Şirketinde otomatik olarak bir şirketlerarası satınalma siparişi oluşturulur. İki taraflı sipariş zinciri, B Şirketindeki bir satış siparişinden ve A Şirketindeki bir şirketlerarası satınalma siparişinden oluşur.
- Önce A şirketi harici bir müşteri için satış siparişi oluşturduğunda A Şirketinde otomatik olarak bir satınalma siparişi oluşturulabilir. Bunun sonucunda B Şirketinde otomatik olarak bir şirketlerarası satınalma siparişi oluşturulur. Üç taraflı sipariş zinciri, A Şirketindeki bir satış siparişi ile bir satınalma siparişinden ve B Şirketindeki bir şirketlerarası satış siparişinden oluşur.

## <a name="about-intercompany-return-orders"></a>Şirketlerarası sipariş iadeleri hakkında

Şirketlerarası maddeleri, olağan iadelerle çok benzer şekilde iade edebilirsiniz. Ancak şirketlerarası maddelerde, harici müşteriden gelen sipariş iadesi şirketlerarası bir satınalma siparişi oluşturur. Bu da otomatik olarak bir şirketlerarası satış sipariş iadesi oluşturur. Ayrıca bir şirketlerarası maddeyi harici bir müşteri sipariş iadesi olmadan iade edebilirsiniz.

Şirketlerarası sipariş iadeleri, normal sipariş iadelerine benzer şekilde **Sipariş iadesi oluştur** sayfasında başlatılır.

Microsoft Dynamics 365 Supply Chain Management'ta şirketlerarası satış ve satınalma sözleşmeleri, iade edilen maddeyi yansıtmak için otomatik olarak güncelleştirilir. Bu madde için satış veya satınalma sözleşmesi taahhüdü, madde iade edildiğinde miktar ya da tutardaki değişikliği yansıtmak üzere otomatik olarak ayarlanır.

## <a name="intercompany-return-order-example"></a>Şirketlerarası sipariş iadesi örneği

A Şirketi, şirketlerarası bir madde için satınalma sözleşmesiyle bağlantılı bir satınalma siparişi oluşturur. B Şirketinde karşılık gelen satış sözleşmesiyle bağlantılı bir şirketlerarası satış siparişi otomatik olarak oluşturulur. Satınalma sözleşmesi ve satış sözleşmesi, şirketlerarası sözleşmeler olarak ilişkilidir.

A Şirketi, şirketlerarası maddeyi B Şirketine iade eder. B Şirketi, madde için bir sipariş iadesi oluşturur ve A Şirketinde otomatik olarak bir satınalma sipariş iadesi oluşturulur. Orijinal siparişlerle bağlantılı satın alma sözleşmesi ve satış sözleşmesi taahhütleri, miktar veya tutardaki değişikliği yansıtmak için otomatik olarak ayarlanır.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
