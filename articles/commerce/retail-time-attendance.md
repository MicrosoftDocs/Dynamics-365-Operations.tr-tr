---
title: Retail'de saat ve işe devam yönetimi
description: Bu konuda, Dynamics 365 Commerce süre ve işe devam yönetimi için desteklenen senaryolar açıklanmaktadır.
author: aamirallaqaband
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JMGParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 9bec213cd4954f69605387ae2801d8af98a8111c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791907"
---
# <a name="time-and-attendance-management-in-retail"></a><span data-ttu-id="ca896-103">Retail'de saat ve işe devam yönetimi</span><span class="sxs-lookup"><span data-stu-id="ca896-103">Time and attendance management in Retail</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ca896-104">Bu konuda, Dynamics 365 Commerce süre ve işe devam yönetimi için desteklenen senaryolar açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="ca896-104">This topic describes the scenarios that are supported for time and attendance management in Dynamics 365 Commerce.</span></span>

## <a name="manage-worker-setup-and-scheduling"></a><span data-ttu-id="ca896-105">Çalışan kurulumunu ve planlamasını yönetme</span><span class="sxs-lookup"><span data-stu-id="ca896-105">Manage worker setup and scheduling</span></span>

### <a name="initial-configuration"></a><span data-ttu-id="ca896-106">Başlangıç konfigürasyonu</span><span class="sxs-lookup"><span data-stu-id="ca896-106">Initial configuration</span></span>

- <span data-ttu-id="ca896-107">Yapılandırma sihirbazını çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="ca896-107">Run the configuration wizard.</span></span>
- <span data-ttu-id="ca896-108">Çalışanları zaman kayıt çalışanları olarak kaydedin.</span><span class="sxs-lookup"><span data-stu-id="ca896-108">Register workers as time registration workers.</span></span>

### <a name="plan-worker-schedules"></a><span data-ttu-id="ca896-109">Çalışan zaman cetvelini planlayın</span><span class="sxs-lookup"><span data-stu-id="ca896-109">Plan worker schedules</span></span>

- <span data-ttu-id="ca896-110">İş planlayıcısını kullanarak profilleri uygulayın.</span><span class="sxs-lookup"><span data-stu-id="ca896-110">Apply profiles by using the work planner.</span></span> <span data-ttu-id="ca896-111">Daha fazla bilgi için bkz. [İş planlayıcı kullanarak profiller uygulamak](https://technet.microsoft.com/library/aa551234.aspx).</span><span class="sxs-lookup"><span data-stu-id="ca896-111">For more information, see [Apply profiles using work planner](https://technet.microsoft.com/library/aa551234.aspx).</span></span>

<span data-ttu-id="ca896-112">Yapılandırma adımları hakkında daha fazla bilgi için bkz. [Zaman ve katılım ayarlama](https://technet.microsoft.com/library/aa496971.aspx).</span><span class="sxs-lookup"><span data-stu-id="ca896-112">For information about the configuration steps, see [Setting up time and attendance](https://technet.microsoft.com/library/aa496971.aspx).</span></span>

### <a name="commerce-specific-configuration"></a><span data-ttu-id="ca896-113">Commerce yapılandırması</span><span class="sxs-lookup"><span data-stu-id="ca896-113">Commerce-specific configuration</span></span>

- <span data-ttu-id="ca896-114">Zaman kayıtlarını geçerli kılmak istediğiniz çalışanlara yönelik olarak, Saat için bir işlevsellik profilini etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="ca896-114">Enable a functionality profile for Time Clock, for workers that you want to enable time registrations for.</span></span> <span data-ttu-id="ca896-115">**POS işlevsellik profilleri** &gt; **İşlevler** &gt; **POS zaman kayıtları** &gt; **Zaman kayıtlarını etkinleştir** seçeneklerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca896-115">Click **POS functionality profiles** &gt; **Functions** &gt; **POS time registrations** &gt; **Enable time registrations**.</span></span>
- <span data-ttu-id="ca896-116">Saat girişleri iznini görüntülemeyi etkinleştirmek için satış noktası (POS) izinleri gruplarını yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="ca896-116">Configure point of sale (POS) permissions groups to enable the View timeclock entries permission.</span></span> <span data-ttu-id="ca896-117">Bu izinle, bir kullanıcı mağazadaki (rehber yoluyla, ilişkili olduğu başka bir mağazadan) diğer çalışanların saat kayıtlarını görüntüleyebilir.</span><span class="sxs-lookup"><span data-stu-id="ca896-117">This permission lets a user view the time clock registrations of other workers in the store (and from any other store that the user is associated with, via the address book).</span></span> <span data-ttu-id="ca896-118">Bu izni bir yönetici görevi için geçerli hale getirebilirsiniz, ancak bir kasiyer görevi için geçerli hale getiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="ca896-118">You might want to enable this permission for a manager role but not for a cashier role.</span></span> <span data-ttu-id="ca896-119">**POS izin grupları** &gt; **Saat girişlerini görüntüle** seçeneklerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca896-119">Click **POS permission groups** &gt; **View time clock entries**.</span></span>

## <a name="register-time"></a><span data-ttu-id="ca896-120">Kayıt saati</span><span class="sxs-lookup"><span data-stu-id="ca896-120">Register time</span></span>

### <a name="cashier-and-non-cashier-time-registrations"></a><span data-ttu-id="ca896-121">Kasiyer ve kasiyer dışı çalışan zaman kayıtları</span><span class="sxs-lookup"><span data-stu-id="ca896-121">Cashier and non-cashier time registrations</span></span>

- <span data-ttu-id="ca896-122">POS'de:</span><span class="sxs-lookup"><span data-stu-id="ca896-122">On POS:</span></span>

    - <span data-ttu-id="ca896-123">Giriş saati işlemleri:</span><span class="sxs-lookup"><span data-stu-id="ca896-123">Clock-in operations:</span></span>

        - <span data-ttu-id="ca896-124">Çekmece işlemi olmayan bir işlem veya Yeni vardiya ile oturum açın.</span><span class="sxs-lookup"><span data-stu-id="ca896-124">Log on with a non-drawer operation or New shift.</span></span>
        - <span data-ttu-id="ca896-125">Bir Saat işlemi seçin.</span><span class="sxs-lookup"><span data-stu-id="ca896-125">Select a Time Clock operation.</span></span>
        - <span data-ttu-id="ca896-126">İstenen bir işlemi seçin:</span><span class="sxs-lookup"><span data-stu-id="ca896-126">Select a desired operation:</span></span>

            - <span data-ttu-id="ca896-127">Giriş saati</span><span class="sxs-lookup"><span data-stu-id="ca896-127">Clock-in</span></span>
            - <span data-ttu-id="ca896-128">İş Arası</span><span class="sxs-lookup"><span data-stu-id="ca896-128">Break for Work</span></span>
            - <span data-ttu-id="ca896-129">Öğle Yemeği Molası</span><span class="sxs-lookup"><span data-stu-id="ca896-129">Break for Lunch</span></span>
            - <span data-ttu-id="ca896-130">Çıkış saati</span><span class="sxs-lookup"><span data-stu-id="ca896-130">Clock-out</span></span>

        <table>
        <thead>
        <tr>
        <th><span data-ttu-id="ca896-131">Geçerli durum</span><span class="sxs-lookup"><span data-stu-id="ca896-131">Current state</span></span></th>
        <th><span data-ttu-id="ca896-132">Geçerli işlemler</span><span class="sxs-lookup"><span data-stu-id="ca896-132">Available operations</span></span></th>
        </tr>
        </thead>
        <tbody>
        <tr>
        <td><span data-ttu-id="ca896-133">Giriş saati</span><span class="sxs-lookup"><span data-stu-id="ca896-133">Clock-in</span></span></td>
        <td>
        <ul>
        <li><span data-ttu-id="ca896-134">İş Arası</span><span class="sxs-lookup"><span data-stu-id="ca896-134">Break for Work</span></span></li>
        <li><span data-ttu-id="ca896-135">Öğle Yemeği Molası</span><span class="sxs-lookup"><span data-stu-id="ca896-135">Break for Lunch</span></span></li>
        <li><span data-ttu-id="ca896-136">Çıkış saati</span><span class="sxs-lookup"><span data-stu-id="ca896-136">Clock-out</span></span></li>
        </ul>
        </td>
        </tr>
        <tr>
        <td><span data-ttu-id="ca896-137">İş Arası</span><span class="sxs-lookup"><span data-stu-id="ca896-137">Break for Work</span></span></td>
        <td><span data-ttu-id="ca896-138">Giriş saati</span><span class="sxs-lookup"><span data-stu-id="ca896-138">Clock-in</span></span></td>
        </tr>
        <tr>
        <td><span data-ttu-id="ca896-139">Öğle Yemeği Molası</span><span class="sxs-lookup"><span data-stu-id="ca896-139">Break for Lunch</span></span></td>
        <td><span data-ttu-id="ca896-140">Giriş saati</span><span class="sxs-lookup"><span data-stu-id="ca896-140">Clock-in</span></span></td>
        </tr>
        <tr>
        <td><span data-ttu-id="ca896-141">Çıkış saati</span><span class="sxs-lookup"><span data-stu-id="ca896-141">Clock-out</span></span></td>
        <td><span data-ttu-id="ca896-142">Giriş saati</span><span class="sxs-lookup"><span data-stu-id="ca896-142">Clock-in</span></span></td>
        </tr>
        </tbody>
        </table>

        <span data-ttu-id="ca896-143">[![Saat Durumları](./media/timeclockstates.png)](./media/timeclockstates.png)</span><span class="sxs-lookup"><span data-stu-id="ca896-143">[![Time Clock States](./media/timeclockstates.png)](./media/timeclockstates.png)</span></span>

- <span data-ttu-id="ca896-144">Onay mesajını görüntüleyin ve geçerli etkinlik saatinin doğru olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="ca896-144">View the confirmation message, and validate that the current activity time is correct.</span></span>
- <span data-ttu-id="ca896-145">Günlük defteri:</span><span class="sxs-lookup"><span data-stu-id="ca896-145">Logbook:</span></span>

    - <span data-ttu-id="ca896-146">Saat etkinliğini görüntülemek için **Günlük Defteri** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca896-146">Click **Logbook** to view time clock activity.</span></span>
    - <span data-ttu-id="ca896-147">Farklı zaman pencerelerini seçmek için zaman filtrelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ca896-147">Use time filters to select different time windows.</span></span>
    - <span data-ttu-id="ca896-148">Birden çok mağaza konumunda çalışıyorsanız, zaman kayıtlarınızı zamanı kaydettiğiniz tüm mağazalardan görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ca896-148">If you work at multiple store locations, you see your time registrations from all the stores where you recorded time.</span></span> <span data-ttu-id="ca896-149">Seçilen bir mağazadan zaman kayıtlarını görüntülemek için mağaza filtresini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ca896-149">You can use the store filter to view time registrations from a selected store.</span></span>

- <span data-ttu-id="ca896-150">Farklı saat dilimleri:</span><span class="sxs-lookup"><span data-stu-id="ca896-150">Different time zones:</span></span>

    - <span data-ttu-id="ca896-151">Saati farklı bir konumdan görüntülüyorsanız (kasiyer günlük defteri için; veya yönetici senaryosu için **Saat girişlerini görüntüle** seçeneğini kullanarak) ve o konum farklı bir saat dilimindeyse, gördüğünüz zaman kayıtları yerel saat diliminize dönüştürülür.</span><span class="sxs-lookup"><span data-stu-id="ca896-151">If you view time from a different location (for the cashier logbook, or by using **View timeclock entries** for a manager scenario), and that location is in a different time zone, the time records that you see are converted to your local time zone.</span></span> <span data-ttu-id="ca896-152">Örneğin, biri Arizona'da diğer Nevada'da olan iki mağazanın yöneticisisiniz.</span><span class="sxs-lookup"><span data-stu-id="ca896-152">For example, you are a manager for two stores, one in Arizona and the other in Nevada.</span></span> <span data-ttu-id="ca896-153">Bir kasiyer saat 9:00'da bir giriş saati kaydediyor</span><span class="sxs-lookup"><span data-stu-id="ca896-153">A cashier registers a clock-in at 9:00 A.M.</span></span> <span data-ttu-id="ca896-154">Arizona'da.</span><span class="sxs-lookup"><span data-stu-id="ca896-154">in Arizona.</span></span> <span data-ttu-id="ca896-155">O anda, Nevada'da saat sabah 08:00.</span><span class="sxs-lookup"><span data-stu-id="ca896-155">At that moment, the time in Nevada is 8:00 A.M.</span></span> <span data-ttu-id="ca896-156">Bu nedenle, Nevada mağazasındaysanız ve zaman kaydı kayıtlarına bakarsanız, zaman kaydı sabah 08:00 olarak işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="ca896-156">Therefore, if you are in the Nevada store and look at time registration records, the time registration is marked as 8 A.M.</span></span>

## <a name="view-worker-time-registrations"></a><span data-ttu-id="ca896-157">Çalışan zaman kayıtlarını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="ca896-157">View worker time registrations</span></span>

### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a><span data-ttu-id="ca896-158">Çalışan zaman kayıtlarını görüntüleyin ve mağazaya ya da etkinlik türüne göre filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="ca896-158">View worker time registrations, and filter by store or activity type</span></span>

<span data-ttu-id="ca896-159">POS'de:</span><span class="sxs-lookup"><span data-stu-id="ca896-159">On POS:</span></span>

- <span data-ttu-id="ca896-160">**Saat girişlerini görüntüle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="ca896-160">Select **View timeclock entries**.</span></span>
- <span data-ttu-id="ca896-161">Sizinle aynı mağazaya atanan tüm çalışanlardan saat kayıt etkinliklerini görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="ca896-161">You see time clock registration activities from all workers that are assigned to the same stores that you're assigned to.</span></span>
- <span data-ttu-id="ca896-162">Zaman kayıtlarını filtrelemek için etkinlik türünü ve mağaza filtrelerini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ca896-162">You can use the activity type and store filters to filter on time registrations.</span></span>

## <a name="process-and-manage-time-registrations"></a><span data-ttu-id="ca896-163">Zaman kayıtlarını işleme ve yönetme</span><span class="sxs-lookup"><span data-stu-id="ca896-163">Process and manage time registrations</span></span>

<span data-ttu-id="ca896-164">Bir Commerce kullanıcısı, zaman kayıtlarını hesaplamak, onaylamak ve ücret bordrosuna aktarmak için iş akışını takip eder.</span><span class="sxs-lookup"><span data-stu-id="ca896-164">A Commerce user follows the workflow to calculate, approve, and transfer time registrations to payroll.</span></span>

### <a name="primary-operations"></a><span data-ttu-id="ca896-165">Birincil işlemler</span><span class="sxs-lookup"><span data-stu-id="ca896-165">Primary operations</span></span>

- <span data-ttu-id="ca896-166">Hesapla</span><span class="sxs-lookup"><span data-stu-id="ca896-166">Calculate</span></span>
- <span data-ttu-id="ca896-167">Onayla</span><span class="sxs-lookup"><span data-stu-id="ca896-167">Approve</span></span>
- <span data-ttu-id="ca896-168">Ücret bordrosuna aktar</span><span class="sxs-lookup"><span data-stu-id="ca896-168">Submit to payroll</span></span>

### <a name="other-common-operations"></a><span data-ttu-id="ca896-169">Diğer ortak işlemler</span><span class="sxs-lookup"><span data-stu-id="ca896-169">Other common operations</span></span>

- <span data-ttu-id="ca896-170">Toplu Çıkış</span><span class="sxs-lookup"><span data-stu-id="ca896-170">Bulk Clock-out</span></span>
- <span data-ttu-id="ca896-171">Devamsızlığı Kaydet</span><span class="sxs-lookup"><span data-stu-id="ca896-171">Register Absence</span></span>

<span data-ttu-id="ca896-172">Zaman ve katılım kayıtlarını ayarlamak hakkında daha fazla bilgi için bkz. [Zaman ve katılım kayıtlarını işleme](https://technet.microsoft.com/library/aa573180.aspx).</span><span class="sxs-lookup"><span data-stu-id="ca896-172">For more information about how to process time and attendance registrations, see [Process time and attendance registrations](https://technet.microsoft.com/library/aa573180.aspx).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]