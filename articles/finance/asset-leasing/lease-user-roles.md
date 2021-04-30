---
title: Kiralama kullanıcı rolleri atama
description: Bu konuda, Varlık kiralamada kullanılan güvenlik rolleri açıklanmıştır. Ayrıca, kullanıcıların bu rollere nasıl atanacağını da açıklanmıştır.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 05728f5027dc079dd413dde1c3aa78cddcea136b
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881072"
---
# <a name="assign-lease-user-roles"></a><span data-ttu-id="34d3f-104">Kiralama kullanıcı rolleri atama</span><span class="sxs-lookup"><span data-stu-id="34d3f-104">Assign lease user roles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="34d3f-105">Bu konuda, Varlık kiralamada kullanılan güvenlik rolleri açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="34d3f-105">This topic describes the security roles that are used in Asset leasing.</span></span> <span data-ttu-id="34d3f-106">Ayrıca, kullanıcıların bu rollere nasıl atanacağını da açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="34d3f-106">It also explains how to assign users to those roles.</span></span>

<span data-ttu-id="34d3f-107">Varlık kiralamada erişim izinlerini ayırmak için üç kullanıcı rolü bulunur.</span><span class="sxs-lookup"><span data-stu-id="34d3f-107">Three user roles differentiate access in Asset leasing.</span></span> <span data-ttu-id="34d3f-108">Bu rollerden biri kiralamaların bakımını yapmak, biri kiralamaları görüntülemek ve biri kiralama uzmanı görevlerini yerine getirmek için uygundur.</span><span class="sxs-lookup"><span data-stu-id="34d3f-108">One role is appropriate for maintaining leases, one is appropriate for viewing leases, and one is appropriate for performing a lease clerk's duties.</span></span> <span data-ttu-id="34d3f-109">Her rolün tüm kiralama sayfaları için özel izinleri vardır ve her biri, kullanıcıların iş sorumluluklarına göre kiralamaları görüntülemesine, oluşturmasına, düzenlemesine veya silmesine izin verir.</span><span class="sxs-lookup"><span data-stu-id="34d3f-109">Each role has specific permissions for all lease pages, and each lets users view, create, edit, or delete leases, according to their job duties.</span></span>

| <span data-ttu-id="34d3f-110">Rol</span><span class="sxs-lookup"><span data-stu-id="34d3f-110">Role</span></span>           | <span data-ttu-id="34d3f-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="34d3f-111">Description</span></span> |
|----------------|-------------|
| <span data-ttu-id="34d3f-112">Kiralama Bakımını Yapma</span><span class="sxs-lookup"><span data-stu-id="34d3f-112">Maintain Lease</span></span> | <span data-ttu-id="34d3f-113">Bu roldeki kullanıcılar kiralama ekleyebilir, düzenleyebilir, silebilir ve görüntüleyebilir.</span><span class="sxs-lookup"><span data-stu-id="34d3f-113">Users in this role can add, edit, delete, and view leases.</span></span> <span data-ttu-id="34d3f-114">Bu rol, aylık günlük girişleri oluşturma ve deftere nakletme ve yeni kiralama ekleme gibi görevleri olan günlük kullanıcılar için tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="34d3f-114">This role is designed for daily users whose tasks include creating and posting monthly journal entries and adding new leases.</span></span> <span data-ttu-id="34d3f-115">Bu rol, tüm Varlık kiralama işlevlerine erişim sağlar.</span><span class="sxs-lookup"><span data-stu-id="34d3f-115">This role gives access to all Asset leasing functionality.</span></span> |
| <span data-ttu-id="34d3f-116">Kiralamayı Görüntüleme</span><span class="sxs-lookup"><span data-stu-id="34d3f-116">View Lease</span></span>     | <span data-ttu-id="34d3f-117">Bu roldeki kullanıcılar yalnızca kiralama kayıtlarını ve planları görüntüleyebilir ve raporları çalıştırabilir.</span><span class="sxs-lookup"><span data-stu-id="34d3f-117">Users in this role can only view lease records, schedules, and run reports.</span></span> <span data-ttu-id="34d3f-118">Bu kullanıcılar yeni kiralamalar oluşturamaz, mevcut kiralamaları düzenleyemez veya kiralar için günlük girişleri oluşturamaz.</span><span class="sxs-lookup"><span data-stu-id="34d3f-118">They can't create new leases, edit existing leases, or create journal entries against leases.</span></span> <span data-ttu-id="34d3f-119">Bu rol, yalnızca kiralamaları ve kira planlarını görüntülemesi ve bu kiralamalar için oluşan hareketleri görmesi gereken kullanıcılar için tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="34d3f-119">The role is designed for users who just have to view leases, lease schedules, and the transactions that occur against those leases.</span></span> |
| <span data-ttu-id="34d3f-120">Kiralama Memuru</span><span class="sxs-lookup"><span data-stu-id="34d3f-120">Lease Clerk</span></span>    | <span data-ttu-id="34d3f-121">Bu roldeki kullanıcılar yalnızca yeni kiralamalar oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="34d3f-121">Users in this role can only create new leases.</span></span> <span data-ttu-id="34d3f-122">Mevcut kiraları düzenleyemez veya silemez, kira planlarını görüntüleyemez veya kira günlüğü girişlerini deftere nakledemez.</span><span class="sxs-lookup"><span data-stu-id="34d3f-122">They can't edit or delete existing leases, view lease schedules, or post leasing journal entries.</span></span> <span data-ttu-id="34d3f-123">Bu rol, veri girişi kapasitesiyle çalışan kullanıcılar için tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="34d3f-123">This role is designed for users who work in a data entry capacity.</span></span> |

<span data-ttu-id="34d3f-124">Varlık kiralamada kullanıcıları bu rollere atamak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="34d3f-124">Follow these steps to assign users to the roles that are used in Asset leasing.</span></span>

1. <span data-ttu-id="34d3f-125">**Sistem Yönetimi \> Güvenlik \> Kullanıcılara roller atayın**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="34d3f-125">Go to **System administration \> Security \> Assign users to roles**.</span></span>
2. <span data-ttu-id="34d3f-126">**Kiralama bakımını yapma**, **Kiralama memuru** veya **Kiralamayı görüntüleme** rolünü seçin ve ardından **Kullanıcıları el ile ata/dışarıda tut** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="34d3f-126">Select the **Maintain lease**, **Lease clerk**, or **View lease** role, and then select **Manually assign/exclude users**.</span></span>
3. <span data-ttu-id="34d3f-127">Role atanacak kullanıcıyı seçin ve **Role ata**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="34d3f-127">Select the user to assign to the role, and then select **Assign to role**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
