---
title: "Şablon Ürün Reçeteleri"
description: "Şablon ürün reçetesi (BOM), düzenli olarak servis verilen servis nesnelerinin bileşenlerinin standart bir listesini sağlar."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 6e3a16b9938f6d4222e0a95078356f457e71a1bb
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---

# <a name="template-boms"></a><span data-ttu-id="aadc0-103">Şablon Ürün Reçeteleri</span><span class="sxs-lookup"><span data-stu-id="aadc0-103">Template BOMs</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="aadc0-104">Şablon ürün reçetesi (BOM), düzenli olarak servis verilen servis nesnelerinin bileşenlerinin standart bir listesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="aadc0-104">A template bill of materials (BOM) provides you with a standardized list of components for service objects that are serviced regularly.</span></span> <span data-ttu-id="aadc0-105">Şablon ürün reçetesinde listelenen bileşenler servis nesnesinin ayrı ayrı alt bileşenlerini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="aadc0-105">The components that are listed in the template BOM represent the individual subcomponents of the service object.</span></span> <span data-ttu-id="aadc0-106">Bir şablon ürün reçetesini bir servis nesnesine uyguladığınızda, servis nesnesinde değiştirilen alt bileşenlerin kaydını tutabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aadc0-106">By applying a template BOM to a service object, you can keep a record of the subcomponents that have been replaced on the service object.</span></span>

<span data-ttu-id="aadc0-107">Şablon ürün reçetesini bir servis anlaşmasına veya servis siparişine uygulamak için onu bir servis nesnesi ilişkisine eklersiniz.</span><span class="sxs-lookup"><span data-stu-id="aadc0-107">To apply a template BOM to a service agreement or a service order, you attach it to a service object relation.</span></span>


> [!NOTE]
> <P><span data-ttu-id="aadc0-108">Her servis nesnesine yalnızca bir şablon ürün reçetesi uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aadc0-108">You can apply only one template BOM to a service object.</span></span></P>

## <a name="create-a-template-bom"></a><span data-ttu-id="aadc0-109">Şablon ürün reçetesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="aadc0-109">Create a template BOM</span></span>

<span data-ttu-id="aadc0-110">Aşağıdaki tablo bir şablon ürün reçetesi oluşturmak için kullanabileceğiniz çeşitli yöntemlerle ilgili bilgiler içerir.</span><span class="sxs-lookup"><span data-stu-id="aadc0-110">The following table contains information about the various methods that you can use to create a template BOM.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="aadc0-111">Yöntem</span><span class="sxs-lookup"><span data-stu-id="aadc0-111">Method</span></span></p></th>
<th><p><span data-ttu-id="aadc0-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="aadc0-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aadc0-113">Üretim</span><span class="sxs-lookup"><span data-stu-id="aadc0-113">Production</span></span></p></td>
<td><p><span data-ttu-id="aadc0-114">Şablon ürün reçetesi üretim emrini temel alır.</span><span class="sxs-lookup"><span data-stu-id="aadc0-114">The template BOM is based on a production order.</span></span> <span data-ttu-id="aadc0-115">Bu seçenek yalnızca bir üretim ortamında iş yapıyorsanız kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="aadc0-115">This option is applicable only if you operate in a production environment.</span></span> <span data-ttu-id="aadc0-116">Yararı, bir maddeyi oluşturan bileşenlerin güncel ve ayrıntılı bir listesini sağlamasıdır.</span><span class="sxs-lookup"><span data-stu-id="aadc0-116">The benefit is that you have a current, detailed listing of the components that make up an item.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aadc0-117">Madde BOM</span><span class="sxs-lookup"><span data-stu-id="aadc0-117">Item BOM</span></span></p></td>
<td><p><span data-ttu-id="aadc0-118">Şablon ürün reçetesi bir madde ürün reçetesini temel alır.</span><span class="sxs-lookup"><span data-stu-id="aadc0-118">The template BOM is based on an item BOM.</span></span> <span data-ttu-id="aadc0-119">Madde ürün reçetesi, üretim ürün reçetesinden farklı olarak bir maddeyi oluşturan bileşenlerin statik listesidir.</span><span class="sxs-lookup"><span data-stu-id="aadc0-119">The item BOM, unlike the production BOM, is a static list of the components that make up an item.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aadc0-120">Mevcut şablon</span><span class="sxs-lookup"><span data-stu-id="aadc0-120">Existing template</span></span></p></td>
<td><p><span data-ttu-id="aadc0-121">Şablon mevcut bir şablon ürün reçetesini temel alır.</span><span class="sxs-lookup"><span data-stu-id="aadc0-121">The template is based on an existing template BOM.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aadc0-122">El ile</span><span class="sxs-lookup"><span data-stu-id="aadc0-122">Manual</span></span></p></td>
<td><p><span data-ttu-id="aadc0-123">Bir servis nesnesinde normalde hangi parçaların değiştirildiğini tam olarak biliyorsanız ürün reçetenizi el ile oluşturmayı tercih edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aadc0-123">If you know what spare parts are typically replaced on a service object, you can create your template BOM manually.</span></span> <span data-ttu-id="aadc0-124">Bu yöntem, şablona dahil edilen bileşenlerin çalışma alanınızın gerçek gereksinimlerini yansıttığından emin olmanıza yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="aadc0-124">This method helps make sure that the components that are included in the template reflect the actual requirements of your workplace.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="apply-the-template-bom-to-a-service-agreement-or-service-order"></a><span data-ttu-id="aadc0-125">Şablon ürün reçetesini servis sözleşmesine veya servis siparişine uygulama</span><span class="sxs-lookup"><span data-stu-id="aadc0-125">Apply the template BOM to a service agreement or service order</span></span>

<span data-ttu-id="aadc0-126">Şablon ürün reçetesini servis sözleşmesine, servis siparişine veya her ikisine uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aadc0-126">You can apply a template BOM to a service agreement, a service order, or both.</span></span> <span data-ttu-id="aadc0-127">Servis anlaşması genellikle müşteriyle uzun dönemli bir ilişkiyi kapsar.</span><span class="sxs-lookup"><span data-stu-id="aadc0-127">The service agreement usually covers a long-term relationship with a customer.</span></span> <span data-ttu-id="aadc0-128">Servis ürün reçetesine kaydedilen değiştirmelerin geçmişi, servis sözleşmesinde bulunacak kullanışlı verilerdir.</span><span class="sxs-lookup"><span data-stu-id="aadc0-128">The history of replacements that is recorded in the service BOM is useful data to have for the service agreement.</span></span>

<span data-ttu-id="aadc0-129">Ayrıca, bir servis nesnesinde gerçekleştirilen bir servisin geçmişini kaydetmek için de bir servis siparişine bir şablon ürün reçetesi uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aadc0-129">You can also apply a template BOM to a service order to record the history of the service that has been performed on a service object.</span></span>

## <a name="copy-the-history-of-a-service-bom"></a><span data-ttu-id="aadc0-130">Servis ürün reçetesinin geçmişini kopyalama</span><span class="sxs-lookup"><span data-stu-id="aadc0-130">Copy the history of a service BOM</span></span>

<span data-ttu-id="aadc0-131">Bir servis ürün reçetesi satırının geçmişini bir servis sözleşmesinden diğerine kopyalayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aadc0-131">You can copy the history of a service BOM line from one service agreement to another service agreement.</span></span> <span data-ttu-id="aadc0-132">Servis geçmişini servis sözleşmeleri arasında kopyalayarak bir madde için değiştirme kaydını koruyabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aadc0-132">By copying the service history between service agreements, you can preserve the record of replacements for an item.</span></span>

<span data-ttu-id="aadc0-133">**Örnek**</span><span class="sxs-lookup"><span data-stu-id="aadc0-133">**Example**</span></span>

<span data-ttu-id="aadc0-134">Bir müşterinin arabası için üç yıllık bir servis anlaşması yaptınız.</span><span class="sxs-lookup"><span data-stu-id="aadc0-134">You have set up a three-year service agreement for a customer's car.</span></span> <span data-ttu-id="aadc0-135">Bu dönem süresince, müşteri şirketin sunduğu iyi servise alışır.</span><span class="sxs-lookup"><span data-stu-id="aadc0-135">During that period, the customer becomes accustomed to the good service that the company provides.</span></span> <span data-ttu-id="aadc0-136">Bu nedenle, sözleşmenin süresi dolduğunda, müşteri yeni bir sözleşme yapmak ister.</span><span class="sxs-lookup"><span data-stu-id="aadc0-136">Therefore, after the agreement expires, the customer wants to set up a new one.</span></span> <span data-ttu-id="aadc0-137">Artık şirket için daha avantajlı bir anlaşma yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aadc0-137">You are now able to negotiate a more favorable agreement for the company.</span></span> <span data-ttu-id="aadc0-138">Değiştirilen bileşenlerin kaydı gelecekte işinize yarayabileceğinden, servis ürün reçetesinin geçmişini yeni sözleşmeye kopyalarsınız.</span><span class="sxs-lookup"><span data-stu-id="aadc0-138">Because the record of replaced components might be useful in the future, you copy the history of the service BOM to the new agreement.</span></span>

## <a name="modify-the-template-bom"></a><span data-ttu-id="aadc0-139">Şablon ürün reçetesini değiştirme</span><span class="sxs-lookup"><span data-stu-id="aadc0-139">Modify the template BOM</span></span>

<span data-ttu-id="aadc0-140">Şablon ürün reçetesi bir servis nesnesine eklenmemiş ise, içindeki satırları değiştirebilir veya silebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aadc0-140">If a template BOM has not been attached to a service object, you can modify or delete lines in it.</span></span> <span data-ttu-id="aadc0-141">Şablon ürün reçetesi servis nesnesine eklendikten sonra yalnızca ürün reçetesinin yerel sürümünü değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aadc0-141">After the template BOM is attached to a service object, you can modify only the local version of the BOM.</span></span> <span data-ttu-id="aadc0-142">Bir şablon ürün reçetesinin yerel sürümünün ayarını çoğaltmak isterseniz, yerel sürümü temel alan yeni bir şablon ürün reçetesi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aadc0-142">If you want to duplicate the setup of a local version of a template BOM, you can create a new template BOM based on the local version.</span></span> <span data-ttu-id="aadc0-143">Daha fazla bilgi için bkz. [Servis ürün reçetesini değiştirme](modify-service-bom.md).</span><span class="sxs-lookup"><span data-stu-id="aadc0-143">For more information, see [Modify a Service BOM](modify-service-bom.md).</span></span>

<span data-ttu-id="aadc0-144">Ürün reçetesinde bir maddeyi değiştirirseniz, değiştirme işlemini ürün reçetesi tasarımcısındaki ürün reçetesi satırına kaydedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aadc0-144">If you replace an item in the BOM, you can register the replacement on the BOM line in the BOM designer.</span></span> <span data-ttu-id="aadc0-145">İsteğe bağlı olarak, değiştirilen nesne için bir servis siparişi satırı oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aadc0-145">Optionally, you can create a service order line for the replacement object.</span></span> <span data-ttu-id="aadc0-146">Bir servis siparişi satırı oluşturursanız değiştirilen maddeyi faturalayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aadc0-146">If you create a service order line, you can invoice the replacement item.</span></span> <span data-ttu-id="aadc0-147">Değiştirme için bir servis siparişi satırı oluşturmazsanız, servis nesnesinin geçmişini izlemek üzere değiştirme kaydı korunur.</span><span class="sxs-lookup"><span data-stu-id="aadc0-147">If you do not create a service order line for a replacement, the replacement registration is kept to track the history of the service object.</span></span>

## <a name="change-how-information-on-the-bom-line-is-displayed"></a><span data-ttu-id="aadc0-148">Ürün reçetesi satırı hakkındaki bilgilerin nasıl görüntüleneceğini değiştirme</span><span class="sxs-lookup"><span data-stu-id="aadc0-148">Change how information on the BOM line is displayed</span></span>

<span data-ttu-id="aadc0-149">Tüm şablon ve servis ürün reçeteleri için ürün reçetesindeki bilgilerin görüntülenme şeklini değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aadc0-149">You can change the way that information on the BOM line is displayed for all template and service BOMs.</span></span> <span data-ttu-id="aadc0-150">Değişiklikler tüm şablon ürün reçetelerine ve servis ürün reçetelerine uygulanır.</span><span class="sxs-lookup"><span data-stu-id="aadc0-150">The changes are applied to all template BOMs and service BOMs.</span></span> <span data-ttu-id="aadc0-151">Buna, servis nesnelerine iliştirilenler de dahildir.</span><span class="sxs-lookup"><span data-stu-id="aadc0-151">This includes those that are attached to service objects.</span></span>

## <a name="set-up-number-sequences-for-template-boms"></a><span data-ttu-id="aadc0-152">Şablon ürün reçeteleri için numara serileri ayarlama</span><span class="sxs-lookup"><span data-stu-id="aadc0-152">Set up number sequences for template BOMs</span></span>

<span data-ttu-id="aadc0-153">Şablon ürün reçeteleri kullanmak için iki numara serisi ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="aadc0-153">To use template BOMs, you must set up two number sequences.</span></span> <span data-ttu-id="aadc0-154">Şablon ürün reçetesi için bir numara serisi ve ürün reçetesi geçmişi satır numarası için bir numara serisi ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="aadc0-154">Set up one number sequence for the template BOM and one for the BOM history line number.</span></span>


> [!NOTE]
> <P><span data-ttu-id="aadc0-155">Numara serileri Microsoft Dynamics AX'te tanımlayıcıları onları gerektiren kayıtlara tahsis etmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="aadc0-155">Number sequences are used throughout Microsoft Dynamics AX to allocate identifiers to records that require them.</span></span> <span data-ttu-id="aadc0-156">Bir numara serisini bir şablon ürün reçetesi veya ürün reçetesi geçmişi satır numarasına atamak için önce numara serilerinin kodlarını ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="aadc0-156">Before you can assign a number sequence to a template BOM or a BOM history line number, you must set up number sequences codes.</span></span></P>


## <a name="set-up-number-sequences"></a><span data-ttu-id="aadc0-157">Numara serileri ayarı</span><span class="sxs-lookup"><span data-stu-id="aadc0-157">Set up number sequences</span></span>

1.  <span data-ttu-id="aadc0-158">**Numara serilerinin** liste sayfasında, şablon ürün reçeteleri ve ürün reçetesi geçmişi satır numarası için numara serileri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="aadc0-158">On the **Number sequences** list page, create number sequences for template BOMs and the BOM history line number.</span></span> 

2.  <span data-ttu-id="aadc0-159">**Servis yönetimi** \> **Kurulum** \> **Servis yönetimi parametreleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aadc0-159">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

3.  <span data-ttu-id="aadc0-160">**Numara serileri**'ne tıklayın ve **Numara serileri** formunda oluşturduğunuz numara serisi referansları için bir numara serisi kodu seçin.</span><span class="sxs-lookup"><span data-stu-id="aadc0-160">Click **Number sequences**, and then select a number sequence code for the number sequence references that you created in the **Number sequences** form.</span></span>

4.  <span data-ttu-id="aadc0-161">Değişikliklerinizi kaydetmek için formu kapatın.</span><span class="sxs-lookup"><span data-stu-id="aadc0-161">Close the form to save your changes.</span></span>


> [!NOTE]
> <P><span data-ttu-id="aadc0-162">Ürün reçetesi geçmişi satır numarası sistem tarafından ürün reçetesi geçmişi hareketlerini servis sözleşmesi veya servis siparişi ile ilişkilendirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="aadc0-162">The BOM history line number is used by the system to associate the transactions in the BOM history with a service agreement or service order.</span></span> <span data-ttu-id="aadc0-163">Numara kullanıcı arabiriminde görüntülenmez.</span><span class="sxs-lookup"><span data-stu-id="aadc0-163">The number is not displayed in the user interface.</span></span></P>



## <a name="see-also"></a><span data-ttu-id="aadc0-164">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="aadc0-164">See also</span></span>

[<span data-ttu-id="aadc0-165">Şablon ürün reçetesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="aadc0-165">Create a template BOM</span></span>](create-template-bom.md)

[<span data-ttu-id="aadc0-166">Nesne ilişkilerinde şablon ürün reçetelerini yönetme</span><span class="sxs-lookup"><span data-stu-id="aadc0-166">Manage template BOMs on object relations</span></span>](manage-template-boms-on-object-relations.md)

[<span data-ttu-id="aadc0-167">Servis Ürün Reçetesini Değiştirme</span><span class="sxs-lookup"><span data-stu-id="aadc0-167">Modify a Service BOM</span></span>](modify-service-bom.md)

 



