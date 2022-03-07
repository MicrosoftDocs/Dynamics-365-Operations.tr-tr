---
title: Faturalarda TDS hesaplaması
description: Bu konu, Kaynakta Kesilen Vergi (TDS) fatura düzeyinde hesaplandığında hareketler için bir referans sağlar.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 496e87e3028025f738d2f0a697d91c18b77ad1c9
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023662"
---
# <a name="tds-calculation-on-invoices"></a>Faturalarda TDS hesaplaması

[!include [banner](../includes/banner.md)]

Bu konu, Kaynakta Kesilen Vergi (TDS) fatura düzeyinde hesaplandığında hareketler için bir referans sağlar.

| Seri numarası | Hareket türü                                 | Hareket tutarı | Sayfa adı ve seçim yolu                                 | Hesap türü ve mahsup hesap türü                         |
| ------------- | ------------------------------------------------ | ------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 1.            | Satıcı/kayıt giderlerinden yapılan satınalma   | Borç  Veya  Alacak  | Yevmiye defterleri sayfası (Genel muhasebe > Günlük girişleri > Yevmiye defterleri), Fatura onay günlüğü sayfası (Borç hesapları > Faturalar > Fatura onayı), Fatura günlüğü sayfası (Borç hesapları > Fatura > Fatura günlüğü) | Genel muhasebe (Dr.)  Satıcı (Cr.).  Stopaj vergisi, Genel muhasebe hesabının deftere nakil türü **Nakit** **satınalmalar** olduğunda, yalnızca Satıcı-Genel muhasebe  birleşimi için hesaplanır. |
| 2.            | Müşteri/kayıt giderlerinden yapılan satınalma | Borç  Veya  Alacak  | Yevmiye defterleri sayfası (Genel muhasebe >  Günlük girişleri > Yevmiye defterleri), Fatura günlüğü sayfası (Borç hesapları >  Faturalar > Fatura günlüğü) | Genel muhasebe (Dr.)  Müşteri (Cr.)                                 |
| 3.            | Satıcıdan sabit kıymet satınalma              | Borç  Veya  Alacak  | Yevmiye defterleri sayfası (Genel muhasebe > Günlük girişleri > Yevmiye defterleri), Fatura kaydı günlüğü sayfası (Borç hesapları > Faturalar > Fatura kaydı), Fatura günlüğü sayfası (Borç hesapları > Fatura > Fatura günlüğü) | Sabit kıymetler (Dr.)  Satıcı (Cr.)                             |
| 4.            | Müşteriden sabit kıymet satınalma            | Borç  Veya  Alacak  | Yevmiye defterleri sayfası (Genel muhasebe >  Günlük girişleri > Yevmiye defterleri), Fatura günlüğü sayfası (Borç hesapları >  Faturalar > Fatura günlüğü) | Sabit kıymetler (Dr.)  Müşteri (Cr.)                           |
| 5.            | Satınalma faturası  (TDS borçları)                  |                    | Satınalma siparişi sayfası (Borç hesapları > Satınalma siparişleri > Tüm satınalma siparişleri) |                                                              |
| 6.            | Satış faturası  (TDS alacakları)                  |                    | Satış siparişi sayfası (Alacak hesapları > Siparişler > Tüm satış siparişleri), Serbest metin fatura sayfası (Alacak hesapları > Faturalar > Tüm serbest metin faturaları) |                                                              |
