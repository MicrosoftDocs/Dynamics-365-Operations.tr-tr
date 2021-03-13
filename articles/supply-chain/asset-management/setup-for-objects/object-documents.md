---
title: Kıymet belgeleri
description: Bu konuda Kıymet Yönetimi'ndeki kıymet belgeleri açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectDocument
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0f8bcae99a96ccd83dc4543b1c56007a4263a19b
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021691"
---
# <a name="asset-documents"></a><span data-ttu-id="13b8e-103">Kıymet belgeleri</span><span class="sxs-lookup"><span data-stu-id="13b8e-103">Asset documents</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="13b8e-104">Bu konuda Kıymet Yönetimi'ndeki kıymet belgeleri açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="13b8e-104">This topic explains asset documents in Asset Management.</span></span>

<span data-ttu-id="13b8e-105">Kıymet Yönetimi'nde belgeleri örneğin iş türleriyle, kıymet üreticileriyle, kıymet türleriyle veya kıymetlerle otomatik olarak ilişkilendirilecek şekilde ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="13b8e-105">In Asset Management, you can set up documents so that they are automatically related to job types, asset manufacturers, asset types, or assets, for example.</span></span> <span data-ttu-id="13b8e-106">Bu işlevsellik, güncelleştirilmiş belge sürümleri yayımlandığında yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="13b8e-106">This functionality is useful when updated document versions are released.</span></span> <span data-ttu-id="13b8e-107">Bu durumda, güncelleştirilmiş belgeyi Supply Chain Management belgeleriniz için kullandığınız standart konuma koymanız ve bu belgeyi oluşturduğunuz varlık belgesi kaydına eklemeniz yeterlidir.</span><span class="sxs-lookup"><span data-stu-id="13b8e-107">In that case, you just have to put the updated document in the standard location that you use for your Supply Chain Management documents, and attach the document to the asset document record that you've created.</span></span> <span data-ttu-id="13b8e-108">Bundan sonra güncelleştirilmiş belgeye **Tüm kıymetler**, **Etkin kıymetler**, **Etkin kıymetlerim**, **Tüm iş emirleri** ve **Etkin iş emri işleri** menü öğelerinden erişebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="13b8e-108">The updated document can then be accessed from the **All assets**, **Active assets**, **My active assets**, **All work orders**, and **Active work order jobs** menu items.</span></span> <span data-ttu-id="13b8e-109">Belgelerin bir varlık belgesi kaydına eklenmesi işleminde standart belge işleme sistemi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="13b8e-109">The process for attaching documents to an asset document record uses the standard document handling system.</span></span>

<span data-ttu-id="13b8e-110">**Örnek 1:** Bir iş türüyle ilgili bir belge bu iş türü için bir yordamı tanımlayabilir.</span><span class="sxs-lookup"><span data-stu-id="13b8e-110">**Example 1:** A document that is related to a job type might describe a procedure for that job type.</span></span>

<span data-ttu-id="13b8e-111">**Örnek 2:** Bir kıymet türü, üretici ve model birleşimiyle ilgili bir belge seçili kıymet üreticisi modeli için standart kullanım kılavuzu olabilir.</span><span class="sxs-lookup"><span data-stu-id="13b8e-111">**Example 2:** A document that is related to a combination of an asset type, manufacturer, and model might be the standard manual for the selected asset manufacturer model.</span></span>

## <a name="create-asset-document-relation"></a><span data-ttu-id="13b8e-112">Kıymet belgesi ilişkili oluşturma</span><span class="sxs-lookup"><span data-stu-id="13b8e-112">Create asset document relation</span></span>

1. <span data-ttu-id="13b8e-113">**Kıymet yönetimi** \> **Kurulum** \> **Kıymet belgeleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="13b8e-113">Select **Asset management** \> **Setup** \> **Asset documents**.</span></span>
2. <span data-ttu-id="13b8e-114">Bir kıymet belgesi kaydı oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="13b8e-114">Select **New** to create an asset document record.</span></span>
3. <span data-ttu-id="13b8e-115">Tercih ettiğiniz belge ilişkisi ayrıntılarına bağlı olarak aşağıdaki alanların birinde veya birkaçında ilgili seçimleri yapın: **Kıymet türü**, **Üretici**, **Model**, **Kıymet**, **İş türü kategorisi**, **İş türü**, **İş türü çeşidi** ve **İş gereksinimi**.</span><span class="sxs-lookup"><span data-stu-id="13b8e-115">Depending on how specific you want the document relation to be, make relevant selections in one or more of the following fields: **Asset type**, **Manufacturer**, **Model**, **Asset**, **Job type category**, **Job type**, **Job type variant**, and **Job requirement**.</span></span> <span data-ttu-id="13b8e-116">**İş türü çeşidi** ve **İş gereksinimi** alanlarındaki kullanılabilir seçenekler **İş türü** alanındaki seçiminize bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="13b8e-116">The options that are available in the **Job type variant** and **Job requirement** fields depend on your selection in the **Job type** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="13b8e-117">Sistem bir kıymet veya iş emriyle ilgili olması gereken belgeleri aradığında Kıymet Yönetimi olası eşleşmeleri denetlemek için tüm kıymet belgesi kayıtlarını tarar.</span><span class="sxs-lookup"><span data-stu-id="13b8e-117">When the system searches for documents that should be related to an asset or a work order, Asset Management goes through all asset document records to check for a possible match.</span></span> <span data-ttu-id="13b8e-118">Her zaman ilk önce en belirgin birleşimi denetler.</span><span class="sxs-lookup"><span data-stu-id="13b8e-118">It always checks the most specific combination first.</span></span> <span data-ttu-id="13b8e-119">Diğer bir deyişle, Kıymet Yönetimi önce **İş gereksinimi** alanı için bir eşleşme arar.</span><span class="sxs-lookup"><span data-stu-id="13b8e-119">In other words, Asset Management first checks for a match for the **Job requirement** field.</span></span> <span data-ttu-id="13b8e-120">Eşleşme bulamazsa **İş türü çeşidi** alanı için eşleşmeleri denetler.</span><span class="sxs-lookup"><span data-stu-id="13b8e-120">If no match is found, it checks for a match for the **Job type variant** field.</span></span> <span data-ttu-id="13b8e-121">Eşleşme bulamazsa **İş türü** alanı için eşleşmeleri denetler ve bu şekilde devam eder.</span><span class="sxs-lookup"><span data-stu-id="13b8e-121">If no match is found, it checks for a match for the **Job type** field, and so on.</span></span> <span data-ttu-id="13b8e-122">**Kıymet belgeleri** sayfasının düzeninde gördüğünüz gibi bu davranış en belirgin birleşimi bulmak için Kıymet Yönetimi'nin eşleşme için sağdan sola her kaydı denetleyeceği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="13b8e-122">As you can see in the layout of the **Asset documents** page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="13b8e-123">Bir kıymet veya iş emriyle birkaç belge ilgili olabilir.</span><span class="sxs-lookup"><span data-stu-id="13b8e-123">Several documents might be related to an asset or a work order.</span></span> <span data-ttu-id="13b8e-124">Bir bakım talebinin veya iş emrinin hizmet düzeyini gerektiği şekilde düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="13b8e-124">You can edit the service level on a maintenance request or a work order as you require.</span></span>

4. <span data-ttu-id="13b8e-125">**Ekler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="13b8e-125">Select **Attachments**.</span></span> <span data-ttu-id="13b8e-126">Standart **Belge işleme** sayfası görünür.</span><span class="sxs-lookup"><span data-stu-id="13b8e-126">The standard **Document handling** page appears.</span></span>
5. <span data-ttu-id="13b8e-127">Kıymet belgesi kaydına eklenmesi gereken belgeleri veya notları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="13b8e-127">Set up the documents or notes that should be attached to the asset document record.</span></span> <span data-ttu-id="13b8e-128">Belgeleri ekledikten sonra **Ekler** alanı kayıtla ilgili belgelerin sayısını gösterir.</span><span class="sxs-lookup"><span data-stu-id="13b8e-128">After you attach documents, the **Attachments** field shows the number of documents that are related to the record.</span></span>
