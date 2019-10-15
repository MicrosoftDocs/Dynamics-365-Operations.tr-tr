---
title: Boş durumunda olan çek oluşturma
description: Bu konuda, Çekler sayfasında bir banka hesabı için boş çeklerin nasıl oluşturulacağı açıklanmaktadır.
author: abruer
manager: AnnBe
ms.date: 10/26/2017
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankChequeTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 21941
ms.assetid: d7e22bd8-fd0d-47e1-843f-45ab0193ff8d
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2019-09-17
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: af79dd4831f2e7fc71c296922d73a9e42f7955b3
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176123"
---
# <a name="create-checks-that-have-blank-status"></a><span data-ttu-id="941c8-103">Boş durumunda olan çek oluşturma</span><span class="sxs-lookup"><span data-stu-id="941c8-103">Create checks that have Blank status</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="941c8-104">Bu konuda, boş çeklerin nasıl oluşturulacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="941c8-104">This topic explains how to create blank checks.</span></span> <span data-ttu-id="941c8-105">Örneğin, zarar görmüş ve ödeme için kullanılamayacak bir çek kaydetmek üzere boş bir çek oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="941c8-105">For example, you might create a blank check to record a check that has been damaged and can't be used for payment.</span></span>

<span data-ttu-id="941c8-106">**Çekler** sayfasında, çekler için bakım görevleri gerçekleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="941c8-106">On the **Checks** page, you perform maintenance tasks for checks.</span></span> <span data-ttu-id="941c8-107">Örneğin, yeni çek numaraları oluşturabilir ve çekleri silebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="941c8-107">For example, you can create new check numbers and delete checks.</span></span> <span data-ttu-id="941c8-108">Ayrıca **Boş** durumunda olan çekler de oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="941c8-108">You can also create checks that have a status of **Blank**.</span></span> <span data-ttu-id="941c8-109">Boş çekler oluşturulduktan sonra sistemde silinemez veya yeniden kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="941c8-109">After blank checks are created, they can't be deleted or reused in the system.</span></span>

> [!NOTE]
> <span data-ttu-id="941c8-110">Bu özellik yalnızca **Özellik yönetimi** sayfasında **Çekler sayfasında boş durumunda olan çek oluştur** özelliğini açarsanız **Çekler** sayfasında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="941c8-110">This feature is available on the **Checks** page only if you turn on the **Create checks with a blank status on the Checks page** feature on the **Feature management** page.</span></span> <span data-ttu-id="941c8-111">Özellik açılmazsa **Boş** durumunda olan çekler yalnızca Borç hesaplarında ödeme oluşturma işlemi sırasında **Çekle ödeme** iletişim kutusundan oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="941c8-111">If the feature isn't turned on, checks that have **Blank** status can be created only from the **Payment by check** dialog box during the payment generation process in Accounts payable.</span></span>

<span data-ttu-id="941c8-112">**Çekler** sayfasını açmak için **Nakit ve banka yönetimi \> Banka hesapları \> Banka hesapları**'na gidin ve ardından Eylem Bölmesi'ndeki **Ödemeleri yönetme** sekmesinin **İlgili bilgiler** grubunda **Çekler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="941c8-112">To open the **Checks** page, go to **Cash and bank management \> Bank accounts \> Bank accounts**, and then, on the Action Pane, on the **Manage payments** tab, in the **Related information** group, select **Checks**.</span></span> <span data-ttu-id="941c8-113">Alternatif olarak, **Nakit ve banka yönetimi \> Sorgular ve raporlar \> Çekler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="941c8-113">Alternatively, go to **Cash and bank management \> Inquiries and reports \> Checks**.</span></span>

<span data-ttu-id="941c8-114">Ardından **Boş** durumunda olan çek oluşturmak için Eylem Bölmesi'nde **Boş çek oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="941c8-114">Then, to create checks that have **Blank** status, on the Action Pane, select **Create blank checks**.</span></span> <span data-ttu-id="941c8-115">Sistem boş çek oluştururken ilişkili banka hesabı geçici olarak devre dışı bırakılır.</span><span class="sxs-lookup"><span data-stu-id="941c8-115">While the system is creating blank checks, the associated bank account is temporarily inactivated.</span></span> <span data-ttu-id="941c8-116">Bu davranış, boş çekler oluşturulurken aynı anda ödemelerin de oluşturulması riskini azaltır.</span><span class="sxs-lookup"><span data-stu-id="941c8-116">This behavior reduces the risk that payments will be generated at the same time that blank checks are created.</span></span> <span data-ttu-id="941c8-117">İşlem tamamlandığında ilişkili banka hesabı yeniden etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="941c8-117">When the processing is completed, the associated bank account is reactivated.</span></span>
