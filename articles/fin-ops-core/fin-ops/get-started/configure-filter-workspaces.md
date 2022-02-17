---
title: Çalışma alanlarını yapılandırma ve filtreleme
description: Bu makalede, çalışma alanlarının nasıl yapılandırılacağı ve filtreleneceğine ilişkin bir genel bakış verilmektedir.
author: jasongre
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankTreasurerWorkspace, HcmBenefitWorkspace, BudgetPlanningWorkspace, BusinessProcessGenericWorkspace, RetailCatalogManagementWorkspace, RetailCategoryAndProductWorkspace, RetailChannelManagementWorkspace, HcmCompensationWorkspace, CAMCostAccountingLedgerAdminWorkspace, CostAdminWorkspace, CostAnalysisWorkspace, CAMCostControlWorkspace, CustomerCollectionManagerWorkspace, CustomerInvoiceWorkspace, CustPaymentWorkspace, DataManagementWorkspace, DataValidationWorkspace, ERWorkspace, LedgerPeriodCloseProjectWorkspace, AssetWorkspace, GeneralJournalEntryWorkspace, VendVendorPortalInvoiceWorkspace, BudgetTrackingWorkspace, ReqCreatePlanWorkspace, BusinessProcessGenericOwnerWorkspace, SelfHealingWorkspace, WHSOutboundWorkMonitoringWorkspace, WHSWavePlanningWorkspace, PayrollWorkspace, HcmWorkforceWorkspace, RetailDiscountPricingWorkspace, EcoResProductDiscreteManufacturingWorkspace, KanbanPrepareProductForLeanWorkspace, EcoResProductProcessManufacturingWorkspace, EcoResProductVariantMaintainWorkspace, JmgShopSupervisorWorkspace, ProjProjectManagementWorkspace, VendVendorPortalWorkspace, PurchOrderMaintainWorkspace, PurchOrderProcessReceiptsWorkspace, HcmRecruitmentWorkspace, EcoResProductMaintainWorkspace, FMClerkWorkspace, OpResLifecycleManagementWorkspace, RetailITWorkspace, RetailChannelOperationsWorkspace, RetailStoreManagementWorkspace, SalesOrderProcessingWorkspace, SalesReturnWorkspace, SystemAdministrationWorkspaceForm, VendVendorRequestForQuotationsWorkspace, VendVendorProfileManagementWorkspace, VendInvoiceWorkspace, VendPaymentWorkspace
audience: Application User
ms.reviewer: sericks
ms.custom: 17491
ms.assetid: 541e6012-4680-4684-8494-e9b5ca4684ee
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e96b61457f222836d50a75ed15305c3c1267600c
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068746"
---
# <a name="configure-and-filter-workspaces"></a>Çalışma alanlarını yapılandırma ve filtreleme

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Bu makalede, çalışma alanlarının nasıl yapılandırılacağı ve filtreleneceğine ilişkin bir genel bakış verilmektedir.

## <a name="configuring-a-workspace"></a>Bir çalışma alanını yapılandırma

Tüm çalışma alanı için uygulanan ayarları güncelleştirerek, bazı çalışma alanlarının görünümünü ve davranışını değiştirebilirsiniz. Çalışma alanı yapılandırılabiliyorsa, Eylem Bölmesinde, yapılandırma değişikliklerini yapmak üzere tıklamanız gerektiği belirtilen bir düğme görünür. Örneğin aşağıdaki çizimde düğme adı **Çalışma alanımı yapılandır**'dır.

[![çalışma-alanları-yapılandır-ve-filtrele.](./media/configure-and-filter-workspaces.png)](./media/configure-and-filter-workspaces.png)

Düğmeye tıkladığınızda çalışma alanı için önceden tanımlanmış olan ayarlarda değişiklik yapabileceğiniz bir iletişim görünür. Bu iletişim kutusunda gördüğünüz belirli ayarlar çalışma alanına göre değişir ve çalışma alanında kullanılabilir olan belirli denetimlere ve iş verilerine bağlıdır.

[![çalışma-alanımı-yapılandır.](./media/configure-my-workspace.png)](./media/configure-my-workspace.png)

## <a name="filtering-a-workspace"></a>Bir çalışma alanını filtreleme

Birçok çalışma alanı, içinde görüntülenen içeriği filtrelemenize izin verir. Kullanılabilen denetimler, çalışma alanındaki tüm içeriği veya belirli bir bölümdeki içeriği filtrelemenize izin verebilir. Çalışma alanlarındaki filtreler aramalar, açılan kutular, serbest biçimli metin alanları veya diğer türde denetimler olabilir. Ancak, her filtre türü, aşağıdaki bölümlerde açıklandığı gibi, aynı etkilere sahiptir.

### <a name="workspace-wide-filters"></a>Çalışma alanı genelindeki filtreler

Çalışma alanı genelinde filtre kullanarak tüm çalışma alanını filtreleyebilirsiniz. Çalışma alanının sol üst köşesinde, çalışma alanı genelinde bir filtre görünür. Açılır listeden belirli bir değer seçtiğiniz zaman, çalışma alanının içeriği o seçime bağlı olarak filtrelenir.

[![çalışma-alanı-filtresi.](./media/workspace-filter.png)](./media/workspace-filter.png)

Filtreyi açmak için tıkladığınızda karşınıza çeşitli seçenekler çıkar.

[![genişletilmiş-çalışma-alanı-filtresi.](./media/workspace-filter-expanded.png)](./media/workspace-filter-expanded.png)

O seçeneğe bağlı olarak çalışma alanını filtrelemek için bir seçenek belirleyin.

### <a name="workspace-section-filters"></a>Çalışma alanı bölümü filtreleri

Çalışma alanının ayrı ayrı bölümlerinde filtreler varsa, her bölüme ayrı ayrı filtre uygulayabilirsiniz. Aşağıdaki çizimde, filtre (içinde "Filtre" yazan alan) serbest biçimli bir metin alanı filtresi örneğidir.

[![çalışma-alanı-bölüm-filtreleri.](./media/workspace-section-filters.png)](./media/workspace-section-filters.png)

Çalışma alanı genelinde filtrede olduğu gibi, bölümün içeriğini filtrelemek için, alanda bir değer seçin veya girin.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]