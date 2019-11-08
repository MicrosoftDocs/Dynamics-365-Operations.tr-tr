---
title: Bakım talebi türleri
description: Bu konuda Kıymet Yönetimi'nde bakım talebi türleri ayarlama işlemi açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 430e475b52638dd80512ffd79d42aac6f5f340e1
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571151"
---
# <a name="maintenance-request-types"></a><span data-ttu-id="38892-103">Bakım talebi türleri</span><span class="sxs-lookup"><span data-stu-id="38892-103">Maintenance request types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="38892-104">Bakım talebi türleri, bakım taleplerini kategorilere ayırmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="38892-104">Maintenance request types are used to categorize maintenance requests.</span></span> <span data-ttu-id="38892-105">Örneğin, önleyici bakım ve düzeltici bakım ile ilgili bakım talebi türlerine sahip olabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="38892-105">For example, you might have maintenance request types that are related to preventive maintenance and corrective maintenance.</span></span> <span data-ttu-id="38892-106">Veya varlıkların onarımını yönetmek için kullanılan özel bir bakım talebi türü olabilir (depo onarımı).</span><span class="sxs-lookup"><span data-stu-id="38892-106">Or you might have a special maintenance request type that is used to manage repair of assets (depot repair).</span></span>

<span data-ttu-id="38892-107">Bakım talebi türü, bir bakım talebi yaşam döngüsü durumu grubu (bakım yaşam döngüsü modeli) ile ilişkisini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="38892-107">A maintenance request type defines the affiliation with a maintenance request lifecycle state group (maintenance lifecycle model).</span></span> <span data-ttu-id="38892-108">Bakım talebi yaşam döngüsü modelleri, bakım talebi için ayarlanacak yaşam döngüsü durumlarını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="38892-108">Maintenance request lifecycle models define the lifecycle states that can be set for a maintenance request.</span></span> <span data-ttu-id="38892-109">(Bakım talebi yaşam döngüsü durumlarına örnekler **Oluşturuldu**, **Etkin**, ve **Bitti** öğelerini içerir.)</span><span class="sxs-lookup"><span data-stu-id="38892-109">(Examples of maintenance request lifecycle states include **Created**, **Active**, and **Ended**.)</span></span>

1. <span data-ttu-id="38892-110">**Varlık yönetimi** \> **Kurulum** \> **Bakım talepleri** \> **Bakım talepleri türleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="38892-110">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Maintenance request types**.</span></span>
2. <span data-ttu-id="38892-111">Bakım talebi türü oluşturmak için **Yeni** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="38892-111">Select **New** to create a maintenance request type.</span></span>
3. <span data-ttu-id="38892-112">**Bakım talebi türü** alanına bakım talebi türü için bir kimlik girin.</span><span class="sxs-lookup"><span data-stu-id="38892-112">In the **Maintenance request type** field, enter an ID for the maintenance request type.</span></span>
4. <span data-ttu-id="38892-113">**Ad** alanına, bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="38892-113">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="38892-114">**Bakım talebi yaşam döngüsü modeli**'ndeki **Genel** hızlı sekmesinde bir bakım talebi yaşam döngüsü modeli seçin.</span><span class="sxs-lookup"><span data-stu-id="38892-114">On the **General** FastTab, in the **Maintenance request lifecycle model** field, select a maintenance request lifecycle model.</span></span>
6. <span data-ttu-id="38892-115">**İş emri türü** alanında bir iş emri türü seçin.</span><span class="sxs-lookup"><span data-stu-id="38892-115">In the **Work order type** field, select a work order type.</span></span> <span data-ttu-id="38892-116">Bir bakım talebi iş emrine dönüştürüldüğünde, iş emri, bakım talebi türüyle ilişkili iş emri türünü otomatik olarak alır.</span><span class="sxs-lookup"><span data-stu-id="38892-116">When a maintenance request is converted to a work order, the work order automatically gets the work order type that is related to the maintenance request type.</span></span>

<span data-ttu-id="38892-117">Aşağıdaki çizimde bir **Bakım talebi türleri** liste sayfasının bir örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="38892-117">The following illustration shows an example of the **Maintenance request types** page.</span></span>

![Bakım talebi türleri sayfası](media/07-setup-for-requests.png)
