---
title: Faturalarda TDS hesaplaması
description: Bu makale, Kaynakta Kesilen Verginin (TDS) fatura düzeyinde hesaplandığı hareketler için bir başvuru kaynağıdır.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: efc12e0839fe87e9db435f481ce1fd733c286d6c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855377"
---
# <a name="tds-calculation-on-invoices"></a>Faturalarda TDS hesaplaması

[!include [banner](../includes/banner.md)]

Bu makale, Kaynakta Kesilen Verginin (TDS) fatura düzeyinde hesaplandığı hareketler için bir başvuru kaynağıdır.

| Seri numarası | Hareket türü                                 | Hareket tutarı | Sayfa adı ve seçim yolu                                 | Hesap türü ve mahsup hesap türü                         |
| ------------- | ------------------------------------------------ | ------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 1.            | Satıcı/kayıt giderlerinden yapılan satınalma   | Borç  Veya  Alacak  | Yevmiye defterleri sayfası (Genel muhasebe > Günlük girişleri > Yevmiye defterleri), Fatura onay günlüğü sayfası (Borç hesapları > Faturalar > Fatura onayı), Fatura günlüğü sayfası (Borç hesapları > Fatura > Fatura günlüğü) | Genel muhasebe (Dr.)  Satıcı (Cr.).  Stopaj vergisi, Genel muhasebe hesabının deftere nakil türü **Nakit** **satınalmalar** olduğunda, yalnızca Satıcı-Genel muhasebe  birleşimi için hesaplanır. |
| 2.            | Müşteri/kayıt giderlerinden yapılan satınalma | Borç  Veya  Alacak  | Yevmiye defterleri sayfası (Genel muhasebe >  Günlük girişleri > Yevmiye defterleri), Fatura günlüğü sayfası (Borç hesapları >  Faturalar > Fatura günlüğü) | Genel muhasebe (Dr.)  Müşteri (Cr.)                                 |
| 3.            | Satıcıdan sabit kıymet satınalma              | Borç  Veya  Alacak  | Yevmiye defterleri sayfası (Genel muhasebe > Günlük girişleri > Yevmiye defterleri), Fatura kaydı günlüğü sayfası (Borç hesapları > Faturalar > Fatura kaydı), Fatura günlüğü sayfası (Borç hesapları > Fatura > Fatura günlüğü) | Sabit kıymetler (Dr.)  Satıcı (Cr.)                             |
| 4.            | Müşteriden sabit kıymet satınalma            | Borç  Veya  Alacak  | Yevmiye defterleri sayfası (Genel muhasebe >  Günlük girişleri > Yevmiye defterleri), Fatura günlüğü sayfası (Borç hesapları >  Faturalar > Fatura günlüğü) | Sabit kıymetler (Dr.)  Müşteri (Cr.)                           |
| 5.            | Satınalma faturası  (TDS borçları)                  |                    | Satınalma siparişi sayfası (Borç hesapları > Satınalma siparişleri > Tüm satınalma siparişleri) |                                                              |
| 6.            | Satış faturası  (TDS alacakları)                  |                    | Satış siparişi sayfası (Alacak hesapları > Siparişler > Tüm satış siparişleri), Serbest metin fatura sayfası (Alacak hesapları > Faturalar > Tüm serbest metin faturaları) |                                                              |
