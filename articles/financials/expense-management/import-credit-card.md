---
title: "Kredi kartı hareketlerini içe aktarma ve yönetme"
description: "Bu konu, giderle ilişkili kredi kartı hareketlerinin nasıl içe aktarılacağını ve korunacağını açıklar. Bu hareketler, otomatik olarak yinelenen bir zamanlamada içe aktarılacak şekilde ayarlanabilir veya ihtiyaç duyuldukça el ile içe aktarılabilir."
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: knelson
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 9674cf495b7fdd40d8672580b9d10e9ebe626bb0
ms.contentlocale: tr-tr
ms.lasthandoff: 08/07/2018

---

# <a name="import-and-maintain-credit-card-transactions"></a><span data-ttu-id="2cd26-104">Kredi kartı hareketlerini içe aktarma ve yönetme</span><span class="sxs-lookup"><span data-stu-id="2cd26-104">Import and maintain credit card transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2cd26-105">Giderle ilişkili kredi kartı hareketleri, yinelenen bir zamanlamada otomatik içe aktarılacak şekilde ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="2cd26-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="2cd26-106">Alternatif olarak, hareketler ihtiyaç duyuldukça el ile içe aktarılabilir.</span><span class="sxs-lookup"><span data-stu-id="2cd26-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="2cd26-107">Kredi kartı hareketleri Kredi kartı hareketleri veri varlığı üzerinden içe aktarılır.</span><span class="sxs-lookup"><span data-stu-id="2cd26-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

<span data-ttu-id="2cd26-108">Veri varlıkları hakkında daha fazla bilgi için bkz. [Veri varlıkları](../../dev-itpro/data-entities/data-entities.md).</span><span class="sxs-lookup"><span data-stu-id="2cd26-108">For more information about data entities, see [Data entities](../../dev-itpro/data-entities/data-entities.md).</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="2cd26-109">Kredi kartı hareketlerini içe aktar</span><span class="sxs-lookup"><span data-stu-id="2cd26-109">Import credit card transactions</span></span>

1. <span data-ttu-id="2cd26-110">**Kredi kartı hareketleri** sayfasında, **Hareketleri içe aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2cd26-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="2cd26-111">Veri yönetimini ilk kez açıyorsanız, devam etmeden önce sistemin veri varlıkları listesini güncelleştirmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="2cd26-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="2cd26-112">**Ad** alanında, içe aktarma işinin benzersiz bir açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="2cd26-112">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="2cd26-113">**Kaynak veri biçimi** alanında, içe aktarılacak kredi kartı hareketlerini içeren dosyanın biçimini seçin.</span><span class="sxs-lookup"><span data-stu-id="2cd26-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="2cd26-114">**Karşıya yükle**'yi seçin ve içe aktarılacak dosyayı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="2cd26-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="2cd26-115">Dosya karşıya yüklendikten sonra, kutucuktaki **Görünüm eşleme** bağlantısına tıklayarak Kredi kartı hareketleri veri varlığı ve kredi kartı hareket dosyasının eşleşmesini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="2cd26-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="2cd26-116">Eşleme hataları varsa veya eşlemeyi değiştirmeniz gerekiyorsa, eşleme değişikliklerini **Eşleme görselleştirme** sekmesi veya **Eşleme ayrıntıları** sekmesi üzerinden yapın.</span><span class="sxs-lookup"><span data-stu-id="2cd26-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="2cd26-117">Kredi kartı hareketlerini otomatikleştirmek için **Yinelenen bir veri işi oluştur** seçin.</span><span class="sxs-lookup"><span data-stu-id="2cd26-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="2cd26-118">Daha sonra, kredi kartı hareketlerinin ne sıklıkta içe aktarılacağını belirten yinelemeyi ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2cd26-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="2cd26-119">Tamamladıktan sonra **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2cd26-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="2cd26-120">Seçilen dosyayı şimdi içe aktarmak için **İçe aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2cd26-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="2cd26-121">İçe aktarma sırasında hatalar oluşursa, başarılı bir içe aktarmayı garanti etmeye yardımcı olmak için yürütme günlüğünü veya hazırlama verisini görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2cd26-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="2cd26-122">Birden fazla dosya biçimi içe aktarmanız gerekiyorsa, her bir biçim türü için ayrı içe aktarma işleri oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2cd26-122">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="2cd26-123">İşten çıkarılan personeller için kredi kartı hareketlerini yeniden atayın</span><span class="sxs-lookup"><span data-stu-id="2cd26-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="2cd26-124">Bir personel kaydı sonlandırıldıktan sonra, personelin Active Directory Etki Alanı Hizmetleri (AD DS) hesabı devre dışı bırakılır.</span><span class="sxs-lookup"><span data-stu-id="2cd26-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="2cd26-125">Ancak, halen gider haline getirilecek ve ödenecek etkin kredi kartı hareketleri olabilir.</span><span class="sxs-lookup"><span data-stu-id="2cd26-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="2cd26-126">**Kredi kartı hareketleri** sayfasından, ilişkili personelin işten çıkarıldığı her türlü kredi kartı hareketi için personeli yeniden atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2cd26-126">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="2cd26-127">Bir veya daha fazla kredi kartı hareketi seçin ve sonra **Hareketleri yeniden ata**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="2cd26-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="2cd26-128">Daha sonra kredi kartı hareketlerinin atanacağı başka bir çalışan seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2cd26-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="2cd26-129">Kredi kartı hareketleri yeniden atadıktan sonra, bunlar bir gider raporu için seçilebilir ve gider raporu geri ödemeleri için uygulanan sıradan işlemlerle ödenebilir.</span><span class="sxs-lookup"><span data-stu-id="2cd26-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>

