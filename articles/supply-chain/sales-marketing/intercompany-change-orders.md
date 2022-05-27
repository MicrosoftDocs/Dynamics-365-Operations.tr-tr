---
title: Şirketlerarası siparişleri değiştirme
description: Bu konuda, şirketlerarası siparişlerin değiştirilme işlevi açıklanmaktadır
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
ms.openlocfilehash: 10efc397c64833785f286983987fd05854a69c0f
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672920"
---
# <a name="change-intercompany-orders"></a>Şirketlerarası siparişleri değiştirme

[!include [banner](../../includes/banner.md)]

Şirketlerarası bir satış siparişini veya satın alma siparişini değiştirirseniz ilgili şirkette buna karşılık gelen satış siparişi ya da satın alma siparişi de bu değişikliği yansıtır.

## <a name="adding-new-lines"></a>Yeni satırlar ekleme

Özgün satış siparişi şirketlerarası sipariş zincirinin bir parçasıysa şirketlerarası satış siparişine ve satın alma siparişine yeni satırlar ekleyebilirsiniz. Özgün satış siparişi doğrudan teslimat değilse bile yeni satırlar ekleyebilirsiniz. Özgün satış siparişi doğrudan teslimat ise şirketlerarası satış siparişine ve satın alma siparişine yalnızca özgün satış siparişindeki **Şirketlerarası ayarlar** hızlı sekmesinde **Dolaylı oluşturmaya izin ver** alanı seçiliyse yeni sipariş satırları ekleyebilirsiniz.

## <a name="changing-prices-and-discounts"></a>Fiyatları ve iskontoları değiştirme

**Şirketlerarası** sayfasında **Fiyat düzenlemesine izin ver** ve **İskonto düzenlemesine izin ver** onay kutuları işaretliyse fiyatları ve iskontoları değiştirebilirsiniz.

Şirketlerarası satış siparişi satırındaki mevcut satırlardan birindeki birim fiyatı değiştirirseniz şirketlerarası satın alma siparişindeki birim fiyat da değişir.

Şirketlerarası satış siparişi satırındaki iskonto alanlarından herhangi birini değiştirirseniz şirketlerarası satın alma siparişindeki ilgili iskonto alanları güncelleştirilir.

## <a name="changing-and-adding-new-charges"></a>Yeni masrafları değiştirme ve yeni masraflar ekleme

**Şirketlerarası** sayfasında **Fiyat düzenlemesine izin ver** ve **İskonto düzenlemesine izin ver** onay kutuları işaretliyse masrafları değiştirebilirsiniz.

Şirketlerarası satış siparişi başlığına ve şirketlerarası satış satırına yeni bir masraf eklerseniz her iki masraf da şirketlerarası satın alma siparişine kopyalanır. Bu nedenle, şirketlerarası satış siparişi ve şirketlerarası satın alma siparişi aynı toplam tutara sahiptir. Masraflar hiçbir zaman özgün satış siparişine kopyalanmaz.

## <a name="copying-a-fee"></a>Masraf kopyalama

Özgün satış siparişine kopyalamak için masrafı **Servis** türünde bir maddeye sahip yeni bir satış satırı olarak oluşturun.

## <a name="changing-quantities-and-deleting-intercompany-purchases-and-sales-order-lines"></a>Miktarları değiştirme ve şirketlerarası satın almaları ve satış siparişi satırlarını silme

Satır yalnızca doğrudan **Satış siparişi** veya **Satın alma siparişi** formundan oluşturulmuşsa miktarı değiştirebilir veya bir şirketlerarası satın alma siparişi satırını ya da satış siparişi satırını silebilirsiniz. Bu değişiklik, şirketlerarası satın alma siparişini veya satış siparişini ya da sipariş satırlarını kaynak haline getirir.

## <a name="origins-of-orders-and-order-lines"></a>Siparişlerin ve sipariş satırlarının menşeleri

Şirketlerarası siparişler ve sipariş satırları iki menşeden birine sahip olabilir:

- **Türetilen**: Sipariş, şirketlerarası bir sipariş zincirinden otomatik olarak oluşturulmuş.
- **Kaynak**: Sipariş, bir kullanıcı tarafından el ile oluşturulmuş.

Menşe, şirketlerarası satın alma siparişlerinin ve satış siparişlerinin sipariş başlığındaki **Menşe** alanında gösterilir. Bu alan, satış siparişindeki **Şirketlerarası ayarlar** hızlı sekmesinde ve satın alma siparişindeki **Kurulum** hızlı sekmesinde bulunur.

**Türetilen** ve **Kaynak** menşeleri yalnızca şirketlerarası siparişler için geçerlidir. **Menşe** alanı diğer tüm satış siparişleri, satın alma siparişleri ve sipariş satırları için boş bırakılır. Bu alan, özgün satış siparişinde de boştur.

## <a name="example-derived-origin"></a>Örnek: Türetilen menşe

Harici bir müşteri için özgün satış siparişi oluşturabilirsiniz. Bu satış siparişi bir satış satırı içerir. Bu özgün satış siparişi bir sipariş satırı içeren bir şirketlerarası satın alma siparişi oluşturur ve bu da bir satış siparişi içeren bir şirketlerarası satış siparişi oluşturur. Şirketlerarası satın alma siparişi başlığı ve sipariş satırı otomatik olarak özgün satış siparişinden oluşturulur.

Şirketlerarası satın alma siparişinin **Kurulum** hızlı sekmesinde ve şirketlerarası satış siparişi başlıklarının **Şirketlerarası ayarlar** hızlı sekmesindeki **Menşe** alanının değeri **Türetilen**'dir. Satın alma siparişi ve satış siparişi satırlarının **Satır ayrıntıları** sekmesindeki **Menşe** alanının değeri de **Türetilen**'dir.

Sipariş satırının menşei **Türetilen** ise sipariş satırını doğrudan silemezsiniz. Sipariş satırını yalnızca sipariş satırını oluşturan kaynaktan silebilirsiniz. Ayrıca, sipariş edilen miktarı yalnızca sipariş satırını oluşturan kaynaktan değiştirebilirsiniz.

Özgün satış siparişi ve özgün satış siparişi satırı, şirketlerarası sipariş zincirinin bir parçasıysa sipariş edilen miktarları özgün satış siparişinden değiştirebilirsiniz ve sipariş satırlarını özgün satış siparişinden silebilirsiniz.

## <a name="example-source-origin"></a>Örnek: Kaynak menşei

Şirketlerarası satıcı için bir satın alma siparişi oluşturursunuz. Şirketlerarası satın alma siparişi ve sipariş satırının her ikisinin de menşei **Kaynak**'tır. Bu nedenle, bu şirketlerarası satın alma siparişi denetleyicidir ve satıcı şirkette otomatik olarak oluşturulan şirketlerarası satış siparişinin menşei **Türetilen**'dir.

Ayrıca, şirketlerarası satın alma siparişinde oluşturulan bir sipariş satırının sipariş edilen miktarları, şirketlerarası satış siparişinde değiştirilemez. Sipariş satırı yalnızca şirketlerarası satın alma siparişinden silinebilir. Şirketlerarası satış siparişine yeni bir satır eklenirse şirketlerarası satış siparişi satırının menşei **Kaynak** olur.

Özgün satış siparişi, şirketlerarası sipariş zincirinin bir parçası olduğunda özgün satış siparişinden şirketlerarası siparişleri ve şirketlerarası sipariş satırlarını her zaman denetleyebilirsiniz.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
