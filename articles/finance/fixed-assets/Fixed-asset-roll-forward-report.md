---
title: Sabit kıymet ileri taşıma raporu
description: Bu makalede, Sabit kıymet ileri sarma raporunun nasıl kullanıldığı açıklanmaktadır.
author: moaamer
ms.date: 01/08/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2017-12-20
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: a4d423b149957e624269231aede510190f0c14c7
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068795"
---
# <a name="fixed-assets-roll-forward-report"></a>Sabit kıymet ileri taşıma raporu

[!include [banner](../includes/banner.md)]

**Sabit kıymet ileri taşıma** raporu dönem kapanışı, mali tablolar ve vergi raporlama için gerekli olarak ayrıntılı sabit kıymet verilerini okunması kolay Microsoft Excel biçiminde sunar. Rapor sabit kıymetlere ilişkin başlangıç ve bitiş bakiyelerini, döneme ait değerleme hareketlerini ve dönem süresinde gerçekleşen yeni kıymet alımlarını ve elden çıkarmaları içerir. Veriler her sabit kıymet için ayrı olarak rapor edilir ve değerler sabit kıymet grupları ve tüzel kişilik için özetlenir.

**Sabit kıymet ileri taşıma** raporu Elektronik raporlama (ER) altyapısını kullanır. Raporu çalıştırmadan önce Sabit kıymet modeli ve Sabit kıymet ileri taşıma yapılandırmalarının Microsoft Dynamics Lifecycle Services'dan (LCS) içe aktarılması gerekir. Yönergeler için bkz. [Lifecycle Services'dan Elektronik raporlama yapılandırmalarını karşıdan yükle](/dynamics365/unified-operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).

Bu rapor, Microsoft Dynamics 365 Finance, Enterprise edition 7.3 içinde veya bir düzeltme olarak Microsoft Dynamics 365 Finance, Enterprise edition (Temmuz 2017) içinde kullanılabilir. Temmuz 2017 sürümüne sahip ortamlara üç düzeltme uygulanması gerekir:

- **BB 4041754:** Elektronik raporlama (ER) yapılandırması, platform güncelleştirme paketi uygulandıktan sonra geçerli sürüm için uygun olmadığından LCS'den indirilemez.
- **BB 4056107:** Elektronik raporlama (GER) toplu güncelleştirmesi 5
- **BB 4056353:** Sabit Kıymet Ekstre ve Notlar raporu GAAP ve IFRS'deki gereklilikleri karşılamamaktadır

Aşağıdaki tabloda, raporda kullanılabilecek alanlar açıklanmıştır.


|                    Alan                    |                                                                                                                                Tanım                                                                                                                                |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|              Bakiyeler: Açılış              |                                                                                           Raporda belirtilen başlangıç tarihinden itibaren sabit kıymetin net defter değeri.                                                                                           |
|              Bakiyeler: Kapanış              |                                                                                            Raporda belirtilen bitiş tarihi itibarıyla sabit kıymetin net defter değeri.                                                                                            |
|         Alımlar: Açılış değeri         |                                                 <strong>Alım</strong> ve <strong>Alım düzeltmesi</strong> türündeki tüm hareketlerin raporda belirtilen "başlangıç" tarihine kadar olan toplamı.                                                  |
|      Alımlar: Dönem alımları      |                                                 Rapor tarih aralığında deftere nakledilmiş olan <strong>Alım</strong> ve <strong>Alım düzeltmesi</strong> türündeki tüm hareketlerinin toplamı.                                                  |
|       Alımlar: Dönem elden çıkarmaları        |                                                                        Rapor tarih aralığında elden çıkarma hareketi olan deftere nakledilmiş tüm alım ters işlemlerinin toplamı.                                                                        |
|         Alımlar: Kapanış değeri         |                                                  <strong>Alım</strong> ve <strong>Alım düzeltmesi</strong> türündeki tüm hareketlerin raporda belirtilen "bitiş" tarihine kadar olan toplamı.                                                   |
|        Amortismanlar: Açılış değeri         | <strong>Amortisman</strong>, <strong>Amortisman düzeltmesi</strong>, <strong>Özel amortisman payı</strong> ve <strong>Olağanüstü amortisman</strong> türündeki tüm hareketlerin raporda belirtilen "başlangıç" tarihine kadar olan toplamı. |
|     Amortismanlar: Dönem amortismanları     |                         Rapor tarih aralığında deftere nakledilmiş olan <strong>Amortisman</strong>, <strong>Amortisman düzeltmesi</strong> ve <strong>Olağanüstü amortisman</strong> türündeki tüm hareketlerinin toplamı.                          |
| Amortismanlar: Dönem özel amortismanları |                                                              Rapor tarih aralığında deftere nakledilmiş olan <strong>Özel amortisman payı</strong> türündeki tüm hareketlerinin toplamı.                                                               |
|       Amortismanlar: Dönem elden çıkarmaları       |                                                                       Rapor tarih aralığında elden çıkarma hareketi olan deftere nakledilmiş tüm amortisman ters işlemlerinin toplamı.                                                                        |
|        Amortismanlar: Kapanış değeri         |  <strong>Amortisman</strong>, <strong>Amortisman düzeltmesi</strong>, <strong>Özel amortisman payı</strong> ve <strong>Olağanüstü amortisman</strong> türündeki tüm hareketlerin raporda belirtilen "bitiş" tarihine kadar olan toplamı.  |
|    Değer artışları/Değer azalışları: Açılış değeri     |                              <strong>Değer artışı düzeltmesi</strong>, <strong>Değer azalışı düzeltmesi</strong> ve <strong>Yeniden değerleme</strong> türündeki tüm hareketlerin raporda belirtilen "başlangıç" tarihine kadar olan toplamı.                               |
|   Değer artışları/Değer azalışları: Dönem değer artışları   |                                                                    Rapor tarih aralığında deftere nakledilmiş olan <strong>Değer artışı düzeltmesi</strong> türündeki tüm hareketlerinin toplamı.                                                                    |
|  Değer artışları/Değer azalışları: Dönem değer azalışları  |                                                                   Rapor tarih aralığında deftere nakledilmiş olan <strong>Değer azalışı düzeltmesi</strong> türündeki tüm hareketlerinin toplamı.                                                                   |
| Değer artışları/Değer azalışları: Dönem yeniden değerlemeleri  |                                                                        Rapor tarih aralığında deftere nakledilmiş olan <strong>Yeniden değerleme</strong> türündeki tüm hareketlerinin toplamı.                                                                        |
|   Değer artışları/Değer azalışları: Dönem elden çıkarmaları   |                                                           Rapor tarih aralığında elden çıkarma hareketi olan deftere nakledilmiş tüm değer artışı, değer azalışı ve yeniden değerleme ters işlemlerinin toplamı.                                                           |
|    Değer artışları/Değer azalışları: Kapanış değeri     |                               <strong>Değer artışı düzeltmesi</strong>, <strong>Değer azalışı düzeltmesi</strong> ve <strong>Yeniden değerleme</strong> türündeki tüm hareketlerin raporda belirtilen "bitiş" tarihine kadar olan toplamı.                                |
|          Elden çıkarmalar: Elden çıkarma tarihi           |                                                                                                                Sabit kıymet defteri için elden çıkarma tarihi.                                                                                                                |
|    Elden çıkarmalar: Elden çıkarmadaki net defter değeri    |                                                                                                    Sabit kıymet defterinin elden çıkarma tarihindeki net defter değeri.                                                                                                    |
|            Elden çıkarmalar: Satış değeri            |                                                                                               Sabit kıymet defteri için bir elden çıkarma - satış hareketiyle satış değeri.                                                                                                |
|           Elden çıkarmalar: Hurda değeri            |                                                                                               Sabit kıymet defteri için bir elden çıkarma - hurda hareketiyle hurda değeri.                                                                                               |
|           Elden çıkarmalar: Kar/Zarar            |                                                                                 Sabit kıymet defteri için elden çıkarma hareketinin bir parçası olarak hesaplanan kar veya zarar değeri.                                                                                 |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]

