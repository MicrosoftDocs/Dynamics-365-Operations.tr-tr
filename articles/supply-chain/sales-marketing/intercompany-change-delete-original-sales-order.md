---
title: Orijinal şirketlerarası satış siparişini değiştirme veya silme
description: Bu konuda, orijinal satış siparişi işlevini değiştirme ve silme açıklanmaktadır
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
ms.openlocfilehash: 6ff7eeb00fec7c1b9fa1dc08fa231669f728ed3c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859091"
---
# <a name="change-or-delete-an-original-intercompany-sales-order"></a>Orijinal şirketlerarası satış siparişini değiştirme veya silme

[!include [banner](../../includes/banner.md)]

Satış siparişinde değişiklik yaptığınızda değişiklikleriniz otomatik olarak ilgili şirketlerarası satınalma siparişi ve şirketlerarası satış siparişi ile eşitlenir.

> [!NOTE]
> Yaptığınız değişiklikler harici satıcılara verdiğiniz satınalma siparişlerini etkilemez; ayrıca harici satıcılara yönelik satınalma siparişi satırlarıyla bağlantılı orijinal satış satırları da etkilenmez.

Aşağıdaki tabloda, yapabileceğiniz değişiklikler ve beklenen sonuçlar özetlenmektedir.

| Operasyon | Sonuç |
|---|---|
| Orijinal&nbsp;bir&nbsp;satış&nbsp;siparişini&nbsp;silin. | İlgili şirketlerarası satınalma siparişi ve şirketlerarası satış siparişi de silinir. Siparişin durumu **Malzeme çekme listesi** veya işlemin daha ilerisindeki bir durum ise satış siparişini silemezsiniz. |
| Orijinal bir satış sipariş satırını silin. | İlgili şirketlerarası satınalma siparişi satırı ve şirketlerarası satış siparişi satırı silinir. Siparişin durumu **Malzeme çekme listesi** veya işlemin daha ilerisindeki bir durum ise satış siparişi satırını silemezsiniz. |
| Orijinal satış siparişine yeni bir satış satırı ekleyin. | Yeni satış satırı hem şirketlerarası satınalma siparişinde hem şirketlerarası satış siparişinde oluşturulur. |
| Orijinal bir satış siparişi satırındaki miktarı değiştirin. | Miktar hem şirketlerarası satınalma siparişi satırı hem şirketlerarası satış siparişi satırı ile eşitlenir. Net tutar tüm siparişlerde yeniden hesaplanır. |
| Orijinal bir satış siparişinde doğrudan teslimatı devre dışı bırakın. | Şirketlerarası satış siparişi satırı minimum **Malzeme çekme listesi**, **Çıkış emri** veya **Malzeme çekme listesi günlüğü** durumuna ulaştıysa orijinal satış siparişindeki **Doğrudan teslimat** alanını değiştiremezsiniz. Şirketlerarası satınalma siparişindeki teslimat adresi, standart teslimat adresi (standart satınalma siparişi teslimat adresi) olarak değiştirilir. Ayrıca şirketlerarası satınalma siparişi satırları, satırlar için standart teslimat adresi olarak değiştirilir. İkisi de şirketlerarası satış siparişi ve satırlar ile eşitlenir. Orijinal satış siparişindeki tüm satırlarda teslimat türü **Yok** olarak değiştirilir ve alan, şirketlerarası satınalma siparişi satırı ile eşitlenir. Harici satıcılara verdiğiniz satınalma siparişleri etkilenmez; ayrıca harici satıcılara yönelik satınalma siparişi satırlarıyla bağlantılı orijinal satış satırları da etkilenmez. Şirketlerarası satınalma siparişi ve satırlarındaki teslimat tarihi ve şirketlerarası satış siparişi ve satırlarındaki Talep edilen giriş/sevkiyat tarihleri güncelleştirilir. |
| Orijinal bir satış siparişinde doğrudan teslimatı etkinleştirin. | Şirketlerarası satış siparişi satırı minimum **Malzeme çekme listesi**, **Çıkış emri** veya **Malzeme çekme listesi günlüğü** durumuna ulaştıysa orijinal satış siparişindeki **Doğrudan teslimat** alanını değiştiremezsiniz. Şirketlerarası satınalma siparişindeki teslimat adresi orijinal satış siparişindeki teslimat adresine dönüştürülür ve şirketlerarası satış siparişiyle eşitlenir. Orijinal satış siparişindeki tüm satırlarda teslimat türü **Doğrudan teslimat** olarak değiştirilir ve alan, şirketlerarası satınalma siparişi satırı ile eşitlenir. Her orijinal satış siparişi satırındaki teslimat adresi hem şirketlerarası satınalma siparişi satırlarıyla hem şirketlerarası satış siparişi satırlarıyla eşitlenir. Şirketlerarası satınalma siparişi ve satırlarındaki teslimat tarihi ve şirketlerarası satış siparişi ve satırlarındaki Talep edilen giriş/sevkiyat tarihleri güncelleştirilir. |
| Orijinal satış siparişi başlığına ve satırlara not ekleyin. | Not, şirketlerarası satınalma siparişine ve şirketlerarası satış siparişine kopyalanır. |
| Notu değiştirin veya silin. | Notu değiştirir veya silerseniz şirketlerarası satınalma siparişi ve şirketlerarası satış siparişindeki karşılık gelen not da buna göre değiştirilir veya silinir. |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
