---
title: "Otomatik kapatma ve önceliği"
description: "Bu makalede Alacak hesapları parametreleri sayfasında Otomatik kapatmayı seçtiğinizde hareketlerin nasıl kapatılacağı açıklanmıştır. Ayrıca, otomatik kapatmanın ödeme önceliği ile birlikte nasıl kullanılabileceği de açıklanmıştır."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustOpenTrans, CustParameters, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14531
ms.assetid: e7837cf6-ec69-44b4-8d47-eba38d5c7b1f
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: a751973b49febd6925267d00fb1d2c72114f86b0
ms.lasthandoff: 03/31/2017


---

# <a name="automatic-settlement-and-prioritization"></a>Otomatik kapatma ve önceliği

Bu makalede Alacak hesapları parametreleri sayfasında Otomatik kapatmayı seçtiğinizde hareketlerin nasıl kapatılacağı açıklanmıştır. Ayrıca, otomatik kapatmanın ödeme önceliği ile birlikte nasıl kullanılabileceği de açıklanmıştır.

Ödemeleri faturalar ve diğer hareketlerle kapatma sırasında iki seçeneğiniz vardır. Hareketleri kapatmak için el ile seçebilir veya Microsoft Dynamics 365 işlemleri için hareketleri otomatik olarak otomatik kapatma işlevini kullanarak seçebilirsiniz. **Kapatma önceliklendirme** seçeneğini kullanarak otomatik kapatmaların nasıl işleneceğini de özelleştirebilirsiniz. Bu seçenekler üzerinde tanımlanan kapanış parametreleri parçası olan **Accounts receivable parameters** sayfa. Hareketlerin otomatik olarak kapatılabileceği yollar, otomatik kapatma için kullandığınız yönteme bağlı olarak farklılık gösterebilir. Aşağıdaki yöntemler kullanılabilir:

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
| Vade farkı dekontu | 15 Ekim  | 7,00   |                     |                    | Bu vade farkı dekontu 1 ve 2 fatura için fatura edilir. Tutar, yüzde 2 oranında faiz en az 30 gün olan tutarları üzerinden hesaplanır Kaçırılmış. Örneğin, 0,02 × (100,00 + 250,00) = 7,00. |

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




