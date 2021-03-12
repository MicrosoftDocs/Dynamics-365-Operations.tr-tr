---
title: Field Service'daki sözleşme faturalarını Supply Chain Management'daki serbest metin faturalarıyla eşitleme
description: Sözleşme faturalarını Dynamics 365 Field Service üzerinden Dynamics 365 Supply Chain Management içindeki serbest metin faturalarına eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.
author: ChristianRytt
manager: tfehr
ms.date: 04/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: f1790366cebf317472bc1ef9a5ecd2a19fe755d3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980843"
---
# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-supply-chain-management"></a>Field Service'daki sözleşme faturalarını Supply Chain Management'daki serbest metin faturalarıyla eşitleme

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Sözleşme faturalarını Dynamics 365 Field Service üzerinden Dynamics 365 Supply Chain Management içindeki serbest metin faturalarına eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.

## <a name="templates-and-tasks"></a>Şablonlar ve görevler

Aşağıdaki şablon ve temel görevler Field Service'taki sözleşme faturaları ile Supply Chain Management'taki serbest metin faturaları eşitlemesi çalıştırmak için kullanılır.

**Veri tümleştirmesindeki şablonun adı**

- Sözleşme faturaları (Field Service'tan Supply Chain Management'a)

**Veri tümleştirme projesindeki görevlerin adları**

- Fatura başlıkları
- Fatura satırları

Aşağıdaki eşitleme faturası faturalarının eşitlemesinin gerçekleştirilebilmesi için gereklidir:

- Hesaplar (Sales'ten Supply Chain Management'a) - Doğrudan

## <a name="entity-set"></a>Varlık kümesi

| Field Service  | Supply Chain Management                 |
|----------------|----------------------------------------|
| faturalar       | Dataverse müşteri serbest metin faturası üst bilgileri |
| invoicedetails | Dataverse müşteri serbest metin faturası satırları   |

## <a name="entity-flow"></a>Varlık akışı

Field Service'taki bir sözlemeden oluşturulan faturalar Microsoft Dataverse Veri tümleştirme projesi aracılığıyla Supply Chain Management ile eşitlenebilir. Bu faturalardaki güncelleştirmeler serbest metin faturaları muhasebe durumunun **İşlemde** olması durumunda Supply Chain Management'taki serbest metin faturalarıyla eşitlenecektir. Serbest metin faturaları Supply Chain Management'da defetere nakledildikten ve muhasebe durumu **Tamamlandı** olarak güncelleştirildikten sonra Field Service'tan güncelleştirmeleri eşitleyemezsiniz.

## <a name="field-service-crm-solution"></a>Field Service CRM çözümü

**Sözleşme Kaynaklı Satırlar Var** sütunu **Fatura** tablosuna eklenmiştir. Bu sütun, yalnızca bir sözleşmeden oluşturulan faturaların eşitlenmesini sağlamaya yardımcı olur. Fatura bir sözleşemeden kaynaklanan en az bir satır içeriyorsa değer **doğru** olur.

**Sözleşme Kaynağı Var** sütunu **Fatura Satırı** tablosuna eklenmiştir. Bu sütun, yalnızca bir sözleşmeden oluşturulan fatura satırlarının eşitlenmesini sağlamaya yardımcı olur. Fatura satırının kaynağı bir sözleşmeyse değer **doğru** olur.

**Fatura tarihi** Supply Chain Management'ta zorunlu bir alandır. Bu nedenle, eşitlemeden önce Field Service'ta sütunun bir değeri olmalıdır. Bu gereksinimi karşılamak için aşağıdaki mantık eklenir:

- **Fatura Tarihi** sütunu **Fatura** tablosunda boşsa (diğer bir ifadeyle, değer yoksa), bu sütun bir sözleşmeden kaynaklanan bir fatura satırının eklendiği geçerli tarih olarak ayarlanır.
- Kullanıcı, **Fatura Tarihi** sütununu değiştirebilir. Ancak, kullanıcı bir sözleşemeden gelen bir fatura kaydetmeye çalıştığında, faturada **Fatura Tarihi** sütununun boş olması durumunda bir iş süreci hatası alır.

## <a name="prerequisites-and-mapping-setup"></a>Önkoşullar ve eşleme kurulumu

### <a name="in-supply-chain-management"></a>Supply Chain Management'ta

Field Service'ta sözleşme faturalarından oluşturulan Supply Chain Management'taki serbest metin faturalarını ayırmak amacıyla tümleştirmek için bir fatura kaynağı ayarlanmalıdır. Bir faturanın kaynağı **Sözleşme faturası tümleştirmesi** türünde olduğunda, **Harici fatura numarası** alanı **Satış faturası** başlığında gösterilir.

Fatura başlığında görünmesinin yanı sıra **Harici fatura numarası** bilgileri Filed Service'taki sözleşme faturalarından oluşturulan faturaların Supply Chain Management'tan Field Service'a fatura eşitleme sırasında filtrelenmesini sağlamaya yardımcı olur.

1. **Alacak hesapları** \> **Kurulum** \> **Fatura kaynağı kodları**'na gidin.
2. **Yeni**'yi seçerek yeni bir fatura kaynağı oluşturun.
3. **Fatura kaynağı** alanına, fatura kaynağı için **FS** gibi bir ad girin.
4. **Açıklama** alanında, **Field Service Sözleşme Faturası** gibi bir açıklama girin.
5. **Kaynak türü ataması** onay kutusunu seçin.
6. **Fatura kaynağı türü** alanını **Sözleşme faturası tümleştirmesi** olarak ayarlayın.
7. **Kaydet**'i seçin.

### <a name="in-the-data-integration-project"></a>Veri Tümleştirme projesinde

Görev: **Fatura satırları**  

Supply Chain Management **Ana Hesap Görünen Değeri** alanı için varsayılan değerin istenen değerle eşleşmek üzere güncelleştirilmesini sağlayın.

Varsayılan şablon değeri **401100**'dur.

## <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşleme

Aşağıdaki görseller, Veri tümleştirmede şablon eşlemeyi gösterir.

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-headers"></a>Sözleşme faturaları (Field Service'tan Supply Chain Management'a): Fatura başlıkları

[![Veri tümleştirmede şablon eşleme](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-lines"></a>Sözleşme faturaları (Field Service'tan Supply Chain Management'a): Fatura satırları

[![Veri tümleştirmede şablon eşleme](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)
