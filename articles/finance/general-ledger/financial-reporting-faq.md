---
title: Mali raporlama ile ilgili SSS
description: Bu konuda, diğer kullanıcıların mali raporlama ile ilgili soruları listelenmektedir.
author: jiwo
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a0718db77399901acc8c88278c5b373b77b3cb16
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811322"
---
# <a name="financial-reporting-faq"></a><span data-ttu-id="492c9-103">Mali raporlama ile ilgili SSS</span><span class="sxs-lookup"><span data-stu-id="492c9-103">Financial reporting FAQ</span></span> 

<span data-ttu-id="492c9-104">Bu konuda, diğer kullanıcıların mali raporlama ile ilgili soruları listelenmektedir.</span><span class="sxs-lookup"><span data-stu-id="492c9-104">This topic lists questions related to financial reporting that other users have had.</span></span> 


## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a><span data-ttu-id="492c9-105">Ağaç güvenliğini kullanarak bir rapora erişimi nasıl kısıtlayabilirim?</span><span class="sxs-lookup"><span data-stu-id="492c9-105">How do I restrict access to a report using Tree security?</span></span>

<span data-ttu-id="492c9-106">Senaryo: USMF demo şirketinin tüm mali raporlama kullanıcılarının D365'te görüntülemesini istemediği bir bilanço raporu bulunuyor.</span><span class="sxs-lookup"><span data-stu-id="492c9-106">Scenario: The USMF demo company has a Balance sheet report that it doesn’t want all Financial reporting users to be able to view in D365.</span></span> <span data-ttu-id="492c9-107">Çözüm: Rapora yalnızca belirli kullanıcıların erişmesini sağlamak üzere tek bir rapora erişimi kısıtlamak için Ağaç güvenliğini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="492c9-107">Solution: You can utilize Tree security to restrict access to a single report so that only certain users can access the report.</span></span> 

1.  <span data-ttu-id="492c9-108">Mali Raporlayıcı Rapor Tasarımcısında oturum açma</span><span class="sxs-lookup"><span data-stu-id="492c9-108">Log into Financial Reporter Report Designer</span></span>

2.  <span data-ttu-id="492c9-109">Yeni Ağaç Tanımı oluşturma (Dosya | Yeni | Ağaç Tanımı) a.</span><span class="sxs-lookup"><span data-stu-id="492c9-109">Create a new Tree Definition (File | New | Tree Definition) a.</span></span>    <span data-ttu-id="492c9-110">**Birim Güvenliği** sütununda **Özet** satırına çift tıklayın.</span><span class="sxs-lookup"><span data-stu-id="492c9-110">Double-click the **Summary** line in the **Unit Security** column.</span></span>
  <span data-ttu-id="492c9-111">i.</span><span class="sxs-lookup"><span data-stu-id="492c9-111">i.</span></span>    <span data-ttu-id="492c9-112">Kullanıcılar ve Gruplar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="492c9-112">Click Users and Groups.</span></span>  
          <span data-ttu-id="492c9-113">1. Bu rapora erişmesini istediğiniz Kullanıcılar veya Grupları seçin.</span><span class="sxs-lookup"><span data-stu-id="492c9-113">1.    Select the User(s) or Group that would like to access this report.</span></span> 
          
<span data-ttu-id="492c9-114">[![kullanıcı ekranı](./media/FR-FAQ_users.png)](./media/FR-FAQ_users.png)</span><span class="sxs-lookup"><span data-stu-id="492c9-114">[![user screen](./media/FR-FAQ_users.png)](./media/FR-FAQ_users.png)</span></span>

<span data-ttu-id="492c9-115">[![güvenlik ekranı](./media/FR-FAQ_security.jpg)](./media/FR-FAQ_security.jpg)</span><span class="sxs-lookup"><span data-stu-id="492c9-115">[![security screen](./media/FR-FAQ_security.jpg)](./media/FR-FAQ_security.jpg)</span></span>

  <span data-ttu-id="492c9-116">b.</span><span class="sxs-lookup"><span data-stu-id="492c9-116">b.</span></span>    <span data-ttu-id="492c9-117">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="492c9-117">Click **Save**.</span></span>
  
<span data-ttu-id="492c9-118">[![kaydet düğmesi](./media/FR-FAQ_save.png)](./media/FR-FAQ_save.png)</span><span class="sxs-lookup"><span data-stu-id="492c9-118">[![save button](./media/FR-FAQ_save.png)](./media/FR-FAQ_save.png)</span></span>

3.  <span data-ttu-id="492c9-119">Rapor Tanımınızda, yeni Ağaç Tanımınızı ekleyin</span><span class="sxs-lookup"><span data-stu-id="492c9-119">In your Report Definition add your new Tree Definition</span></span>

<span data-ttu-id="492c9-120">[![ağaç tanımı formu](./media/FR-FAQ_tree-definition.jpg)](./media/FR-FAQ_tree-definition.jpg)</span><span class="sxs-lookup"><span data-stu-id="492c9-120">[![tree definition form](./media/FR-FAQ_tree-definition.jpg)](./media/FR-FAQ_tree-definition.jpg)</span></span>

<span data-ttu-id="492c9-121">A.</span><span class="sxs-lookup"><span data-stu-id="492c9-121">A.</span></span>  <span data-ttu-id="492c9-122">Ağaç Tanımındayken, Ayar'a tıklayın ve "Raporlama birimi seçimi" altından, "Tüm birimleri dahil et"i işaretleyin</span><span class="sxs-lookup"><span data-stu-id="492c9-122">While in the Tree Definition click on Setting and under “Reporting unit selection” check “Include all units”</span></span>

<span data-ttu-id="492c9-123">[![raporlama birimi seçim formu](./media/FR-FAQ_reporting-unit-selection.jpg)](./media/FR-FAQ_reporting-unit-selection.jpg)</span><span class="sxs-lookup"><span data-stu-id="492c9-123">[![reporting unit selection form](./media/FR-FAQ_reporting-unit-selection.jpg)](./media/FR-FAQ_reporting-unit-selection.jpg)</span></span>

<span data-ttu-id="492c9-124">**Öncesi:** [![öncesi ekran görüntüsü](./media/FR-FAQ_before.png)](./media/FR-FAQ_before.png)</span><span class="sxs-lookup"><span data-stu-id="492c9-124">**Before:** [![before screenshot](./media/FR-FAQ_before.png)](./media/FR-FAQ_before.png)</span></span>

<span data-ttu-id="492c9-125">**Sonrası:** [![sonrası ekran görüntüsü](./media/FR-FAQ_after.png)](./media/FR-FAQ_after.png)</span><span class="sxs-lookup"><span data-stu-id="492c9-125">**After:** [![after screenshot](./media/FR-FAQ_after.png)](./media/FR-FAQ_after.png)</span></span>

<span data-ttu-id="492c9-126">Not: Yukarıdaki iletinin nedeni, Birim Güvenliği uygulandıktan sonra kullanıcımın o rapora erişim izninin olmamasıdır</span><span class="sxs-lookup"><span data-stu-id="492c9-126">Note: Reason for the above message is my user does not have access to that report after applying Unit Security</span></span>



## <a name="how-do-i-determine-which-accounts-do-not-matching-my-balances-in-d365"></a><span data-ttu-id="492c9-127">D365'te hangi hesaplarda bakiyelerin eşleşmediğini nasıl belirleyebilirim?</span><span class="sxs-lookup"><span data-stu-id="492c9-127">How do I determine which account(s) do not matching my balances in D365?</span></span>

<span data-ttu-id="492c9-128">D365'te beklediğiniz şekilde eşleşmeyen bir raporunuz varsa bu hesapları ve farkları tanımlamak için gerçekleştirebileceğiniz adımlar burada verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="492c9-128">When you have a report that doesn't match what you would expect in D365, here are some steps you could take to identify those accounts and the variances.</span></span> 

### <a name="in-financial-reporter-report-designer"></a><span data-ttu-id="492c9-129">Mali Raporlayıcı Rapor Tasarımcısında</span><span class="sxs-lookup"><span data-stu-id="492c9-129">In Financial Reporter Report Designer</span></span>

1.  <span data-ttu-id="492c9-130">Yeni Satır Tanımı oluşturun a.</span><span class="sxs-lookup"><span data-stu-id="492c9-130">Create a new Row Definition a.</span></span>    <span data-ttu-id="492c9-131">Düzenle | Boyutlardan Satır Ekle'yi tıklayın i.</span><span class="sxs-lookup"><span data-stu-id="492c9-131">Click Edit | Insert Rows from Dimensions i.</span></span>  <span data-ttu-id="492c9-132">MainAccount'u seçme [![Ana ekranı seçme_](./media/FR-FAQ_selectmain_.png)](./media/FR-FAQ_selectmain_.png)</span><span class="sxs-lookup"><span data-stu-id="492c9-132">Select MainAccount [![Select Main screen_](./media/FR-FAQ_selectmain_.png)](./media/FR-FAQ_selectmain_.png)</span></span>
    
    <span data-ttu-id="492c9-133">ii.</span><span class="sxs-lookup"><span data-stu-id="492c9-133">ii.</span></span> <span data-ttu-id="492c9-134">Tamam'a tıklayın b.</span><span class="sxs-lookup"><span data-stu-id="492c9-134">Click Ok b.</span></span>    <span data-ttu-id="492c9-135">Satır Tanımını kaydedin</span><span class="sxs-lookup"><span data-stu-id="492c9-135">Save the Row Definition</span></span>

2.  <span data-ttu-id="492c9-136">Yeni Sütun Tanımı oluşturma     [![Yeni Sütun Tanımı oluşturma](./media/FR-FAQ_column.png)](./media/FR-FAQ_column.png)</span><span class="sxs-lookup"><span data-stu-id="492c9-136">Create a new Column Definition     [![Create a new column definition](./media/FR-FAQ_column.png)](./media/FR-FAQ_column.png)</span></span>

3.  <span data-ttu-id="492c9-137">Yeni Rapor Tanımı oluşturun a.</span><span class="sxs-lookup"><span data-stu-id="492c9-137">Create a new Report Definition a.</span></span>    <span data-ttu-id="492c9-138">Ayarlar'a tıklayın ve işaretleri kaldırın [![Ayarlar formu](./media/FR-FAQ_settings.png)](./media/FR-FAQ_settings.png)</span><span class="sxs-lookup"><span data-stu-id="492c9-138">Click Settings and uncheck [![Settings form](./media/FR-FAQ_settings.png)](./media/FR-FAQ_settings.png)</span></span>
   
4.  <span data-ttu-id="492c9-139&quot;>Raporu oluşturun.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;492c9-139&quot;>Generate the Report.</span></span> 

5.  <span data-ttu-id=&quot;492c9-140&quot;>Raporu Excel'e dışarı aktarın.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;492c9-140&quot;>Export the Report to Excel.</span></span>

### <a name=&quot;in-d365&quot;></a><span data-ttu-id=&quot;492c9-141&quot;>D365'te:</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;492c9-141&quot;>In D365:</span></span> 
1.  <span data-ttu-id=&quot;492c9-142&quot;>Genel Muhasebe | Sorgular ve Raporlar | Mizan'a tıklayın a.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;492c9-142&quot;>Click General Ledger | Inquiries and Reports | Trial Balance a.</span></span>    <span data-ttu-id=&quot;492c9-143&quot;>Parametreler i.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;492c9-143&quot;>Parameters i.</span></span>  <span data-ttu-id=&quot;492c9-144&quot;>Başlangıç Tarihi: Mali Yılın başlangıcı ii.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;492c9-144&quot;>From Date: Start of Fiscal Year ii.</span></span> <span data-ttu-id=&quot;492c9-145&quot;>Bitiş Tarihi: Raporu oluşturduğunuz tarih (şunun için: iii.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;492c9-145&quot;>To Date: Date you generated the report for iii.</span></span>    <span data-ttu-id=&quot;492c9-146&quot;>Finansal Boyut Ayarı &quot;Ana Hesap Ayarı") [![Ana Hesap Formu](./media/FR-FAQ_mainacct.png)](./media/FR-FAQ_mainacct.png)</span><span class="sxs-lookup"><span data-stu-id="492c9-146">Financial Dimension Set “Main Account set” [![Main Account Form](./media/FR-FAQ_mainacct.png)](./media/FR-FAQ_mainacct.png)</span></span>
      
  <span data-ttu-id="492c9-147">b.</span><span class="sxs-lookup"><span data-stu-id="492c9-147">b.</span></span>    <span data-ttu-id="492c9-148">Hesapla'ya tıklayın</span><span class="sxs-lookup"><span data-stu-id="492c9-148">Click Calculate</span></span>

2.  <span data-ttu-id="492c9-149">Raporu Excel'e dışarı aktarın</span><span class="sxs-lookup"><span data-stu-id="492c9-149">Export the report to Excel</span></span>

<span data-ttu-id="492c9-150">Artık FR Excel raporundan ve D365 Mizan raporuna veri kopyalayabilir ve "Kapanış Bakiyesi" sütunlarını karşılaştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="492c9-150">You should now be able to copy the data from the FR Excel Report and to the D365 Trial Balance report and compare the “Closing Balance” columns.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]