---
title: Serbest bırakılan bir ürüne şablon uygulayamazsınız
description: Serbest bırakılan bir ürüne şablon uygulayamazsınız.
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1ad6efdced9bce924fbf5bc207c92fa2c3a6c79d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026976"
---
# <a name="you-cant-apply-a-template-to-create-a-released-product"></a><span data-ttu-id="b3585-103">Serbest bırakılan bir ürün oluşturmak için şablon uygulayamazsınız.</span><span class="sxs-lookup"><span data-stu-id="b3585-103">You can't apply a template to create a released product</span></span>

<span data-ttu-id="b3585-104">KB numarası: 4612097</span><span class="sxs-lookup"><span data-stu-id="b3585-104">KB number: 4612097</span></span>

## <a name="symptoms"></a><span data-ttu-id="b3585-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="b3585-105">Symptoms</span></span>

<span data-ttu-id="b3585-106">**Yeni serbest bırakılan ürün** iletişim kutusunu kullanarak yeni bir serbest bırakılmış ürün oluşturduğunuzda, bir şablon seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b3585-106">When you create a new released product by using the **New released product** dialog box, you can select a template.</span></span> <span data-ttu-id="b3585-107">Şablon, serbest bırakılan yeni ürünün birçok alanı için varsayılan ayarlar sağlamalıdır.</span><span class="sxs-lookup"><span data-stu-id="b3585-107">The template is supposed to provide default settings for many fields of the new released product.</span></span> <span data-ttu-id="b3585-108">Ancak, siz şablonu seçtikten sonra alanların bir kısmı veya tümü ayarlanamaz.</span><span class="sxs-lookup"><span data-stu-id="b3585-108">However, some or all of the fields aren't set after you select the template.</span></span>

## <a name="cause"></a><span data-ttu-id="b3585-109">Nedeni</span><span class="sxs-lookup"><span data-stu-id="b3585-109">Cause</span></span>

<span data-ttu-id="b3585-110">Microsoft Dynamics 365 Supply Chain Management'ın birçok sayfası , bu sayfalarda gösterilen kayıtlar için başlangıç ayarlarını oluşturan bir şablon oluşturmanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="b3585-110">Many pages in Microsoft Dynamics 365 Supply Chain Management let you create a template that establishes initial settings for the records that are shown on those pages.</span></span> <span data-ttu-id="b3585-111">Eylem Bölmesinin **Seçenekler** sekmesinde **Kayıt bilgileri**'ni seçerek bu şablonlardan birini oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b3585-111">You can create one of these templates by selecting **Record info** on the **Options** tab of the Action Pane.</span></span> <span data-ttu-id="b3585-112">Ancak, serbest bırakılan ürünler birçok kayıt türünden çok daha karmaşıktır.</span><span class="sxs-lookup"><span data-stu-id="b3585-112">However, released products are much more complex than most other types of records.</span></span> <span data-ttu-id="b3585-113">Bir şablon oluşturmak için **Serbest bırakılan ürünler** sayfasında **Kayıt bilgileri**'ni seçebilir ve serbest bırakılan bir ürün oluşturduğunuzda bu şablonu seçebilirsiniz ancak şablon yeni serbest bırakılan ürün için beklenen alan değerlerini sağlamaz.</span><span class="sxs-lookup"><span data-stu-id="b3585-113">Although you can select **Record info** on the **Released products** page to create a template, and although you can select that template when you create a released product, the template won't provide the expected field values for the new released product.</span></span> <span data-ttu-id="b3585-114">Bu nedenle, serbest bırakılan ürünler için "kayıt bilgileri" şablonlarını kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="b3585-114">Therefore, you can't use "record info" templates for released products.</span></span> <span data-ttu-id="b3585-115">Bunun yerine, özel ürün şablonları oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="b3585-115">Instead, you must create dedicated product templates.</span></span>

## <a name="resolution"></a><span data-ttu-id="b3585-116">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="b3585-116">Resolution</span></span>

<span data-ttu-id="b3585-117">Ürün şablonu oluşturmak için, **Seçenekler** sekmesindeki **Kayıt bilgileri** düğmesini değil, Eylem Bölmesinin **Ürün** sekmesindeki **Şablon** menüsünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="b3585-117">To create a product template, use the **Template** menu on the **Product** tab of the Action Pane, not the **Record info** button on the **Options** tab.</span></span>

1. <span data-ttu-id="b3585-118">**Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="b3585-118">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="b3585-119">Eylem Bölmesinde, **Ürün** sekmesinde, **Yeni** grubunda, **Şablon** seçeneğini belirleyip , gerektiği şekilde **Kişisel Şablon oluştur** ya da **Paylaşılan şablon oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="b3585-119">On the Action Pane, on the **Product** tab, in the **New** group, select **Template**, and then select either **Create personal template** or **Create shared template**, as appropriate.</span></span>
