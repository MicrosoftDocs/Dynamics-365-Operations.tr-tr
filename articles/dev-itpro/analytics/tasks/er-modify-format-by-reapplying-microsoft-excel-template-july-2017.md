--- 
title: "Elektronik raporlama (ER) için bir Microsoft Excel şablonunu yeniden uygulayarak biçimi değiştirme"
description: "Bu yordamdaki bu adımı tamamlamak için öncelikle \"OPENXML biçiminde raporlar oluşturmak için bir ER yapılandırması tasarlama\" yordamındaki adımları tamamlamanız gerekir."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: b49cfe39732a450e4723419c50d8bcc3d64b7ec9
ms.openlocfilehash: 2f35727376812b0de428ce929ebe0d33bc497984
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="modify-a-format-by-reapplying-a-microsoft-excel-template-for-electronic-reporting-er"></a><span data-ttu-id="8f224-103">Elektronik raporlama (ER) için bir Microsoft Excel şablonunu yeniden uygulayarak biçimi değiştirme</span><span class="sxs-lookup"><span data-stu-id="8f224-103">Modify a format by reapplying a Microsoft Excel template for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8f224-104">Bu yordamdaki bu adımı tamamlamak için öncelikle "OPENXML biçiminde raporlar oluşturmak için bir ER yapılandırması tasarlama" yordamındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="8f224-104">To complete the steps in this procedure, you must first complete the procedure, ER - Design a configuration for generating reports in OPENXML format.</span></span>

<span data-ttu-id="8f224-105">Bu yordam, değiştirilmiş bir Microsoft Excel şablonu kullanarak bir Elektronik raporlama (ER) biçim yapılandırmasını nasıl değiştireceğinizi açıklar.</span><span class="sxs-lookup"><span data-stu-id="8f224-105">This procedure explains how to modify an Electronic reporting (ER) format configuration by reapplying a Microsoft Excel template that has been modified.</span></span> <span data-ttu-id="8f224-106">Bu yordamda, değiştirilmiş bir Excel şablonunu, aynı şirket Litware, Inc. için oluşturulmuş bir ER biçim yapılandırmasına içe aktaracak ve daha sonra elektronik belgeler oluşturacaksınız.</span><span class="sxs-lookup"><span data-stu-id="8f224-106">In this procedure, you will import a modified Excel template into ER format configurations that have been created for the sample company, Litware, Inc., and then generate electronic documents.</span></span> <span data-ttu-id="8f224-107">Bu yordam sistem yöneticisi veya elektronik raporlama geliştiricisi rolüne sahip kullanıcılar içindir.</span><span class="sxs-lookup"><span data-stu-id="8f224-107">This procedure is intended for users who have the system administrator or electronic reporting developer role.</span></span> <span data-ttu-id="8f224-108">Bu adımlar GBSI veri kümesi kullanılarak tamamlanabilir.</span><span class="sxs-lookup"><span data-stu-id="8f224-108">These steps can be completed by using the GBSI dataset.</span></span> <span data-ttu-id="8f224-109">Başlamadan önce, Elektronik raporlama biçimini bir Excel şablonunu yeniden uygulayarak değiştir Yardım konusu içerisinde listelenen SampleVendPaymWsReport2.xlsx dosyasını indirin ve kaydedin (modify-electronic-reporting-format-reapply-excel-template/).</span><span class="sxs-lookup"><span data-stu-id="8f224-109">Before you begin, download and save the file, SampleVendPaymWsReport2.xlsx, which is listed in the Help topic, Modify Electronic reporting format by reapplying an Excel template (modify-electronic-reporting-format-reapply-excel-template/).</span></span>

1. <span data-ttu-id="8f224-110">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="8f224-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="8f224-111">Örnek şirket ‘Litware, Inc.’ için yapılandırma sağlayıcısının kullanılabilir olduğunu ve etkin olarak işaretlemiş olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="8f224-111">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="8f224-112">Bu yapılandırma sağlayıcısını göremiyorsanız "Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="8f224-112">If you don’t see this configuration provider, complete the steps in the procedure, Create a configuration provider and mark it as active.</span></span>  

## <a name="select-the-er-format"></a><span data-ttu-id="8f224-113">ER biçimini seçin</span><span class="sxs-lookup"><span data-stu-id="8f224-113">Select the ER format</span></span>
1. <span data-ttu-id="8f224-114">Raporlama konfigürasyonları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8f224-114">Click Reporting configurations.</span></span>
2. <span data-ttu-id="8f224-115">Ağaçta, 'Ödeme modeli' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="8f224-115">In the tree, expand 'Payment model'.</span></span>
3. <span data-ttu-id="8f224-116">Ağaçta, 'Ödeme modeli\Örnek çalışma sayfası raporu' seçin.</span><span class="sxs-lookup"><span data-stu-id="8f224-116">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
4. <span data-ttu-id="8f224-117">Ekler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8f224-117">Click Attachments.</span></span>
    * <span data-ttu-id="8f224-118">SampleVendPaymWsReport.xlsx Excel dosyasının şu an ödeme günlüğü işlem için bir şablon olarak kullanıldığını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="8f224-118">Note that the SampleVendPaymWsReport.xlsx Excel file is currently used as a template for payment journal processing.</span></span>   
5. <span data-ttu-id="8f224-119">Aç'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8f224-119">Click Open.</span></span>
    * <span data-ttu-id="8f224-120">Excel şablonunun düzenini keşfetmek için Aç'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8f224-120">Click Open to explore the layout of the Excel template.</span></span>  
    * <span data-ttu-id="8f224-121">Şablonu gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="8f224-121">Review the template.</span></span> <span data-ttu-id="8f224-122">Mevcut olarak her bir ödeme satırı için aşağıdaki ayrıntıları içerdiğini unutmayın: satıcı hesap numarası, satıcı adı, banka rota numarası, hesap numarası, borç, alacak ve para birimi.</span><span class="sxs-lookup"><span data-stu-id="8f224-122">Note that it currently includes the following details for each payment line: vendor account number, vendor name, bank, routing number, account number, debit, credit, and currency.</span></span> <span data-ttu-id="8f224-123">Bu örnek için bu listeyi ödeme tarihi hakkında ayrıntılar girerek genişletmek istiyoruz.</span><span class="sxs-lookup"><span data-stu-id="8f224-123">For this example, we want to extend this list by adding details about the payment date.</span></span>   
6. <span data-ttu-id="8f224-124">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="8f224-124">Close the page.</span></span>

## <a name="reapply-a-new-excel-template-to-er-format"></a><span data-ttu-id="8f224-125">ER biçimine yeni bir Excel şablonunu yeniden uygulayın</span><span class="sxs-lookup"><span data-stu-id="8f224-125">Reapply a new Excel template to ER format</span></span>
1. <span data-ttu-id="8f224-126">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8f224-126">Click Designer.</span></span>
    * <span data-ttu-id="8f224-127">Düzenlemek için seçilen ER biçiminin taslak sürümünü açın.</span><span class="sxs-lookup"><span data-stu-id="8f224-127">Open the draft version of the selected ER format for editing.</span></span>  
2. <span data-ttu-id="8f224-128">Eylem Bölmesinde, İçeri Al'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8f224-128">On the Action Pane, click Import.</span></span>
3. <span data-ttu-id="8f224-129">Excel'den güncelleştir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8f224-129">Click Update from Excel.</span></span>
    * <span data-ttu-id="8f224-130">'Şablonu güncelleştir' üzerine tıklayın ve daha sonra SampleVendPaymWsReport2.xlsx dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="8f224-130">Click ‘Update template’, and then select the file, SampleVendPaymWsReport2.xlsx.</span></span>  
    * <span data-ttu-id="8f224-131">Daha önce indirilen SampleVendPaymWsReport2.xlsx dosyasına erişmek için Şablonu güncelleştir ve göz at üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8f224-131">Click Update template and browse to get the downloaded earlier SampleVendPaymWsReport2.xlsx file.</span></span>  
4. <span data-ttu-id="8f224-132">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8f224-132">Click OK.</span></span>
    * <span data-ttu-id="8f224-133">The SampleVendPaymWsReport2.xlsx şablonu uygulanır.</span><span class="sxs-lookup"><span data-stu-id="8f224-133">The SampleVendPaymWsReport2.xlsx template is applied.</span></span> <span data-ttu-id="8f224-134">ER biçiminin yapısı, öğeleri ER biçimine aktarılan şablonun içeriğiyle eşleştirilir.</span><span class="sxs-lookup"><span data-stu-id="8f224-134">The structure of the ER format is synchronized with the content of the template, whose elements are added to the ER format.</span></span> <span data-ttu-id="8f224-135">ER biçimindeki şablona eklenmeyen tüm mevcut öğeler biçim tanımından çıkartılır.</span><span class="sxs-lookup"><span data-stu-id="8f224-135">Any existing elements in the ER format that aren’t included in the template are removed from the format definition.</span></span>  
5. <span data-ttu-id="8f224-136">Ağaçta, 'Excel' metnini seçin.</span><span class="sxs-lookup"><span data-stu-id="8f224-136">In the tree, select 'Excel'.</span></span>
    * <span data-ttu-id="8f224-137">Şablon alanının şimdi yeni şablona bir referans içerdiğini dikkate alın.</span><span class="sxs-lookup"><span data-stu-id="8f224-137">Note that the Template field now contains a reference to the new template.</span></span>   
6. <span data-ttu-id="8f224-138">Ekler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8f224-138">Click Attachments.</span></span>
7. <span data-ttu-id="8f224-139">Aç'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8f224-139">Click Open.</span></span>
    * <span data-ttu-id="8f224-140">Değiştirilen Excel şablonunun düzenini keşfetmek için Aç'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8f224-140">Click Open to explore the layout of the modified Excel template.</span></span>  
    * <span data-ttu-id="8f224-141">Şablonu gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="8f224-141">Review the template.</span></span> <span data-ttu-id="8f224-142">Şimdi ödeme tarihi için bir satır içerdiğini dikkate alın.</span><span class="sxs-lookup"><span data-stu-id="8f224-142">Note that it now contains a line for the payment date.</span></span>   
8. <span data-ttu-id="8f224-143">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="8f224-143">Close the page.</span></span>
9. <span data-ttu-id="8f224-144">Ağaçta, 'Excel' metnini genişletin.</span><span class="sxs-lookup"><span data-stu-id="8f224-144">In the tree, expand 'Excel'.</span></span>
10. <span data-ttu-id="8f224-145">Ağaçta, "Excel\PaymLines" öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="8f224-145">In the tree, expand 'Excel\PaymLines'.</span></span>
11. <span data-ttu-id="8f224-146">Ağaçta 'Excel\PaymLines\PaymDate' seçin.</span><span class="sxs-lookup"><span data-stu-id="8f224-146">In the tree, select 'Excel\PaymLines\PaymDate'.</span></span>
    * <span data-ttu-id="8f224-147">ER biçiminin şimdi bir öğe daha içerdiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="8f224-147">Note that the ER format now contains one more item.</span></span> <span data-ttu-id="8f224-148">Bir hücre, PaymDate şimdi Excel şablonuna eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="8f224-148">A cell, PaymDate, has been added to the Excel template.</span></span>  
12. <span data-ttu-id="8f224-149">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8f224-149">Click the Mapping tab.</span></span>
13. <span data-ttu-id="8f224-150">Ağaçta, 'model'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="8f224-150">In the tree, expand 'model'.</span></span>
14. <span data-ttu-id="8f224-151">Ağaçta genişletin 'model\Payments'.</span><span class="sxs-lookup"><span data-stu-id="8f224-151">In the tree, expand 'model\Payments'.</span></span>
15. <span data-ttu-id="8f224-152">Ağaçta seçin 'model\Payments\Transaction date(TransactionDate)'.</span><span class="sxs-lookup"><span data-stu-id="8f224-152">In the tree, select 'model\Payments\Transaction date(TransactionDate)'.</span></span>
16. <span data-ttu-id="8f224-153">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8f224-153">Click Bind.</span></span>
    * <span data-ttu-id="8f224-154">Hangi verinin çalışma zamanında yeni hücreye ekleneceğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="8f224-154">Specify what data is added to the new cell at runtime.</span></span>  
17. <span data-ttu-id="8f224-155">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8f224-155">Click Save.</span></span>
18. <span data-ttu-id="8f224-156">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="8f224-156">Close the page.</span></span>

## <a name="enable-the-modified-draft-version-of-the-er-format-for-use-in-payment-journal-processing"></a><span data-ttu-id="8f224-157">ER biçiminin değiştirilmiş taslak sürümünü, ödeme günlüğü işlemede kullanmak için etkinleştirin</span><span class="sxs-lookup"><span data-stu-id="8f224-157">Enable the modified draft version of the ER format for use in payment journal processing</span></span>
1. <span data-ttu-id="8f224-158">Eylem Bölmesi'nde, Yapılandırmalar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8f224-158">On the Action Pane, click Configurations.</span></span>
2. <span data-ttu-id="8f224-159">Kullanıcı parametreleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8f224-159">Click User parameters.</span></span>
3. <span data-ttu-id="8f224-160">Çalıştırma ayarları alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8f224-160">Select Yes in the Run settings field.</span></span>
4. <span data-ttu-id="8f224-161">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8f224-161">Click OK.</span></span>
5. <span data-ttu-id="8f224-162">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8f224-162">Click Edit.</span></span>
6. <span data-ttu-id="8f224-163">Taslak Çalıştır alanında Evet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8f224-163">Select Yes in the Run Draft field.</span></span>

## <a name="use-the-modified-draft-version-of-the-er-format-for-payment-journal-processing"></a><span data-ttu-id="8f224-164">ER biçiminin değiştirilmiş taslak sürümünü, ödeme günlüğü işlemede kullanın</span><span class="sxs-lookup"><span data-stu-id="8f224-164">Use the modified draft version of the ER format for payment journal processing</span></span>
    * <span data-ttu-id="8f224-165">Yeni ödeme satırlarının - ödeme tarihinin ayrıntıları da dahil oluşturulan çalışma sayfasını gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="8f224-165">Review the created worksheet, including new detail of payment lines – payment date.</span></span>  

