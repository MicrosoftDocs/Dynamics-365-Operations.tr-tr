---
title: Finance and Operations ve Common Data Service arasındaki yakın gerçek zamanlı veri tümleştirmesi
description: Bu konu Microsoft Dynamics 365 for Finance and Operations ve Common Data Service arasındaki tümleştirme hakkında bilgi sağlar.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: aa614c8e6a79a3f7a4f8f2f99f1f1bd1a67ac921
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797240"
---
# <a name="near-real-time-data-integration-between-finance-and-operations-and-common-data-service"></a>Finance and Operations ve Common Data Service arasındaki yakın gerçek zamanlı veri tümleştirmesi

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Geçerli dijital dünyada, işletme ekosistemleri Microsoft Dynamics 365 grubunu bir bütün olarak kullanırlar. Kişilerin, müşterilerin, işlemlerin ve Nesnelerin İnterneti'nin (IoT) verileri tek bir kaynağa aktığından, dijital geri bildirim döngüleri için bir fırsat vardır. Bu deneyimi gerçekleştirmek için,  Dynamics 365 for Finance and Operations ve Dynamics 365 for Customer Engagement uygulamaları arasındaki entegrasyon esastır. Customer Engagement uygulamaları Common Data Service üzerine inşa edilir. Finance and Operations verileriyle Common Data Service arasındaki entegrasyon Customer Engagement uygulamalarının Finance and Operations ile tutarlı ve akıcı bir şekilde iletişim kurmasını sağlar.

Finance and Operations ve Common Data Service çift yazma çerçevesi ile Finance and Operations ve Customer Engagement uygulamaları arasında gerçek zamanlıya yakın veri eşitlemesi sağlarlar. Kapsam çok geniş olup, Finance and Operations'ın 28 yüzey alanına yayılır. Amaç, iş süreçlerini uygulamalar arasında bağlayan kesintisiz veri akışları üzerinden "Bir Dynamics 365" kullanıcı deneyimi sağlamaktır.

![Mimariye genel bakış diyagramı](media/dual-write-overview.jpg)

Müşteriler için aşağıdaki değer önermeleri kullanılabilir:

+ [Common Data Service'te kuruluş hiyerarşisi](dual-write-organization.md)
+ [Common Data Service'te şirket kavramı](dual-write-company.md)
+ [Tümleşik müşteri aslı](dual-write-customer.md)
+ [Tümleşik satıcı aslı](dual-write-vendor.md)
+ Birleştirilmiş ana ürün

## <a name="system-requirements"></a>Sistem gereksinimleri

Eşzamanlı, iki yönlü, yakın zamanda gerçek zamanlı veri akışları aşağıdaki sürümleri gerektirir:

+ Microsoft Dynamics 365 for Finance and Operations sürüm 10.0.4 (Temmuz 2019) Platform güncelleştirmesi 28 veya daha sonraki ile
+ Microsoft Dynamics 365 for Customer Engagement Platform sürüm 9.1 (4.2) veya üstü

## <a name="setup-instructions"></a>Ayar yönergeleri

Finance and Operations ve Common Data Service arasındaki tümleştirmeyi ayarlamak için şu adımları izleyin.
    
1. İkili yazma sisteminin kurulumu için, Çift yazma önizlemesini duyurmada bkz. [adım adım kılavuz](https://aka.ms/dualwrite-docs).
2. Çözümü [Finance and Operations, Common Data Service, ve Customer Engagement Entegrasyonu](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer grup'tan indirin. Paket beş çözüm içerir:

    + Dynamics365Company
    + CurrencyExchangeRates
    + Dynamics365FinanceAndOperationsCommon
    + Dynamics365FinanceCommon
    + Dynamics365SupplyChainCommon

3. Kuralları yürütme sırası için [ilk başvuru verilerini eşitleme](dual-write-initial.md)'yi izleyin.
4. Çift yazma eşitleme sorunlarıyla karşılaşırsanız veri tümleştirmesi için bkz. [Sorun giderme kılavuzu](dual-write-troubleshooting.md).

> [!IMPORTANT]
> Çift yazma ve [Aday müşteriden nakde](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct)'yi yan yana çalıştıramazsınız. Aday müşteriden nakde çözümünü çalıştırıyorsanız bunu kaldırmanız gerekir. Ayrıca Aday müşteriden nakde çözümünün bir parçası olan müşteri ve satıcı çift yazma şablonlarını devre dışı bırakmanız gerekir.
