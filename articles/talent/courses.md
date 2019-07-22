---
title: Eğitim kursları ayarlama
description: İnsan Kaynakları yöneticileri ve yöneticileri, kursları özelliğini kullanarak işçilere sunulan eğitim hakkındaki bilgileri tutabilirler.
author: andreabichsel
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: 26e76d68c6d5c8bd965e65e65d57f239fb8a2918
ms.sourcegitcommit: 87e8b811680b1f87a973ce1680f07d657fa23046
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/24/2019
ms.locfileid: "1701402"
---
# <a name="set-up-training-courses"></a><span data-ttu-id="e6e6f-103">Eğitim kursları ayarlama</span><span class="sxs-lookup"><span data-stu-id="e6e6f-103">Set up training courses</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e6e6f-104">İnsan Kaynakları yöneticileri ve yöneticileri, kursları özelliğini kullanarak işçilere sunulan eğitim hakkındaki bilgileri tutabilirler.</span><span class="sxs-lookup"><span data-stu-id="e6e6f-104">Human resources administrators and managers can use the courses features to maintain information about the training that's offered to workers.</span></span>

 <a name="set-up-prerequisites"></a><span data-ttu-id="e6e6f-105">Önkoşulları ayarlama</span><span class="sxs-lookup"><span data-stu-id="e6e6f-105">Set up prerequisites</span></span>
---------------------

<span data-ttu-id="e6e6f-106">Aşağıdaki bilgiler gereklidir ve kurslar oluşturmadan önce ayarlanmış olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="e6e6f-106">The following information is required and must be set up before you create courses.</span></span>
-   <span data-ttu-id="e6e6f-107">**Kurs tipleri**</span><span class="sxs-lookup"><span data-stu-id="e6e6f-107">**Course types**</span></span>

<span data-ttu-id="e6e6f-108">Aşağdaki bilgiler kurslar için belirtebileceğiniz isteğe bağlı bilgilerdir.</span><span class="sxs-lookup"><span data-stu-id="e6e6f-108">The following information is optional information that you can specify for courses.</span></span> <span data-ttu-id="e6e6f-109">Kurslar için bu bilgiyi gireceğinizi biliyorsanız, bu bilgileri kurs kayıtlarını oluşturmadan önce ayarlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="e6e6f-109">If you know that you will be entering this information for courses, you should set up this information before you create course records.</span></span>
-   <span data-ttu-id="e6e6f-110">**Derslik grupları**</span><span class="sxs-lookup"><span data-stu-id="e6e6f-110">**Classroom groups**</span></span>
-   <span data-ttu-id="e6e6f-111">**Kurs grupları**</span><span class="sxs-lookup"><span data-stu-id="e6e6f-111">**Course groups**</span></span>
-   <span data-ttu-id="e6e6f-112">**Kurs yerleşimleri**</span><span class="sxs-lookup"><span data-stu-id="e6e6f-112">**Course locations**</span></span>
-   <span data-ttu-id="e6e6f-113">**Derslikler**</span><span class="sxs-lookup"><span data-stu-id="e6e6f-113">**Classrooms**</span></span>
-   <span data-ttu-id="e6e6f-114">**Eğitmenler**</span><span class="sxs-lookup"><span data-stu-id="e6e6f-114">**Instructors**</span></span>

## <a name="course-types"></a><span data-ttu-id="e6e6f-115">Kurs türleri</span><span class="sxs-lookup"><span data-stu-id="e6e6f-115">Course types</span></span>
<span data-ttu-id="e6e6f-116">Kurs yapısı veya kurs içeriğine göre kategorilere ayırmak için Kurs türlerini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e6e6f-116">You can use course types to categorize courses according to the structure or content of the course.</span></span> <span data-ttu-id="e6e6f-117">**Kurs türleri** sayfasın kurs türlerini oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e6e6f-117">You can create course types on the **Course types** page.</span></span> <span data-ttu-id="e6e6f-118">Bir kurs kaydı oluştururken bir kurs türü seçmeniz gerekmektedir.</span><span class="sxs-lookup"><span data-stu-id="e6e6f-118">You must select a course type when you create a course record.</span></span>

## <a name="course-setup-type"></a><span data-ttu-id="e6e6f-119"> Kurs kurulum türü</span><span class="sxs-lookup"><span data-stu-id="e6e6f-119">Course setup type</span></span>
<span data-ttu-id="e6e6f-120">Kurslar için üç kurulum türü aşağıdaki tabloda listelenmektedir.</span><span class="sxs-lookup"><span data-stu-id="e6e6f-120">The following table lists the three setup types for courses.</span></span> <span data-ttu-id="e6e6f-121">Kursun yapısını kurulum türleri belirler.</span><span class="sxs-lookup"><span data-stu-id="e6e6f-121">Setup types determine the structure of the course.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e6e6f-122">Kurulum türü</span><span class="sxs-lookup"><span data-stu-id="e6e6f-122">Setup type</span></span></th>
<th><span data-ttu-id="e6e6f-123">Açıklama</span><span class="sxs-lookup"><span data-stu-id="e6e6f-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e6e6f-124"><strong>Standart</strong></span><span class="sxs-lookup"><span data-stu-id="e6e6f-124"><strong>Standard</strong></span></span></td>
<td><span data-ttu-id="e6e6f-125">Günlük bir gündemi olmayan kurslar için bu türü seçin.</span><span class="sxs-lookup"><span data-stu-id="e6e6f-125">Select this type for courses that will not have a daily agenda.</span></span> <span data-ttu-id="e6e6f-126">Yeni bir kurs oluşturduğunuzda, bu varsayılan türdür şeklindedir.</span><span class="sxs-lookup"><span data-stu-id="e6e6f-126">This is the default setup type when you create a new course.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6e6f-127"><strong>Ajanda</strong></span><span class="sxs-lookup"><span data-stu-id="e6e6f-127"><strong>Agenda</strong></span></span></td>
<td><span data-ttu-id="e6e6f-128">Birden fazla gün sürecek kurs için her günün detayını planlamak için bu türü seçin.</span><span class="sxs-lookup"><span data-stu-id="e6e6f-128">Select this type to plan the details of each day of a course that takes place over multiple days.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6e6f-129"><strong>Gündem + oturumlar</strong></span><span class="sxs-lookup"><span data-stu-id="e6e6f-129"><strong>Agenda + session</strong></span></span></td>
<td><span data-ttu-id="e6e6f-130">Daha karmaşık kurslar için bu türü seçin.</span><span class="sxs-lookup"><span data-stu-id="e6e6f-130">Select this type for the more complex courses.</span></span> <span data-ttu-id="e6e6f-131">Örneğin kursun gündemini parçalara ve oturumlara bölebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e6e6f-131">For example, you can divide the agenda for the course into tracks and sessions.</span></span>
<ul>
<li><span data-ttu-id="e6e6f-132"><strong>Parça</strong> – Parçalar bir kurs için belirli konu alanlarıdır.</span><span class="sxs-lookup"><span data-stu-id="e6e6f-132"><strong>Track</strong> – Tracks are specific subject areas for a course.</span></span></li>
<li><span data-ttu-id="e6e6f-133"><strong>Oturumlar</strong> – Oturumlar parçaları böler ve parçaya ilişkin işlemlerin veya tekniklerin tanımlanmasında yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="e6e6f-133"><strong>Sessions</strong> – Sessions divide up tracks and help identify specific processes or techniques that are relevant to the track.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="course-tasks"></a><span data-ttu-id="e6e6f-134"> Kurs görevleri</span><span class="sxs-lookup"><span data-stu-id="e6e6f-134">Course tasks</span></span>
<span data-ttu-id="e6e6f-135">Her kurs için aşağıdaki görevleri yerine getirebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="e6e6f-135">For each course, you can complete the following tasks.</span></span>
- <span data-ttu-id="e6e6f-136">Katılımcı kaydetme</span><span class="sxs-lookup"><span data-stu-id="e6e6f-136">Register participants</span></span>
- <span data-ttu-id="e6e6f-137">Kayıt için süre sonu belirleme</span><span class="sxs-lookup"><span data-stu-id="e6e6f-137">Specify a registration deadline</span></span>
- <span data-ttu-id="e6e6f-138">Katılımcılar için en az ve en fazla sayı belirleme</span><span class="sxs-lookup"><span data-stu-id="e6e6f-138">Define the minimum and maximum number of participants</span></span>
- <span data-ttu-id="e6e6f-139">Bir kurs yeri ve sınıfı atama</span><span class="sxs-lookup"><span data-stu-id="e6e6f-139">Assign a course location and classroom</span></span>
- <span data-ttu-id="e6e6f-140">Kurs katılımcılarına otel önerme</span><span class="sxs-lookup"><span data-stu-id="e6e6f-140">Recommend hotels to course participants</span></span>
- <span data-ttu-id="e6e6f-141">Çalışan self servis portalında daha sonra ilan edebileceğiniz bir kurs açıklaması oluşturma</span><span class="sxs-lookup"><span data-stu-id="e6e6f-141">Create a course description, which you can then advertise on Employee self service</span></span>

  ><span data-ttu-id="e6e6f-142">**Not** Kursu sadece kimse kayıt olmadıysa silebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e6e6f-142">**Note** You can delete a course only if no one has registered for it.</span></span> 

## <a name="course-statuses"></a><span data-ttu-id="e6e6f-143">Kurs durumları</span><span class="sxs-lookup"><span data-stu-id="e6e6f-143">Course statuses</span></span>
<span data-ttu-id="e6e6f-144">Aşağıdaki tabloda olası kurs durumları ve kursun belirli bir durumu varsa tamamlayabilmeniz için eylemler listelenir.</span><span class="sxs-lookup"><span data-stu-id="e6e6f-144">The following table lists the possible course statuses and the actions that you can complete when the course has a specific status.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e6e6f-145">Durum</span><span class="sxs-lookup"><span data-stu-id="e6e6f-145">Status</span></span></th>
<th><span data-ttu-id="e6e6f-146">Eylemler</span><span class="sxs-lookup"><span data-stu-id="e6e6f-146">Actions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e6e6f-147"><strong>Oluşturuldu</strong></span><span class="sxs-lookup"><span data-stu-id="e6e6f-147"><strong>Created</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="e6e6f-148">Kurs bilgilerini girin ve değiştirin.</span><span class="sxs-lookup"><span data-stu-id="e6e6f-148">Enter and modify course information.</span></span></li>
<li><span data-ttu-id="e6e6f-149">Kursun durumunu <strong>Açık</strong> olarak değiştirin ve böylece çalışanların kurs için kayıt yaptırabilir.</span><span class="sxs-lookup"><span data-stu-id="e6e6f-149">Change the course status to <strong>Open</strong> so that workers can register for the course.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6e6f-150"><strong>Aç</strong></span><span class="sxs-lookup"><span data-stu-id="e6e6f-150"><strong>Open</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="e6e6f-151">Kurs için katılımcılar kaydedin.</span><span class="sxs-lookup"><span data-stu-id="e6e6f-151">Register participants for the course.</span></span></li>
<li><span data-ttu-id="e6e6f-152">Kurstan katılımcı çıkartın.</span><span class="sxs-lookup"><span data-stu-id="e6e6f-152">Remove participants from the course.</span></span></li>
<li><span data-ttu-id="e6e6f-153">Kurs için katılımcılar teyit edin.</span><span class="sxs-lookup"><span data-stu-id="e6e6f-153">Confirm participants for the course.</span></span></li>
<li><span data-ttu-id="e6e6f-154">Kursun durumunu <strong> Kapalı</strong> veya <strong>İptal edildi</strong> değiştirin.</span><span class="sxs-lookup"><span data-stu-id="e6e6f-154">Change the course status to <strong>Closed</strong> or <strong>Canceled</strong>.</span></span></li>
<li><span data-ttu-id="e6e6f-155">Durumu <strong>Onaylandı</strong> olan katılımcılar için soru formları planlayın.</span><span class="sxs-lookup"><span data-stu-id="e6e6f-155">Plan questionnaires for participants whose status is <strong>Confirmed</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6e6f-156"><strong>Kapalı</strong></span><span class="sxs-lookup"><span data-stu-id="e6e6f-156"><strong>Closed</strong></span></span></td>
<td><span data-ttu-id="e6e6f-157">Kursu yeniden açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e6e6f-157">You can reopen the course.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6e6f-158"><strong>İptal edildi</strong></span><span class="sxs-lookup"><span data-stu-id="e6e6f-158"><strong>Canceled</strong></span></span></td>
<td><span data-ttu-id="e6e6f-159">Kursu yeniden açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e6e6f-159">You can reopen the course.</span></span></td>
</tr>
</tbody>
</table>

## <a name="course-participants"></a><span data-ttu-id="e6e6f-160">Kurs katılımcıları</span><span class="sxs-lookup"><span data-stu-id="e6e6f-160">Course participants</span></span>
<span data-ttu-id="e6e6f-161">Kurs katılımcıları, bir eğitim kursuna veya etkinliğine katılım gösteren çalışanlardır.</span><span class="sxs-lookup"><span data-stu-id="e6e6f-161">Course participants are workers who participate in a training course or event.</span></span> <span data-ttu-id="e6e6f-162">Yalnızca açık kurslara katılımcıları kayıt yaptırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e6e6f-162">You can only register participants for open courses.</span></span> <span data-ttu-id="e6e6f-163">Bir kursa kaydedebileceğiniz en az ve en çok katılımcı sayısı, **Kurslar** sayfasının **Genel** hızlı sekmesinde tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="e6e6f-163">The minimum and maximum number of participants that you can register for a course is defined on the **General** FastTab on the **Courses** page.</span></span>

<a name="workflow"></a><span data-ttu-id="e6e6f-164">İş Akışı</span><span class="sxs-lookup"><span data-stu-id="e6e6f-164">Workflow</span></span>
--------

<span data-ttu-id="e6e6f-165">**Personel self servis** sayfası üzerinden bir kursa kayıt olan personeller, kayıtlarını onay için çalışma akışından yönlendirebilirler.</span><span class="sxs-lookup"><span data-stu-id="e6e6f-165">Employees who register for a course through the **Employee self service** page can have their registration routed through workflow for approval.</span></span> <span data-ttu-id="e6e6f-166">Bir kursu bir iş akışına, **Kurslar** sayfasında **Genel** hızlı sekmesinden atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e6e6f-166">You can assign a workflow to a course on the **General** FastTab on the **Courses** page.</span></span>





