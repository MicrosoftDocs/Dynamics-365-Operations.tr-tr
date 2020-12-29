---
title: Ödeme faturaları oluşturma
description: Bu konuda, aylık kiralama faturalarının nasıl oluşturulacağı açıklanmaktadır. Kiralamalar için ayrı ayrı fatura oluşturabilir veya birden fazla kiralama için faturalar oluşturmak için toplu iş işlemini kullanabilirsiniz.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 32618814d00cb1e1f1082169a64b187cce1e76b4
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4449001"
---
# <a name="create-payment-invoices"></a><span data-ttu-id="1cbbc-104">Ödeme faturaları oluşturma</span><span class="sxs-lookup"><span data-stu-id="1cbbc-104">Create payment invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1cbbc-105">Kiralamalar için ayrı ayrı aylık fatura oluşturabilir veya birden fazla kiralama için faturalar oluşturmak için toplu iş işlemini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-105">You can create monthly invoices for individual leases, or you can use a batch process to create them for multiple leases.</span></span> <span data-ttu-id="1cbbc-106">Aşağıdaki yordamda, **Kiralama defteri kurulumu** sayfasındaki **Satıcıya Öde** parametresi açıldığında tek bir kira ödemesi girişinin nasıl oluşturulacağı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-106">The following procedure shows how to create an individual lease payment entry when the **Pay to Vendor** parameter on the **Lease book setup** page is turned on.</span></span>

1. <span data-ttu-id="1cbbc-107">**Kiralama özeti** sayfasında bir kiralama seçin ve ardından **Defterler \> Ödeme planı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-107">On the **Lease summary** page, select a lease, and then select **Books \> Payment schedule**.</span></span>
2. <span data-ttu-id="1cbbc-108">Yapılması gereken ödemeyi seçin ve ardından **Günlük oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-108">Select the payment that must be made, and then select **Create journal**.</span></span> <span data-ttu-id="1cbbc-109">Seçili ödemeyle ilgili bir günlüğün oluşturulduğunu bildiren bir ileti alırsınız.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-109">You receive a message that states that a journal was created against the selected payment.</span></span>
3. <span data-ttu-id="1cbbc-110">**Fatura günlükleri**'ni seçin ve ardından ödenmesi gereken faturayı seçin.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-110">Select **Invoice journals**, and then select the invoice that must be paid.</span></span>
4. <span data-ttu-id="1cbbc-111">**Satırlar** sekmesinde, günlük girişini genel muhasebe defterine nakletmeden önce gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-111">On the **Lines** tab, review the journal entry before you post it to the general ledger.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1cbbc-112">Varsayılan olarak, oluşturulan satıcı faturası satırları **Borç hesapları parametreleri** sayfasındaki satıcı deftere nakil profilini kullanır.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-112">By default, the vendor invoice lines that are created use the vendor posting profile from the **Accounts payable parameters** page.</span></span>

5. <span data-ttu-id="1cbbc-113">Doğru günlüğü seçin ve ardından ödenmesi gereken faturayı seçin.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-113">Select the correct journal, and then select the invoice that must be paid.</span></span>

    <span data-ttu-id="1cbbc-114">Bu örnekte, kiralama defterine **Satıcıya Öde** parametresi açıktır.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-114">For this example, the **Pay to Vendor** parameter on the lease book is turned on.</span></span> <span data-ttu-id="1cbbc-115">Bu nedenle, fatura fatura günlüğünde olacaktır.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-115">Therefore, the invoice will be in the invoice journal.</span></span> <span data-ttu-id="1cbbc-116">**Genel Bakış** bölümü günlük girişinin özetini gösterir ve **Satırlar** bölümü, gerçek günlük satırlarının ayrıntılarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-116">The **Overview** section shows a summary of the journal entry, and the **Lines** section shows details of the actual journal lines.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1cbbc-117">**Satıcıya Öde** parametresi kapalıysa ödeme günlüğü girişleri kiralama defteri için **Varlık kiralama** sayfasında listelenir ve sistem fatura yerine bir varlık kiralama girişi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-117">If the **Pay to Vendor** parameter is turned off, payment journal entries will be listed on the **Asset leasing** page for the lease book, and the system will create an asset leasing entry instead of an invoice.</span></span> <span data-ttu-id="1cbbc-118">Kira ödemesi girişi, **Aylık kiralama günlüğü** alanındaki günlük adına deftere nakledilir.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-118">The lease payment entry will be posted to the journal name that is specified in the **Monthly lease journal** field.</span></span>

6. <span data-ttu-id="1cbbc-119">Hareket deftere nakledildikten sonra kiralama defterinde **Yükümlülük hareketleri**'ni seçerek hareket bilgilerini ve kiralama yükümlülüğünün defter değerini görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-119">After the transaction is posted, you can view the transaction information and the carrying value of the lease liability by selecting **Liability transactions** in the lease book.</span></span>

    <span data-ttu-id="1cbbc-120">Ödeme planında, **Günlük deftere nakledildi** onay kutusu seçili olur ve satırda fatura günlük numarası gösterilir.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-120">In the payment schedule, the **Journal posted** check box will be selected, and the line will show the invoice journal number.</span></span> <span data-ttu-id="1cbbc-121">Ödeme günlüğü ve söz konusu günlük için bir giriş oluşturulduktan sonra, yeniden oluşturulabilmesi için girişi tersine çevirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-121">After a payment journal and an entry for that journal have been created, you must reverse the entry before it can be re-created.</span></span>
