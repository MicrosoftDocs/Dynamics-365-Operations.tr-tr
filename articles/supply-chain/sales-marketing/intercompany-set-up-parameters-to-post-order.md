---
title: Şirketlerarası siparişi deftere nakletmek için parametreleri ayarlama
description: Bu konuda, şirketlerarası siparişi deftere nakletmek için parametrelerin nasıl ayarlanacağı açıklanmaktadır
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
ms.openlocfilehash: 24389d8ed3768089d59dc87e5948e9ea7fa1ecfc
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/03/2022
ms.locfileid: "8679261"
---
# <a name="set-up-parameters-to-post-an-intercompany-order"></a>Şirketlerarası siparişi deftere nakletmek için parametreleri ayarlama

[!include [banner](../../includes/banner.md)]

Şirketlerarası bir müşteri faturası deftere nakledildiğinde bunu hem şirketlerarası satınalma siparişi hem orijinal müşteri faturası otomatik olarak deftere nakledilecek şekilde ayarlayabilirsiniz.

> [!NOTE]
> Bu yordamı gerçekleştirmeden önce kuruluşunuzdaki yazdırma yönetimini doğru fatura yazıcısını işaret edecek şekilde ayarlayın. Bu, orijinal satış siparişi faturasının doğru yazıcıda yazdırılmasını sağlar.

Aşağıdaki parametreleri ayarlamanız gerekir:

1. **Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin. Birlikte çalışmak istediğiniz satış siparişini seçin.
1. Satış siparişinde, Eylem Bölmesi'nde **Başlık görünümü** seçeneğini belirleyin ve ardından **Şirketlerarası ayarlar** hızlı sekmesini seçerek açın.
1. **Satış siparişi** sekmesinde Eylem Bölmesi'ne gidin ve ardından **Düzenle**'yi seçin.
1. **Şirketlerarası ayarlar** hızlı sekmesine geri gidin ve şirketlerarası zincir (tüm siparişler) boyunca doğrudan teslimatı etkinleştirmek için **Doğrudan telimat**'ı seçin.
1. Satış siparişini yeni ayarla kaydetmek için **Kaydet**'i seçin. Ardından satış siparişini kapatmak için **Kapat**'ı seçin.
1. **Tedarik ve kaynak \> Satıcılar \> Tüm satıcılar**'a gidin. **Genel** sekmesinde, **Şehirlerarası**'nı seçin.
1. **Şehirlerarası** sayfasında, **Satınalma siparişi politikaları** bağlantısını seçin. **Şirketlerarası satınalma siparişi (doğrudan teslimat)** alan grubunda, **Faturayı otomatik olarak deftere naklet**'i seçin ve **Faturayı otomatik olarak yazdır** alanındaki onay işaretini kaldırın.
1. **Orijinal satış siparişi (doğrudan teslimat)** alan grubunda, **Faturayı otomatik olarak deftere naklet** alanını ve **Faturayı otomatik olarak yazdır** alanını seçin.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
