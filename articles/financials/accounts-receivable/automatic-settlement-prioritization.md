---
title: "Otomatik kapatma ve önceliklendirme"
description: "Bu makalede Alacak hesapları parametreleri sayfasında Otomatik kapatmayı seçtiğinizde hareketlerin nasıl kapatılacağı açıklanmıştır. Ayrıca, otomatik kapatmanın ödeme önceliği ile birlikte nasıl kullanılabileceği de açıklanmıştır."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustOpenTrans, CustParameters, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14531
ms.assetid: e7837cf6-ec69-44b4-8d47-eba38d5c7b1f
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7a0f87aca78f1263f1f6ce65e2629b91312716cb
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="automatic-settlement-and-prioritization"></a>Otomatik kapatma ve önceliklendirme

[!include[banner](../includes/banner.md)]


Bu makalede Alacak hesapları parametreleri sayfasında Otomatik kapatmayı seçtiğinizde hareketlerin nasıl kapatılacağı açıklanmıştır. Ayrıca, otomatik kapatmanın ödeme önceliği ile birlikte nasıl kullanılabileceği de açıklanmıştır.

Ödemeleri faturalar ve diğer hareketlerle kapatma sırasında iki seçeneğiniz vardır. Microsoft Dynamics 365 for Finance and Operations hareketleri otomatik olarak otomatik kapatma işlevini kullanarak seçebilir veya kapatmak için hareketleri el ile seçebilirsiniz. **Kapatma önceliklendirme** seçeneğini kullanarak otomatik kapatmaların nasıl işleneceğini de özelleştirebilirsiniz. Tüm bu özellikler, **Alacak hesapları parametreleri** sayfasında tanımlanan kapatma parametrelerinin parçasıdır. Hareketlerin otomatik olarak kapatılabileceği yollar, otomatik kapatma için kullandığınız yönteme bağlı olarak farklılık gösterebilir. Aşağıdaki yöntemler kullanılabilir:

-   Kullanıcı tanımlı kapatma önceliği
-   Varsayılan otomatik kapatma

Aşağıdaki bölümlerde, her bir yöntem için hareketlerin nasıl kapatılacağı açıklanmaktadır.

## <a name="example-transactions"></a>Örnek hareketler
Bu makalenin sonraki bölümlerindeki kapatma örnekleri, aşağıdaki hareketleri temel alır. Tüm hareketler müşteri 2050 içindir.

| İşlem   | Tarih        | Tutar | Nakit iskontosu koşulları | Nakit iskontosu tarihi | Açıklamalar                                                                                                                                                                                      |
|---------------|-------------|--------|---------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fatura 1     | 15 Ağustos   | 100,00 | %2 14, Net 30        | 29 Ağustos          |                                                                                                                                                                                               |
| Fatura 2     | 1 Eylül | 250,00 | %2 14, Net 30        | 15 Eylül       |                                                                                                                                                                                               |
| Fatura 3     | 15 Ekim  | 500,00 | %2 14/Net 30        | 29 Ekim         |                                                                                                                                                                                               |
| Vade farkı dekontu | 15 Ekim  | 7,00   |                     |                    | Bu vade farkı dekontu fatura 1 ve fatura 2 içindir. Tutar, süresi 30 gün veya daha fazla geçen tutarlar üzerinde yüzde 2 faiz olarak hesaplanır. Örneğin, 0,02 × (100,00 + 250,00) = 7,00. |

## <a name="userdefined-settlement-priority"></a>Kullanıcı tanımlı kapatma önceliği
**Otomatik kapatmalar için öncelik kullan** ayarını **Alacak hesapları parametreleri** sayfasında **Evet** yaparsanız, otomatik kapatma için hareketler seçilirken **Kapatma önceliği** sayfasında tanımladığınız kapatma önceliği kullanılır. Bu örnekte, aşağıdaki kapatma önceliği tanımlanır:

1.  Hareket türü
    -   Ödeme masrafları
    -   Tahsilat mektupları
    -   Vade farkı dekontları
    -   Faturalar

2.  Hareket tarihi, Artarak
3.  Fiş

25 Ekimde 700,00 için bir ödeme naklederseniz, ödeme harekete aşağıdaki sırada kapatılır.

| Fiş       | Tarih       | Fatura | Hareket para birimi cinsinden tutar | Kapatılacak tutar | Kalan | Para Birimi |
|---------------|------------|---------|--------------------------------|------------------|---------|----------|
| Vade farkı dekontu | 15/10/2015 |         | 7,00                           | 7,00             | 0,00    | ABD Doları      |
| Fatura 1     | 15/8/2015  | 10001   | 100,00                         | 100,00           | 0,00    | ABD Doları      |
| Fatura 2     | 1/9/2015   | 10002   | 250,00                         | 250,00           | 0,00    | ABD Doları      |
| Fatura 3     | 15/10/2015 |         | 500,00                         | 343,00           | 157,00  | ABD Doları      |

## <a name="default-automatic-settlement"></a>Varsayılan otomatik kapatma
Kullanıcı tanımlı bir kapatma önceliği yoksa, hareketler otomatik olarak vade tarihi temel alınarak kapatma için seçilecektir. Kapatılan hareketlerin kapatıldıkları hareketle aynı para birimine sahip olması gerekir. 25 Ekimde 700,00 için bir ödeme naklederseniz, kapatma için aşağıdaki hareketler seçilir.

| Fiş       | Tarih       | Fatura | Hareket para birimi cinsinden tutar | Kapatılacak tutar | Kalan | Para Birimi |
|---------------|------------|---------|--------------------------------|------------------|---------|----------|
| Fatura 1     | 15/8/2015  | 10001   | 100,00                         | 100,00           | 0,00    | ABD Doları      |
| Fatura 2     | 1/9/2015   | 10002   | 250,00                         | 250,00           | 0,00    | ABD Doları      |
| Fatura 3     | 15/10/2015 |         | 500,00                         | 350,00           | 150,00  | ABD Doları      |
| Vade farkı dekontu | 15/10/2015 |         | 7,00                           | 0,00             | 0,00    | ABD Doları      |






