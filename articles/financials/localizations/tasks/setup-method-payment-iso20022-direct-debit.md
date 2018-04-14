--- 
title: "ISO20022 hesaptan ödemesi için ödeme yöntemini ayarlama"
description: "Bu yordam, elektronik raporlama kullanılarak ISO20022 hesaptan ödeme için müşteri ödemesi yönteminin veya başka bir ödeme türünün nasıl ayarlanacağını gösterir."
author: mrolecki
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: aa159fdf8a8ef543c338546a389d37e1644676a3
ms.contentlocale: tr-tr
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-method-of-payment-for-iso20022-direct-debit"></a><span data-ttu-id="d08ca-103">ISO20022 hesaptan ödemesi için ödeme yöntemini ayarlama</span><span class="sxs-lookup"><span data-stu-id="d08ca-103">Set up method of payment for ISO20022 direct debit</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d08ca-104">Bu yordam, elektronik raporlama kullanılarak ISO20022 hesaptan ödeme için müşteri ödemesi yönteminin veya başka bir ödeme türünün nasıl ayarlanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d08ca-104">This procedure shows how to set up the customer method of payment for ISO20022 direct debit or any other payment type using electronic reporting.</span></span> 



<span data-ttu-id="d08ca-105">Bu görevi tamamlamadan önce dışa aktarma biçim yapılandırmalarını ve ödeme hesaplarını ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="d08ca-105">Before you complete this task, you must set up export format configurations and payment accounts.</span></span>



<span data-ttu-id="d08ca-106">Bu yöntem oluşturulurken DEMF demo verisi şirketi kullanılmıştır.</span><span class="sxs-lookup"><span data-stu-id="d08ca-106">This procedure was created using the demo data company DEMF.</span></span>



<span data-ttu-id="d08ca-107">Bu, birlikte elektronik raporlama yapılandırmalarını kullanarak müşteri ödemesi işlemini gösteren beş yordamın üçüncüsüdür.</span><span class="sxs-lookup"><span data-stu-id="d08ca-107">This is the third of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>

1. <span data-ttu-id="d08ca-108">Alacak hesapları > Ödeme kurulumu > Ödeme yöntemi'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="d08ca-108">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="d08ca-109">Kayıtları bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="d08ca-109">Use the Quick Filter to find records.</span></span> <span data-ttu-id="d08ca-110">Örneğin, Ödeme yöntemi alanına "ELECTRONIC" değeriyle filtre uygulayın.</span><span class="sxs-lookup"><span data-stu-id="d08ca-110">For example, filter on the Method of payment field with a value of 'ELECTRONIC'.</span></span>
3. <span data-ttu-id="d08ca-111">Düzenle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d08ca-111">Click Edit.</span></span>
4. <span data-ttu-id="d08ca-112">Ödeme hesabı alanında "DEMF OPER" değerlerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="d08ca-112">In the Payment account field, specify the values 'DEMF OPER'.</span></span>
5. <span data-ttu-id="d08ca-113">Dosya biçimleri bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="d08ca-113">Expand the File formats section.</span></span>
6. <span data-ttu-id="d08ca-114">Genel elektronik raporlama alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d08ca-114">Select Yes in the Generic electronic reporting field.</span></span>
7. <span data-ttu-id="d08ca-115">Biçim yapılandırmasını dışa aktar alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="d08ca-115">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="d08ca-116">Listede ISO20022 Hesaptan ödeme (DE) seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="d08ca-116">In the list, select ISO20022 Direct debit (DE).</span></span>  <span data-ttu-id="d08ca-117">Liste boşsa, müşteri ödemesi biçim yapılandırması içe aktarılmamıştır ve etkin değildir.</span><span class="sxs-lookup"><span data-stu-id="d08ca-117">If the list is empty, the customer payment export format configuration has not been imported and active.</span></span>  
8. <span data-ttu-id="d08ca-118">Talimat iste alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d08ca-118">Select Yes in the Require mandate field.</span></span>
    * <span data-ttu-id="d08ca-119">Müşteri ödeme biçimleri için SEPA hesaptan ödemesi gibi ödeme iletisinde talimat bilgilerini içermesini gerektiren, Talimat iste parametresini seçin.</span><span class="sxs-lookup"><span data-stu-id="d08ca-119">Select the Require mandate parameter for customer payment formats, which require including mandate information in the payment message, like SEPA direct debit.</span></span>  
9. <span data-ttu-id="d08ca-120">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d08ca-120">Click Save.</span></span>


