---
title: Projeler ve servis sözleşmeleri için tümleştirme
description: Servis anlaşmalarıyla ve servis anlaşması satırlarıyla çalıştığınızda, Proje yönetimi ve muhasebe bölümünün aşağıdaki alanlarında belirlenmiş verileri kullanırsınız.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd0a7de17e8ff098220fd183b714b77225cc217f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5247322"
---
# <a name="integration-for-service-agreements-and-projects"></a><span data-ttu-id="adf89-103">Projeler ve servis sözleşmeleri için tümleştirme</span><span class="sxs-lookup"><span data-stu-id="adf89-103">Integration for service agreements and projects</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="adf89-104">Servis anlaşmalarıyla ve servis anlaşması satırlarıyla çalıştığınızda, **Proje yönetimi ve muhasebe** bölümünün aşağıdaki alanlarında belirlenmiş verileri kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="adf89-104">When you work with service agreements and service agreement lines, you use data that is set up in the following areas in **Project management and accounting**.</span></span>

## <a name="project-prices"></a><span data-ttu-id="adf89-105">Proje fiyatları</span><span class="sxs-lookup"><span data-stu-id="adf89-105">Project prices</span></span>

<span data-ttu-id="adf89-106">Bir servis anlaşması hareketi için satış fiyatı ve maliyeti, servis anlaşmasına eklenen projeye uygulanan maliyet fiyatı kurulumundan türetilir.</span><span class="sxs-lookup"><span data-stu-id="adf89-106">The cost and the sales price for a service agreement transaction are derived from the cost price setup that applies to the project that is attached to the service agreement.</span></span> <span data-ttu-id="adf89-107">Maliyet ve satış fiyatları proje, çalışan ve kategoriye göre ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="adf89-107">Cost and sales prices can be set up by project, employee, and category.</span></span> 

## <a name="project-validation"></a><span data-ttu-id="adf89-108">Proje doğrulama</span><span class="sxs-lookup"><span data-stu-id="adf89-108">Project validation</span></span>

<span data-ttu-id="adf89-109">Servis anlaşması satırındaki seçilebilecek projeler, çalışanlar ve kategoriler **Proje yönetimi ve muhasebe**'deki doğrulamaya ayarıyla sınırlandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="adf89-109">The projects, employees, and categories that are available for selection on a service agreement line can be limited by the validation setup in **Project management and accounting**.</span></span> <span data-ttu-id="adf89-110">Doğrulama ayarını kullanarak çalışanları, projeleri ve kategorileri erişim denetimi için bir araya getirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="adf89-110">By using the validation setup, you can combine employees, projects, and categories for control access.</span></span> 

## <a name="project-line-properties"></a><span data-ttu-id="adf89-111">Proje satırı özellikleri</span><span class="sxs-lookup"><span data-stu-id="adf89-111">Project line properties</span></span>

<span data-ttu-id="adf89-112">Bir satır özelliği, bir servis anlaşması satırı için otomatik olarak girilir.</span><span class="sxs-lookup"><span data-stu-id="adf89-112">A line property is entered automatically for a service agreement line.</span></span>

<span data-ttu-id="adf89-113">Satır özellikleri **Proje yönetimi ve muhasebe**'deki **Satır özellikleri** formunda oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="adf89-113">Line properties are created in the **Line properties** form in **Project management and accounting**.</span></span> <span data-ttu-id="adf89-114">Bir servis anlaşmasına girilen satır özelliği servis anlaşması için seçilen projeye iliştirilir ve daha sonra servis anlaşması satırı tarafından devralınır.</span><span class="sxs-lookup"><span data-stu-id="adf89-114">The line property that is entered on a service agreement is attached to the project that is selected for the service agreement and inherited subsequently by the service agreement line.</span></span> 

## <a name="default-offset-accounts"></a><span data-ttu-id="adf89-115">Varsayılan mahsup hesaplar</span><span class="sxs-lookup"><span data-stu-id="adf89-115">Default offset accounts</span></span>

<span data-ttu-id="adf89-116">Gider hareketi girerseniz, varsayılan gider mahsup hesabı hareket için otomatik olarak seçilir.</span><span class="sxs-lookup"><span data-stu-id="adf89-116">If you enter an expense transaction, a default expense offset account is selected automatically for the transaction.</span></span> <span data-ttu-id="adf89-117">Varsayılan gider hesabı geçerli servis anlaşmasına eklenen proje için ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="adf89-117">The default expense account is set up for the project that is attached to the current service agreement.</span></span>

## <a name="project-categories"></a><span data-ttu-id="adf89-118">Proje kategorileri</span><span class="sxs-lookup"><span data-stu-id="adf89-118">Project categories</span></span>

<span data-ttu-id="adf89-119">Servis anlaşması satırları için kullanılabilecek kategoriler **Proje yönetimi ve muhasebe** bölümündeki **Proje kategorileri** formunda belirlenir.</span><span class="sxs-lookup"><span data-stu-id="adf89-119">The categories that are available for service agreement lines are set up in the **Project categories** form in **Project management and accounting**.</span></span> 

> [!NOTE]
> <P><span data-ttu-id="adf89-120"><STRONG>Proje kategorileri</STRONG> formundaki <STRONG>Proje</STRONG> sekmesinde <STRONG>Günlüklerde etkin</STRONG> onay kutusu seçili olan kategoriler seçilebilir.</span><span class="sxs-lookup"><span data-stu-id="adf89-120">Categories that have the <STRONG>Active in journals</STRONG> check box selected on the <STRONG>Project</STRONG> tab in the <STRONG>Project categories</STRONG> form are available for selection.</span></span> <span data-ttu-id="adf89-121">Ancak, <STRONG>Proje yönetimi ve muhasebe parametreleri</STRONG> formundaki <STRONG>Günlükler</STRONG> sekmesinde <STRONG>Etkin olmayan kategoriler</STRONG> onay kutusu seçiliyse tüm kategoriler seçilebilir.</span><span class="sxs-lookup"><span data-stu-id="adf89-121">However, if the <STRONG>Inactive categories</STRONG> check box is selected on the <STRONG>Journals</STRONG> tab in the <STRONG>Project management and accounting parameters</STRONG> form, all categories are available for selection.</span></span></P>

## <a name="project-parameters"></a><span data-ttu-id="adf89-122">Proje parametreleri</span><span class="sxs-lookup"><span data-stu-id="adf89-122">Project parameters</span></span>

<span data-ttu-id="adf89-123">**Proje yönetimi ve muhasebe parametreleri** formundaki **Günlükler** sekmesinde **İşine son verilen çalışanlar** alanı seçiliyse, **Servis sözleşmeleri** ve **Servis siparişleri** formlarında etkin olmayan ve etkin olan çalışanları seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="adf89-123">If the **Terminated workers** field on the **Journals** tab in the **Project management and accounting parameters** form is selected, you can select inactive employees and active employees in the **Service agreements** and **Service orders** forms.</span></span>

<span data-ttu-id="adf89-124">Ayrıca, servis siparişi satırlarına başlangıç ve bitiş saatleri girmek için **Servis siparişleri** formundaki **Proje** sekmesinde bulunan **Başlangıç zamanı** ve **Bitiş zamanı** alanlarını etkinleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="adf89-124">Also, you can enable the **Start time** and **End time** fields on the **Project** tab in the **Service orders** form to enter starting and ending times on service order lines.</span></span>

## <a name="enable-the-starting-and-ending-time-feature-for-service-orders"></a><span data-ttu-id="adf89-125">Servis siparişleri için başlangıç ve bitiş zamanı özelliğini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="adf89-125">Enable the starting and ending time feature for service orders</span></span>

1.  <span data-ttu-id="adf89-126">**Proje yönetimi ve muhasebe** \> **Kurulum** \> **Proje yönetimi ve muhasebe parametreleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="adf89-126">Click **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>

2.  <span data-ttu-id="adf89-127">**Günlükler** sekmesine tıklayın ve sonra **Başlangıç/bitiş zamanlarını göster** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="adf89-127">Click the **Journals** tab, and then select the **Show start/end times** check box.</span></span>

3.  <span data-ttu-id="adf89-128">**Proje yönetimi ve muhasebe** \> **Kurulum** \> **Günlükler** \> **Günlük adları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="adf89-128">Click **Project management and accounting** \> **Setup** \> **Journals** \> **Journal names**.</span></span>

4.  <span data-ttu-id="adf89-129">Servis siparişine iliştirilen günlük adını seçin.</span><span class="sxs-lookup"><span data-stu-id="adf89-129">Select the journal name that is attached to the service order.</span></span>

5.  <span data-ttu-id="adf89-130">**Genel** sekmesine tıklayın ve sonra **Başlangıç/bitiş zamanlarını göster** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="adf89-130">Click the **General** tab, and then select the **Show start/end times** check box.</span></span>


> [!NOTE]
> <P><span data-ttu-id="adf89-131"><STRONG>Servis yönetimi parametreleri</STRONG> formundaki <STRONG>Günlükler</STRONG> sekmesinde yer alan <STRONG>Saat</STRONG> alanında servis siparişi için günlük adını seçin.</span><span class="sxs-lookup"><span data-stu-id="adf89-131">Select the journal name for the service order in the <STRONG>Hour</STRONG> field on the <STRONG>Journals</STRONG> tab in the <STRONG>Service management parameters</STRONG> form.</span></span></P>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]