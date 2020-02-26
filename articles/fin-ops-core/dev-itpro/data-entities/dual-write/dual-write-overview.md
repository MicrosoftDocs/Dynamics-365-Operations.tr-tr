---
title: Common Data Service ile yakın gerçek zamanlı veri tümleştirmesi
description: Bu konu Finance and Operations ve Common Data Service arasındaki tümleştirme hakkında bilgi sağlar.
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
ms.openlocfilehash: 1c09b0c0bb695e7695acb7a8821ffb99ae1f6f06
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/04/2020
ms.locfileid: "3020062"
---
# <a name="near-real-time-data-integration-with-common-data-service"></a>Common Data Service ile yakın gerçek zamanlı veri tümleştirmesi

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

Günümüzün dijital dünyasında, işletme ekosistemleri Microsoft Dynamics 365 uygulamalarını bir bütün olarak kullanırlar. Kişilerin, müşterilerin, işlemlerin ve Nesnelerin İnterneti'nin (IoT) verileri tek bir kaynağa aktığından, dijital geri bildirim döngüleri için bir fırsat vardır. Bu deneyimi gerçekleştirmek için, Finance and Operations uygulamaları ve diğer Dynamics 365 uygulamaları arasındaki entegrasyon esastır. Bazı uygulamalar Common Data Service üzerine inşa edilir. Finance and Operations uygulamaları ile Common Data Service arasındaki veri tümleştirmesi, diğer uygulamaların Finance and Operations'la tutarlı ve akıcı şekilde iletişim kurmasını sağlar.

Finance and Operations uygulamaları ve Common Data Service, çift yazma çerçevesi ile Finance and Operations uygulamaları ve diğer Dynamics 365 uygulamaları arasında gerçek zamanlıya yakın veri eşitlemesi sağlar. Kapsam çok geniş olup, uygulamanın 28 yüzey alanına yayılır. Amaç, iş süreçlerini uygulamalar arasında bağlayan kesintisiz veri akışları üzerinden "Bir Dynamics 365" kullanıcı deneyimi sağlamaktır.

![Mimariye genel bakış diyagramı](media/dual-write-overview.jpg)

Aşağıdaki değer önermeleri kullanılabilir:

+ [Common Data Service'te kuruluş hiyerarşisi](organization-mapping.md)
+ [Common Data Service'te şirket kavramı](company-data.md)
+ [Tümleşik müşteri aslı](customer-mapping.md)
+ [Tümleşik genel muhasebe](ledger-mapping.md)
+ [Birleşik ürün deneyimi](product-mapping.md)
+ [Tümleşik satıcı aslı](vendor-mapping.md)
+ [Tümleşik siteler ve ambarlar](sites-warehouses-mapping.md)
+ [Tümleşik vergi aslı](tax-mapping.md)

## <a name="system-requirements"></a>Sistem gereksinimleri

Eşzamanlı, iki yönlü, yakın zamanda gerçek zamanlı veri akışları aşağıdaki sürümleri gerektirir:

+ Microsoft Dynamics 365 for Finance and Operations sürüm 10.0.4 (Temmuz 2019) Platform güncelleştirmesi 28 veya daha sonraki ile
+ Microsoft Dynamics 365 for Customer Engagement Platform sürüm 9.1 (4.2) veya üstü

## <a name="setup-instructions"></a>Ayar yönergeleri

Finance and Operations uygulamaları ve Common Data Service arasında tümleştirme ayarlamak için bu adımları izleyin.
    
1. İkili yazma sisteminin kurulumu için, Çift yazma önizlemesini duyurmada bkz. [adım adım kılavuz](https://aka.ms/dualwrite-docs).
2. [İkili yazma aracılığıyla Fin Ops ve CD/CE tümleştirmesi](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer grubu çözümü karşıdan yükleyin ve kurun. Paket beş çözüm içerir:

    + Dynamics365Company
    + CurrencyExchangeRates
    + Dynamics365FinanceAndOperationsCommon
    + Dynamics365FinanceCommon
    + Dynamics365SupplyChainCommon

3. Kuralları yürütme sırası için [ilk başvuru verilerini eşitleme](initial-sync.md)'yi izleyin.
4. Çift yazma eşitleme sorunlarıyla karşılaşırsanız veri tümleştirmesi için bkz. [Sorun giderme kılavuzu](dual-write-troubleshooting.md).

> [!IMPORTANT]
> Çift yazma ve [Aday müşteriden nakde](../../../../supply-chain/sales-marketing/prospect-to-cash.md)'yi yan yana çalıştıramazsınız. Aday müşteriden nakde çözümünü çalıştırıyorsanız bunu kaldırmanız gerekir. Ayrıca Aday müşteriden nakde çözümünün bir parçası olan müşteri ve satıcı çift yazma şablonlarını devre dışı bırakmanız gerekir.
