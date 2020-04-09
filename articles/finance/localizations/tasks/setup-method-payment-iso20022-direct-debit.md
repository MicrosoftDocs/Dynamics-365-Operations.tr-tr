---
title: ISO20022 hesaptan ödeme için ödeme yöntemi ayarlama
description: Bu yordam, elektronik raporlama kullanılarak ISO20022 hesaptan ödeme için müşteri ödemesi yönteminin veya başka bir ödeme türünün nasıl ayarlanacağını gösterir.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 38afbc3a49d9020540a56e58ce51196b53d6a9e1
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143444"
---
# <a name="setup-method-of-payment-for-iso20022-direct-debit"></a><span data-ttu-id="c1e79-103">ISO20022 hesaptan ödeme için ödeme yöntemi ayarlama</span><span class="sxs-lookup"><span data-stu-id="c1e79-103">Setup method of payment for ISO20022 direct debit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c1e79-104">Bu yordam, elektronik raporlama kullanılarak ISO20022 hesaptan ödeme için müşteri ödemesi yönteminin veya başka bir ödeme türünün nasıl ayarlanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c1e79-104">This procedure shows how to set up the customer method of payment for ISO20022 direct debit or any other payment type using electronic reporting.</span></span> 



<span data-ttu-id="c1e79-105">Bu görevi tamamlamadan önce dışa aktarma biçim yapılandırmalarını ve ödeme hesaplarını ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="c1e79-105">Before you complete this task, you must set up export format configurations and payment accounts.</span></span>



<span data-ttu-id="c1e79-106">Bu yöntem oluşturulurken DEMF demo verisi şirketi kullanılmıştır.</span><span class="sxs-lookup"><span data-stu-id="c1e79-106">This procedure was created using the demo data company DEMF.</span></span>



<span data-ttu-id="c1e79-107">Bu, birlikte elektronik raporlama yapılandırmalarını kullanarak müşteri ödemesi işlemini gösteren beş yordamın üçüncüsüdür.</span><span class="sxs-lookup"><span data-stu-id="c1e79-107">This is the third of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>

1. <span data-ttu-id="c1e79-108">Alacak hesapları > Ödeme kurulumu > Ödeme yöntemi'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="c1e79-108">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="c1e79-109">Kayıtları bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="c1e79-109">Use the Quick Filter to find records.</span></span> <span data-ttu-id="c1e79-110">Örneğin, Ödeme yöntemi alanına "ELECTRONIC" değeriyle filtre uygulayın.</span><span class="sxs-lookup"><span data-stu-id="c1e79-110">For example, filter on the Method of payment field with a value of 'ELECTRONIC'.</span></span>
3. <span data-ttu-id="c1e79-111">Düzenle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c1e79-111">Click Edit.</span></span>
4. <span data-ttu-id="c1e79-112">Ödeme hesabı alanında "DEMF OPER" değerlerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="c1e79-112">In the Payment account field, specify the values 'DEMF OPER'.</span></span>
5. <span data-ttu-id="c1e79-113">Dosya biçimleri bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="c1e79-113">Expand the File formats section.</span></span>
6. <span data-ttu-id="c1e79-114">Genel elektronik raporlama alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c1e79-114">Select Yes in the Generic electronic reporting field.</span></span>
7. <span data-ttu-id="c1e79-115">Biçim yapılandırmasını dışa aktar alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="c1e79-115">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="c1e79-116">Listede ISO20022 Hesaptan ödeme (DE) seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="c1e79-116">In the list, select ISO20022 Direct debit (DE).</span></span>  <span data-ttu-id="c1e79-117">Liste boşsa, müşteri ödemesi biçim yapılandırması içe aktarılmamıştır ve etkin değildir.</span><span class="sxs-lookup"><span data-stu-id="c1e79-117">If the list is empty, the customer payment export format configuration has not been imported and active.</span></span>  
8. <span data-ttu-id="c1e79-118">Talimat iste alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c1e79-118">Select Yes in the Require mandate field.</span></span>
    * <span data-ttu-id="c1e79-119">Müşteri ödeme biçimleri için SEPA hesaptan ödemesi gibi ödeme iletisinde talimat bilgilerini içermesini gerektiren, Talimat iste parametresini seçin.</span><span class="sxs-lookup"><span data-stu-id="c1e79-119">Select the Require mandate parameter for customer payment formats, which require including mandate information in the payment message, like SEPA direct debit.</span></span>  
9. <span data-ttu-id="c1e79-120">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c1e79-120">Click Save.</span></span>

