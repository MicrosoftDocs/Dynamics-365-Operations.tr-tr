---
title: Şirketlerarası parametreler
description: Bu konuda, şirketlerarası parametreler açıklanmaktadır
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchLineOpenOrder, InterCompanyTradingRelationSetupCustomer
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: face3cbd21998edcba528548ec4ae52354330aa3
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/09/2021
ms.locfileid: "7778509"
---
# <a name="intercompany-parameters"></a>Şirketlerarası parametreler

[!include [banner](../../includes/banner.md)]

Şirketlerarası bir organizasyonda farklı tüzel kişilikler arasında nasıl ticaret yaptığınızı belirleyen parametreler ayarlayabilirsiniz. Bu parametreler, seçtiğiniz alanlar tarafından belirlenir. Farklı ticaret senaryolarını yansıtmak için farklı birleşimler seçebilirsiniz.

Aşağıdaki iki örnekte, birinde iki ve diğerinde üç düzey bulunan şirketlerarası organizasyonlar için senaryolar açıklanmaktadır.

## <a name="example-1-two-level-intercompany-chain"></a>Örnek 1: İki düzeyli şirketlerarası zincir

Şirketlerarası organizasyon aşağıdaki tüzel kişilikleri içerir:

- Tüzel kişilik A: Harici müşterilere satış yapar ancak stoku yoktur. Bu tüzel kişilik, Tüzel kişilik B'den satın alır.
- Tüzel kişilik B: Yalnızca Tüzel kişilik A'ya satış yapar.

İki tüzel kişilik, birbirilerinden satın alabilir ve birbirlerine satış yapabilir.

Bu örnekte, harici müşteriye yöneltilen ve orijinal satış siparişinde yer alan fiyatlandırma her zaman satış fiyatını temel alır. Şirketlerarası satış siparişindeki ve şirketlerarası satınalma siparişindeki fiyatlandırma, Tüzel kişilik B'deki şirketlerarası satış siparişinde bulunan dahili satış veya transfer fiyatlandırması tarafından kontrol edilir.

Sipariş başlığı bilgileri, orijinal satış siparişinden harici müşteriye kadar kontrol edilir. Şirketlerarası satış siparişindeki değişiklikler, orijinal satış siparişiyle eşitlenmez.

Tüzel kişilik A'da, satıcılar için **Şirketlerarası** sayfasında **Satınalma siparişi politikaları**'nı seçin. **Orijinal satış siparişi (doğrudan teslimat)** alan grubunda aşağıdaki alanları seçin:

- **Sevk irsaliyesini otomatik olarak yazdır**
- **Faturayı otomatik olarak deftere naklet**
- **Faturayı otomatik olarak yazdır**

**Şirketlerarası satınalma siparişi (doğrudan teslimat)** alan grubunda aşağıdaki alanı seçin:

- **Faturayı otomatik olarak deftere naklet**

**Orijinal satış siparişi <-> Şirketlerarası satınalma siparişi** grubunda aşağıdaki alanları seçin:

- **Müşteri bilgileri**
- **RMA numarası**

**Şirketlerarası satınalma siparişi <-> Şirketlerarası satış siparişi** alan grubunda aşağıdaki alanları seçin:

- **Müşteri bilgileri**
- **RMA numarası**
- **Parti numarası**
- **Seri numarası**

Tüzel kişilik B'de, müşteriler için **Şirketlerarası** sayfasında **Satış siparişi politikaları**'nı seçin. **Şirketlerarası satış siparişi oluşturma** alan grubunda aşağıdaki alanları seçin:

- **Satış siparişi numaralandırma** : **Sipariş + orijinal numara**
- **Orijinal müşteriye ait belgelerin özet güncelleştirmesine izin ver**

**Şirketlerarası satış siparişi fiyatları** alan grubunda aşağıdaki alanları seçin:

- **Fiyat ve iskonto arama**
- **Fiyat düzenlemesine izin ver**
- **İskonto düzenlemesine izin ver**

**Şirketlerarası satış siparişi \> Şirketlerarası satınalma siparişi** alan grubunda aşağıdaki alanları seçin:

- **Parti numarası**
- **Seri numarası**

## <a name="example-2-three-level-intercompany-chain"></a>Örnek 2: Üç düzeyli şirketlerarası zincir

Şirketlerarası organizasyon aşağıdaki tüzel kişilikleri içerir:

- Tüzel kişilik A: Harici müşterilere satış yapan ve Tüzel kişilik B'den satın alan bir satış tüzel kişiliği.
- Tüzel kişilik B: Ürün teslim edemeyen ve Tüzel kişilik C'den satın alan bir üretim veya dağıtım tüzel kişiliği.
- Tüzel kişilik C: Tüzel kişilik B'ye ürün teslim eden bir üretim veya dağıtım tüzel kişiliği.

Tüzel kişilik B ile C arasındaki dahili transfer fiyatlandırması, zincir başlangıcında satış yapan tüzel kişilikten gelen maliyet fiyatıdır. Ayrıca harici müşterilere satış yapan Tüzel kişilik A için de maliyet fiyatıdır. Bununla birlikte, harici müşteriye giden orijinal satış siparişindeki fiyatlandırma her zaman satış fiyatını temel alır.

Tüm şirketlerarası satış siparişleri ve şirketlerarası satınalma siparişlerinde fiyatlandırma, şirketlerarası satış siparişinde kontrol edilir. Bu, zincir başlangıcında kontrol edilir. Bu nedenle Tüzel kişilik B'ye satış yapan Tüzel kişilik C, fiyatı kontrol eder. Şirketlerarası satış siparişi fiyatlandırması, Tüzel kişilik C'de ayarlanan dahili satış veya transfer fiyatlandırmasını temel alır.

Sipariş başlığı bilgileri, orijinal satış siparişinden harici müşteriye kadar kontrol edilir. Şirketlerarası siparişlerdeki değişiklikler, orijinal satış siparişiyle eşitlenmez.

Aşağıdaki parametrelerin seçilmesi gerekir:

Tüzel kişilik A'da, satıcılar için **Şirketlerarası** sayfasında **Satınalma siparişi politikaları**'nı seçin. **Orijinal satış siparişi (doğrudan teslimat)** alan grubunda aşağıdaki alanları seçin:

- **Sevk irsaliyesini otomatik olarak yazdır**
- **Faturayı otomatik olarak deftere naklet**
- **Faturayı otomatik olarak yazdır**

**Şirketlerarası satınalma siparişi (doğrudan teslimat)** alan grubunda aşağıdaki alanı seçin:

- **Faturayı otomatik olarak deftere naklet**

**Orijinal satış siparişi <-> Şirketlerarası satınalma siparişi** alan grubunda aşağıdaki alanları seçin:

- **Müşteri bilgileri**
- **RMA numarası**

**Şirketlerarası satınalma siparişi <-> Şirketlerarası satış siparişi** alan grubunda aşağıdaki alanları seçin:

- **Müşteri bilgileri**
- **RMA numarası**
- **Parti numarası**
- **Seri numarası**

Tüzel kişilik B'de, müşteriler için **Şirketlerarası** sayfasında **Satış siparişi politikaları**'nı seçin. **Şirketlerarası satış siparişi oluşturma** alan grubunda aşağıdaki alanları seçin:

- **Satış siparişi numaralandırma** : **Sipariş + orijinal numara**
- **Orijinal müşteriye ait belgelerin özet güncelleştirmesine izin ver**

**Şirketlerarası satış siparişi \> Şirketlerarası satınalma siparişi** alan grubunda aşağıdaki alanları seçin:

- **Parti numarası**
- **Seri numarası**

**Şirketlerarası müşteri faturasının deftere nakli** alan grubunda aşağıdaki alanları seçin:

- **Birim fiyat eşittir maliyet fiyatı**
- **Orijinal müşteri faturası naklini başlat**

Tüzel kişilik B'de, satıcılar için **Şirketlerarası** sayfasında **Satınalma siparişi politikaları**'nı seçin. **Orijinal satış siparişi (doğrudan teslimat)** alan grubunda aşağıdaki alanları seçin:

- **Sevk irsaliyesini otomatik olarak yazdır**
- **Faturayı otomatik olarak deftere naklet**
- **Faturayı otomatik olarak yazdır**

**Şirketlerarası satınalma siparişi (doğrudan teslimat)** alan grubunda aşağıdaki alanı seçin:

- **Faturayı otomatik olarak deftere naklet**

**Orijinal satış siparişi <-> Şirketlerarası satınalma siparişi** alan grubunda aşağıdaki alanları seçin:

- **Müşteri bilgileri**
- **RMA numarası**
- **Fiyat ve iskonto**

**Şirketlerarası satınalma siparişi <-> Şirketlerarası satış siparişi** alan grubunda aşağıdaki alanları seçin:

- **Müşteri bilgileri**
- **RMA numarası**
- **Parti numarası**
- **Seri numarası**

Tüzel kişilik C'de, müşteriler için **Şirketlerarası** sayfasında **Satış siparişi politikaları**'nı seçin. **Şirketlerarası satış siparişi oluşturma** alan grubunda aşağıdaki alanları seçin:

- **Satış siparişi numaralandırma** : **Numara serisi kodu**
- **Orijinal müşteriye ait belgelerin özet güncelleştirmesine izin ver**

**Şirketlerarası satış siparişi fiyatları** alan grubunda aşağıdaki alanı seçin:

- **Fiyat ve iskonto arama**

**Şirketlerarası müşteri faturasının deftere nakli** alan grubunda aşağıdaki alanları seçin:

- **Birim fiyat eşittir maliyet fiyatı**
- **Orijinal müşteri faturası naklini başlat**

**Şirketlerarası satış siparişi <-> Şirketlerarası satınalma siparişi** alan grubunda aşağıdaki alanları seçin:

- **Parti numarası**
- **Seri numarası**

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
