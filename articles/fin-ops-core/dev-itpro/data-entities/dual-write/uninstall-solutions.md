---
title: Çift yazma uygulama düzenleme çözümlerini kaldırma
description: Bu makale, çift yazma uygulaması düzenleme çözümlerinin nasıl kaldırılacağını açıklar.
author: RamaKrishnamoorthy
ms.date: 03/16/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2022-01-21
ms.openlocfilehash: 676802ddabac69db4947cf806e9103f67cece3de
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870388"
---
# <a name="uninstall-dual-write-application-orchestration-solutions"></a>Çift yazma uygulama düzenleme çözümlerini kaldırma

[!include [banner](../../includes/banner.md)]

Bu makale, çift yazma uygulaması düzenleme çözümlerinin nasıl kaldırılacağını açıklar.

Bazı müşteriler, çift yazmalı uygulama düzenleme paketini kendi Microsoft Dataverse ortamlarında birden çok çözüme farkında olmadan yükler. Paketteki fazlalık çözümlerin yüklenmesi, beklenmeyen ve istenmeyen sorunlara yol açabilir.

İkili yazma uygulaması düzenleme paketinin yüklenmesi ile ilgili sorunları gidermek için, istenmeyen ikili yazma çözümlerini aşağıdaki sırayla kaldırın:

1. Dynamics365FinanceAndOperationsAnchor_managed
1. msdyn_OneFSSCM_managed (varsa)
1. Dynamics365FinanceAndOperationsDualWriteEntityMaps_managed
1. Dynamics365Notes_managed (Bu çözümü kaldırmak için Microsoft'a destek bileti göndermeniz gerekir.)
1. DualWriteCore_managed
1. Dynamics365AssetManagementApp_managed
1. Dynamics365AssetManagement_managed
1. Dynamics365SupplyChainExtended_managed
1. Dynamics365FinanceExtended_managed
1. HCMCommon_managed
1. Dynamics365FinanceAndOperationsCommon_managed
1. Dynamics365Company_managed
1. CurrencyExchangeRates_managed
1. msdyn_AssetCommon_managed
1. FieldServiceCommon_managed

Parti ve genel adres defteri çözümleri yüklenmişse, çözümleri aşağıdaki sırada kaldırın:

1. Dynamics365FinanceAndOperationsAnchor
1. Dynamics365FinanceAndOperationsDualWriteEntityMaps
1. msdyn_DualWriteCore
1. Dynamics365AssetManagementApp
1. Dynamics365AssetManagement
1. Dynamics365SupplyChainExtended
1. Dynamics365FinanceExtended
1. HCMCommon
1. Dynamics365FinanceAndOperationsCommon
1. Taraf
1. Dynamics365Company_managed
1. CurrencyExchangeRates
1. msdyn_AssetCommon
1. FieldServiceCommon
