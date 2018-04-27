---
title: "Field Service'taki sözleşme faturalarını Finance and Operations'taki serbest metin faturalarıyla eşitleme"
description: "Bu konu, Microsoft Dynamics 365 for Field Service'taki sözleşme faturalarını Microsoft Dynamics 365 for Finance and Operations'taki serbest metin faturalarıyla eşitlemek için temel görevleri ve şablonları açıklar."
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08cfd2cfa24bef0f0c92126f5d1052a12ceba37a
ms.openlocfilehash: 1863814d6dd645da8602495858d024fbad2e7149
ms.contentlocale: tr-tr
ms.lasthandoff: 04/11/2018

---

# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-finance-and-operations"></a>Field Service'taki sözleşme faturalarını Finance and Operations'taki serbest metin faturalarıyla eşitleme

[!include[banner](../includes/banner.md)]

Bu konu, Microsoft Dynamics 365 for Field Service'taki sözleşme faturalarını Microsoft Dynamics 365 for Finance and Operations'taki serbest metin faturalarıyla eşitlemek için temel görevleri ve şablonları açıklar.

## <a name="templates-and-tasks"></a>Şablonlar ve görevler

Aşağıdaki şablon ve temel görevler Field Service'taki sözleşme faturaları ile Finance and Operations'taki serbest metin faturaları eşitlemesi çalıştırmak için kullanılır.

**Veri tümleştirmesindeki şablonun adı:**

- Sözleşme faturaları (Field Service to Fin and Ops)

**Veri tümleştirme projesindeki görevlerin adları:**

- Fatura başlıkları
- Fatura satırları

Aşağıdaki eşitleme faturası faturalarının eşitlemesinin gerçekleştirilebilmesi için gereklidir:

- Hesaplar (Sales'ten Fin and Ops'a) - Doğrudan

## <a name="entity-set"></a>Varlık kümesi

| Field Service  | Finance and Operations                 |
|----------------|----------------------------------------|
| faturalar       | CDS müşteri serbest metin faturası başlıkları |
| invoicedetails | CDS müşteri serbest metin faturası satırları   |

## <a name="entity-flow"></a>Varlık akışı

Field Service'taki bir sözlemeden oluşturulan faturalar Common Data Service (CDS) Veri tümleştirme projesi aracılığıyla Finance and Operations ile eşitlenebilir. Bu faturalardaki güncelleştirmeler serbest metin faturaları muhasebe durumunun **İşlemde** olması durumunda Finance and Operations'taki serbest metin faturalarıyla eşitlenecektir. Serbest metin faturaları Finance and Operations'da defetere nakledildikten ve muhasebe durumu **Tamamlandı** olarak güncelleştirildikten sonra Field Service'tan güncelleştirmeleri eşitleyemezsiniz.

## <a name="field-service-crm-solution"></a>Field Service CRM çözümü

**Sözleşme Kaynaklı Satırlar Var** alanı **Fatura** varlığına eklenmiştir. Bu alan yalnızca bir sözleşmeden oluşturulan faturaların eşitlenmesini sağlamaya yardımcı olur. Fatura bir sözleşemeden kaynaklanan en az bir satır içeriyorsa değer **doğru** olur.

**Sözleşme Kaynağı Var** alanı **Fatura Satırı** varlığına eklenmiştir. Bu alan yalnızca bir sözleşmeden oluşturulan fatura satırlarının eşitlenmesini sağlamaya yardımcı olur. Fatura satırının kaynağı bir sözleşmeyse değer **doğru** olur.

**Fatura tarihi** Finance and Operations'ta zorunlu bir alandır. Bu nedenle, eşitlemeden önce Field Service'ta alanın bir değeri olmalıdır. Bu gereksinimi karşılamak için aşağıdaki mantık eklenir:

- **Fatura Tarihi** alanı **Fatura** varlığında boşsa (diğer bir deyişle, değer yoksa), bu alan bir sözleşmeden kaynaklanan bir fatura satırının eklendiği geçerli tarih olarak ayarlanır.
- Kullanıcı, **Fatura Tarihi** alanını değiştirebilir. Ancak, kullanıcı bir sözleşemeden kaynaklanan fatura kaydetmeye çalıştığında, faturada **Fatura Tarihi** alanının boş olması durumunda bir iş süreci hatası alır.

## <a name="prerequisites-and-mapping-setup"></a>Önkoşullar ve eşleme kurulumu

### <a name="in-finance-and-operations"></a>Finance and Operations'ta

Field Service'ta sözleşme faturalarından oluşturulan Finance and Operations'taki serbest metin faturalarını ayırmak amacıyla tümleştirmek için bir fatura kaynağı ayarlanmalıdır. Bir faturanın kaynağı **Sözleşme faturası tümleştirmesi** türünde olduğunda, **Harici fatura numarası** alanı **Satış faturası** başlığında gösterilir.

Fatura başlığında görünmesinin yanı sıra **Harici fatura numarası** bilgileri Filed Service'taki sözleşme faturalarından oluşturulan faturaların Finance and Operations'tan Field Service'a fatura eşitleme sırasında filtrelenmesini sağlamaya yardımcı olur.

1. **Alacak hesapları** \> **Kurulum** \> **Fatura kaynağı kodları**'na gidin.
2. **Yeni**'yi seçerek yeni bir fatura kaynağı oluşturun.
3. **Fatura kaynağı** alanına, fatura kaynağı için **FS** gibi bir ad girin.
4. **Açıklama** alanında, **Field Service Sözleşme Faturası** gibi bir açıklama girin.
5. **Kaynak türü ataması** onay kutusunu seçin.
6. **Fatura kaynağı türü** alanını **Sözleşme faturası tümleştirmesi** olarak ayarlayın.
7. **Kaydet**'i seçin.

### <a name="in-the-data-integration-project"></a>Veri Tümleştirme projesinde

Görev: **Fatura satırları**  

Finance and Operations **Ana Hesap Görünen Değeri** alanı için varsayılan değerin istenen değerle eşleşmek üzere güncelleştirilmesini sağlayın.

Varsayılan şablon değeri **401100**'dur.

