---
title: Koşul değerlendirmesi
description: Bu konuda, Kıymet Yönetimi'nde bir kıymet üzerinde bir koşul değerlendirme şablonu ve kayıt oluşturma açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectCondition, EntAssetConditionTemplate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 18be786e6f78829f61db1521a923e229fc4f0e70
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021129"
---
# <a name="condition-assessment"></a><span data-ttu-id="eb5be-103">Koşul değerlendirmesi</span><span class="sxs-lookup"><span data-stu-id="eb5be-103">Condition assessment</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="eb5be-104">Bu konuda, Kıymet Yönetimi'nde bir kıymet üzerinde bir koşul değerlendirme şablonu ve kayıt oluşturma açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="eb5be-104">This topic explains how to create a condition assessment template and registration on an asset in Asset Management.</span></span> <span data-ttu-id="eb5be-105">Koşul değerlendirmesi düzenli aralıklarla gerçekleştirilir ve birincil amaç kıymetler üzerindeki koşul verilerini oluşturup korumaktır.</span><span class="sxs-lookup"><span data-stu-id="eb5be-105">Condition assessment is performed at regular intervals, and the primary objective is to create and maintain condition data on assets.</span></span> <span data-ttu-id="eb5be-106">Önleyici bakım açısından bakıldığında, mevcut durum ve kalan yaşam süresi gibi önemli bilgileri izlemek önemlidir.</span><span class="sxs-lookup"><span data-stu-id="eb5be-106">Seen from a preventive maintenance perspective, it is important to monitor key information such as current condition, and remaining life span.</span></span> <span data-ttu-id="eb5be-107">Ayrıca, düzenli aralıklarla koşul değerlendirmesi yaparsanız, fabrikanızdaki makinelerin koşullarını izleyip karşılaştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="eb5be-107">Furthermore, if you carry out condition assessment at regular intervals, you will be able to monitor and compare conditions on the machinery in your factory.</span></span>

<span data-ttu-id="eb5be-108">Koşul değerlendirmesi, ekipmanınızda birçok koşulu ölçmek ve izlemek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="eb5be-108">Condition assessment can be used to measure and monitor many conditions on your equipment.</span></span> <span data-ttu-id="eb5be-109">Örnek: Makinelerinizdeki titreşimleri ölçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="eb5be-109">Example: You could measure vibrations on your machinery.</span></span> <span data-ttu-id="eb5be-110">Çeşitli ekipman türleri üzerinde Kıymet Yönetimi'nde titreşim ölçümlerini kaydettikten sonra, en son kayıtlı değerlendirmelerde arama yapabilir ve titreşim ölçümlerini görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="eb5be-110">After you have registered vibration measurements in Asset Management on various types of equipment, you can search for the latest registered assessment and view vibration measurements.</span></span>

<span data-ttu-id="eb5be-111">Koşul değerlendirmesi kıymetler üzerinde oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="eb5be-111">Condition assessment is created on assets.</span></span> <span data-ttu-id="eb5be-112">Koşul değerlendirme yordamını gerçekleştirmeden önce bir kıymet türü üzerinde bir koşul değerlendirme şablonu ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="eb5be-112">You set up a condition assessment template on an asset type before you carry out the condition assessment procedure.</span></span> <span data-ttu-id="eb5be-113">Koşul değerlendirmesinde şablonları kullanmanın nedeni, benzer kıymetlerde koşul verilerinin değişmesini önlemektir.</span><span class="sxs-lookup"><span data-stu-id="eb5be-113">The reason for using templates for condition assessment is to avoid variation of condition data on similar assets.</span></span> <span data-ttu-id="eb5be-114">Kıymet Yönetimi'nde koşul değerlendirmesini ayarlama ve kullanma sırası şudur: Önce gerekli koşul değerlendirme şablonlarını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="eb5be-114">The sequence for setting up and using condition assessment in Asset Management is: First you set up the required condition assessment templates.</span></span> <span data-ttu-id="eb5be-115">Ardından **Kıymet türleri** formunda şablonları kıymet türleriyle ilişkilendirin.</span><span class="sxs-lookup"><span data-stu-id="eb5be-115">Next, you associate templates with asset types in the **Asset types** form.</span></span> <span data-ttu-id="eb5be-116">Son olarak **Kıymet** formunda bir kıymet üzerinde koşul değerlendirmesi kayıtları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="eb5be-116">Finally, you can create condition assessment registrations on an asset in the **Asset** form.</span></span>

## <a name="create-a-condition-assessment-template"></a><span data-ttu-id="eb5be-117">Koşul değerlendirme şablonu oluşturma</span><span class="sxs-lookup"><span data-stu-id="eb5be-117">Create a condition assessment template</span></span>

1. <span data-ttu-id="eb5be-118">**Kıymet yönetimi** > **Kurulum** > **Kıymet türleri** > **Koşul değerlendirmesi** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="eb5be-118">Select **Asset management** > **Setup** > **Asset types** > **Condition assessment**.</span></span>
2. <span data-ttu-id="eb5be-119">Yeni bir şablon oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="eb5be-119">Select **New** to create a new template.</span></span>
3. <span data-ttu-id="eb5be-120">**Şablon** alanına şablonu ekleyip kimliğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="eb5be-120">Insert and ID for the template in the **Template** field.</span></span>
4. <span data-ttu-id="eb5be-121">**Ad** alanında şablon için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="eb5be-121">Insert a name for the template in the **Name** field.</span></span>
5. <span data-ttu-id="eb5be-122">**Koşul değerlendirme satırları** hızlı sekmesinden uygun koşul türü ve ölçü birimi seçimi dahil olmak üzere koşul değerlendirmesi için gerekli satırları ekleyin.</span><span class="sxs-lookup"><span data-stu-id="eb5be-122">On the **Condition assessment lines** FastFab, add the lines required for the condition assessment, including selection of the appropriate condition type and measurement unit.</span></span>
6. <span data-ttu-id="eb5be-123">**Kıymet türleri** hızlı sekmesinden koşul değerlendirme şablonunu kullanması gereken kıymet türlerini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="eb5be-123">On the **Asset types** FastTab, add the asset types that should use the condition assessment template.</span></span>
7. <span data-ttu-id="eb5be-124">Ekranın üst kısmındaki **Ayrıntılar** grubunda **Satırlar** ve **Kıymet türleri** alanlarında seçili koşul değerlendirme şablonuyla ilgili değerlendirme satırlarının ve kıymet türlerinin sayısını görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="eb5be-124">In the **Lines** and **Asset types** fields in the **Details** group at the top of the screen, you will see the number of assessment lines and asset types related to the selected condition assessment template.</span></span>


## <a name="create-condition-assessment-registration-on-an-asset"></a><span data-ttu-id="eb5be-125">Kıymette koşul değerlendirme kaydı oluşturma</span><span class="sxs-lookup"><span data-stu-id="eb5be-125">Create condition assessment registration on an asset</span></span>

1. <span data-ttu-id="eb5be-126">**Kıymet yönetimi** > **Ortak** > **Kıymetler** > **Tüm Kıymetler** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="eb5be-126">Select **Asset management** > **Common** > **Assets** > **All Assets**.</span></span>
2. <span data-ttu-id="eb5be-127">Listede bir koşul değerlendirme kaydı oluşturmak istediğiniz kıymeti seçin.</span><span class="sxs-lookup"><span data-stu-id="eb5be-127">In the list, select the asset for which you want to create a condition assessment registration.</span></span>
3. <span data-ttu-id="eb5be-128">**Genel** sekmesinde, **Koşul değerlendirmesi** seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="eb5be-128">On the **General** tab, click **Condition assessment**.</span></span>
4. <span data-ttu-id="eb5be-129">Yeni kayıt yapmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="eb5be-129">Click **New** to make a new registration.</span></span>
5. <span data-ttu-id="eb5be-130">**Tarih** alanında koşul değerlendirmesinin tarihini seçin.</span><span class="sxs-lookup"><span data-stu-id="eb5be-130">Select the date for the condition assessment in the **Date** field.</span></span>
6. <span data-ttu-id="eb5be-131">**Çalışan** alanında değerlendirme kaydını gerçekleştiren çalışanın adını seçin.</span><span class="sxs-lookup"><span data-stu-id="eb5be-131">Select the name of the worker who carried out the assessment registration in the **Worker** field.</span></span>
7. <span data-ttu-id="eb5be-132">**Satırlar** alanında koşul değerlendirmesinde ayarlanan değerlendirme satırlarının sayısını görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="eb5be-132">In the **Lines** field, you see the number of assessment lines set up on the condition assessment.</span></span>
8. <span data-ttu-id="eb5be-133">**Şablon** alanında koşul değerlendirmesi için bir şablon seçin.</span><span class="sxs-lookup"><span data-stu-id="eb5be-133">Select a template for the condition assessment in the **Template** field.</span></span> <span data-ttu-id="eb5be-134">Şablonun adı **Ad** alanına otomatik olarak eklenir ve ilgili kayıt satırları **Koşul değerlendirme satıları** hızlı sekmesine eklenir.</span><span class="sxs-lookup"><span data-stu-id="eb5be-134">The name of the template is automatically inserted in the **Name** field, and the related registration lines are inserted on the **Condition assessment lines** FastTab.</span></span>
9. <span data-ttu-id="eb5be-135">**Notlar** hızlı sekmesine seçili koşul değerlendirmesiyle ilgili notları ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="eb5be-135">You can insert notes relating to the selected condition assessment on the **Notes** FastTab.</span></span>
10. <span data-ttu-id="eb5be-136">Her koşul değerlendirme satırı için **Değer** alanında ölçüm verilerini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="eb5be-136">For each condition assessment line, insert measurement data in the **Value** field.</span></span>
11. <span data-ttu-id="eb5be-137">**Koşul değerlendirmesi satıları** hızlı sekmesinde > **Yorumlar** alanına seçili kayıt satırıyla ilgili bir yorum ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="eb5be-137">You can insert a comment relating to the selected registration line on the **Condition assessment lines** FastTab > **Comments** field.</span></span> <span data-ttu-id="eb5be-138">Bir satıra bir yorum eklerseniz **Yorum** onay kutusu otomatik olarak seçilir.</span><span class="sxs-lookup"><span data-stu-id="eb5be-138">If you add a comment on a line, the **Comment** check box is automatically selected.</span></span>

<span data-ttu-id="eb5be-139">Kıymet üzerinde bir koşul değerlendirme kaydı yaptıktan sonra bir koşul değerlendirme raporunu yazdırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="eb5be-139">After you have made a condition assessment registration on an asset, you can print a condition assessment report.</span></span>

>[!NOTE]
><span data-ttu-id="eb5be-140">Ayrıca bir iş emrine de koşul değerlendirmesi kaydedebilirsiniz (**Kıymet yönetimi** > **Ortak** > **İş emirleri** > **Tüm İş emirleri** > **Koşul değerlendirmesi** düğmesi).</span><span class="sxs-lookup"><span data-stu-id="eb5be-140">You can also register condition assessment on a work order (**Asset management** > **Common** > **Work orders** > **All Work orders** > **Condition assessment** button.)</span></span>
