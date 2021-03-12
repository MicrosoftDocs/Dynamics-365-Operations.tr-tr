---
title: Kiralama kullanıcı rolleri atama
description: Bu konuda, Varlık kiralamada kullanılan güvenlik rolleri açıklanmıştır. Ayrıca, kullanıcıların bu rollere nasıl atanacağını da açıklanmıştır.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: df23e219f5bd859b0072785dfd5f7a0ec63f540e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995405"
---
# <a name="assign-lease-user-roles"></a><span data-ttu-id="795d0-104">Kiralama kullanıcı rolleri atama</span><span class="sxs-lookup"><span data-stu-id="795d0-104">Assign lease user roles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="795d0-105">Bu konuda, Varlık kiralamada kullanılan güvenlik rolleri açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="795d0-105">This topic describes the security roles that are used in Asset leasing.</span></span> <span data-ttu-id="795d0-106">Ayrıca, kullanıcıların bu rollere nasıl atanacağını da açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="795d0-106">It also explains how to assign users to those roles.</span></span>

<span data-ttu-id="795d0-107">Varlık kiralamada erişim izinlerini ayırmak için üç kullanıcı rolü bulunur.</span><span class="sxs-lookup"><span data-stu-id="795d0-107">Three user roles differentiate access in Asset leasing.</span></span> <span data-ttu-id="795d0-108">Bu rollerden biri kiralamaların bakımını yapmak, biri kiralamaları görüntülemek ve biri kiralama uzmanı görevlerini yerine getirmek için uygundur.</span><span class="sxs-lookup"><span data-stu-id="795d0-108">One role is appropriate for maintaining leases, one is appropriate for viewing leases, and one is appropriate for performing a lease clerk's duties.</span></span> <span data-ttu-id="795d0-109">Her rolün tüm kiralama sayfaları için özel izinleri vardır ve her biri, kullanıcıların iş sorumluluklarına göre kiralamaları görüntülemesine, oluşturmasına, düzenlemesine veya silmesine izin verir.</span><span class="sxs-lookup"><span data-stu-id="795d0-109">Each role has specific permissions for all lease pages, and each lets users view, create, edit, or delete leases, according to their job duties.</span></span>

| <span data-ttu-id="795d0-110">Rol</span><span class="sxs-lookup"><span data-stu-id="795d0-110">Role</span></span>           | <span data-ttu-id="795d0-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="795d0-111">Description</span></span> |
|----------------|-------------|
| <span data-ttu-id="795d0-112">Kiralama Bakımını Yapma</span><span class="sxs-lookup"><span data-stu-id="795d0-112">Maintain Lease</span></span> | <span data-ttu-id="795d0-113">Bu roldeki kullanıcılar kiralama ekleyebilir, düzenleyebilir, silebilir ve görüntüleyebilir.</span><span class="sxs-lookup"><span data-stu-id="795d0-113">Users in this role can add, edit, delete, and view leases.</span></span> <span data-ttu-id="795d0-114">Bu rol, aylık günlük girişleri oluşturma ve deftere nakletme ve yeni kiralama ekleme gibi görevleri olan günlük kullanıcılar için tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="795d0-114">This role is designed for daily users whose tasks include creating and posting monthly journal entries and adding new leases.</span></span> <span data-ttu-id="795d0-115">Bu rol, tüm Varlık kiralama işlevlerine erişim sağlar.</span><span class="sxs-lookup"><span data-stu-id="795d0-115">This role gives access to all Asset leasing functionality.</span></span> |
| <span data-ttu-id="795d0-116">Kiralamayı Görüntüleme</span><span class="sxs-lookup"><span data-stu-id="795d0-116">View Lease</span></span>     | <span data-ttu-id="795d0-117">Bu roldeki kullanıcılar yalnızca kiralama kayıtlarını ve planları görüntüleyebilir ve raporları çalıştırabilir.</span><span class="sxs-lookup"><span data-stu-id="795d0-117">Users in this role can only view lease records, schedules, and run reports.</span></span> <span data-ttu-id="795d0-118">Bu kullanıcılar yeni kiralamalar oluşturamaz, mevcut kiralamaları düzenleyemez veya kiralar için günlük girişleri oluşturamaz.</span><span class="sxs-lookup"><span data-stu-id="795d0-118">They can't create new leases, edit existing leases, or create journal entries against leases.</span></span> <span data-ttu-id="795d0-119">Bu rol, yalnızca kiralamaları ve kira planlarını görüntülemesi ve bu kiralamalar için oluşan hareketleri görmesi gereken kullanıcılar için tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="795d0-119">The role is designed for users who just have to view leases, lease schedules, and the transactions that occur against those leases.</span></span> |
| <span data-ttu-id="795d0-120">Kiralama Memuru</span><span class="sxs-lookup"><span data-stu-id="795d0-120">Lease Clerk</span></span>    | <span data-ttu-id="795d0-121">Bu roldeki kullanıcılar yalnızca yeni kiralamalar oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="795d0-121">Users in this role can only create new leases.</span></span> <span data-ttu-id="795d0-122">Mevcut kiraları düzenleyemez veya silemez, kira planlarını görüntüleyemez veya kira günlüğü girişlerini deftere nakledemez.</span><span class="sxs-lookup"><span data-stu-id="795d0-122">They can't edit or delete existing leases, view lease schedules, or post leasing journal entries.</span></span> <span data-ttu-id="795d0-123">Bu rol, veri girişi kapasitesiyle çalışan kullanıcılar için tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="795d0-123">This role is designed for users who work in a data entry capacity.</span></span> |

<span data-ttu-id="795d0-124">Varlık kiralamada kullanıcıları bu rollere atamak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="795d0-124">Follow these steps to assign users to the roles that are used in Asset leasing.</span></span>

1. <span data-ttu-id="795d0-125">**Sistem Yönetimi \> Güvenlik \> Kullanıcılara roller atayın**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="795d0-125">Go to **System administration \> Security \> Assign users to roles**.</span></span>
2. <span data-ttu-id="795d0-126">**Kiralama bakımını yapma**, **Kiralama memuru** veya **Kiralamayı görüntüleme** rolünü seçin ve ardından **Kullanıcıları el ile ata/dışarıda tut** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="795d0-126">Select the **Maintain lease**, **Lease clerk**, or **View lease** role, and then select **Manually assign/exclude users**.</span></span>
3. <span data-ttu-id="795d0-127">Role atanacak kullanıcıyı seçin ve **Role ata**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="795d0-127">Select the user to assign to the role, and then select **Assign to role**.</span></span>
