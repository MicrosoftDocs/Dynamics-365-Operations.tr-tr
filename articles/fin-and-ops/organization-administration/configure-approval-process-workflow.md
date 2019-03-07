---
title: İş akışında onay işlemlerini yapılandırma
description: Onay işleminin özelliklerini yapılandırmak için aşağıdaki yordamı kullanın.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195643
ms.assetid: f853f57b-83ae-4fb0-a9fa-06ea3fc34fa1
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 08641eaac31813a8bee3231118f8e2bf802ea3e1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "325653"
---
# <a name="configure-approval-processes-in-a-workflow"></a><span data-ttu-id="dc18f-103">İş akışında onay işlemlerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="dc18f-103">Configure approval processes in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dc18f-104">Onay işleminin özelliklerini yapılandırmak için aşağıdaki yordamı kullanın.</span><span class="sxs-lookup"><span data-stu-id="dc18f-104">Use the following procedure to configure the properties of the approval process.</span></span>

<span data-ttu-id="dc18f-105">Onay işlemini yapılandırmak için iş akışı düzenleyicisinde, onay öğesine sağ tıklayın ve ardından **Özellikler** formunu açmak için **Özellikler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dc18f-105">To configure an approval process, in the workflow editor, right-click the approval element, and then click **Properties** to open the **Properties** form.</span></span>

## <a name="name-the-approval-process"></a><span data-ttu-id="dc18f-106">Onay işlemini adlandırma</span><span class="sxs-lookup"><span data-stu-id="dc18f-106">Name the approval process</span></span>

<span data-ttu-id="dc18f-107">Onay işlemi için bir ad girmek üzere aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="dc18f-107">Follow these steps to enter a name for the approval process.</span></span>

1. <span data-ttu-id="dc18f-108">Sol bölmede **Temel Ayarlar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dc18f-108">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="dc18f-109">**Ad** alanına onay işlemi için benzersiz bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="dc18f-109">In the **Name** field, enter a unique name for the approval process.</span></span>

## <a name="specify-when-the-system-automatically-acts-on-the-document"></a><span data-ttu-id="dc18f-110">Sistemin ne zaman belge üzerinde otomatik olarak eylem alacağını belirtin</span><span class="sxs-lookup"><span data-stu-id="dc18f-110">Specify when the system automatically acts on the document</span></span>

<span data-ttu-id="dc18f-111">Sistemi belirli koşullar karşılandığında belge üstünde otomatik olarak işlem yapacak şekilde yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dc18f-111">You can configure the system to automatically act on the document if specific conditions are met.</span></span> <span data-ttu-id="dc18f-112">Örneğin, sistem toplam tutarı 100 ABD Dolarından az olan gider raporlarını onaylayabilir.</span><span class="sxs-lookup"><span data-stu-id="dc18f-112">For example, the system can approve expense reports that have total amounts that are less than USD 100.</span></span> <span data-ttu-id="dc18f-113">Sistemin belge üzerinde eylem alması gereken zamanı belirtmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="dc18f-113">Follow these steps to specify when the system acts on the document.</span></span>

1. <span data-ttu-id="dc18f-114">Sol bölmede **Otomatik eylemler**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dc18f-114">In the left pane, click **Automatic actions**.</span></span>
2. <span data-ttu-id="dc18f-115">**Otomatik eylemleri etkinleştir** onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="dc18f-115">Select the **Enable automatic actions** check box.</span></span>
3. <span data-ttu-id="dc18f-116">**Koşul ekle** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dc18f-116">Click **Add condition**.</span></span>
4. <span data-ttu-id="dc18f-117">Koşulu girin.</span><span class="sxs-lookup"><span data-stu-id="dc18f-117">Enter a condition.</span></span>
5. <span data-ttu-id="dc18f-118">Gerekirse başka koşullar da girin.</span><span class="sxs-lookup"><span data-stu-id="dc18f-118">Enter additional conditions, if necessary.</span></span>
6. <span data-ttu-id="dc18f-119">Girdiğiniz koşulların doğru biçimde yapılandırıldığını doğrulamak için aşağıdaki adımları tamamlayın:</span><span class="sxs-lookup"><span data-stu-id="dc18f-119">To verify that the conditions that you entered are configured correctly, complete the following steps:</span></span>

    1. <span data-ttu-id="dc18f-120">**Sınama iş akışı koşulu** formunu açmak için **Sına**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dc18f-120">Click **Test** to open the **Test workflow condition** form.</span></span>
    2. <span data-ttu-id="dc18f-121">Formdaki **Koşulu doğrula** alanından bir kayıt seçin.</span><span class="sxs-lookup"><span data-stu-id="dc18f-121">Select a record in the **Validate condition** area of the form.</span></span>
    3. <span data-ttu-id="dc18f-122">**Sına**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dc18f-122">Click **Test**.</span></span> <span data-ttu-id="dc18f-123">Sistem, belirtmiş olduğunuz koşullarını yerine getirip getirmediğini belirlemek için kaydı değerlendirir.</span><span class="sxs-lookup"><span data-stu-id="dc18f-123">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="dc18f-124">**Özellikler** formuna geri dönmek için **Tamam** veya **İptal**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dc18f-124">Click **OK** or **Cancel** to return to the **Properties** form.</span></span>

7. <span data-ttu-id="dc18f-125">**Eylemi otomatik tamamla** listesinden sistemin belge üzerinde gerçekleştirmesi gereken eylemi seçin.</span><span class="sxs-lookup"><span data-stu-id="dc18f-125">In the **Auto complete action** list, select the action that the system should take on the document.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="dc18f-126">Bildirimlerin ne zaman gönderileceğini belirtme</span><span class="sxs-lookup"><span data-stu-id="dc18f-126">Specify when notifications are sent</span></span>

<span data-ttu-id="dc18f-127">Bir belge onaylandığında, reddedildiğinde, temsilci atandığında, ilerletildiğinde veya bir değişiklik istendiğinde kişilere bildirim gönderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dc18f-127">You can send notifications to people when a document has been approved, rejected, delegated, or escalated, or when a change has been requested.</span></span> <span data-ttu-id="dc18f-128">Bildirimlerin ne zaman ve kime gönderileceğini belirlemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="dc18f-128">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="dc18f-129">Sol bölmede **Bildirimler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dc18f-129">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="dc18f-130">Bildirim gönderilecek etkinliklerin yanındaki onay kutusunu seçin:</span><span class="sxs-lookup"><span data-stu-id="dc18f-130">Select the check box next to the events to send notifications for:</span></span>

    - <span data-ttu-id="dc18f-131">**Temsilci Seç** – Belge onay için başka kullanıcıya atandığında.</span><span class="sxs-lookup"><span data-stu-id="dc18f-131">**Delegate** – When a document has been assigned to another user for approval.</span></span>
    - <span data-ttu-id="dc18f-132">**İlerlet** – Atanmış kullanıcı ayrılan sürede belge üzerinde eylem gerçekleştirmediğinde.</span><span class="sxs-lookup"><span data-stu-id="dc18f-132">**Escalate** – When the assigned user has not acted on a document in the allotted time.</span></span>
    - <span data-ttu-id="dc18f-133">**Onayla** – Belge onaylandığında.</span><span class="sxs-lookup"><span data-stu-id="dc18f-133">**Approve** – When a document has been approved.</span></span>
    - <span data-ttu-id="dc18f-134">**Reddet** – Belge reddedildiğinde.</span><span class="sxs-lookup"><span data-stu-id="dc18f-134">**Reject** – When a document has been rejected.</span></span>
    - <span data-ttu-id="dc18f-135">**Değişiklik iste** – Atanmış kullanıcı gönderilmiş olan belgede bir değişiklik talep ettiğinde.</span><span class="sxs-lookup"><span data-stu-id="dc18f-135">**Request change** – When the assigned user has requested a change to a document that was submitted.</span></span>

3. <span data-ttu-id="dc18f-136">2. adımda seçtiğiniz bir olay için bir satır seçin.</span><span class="sxs-lookup"><span data-stu-id="dc18f-136">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="dc18f-137">**Bildirim metni** sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dc18f-137">Click the **Notification text** tab.</span></span>
5. <span data-ttu-id="dc18f-138">Metin kutusuna bildirim için metin girin.</span><span class="sxs-lookup"><span data-stu-id="dc18f-138">In the text box, enter the text for the notification.</span></span>
6. <span data-ttu-id="dc18f-139">Metni kişiselleştirmek için kullanıcılara görüntülendiğinde uygun verilerle değiştirilecek yer tutucular ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dc18f-139">To personalize the text, you can insert placeholders, which are replaced with the appropriate data when they are displayed to users.</span></span> <span data-ttu-id="dc18f-140">Yer tutucu girmek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="dc18f-140">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="dc18f-141">Yer tutucunun görünmesini istediğiniz yer için metin kutusuna tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dc18f-141">Click in the text box at the location where the placeholder should appear.</span></span>
    2. <span data-ttu-id="dc18f-142">**Yer tutucu ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dc18f-142">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="dc18f-143">Görüntülenen listede, eklenecek yer tutucuyu seçin.</span><span class="sxs-lookup"><span data-stu-id="dc18f-143">In the list that is displayed, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="dc18f-144">**Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dc18f-144">Click **Insert**.</span></span>

7. <span data-ttu-id="dc18f-145">Bildirimin çevirilerini eklemek için **Çeviriler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dc18f-145">To add translations of the notification, click **Translations**.</span></span> <span data-ttu-id="dc18f-146">Görüntülenen formda, aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="dc18f-146">In the form that is displayed, follow these steps:</span></span>

    1. <span data-ttu-id="dc18f-147">**Ekle** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dc18f-147">Click **Add**.</span></span>
    2. <span data-ttu-id="dc18f-148">Görüntülenen listede, metni gireceğiniz dili seçin.</span><span class="sxs-lookup"><span data-stu-id="dc18f-148">In the list that is displayed, select the language in which you will enter the text.</span></span>
    3. <span data-ttu-id="dc18f-149">**Çevrilmiş metin** metin kutusuna metni girin.</span><span class="sxs-lookup"><span data-stu-id="dc18f-149">In the **Translated text** text box, enter the text.</span></span>
    4. <span data-ttu-id="dc18f-150">Metni kişiselleştirmek için yer tutucular ekleyin.</span><span class="sxs-lookup"><span data-stu-id="dc18f-150">To personalize the text, insert placeholders.</span></span>
    5. <span data-ttu-id="dc18f-151">**Kapat**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dc18f-151">Click **Close**.</span></span>

8. <span data-ttu-id="dc18f-152">**Alıcı** sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dc18f-152">Click the **Recipient** tab.</span></span>
9. <span data-ttu-id="dc18f-153">Bildirimlerin gönderileceği kişiyi belirtin.</span><span class="sxs-lookup"><span data-stu-id="dc18f-153">Specify who the notifications are sent to.</span></span> <span data-ttu-id="dc18f-154">Aşağıdaki tabloda seçeneklerden birini seçin ve 10. adıma geçmeden önce ilgili seçeneğin ek adımlarını uygulayın.</span><span class="sxs-lookup"><span data-stu-id="dc18f-154">Select one of the options in the following table, and then follow the additional steps for the option before you go to step 10.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="dc18f-155">Seçenek</span><span class="sxs-lookup"><span data-stu-id="dc18f-155">Option</span></span></th>
    <th><span data-ttu-id="dc18f-156">Bildirim alıcıları</span><span class="sxs-lookup"><span data-stu-id="dc18f-156">Notification recipients</span></span></th>
    <th><span data-ttu-id="dc18f-157">Ek adımlar</span><span class="sxs-lookup"><span data-stu-id="dc18f-157">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="dc18f-158"><strong>Katılımcı</strong></span><span class="sxs-lookup"><span data-stu-id="dc18f-158"><strong>Participant</strong></span></span></td>
    <td><span data-ttu-id="dc18f-159">Özel bir gruba ya da role atanmış kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="dc18f-159">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="dc18f-160"><strong>Katılımcı</strong>'yı seçtikten sonra, <strong>Rol tabanlı</strong> sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dc18f-160">After you select <strong>Participant</strong>, click the <strong>Role based</strong> tab.</span></span></li>
    <li><span data-ttu-id="dc18f-161"><strong>Katılımcı türü</strong> listesinde, bildirimlerin gönderileceği grup türünü veya rolü seçin.</span><span class="sxs-lookup"><span data-stu-id="dc18f-161">In the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="dc18f-162"><strong>Katılımcı</strong> listesinde, bildirimlerin gönderileceği grubu ya da rolü seçin.</span><span class="sxs-lookup"><span data-stu-id="dc18f-162">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="dc18f-163"><strong>İş akışı kullanıcısı</strong></span><span class="sxs-lookup"><span data-stu-id="dc18f-163"><strong>Workflow user</strong></span></span></td>
    <td><span data-ttu-id="dc18f-164">Mevcut iş akışına katılım gösteren kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="dc18f-164">Users who participate in the current workflow</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="dc18f-165"><strong>İş akışı kullanıcısı</strong>'nı seçtikten sonra, <strong>İş akışı kullanıcısı</strong> sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dc18f-165">After you select <strong>Workflow user</strong>, click the <strong>Workflow user</strong> tab.</span></span></li>
    <li><span data-ttu-id="dc18f-166"><strong>İş akışı kullanıcısı</strong> listesinde, iş akışına katılan bir kullanıcı seçin.</span><span class="sxs-lookup"><span data-stu-id="dc18f-166">In the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="dc18f-167"><strong>Kullanıcı</strong></span><span class="sxs-lookup"><span data-stu-id="dc18f-167"><strong>User</strong></span></span></td>
    <td><span data-ttu-id="dc18f-168">Özel Microsoft Dynamics 365 for Finance and Operations kullanıcıları</span><span class="sxs-lookup"><span data-stu-id="dc18f-168">Specific Microsoft Dynamics 365 for Finance and Operations users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="dc18f-169"><strong>Kullanıcı</strong> seçtikten sonra, <strong>Kullanıcı</strong> sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dc18f-169">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="dc18f-170"><strong>Kullanılabilir kullanıcılar</strong> listesi, tüm Microsoft Dynamics 365 for Finance and Operations kullanıcılarını içerir.</span><span class="sxs-lookup"><span data-stu-id="dc18f-170">The <strong>Available users</strong>: list includes all Microsoft Dynamics 365 for Finance and Operations users.</span></span> <span data-ttu-id="dc18f-171">Bildirimlerin gönderileceği kullanıcıları seçin ve sonra bu kullanıcıları <strong>Seçili kullanıcılar</strong> listesine taşıyın.</span><span class="sxs-lookup"><span data-stu-id="dc18f-171">Select the users to send notifications to, and then move these users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

10. <span data-ttu-id="dc18f-172">Adım 3'ten 9'a kadar olan adımları adım 2'de seçtiğiniz tüm olaylar için yineleyin.</span><span class="sxs-lookup"><span data-stu-id="dc18f-172">Repeat steps 3 through 9 for each event that you selected in step 2.</span></span>

## <a name="specify-a-final-approver"></a><span data-ttu-id="dc18f-173"> Son onaylayıcıyı belirtme</span><span class="sxs-lookup"><span data-stu-id="dc18f-173">Specify a final approver</span></span>

<span data-ttu-id="dc18f-174">Onaylayanın belgeyi onay için gönderen kişi olduğu senaryolar için son onaylayan atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dc18f-174">You may want to designate a final approver for scenarios where the approver is the person who submitted the document for approval.</span></span> <span data-ttu-id="dc18f-175">Son onaylayanı belirtmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="dc18f-175">Follow these steps to specify a final approver.</span></span>

1. <span data-ttu-id="dc18f-176">Sol bölmede **Gelişmiş ayarlar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dc18f-176">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="dc18f-177">**Son onaylayanı kullan** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="dc18f-177">Select the **Use final approver** check box.</span></span>
3. <span data-ttu-id="dc18f-178">Listede, son onaylayan olacak kullanıcıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="dc18f-178">In the list, select the user to be the final approver.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="dc18f-179">Zaman limiti ayarlama</span><span class="sxs-lookup"><span data-stu-id="dc18f-179">Set a time limit</span></span>

<span data-ttu-id="dc18f-180">Onay işleminin belirli bir süre içerisinde tamamlanması gerekiyorsa bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="dc18f-180">Follow these steps if the approval process must be completed in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="dc18f-181">Bu adımlarda belirlediğiniz seçenekler her onay adımının **Atama** ve **İlerletme** alanlarında belirlediğiniz seçenekleri geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="dc18f-181">The options that you select in these steps override the options that you selected in the **Assignment** and **Escalation** areas of each approval step.</span></span>

1. <span data-ttu-id="dc18f-182">Sol bölmede **Gelişmiş ayarlar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dc18f-182">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="dc18f-183">**İş akışı öğesi için bir zaman sınırı** **ayarlayın** onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="dc18f-183">Select the **Set a time limit for the workflow** **element** check box.</span></span>
3. <span data-ttu-id="dc18f-184">**Süre** alanında, onay işleminin ne zaman tamamlanması gerektiğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="dc18f-184">In the **Duration** field, specify when the approval process must be completed.</span></span> <span data-ttu-id="dc18f-185">Aşağıdaki seçeneklerden birini belirleyin:</span><span class="sxs-lookup"><span data-stu-id="dc18f-185">Select one of the following options:</span></span>

    - <span data-ttu-id="dc18f-186">**Saat** – Onay işleminin tamamlanması gereken saat sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="dc18f-186">**Hours** – Enter the number of hours in which the approval process must be completed.</span></span> <span data-ttu-id="dc18f-187">Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.</span><span class="sxs-lookup"><span data-stu-id="dc18f-187">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="dc18f-188">**Gün** – Onay işleminin tamamlanması gereken gün sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="dc18f-188">**Days** – Enter the number of days in which the approval process must be completed.</span></span> <span data-ttu-id="dc18f-189">Daha sonra kuruluşunuzun kullandığı takvimi seçin ve kuruluşunuz iş haftası hakkında bilgi girin.</span><span class="sxs-lookup"><span data-stu-id="dc18f-189">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="dc18f-190">**Hafta** – Onay işleminin tamamlanması gereken hafta sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="dc18f-190">**Weeks** – Enter the number of weeks in which the approval process must be completed.</span></span>
    - <span data-ttu-id="dc18f-191">**Ay** – Onay işleminin tamamlanmış olması gereken günü ve haftayı seçin.</span><span class="sxs-lookup"><span data-stu-id="dc18f-191">**Months** – Select the day and week by which the approval process must be completed.</span></span> <span data-ttu-id="dc18f-192">Örneğin onay işleminin ayın üçüncü haftasının Cuma günü tamamlanmasını isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dc18f-192">For example, you may want the approval process to be completed by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="dc18f-193">**Yıl** – Onay işleminin tamamlanmış olması gereken günü, haftayı ve ayı seçin.</span><span class="sxs-lookup"><span data-stu-id="dc18f-193">**Years** – Select the day, week, and month by which the approval process must be completed.</span></span> <span data-ttu-id="dc18f-194">Örneğin onay işleminin Aralık ayının üçüncü haftasının Cuma günü tamamlanmasını isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dc18f-194">For example, you may want the approval process to be completed by Friday of the third week of December.</span></span>

4. <span data-ttu-id="dc18f-195">Zaman sınırı aşılırsa sistem belge üstünde eylem yapar.</span><span class="sxs-lookup"><span data-stu-id="dc18f-195">If the time limit is exceeded, the system acts on the document.</span></span> <span data-ttu-id="dc18f-196">**Eylem** listesinde sistemin gerçekleştirmesi gereken eylemi seçin.</span><span class="sxs-lookup"><span data-stu-id="dc18f-196">In the **Action** list, select the action that the system should take.</span></span>

## <a name="specify-which-actions-are-available-to-the-user"></a><span data-ttu-id="dc18f-197">Hangi eylemlerin kullanıcı tarafından kullanılabilir olacağını belirtin</span><span class="sxs-lookup"><span data-stu-id="dc18f-197">Specify which actions are available to the user</span></span>

<span data-ttu-id="dc18f-198">Bu belge onay için bir kullanıcıya atandığında kullanıcı belge üstünde işlem yapmalıdır.</span><span class="sxs-lookup"><span data-stu-id="dc18f-198">When a document is assigned to a user for approval, the user must act on the document.</span></span> <span data-ttu-id="dc18f-199">Kullanıcının gönderilmiş olan belge üzerinde hangi eylemleri yapabileceğini belirtmek için bu adımları izler.</span><span class="sxs-lookup"><span data-stu-id="dc18f-199">Follows these steps to specify which actions the user can take on the document that was submitted.</span></span>

1. <span data-ttu-id="dc18f-200">Sol bölmede **Gelişmiş ayarlar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dc18f-200">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="dc18f-201">Kullanıcı belgeyi onaylayabiliyorsa **Onayla** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="dc18f-201">Select the **Approve** check box if the user can approve the document.</span></span>
3. <span data-ttu-id="dc18f-202">Kullanıcı belgeyi reddedebiliyorsa **Reddet** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="dc18f-202">Select the **Reject** check box the user can reject the document.</span></span>
4. <span data-ttu-id="dc18f-203">Kullanıcıların belgelerde değişiklik talep edebilmesi için **Değişiklik iste** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="dc18f-203">Select the **Request change** check box the user can request changes to the document.</span></span>
5. <span data-ttu-id="dc18f-204">Kullanıcı belgeyi başka bir kullanıcıya atayabilecekse **Temsilci Seç** onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="dc18f-204">Select the **Delegate** check box if the user can assign the document to another user for approval.</span></span>

> [!NOTE]
> <span data-ttu-id="dc18f-205">**Kurumsal Portal içindeki iş listesinden eylemleri etkinleştir** onay kutusu kullanımdan kaldırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="dc18f-205">The **Enable actions from the work list in Enterprise Portal** check box has been deprecated.</span></span>

## <a name="configure-the-approval-steps"></a><span data-ttu-id="dc18f-206"> Onay adımlarını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="dc18f-206">Configure the approval steps</span></span>

<span data-ttu-id="dc18f-207">Onay işlemi onay adımlarından oluşur.</span><span class="sxs-lookup"><span data-stu-id="dc18f-207">An approval process consists of approval steps.</span></span> <span data-ttu-id="dc18f-208">Onay işlemine adım eklemek ve adımları yapılandırmak için aşağıdaki yordamı tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="dc18f-208">Complete the following procedure to add steps the approval process and configure the steps.</span></span>

1. <span data-ttu-id="dc18f-209">İş akışı düzenleyicisinde onay işlemine çift tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dc18f-209">In the workflow editor, double-click the approval process.</span></span> <span data-ttu-id="dc18f-210">İş akışı düzenleyicisi onay işleminin adımlarını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="dc18f-210">The workflow editor displays the steps of the approval process.</span></span>
2. <span data-ttu-id="dc18f-211">Onay adımı eklemek için adımları **İş akışı öğeleri** alanından tuvale sürükleyin.</span><span class="sxs-lookup"><span data-stu-id="dc18f-211">To add an approval step, drag the step from the **Workflow elements** area to the canvas.</span></span>
3. <span data-ttu-id="dc18f-212">Onay adımını yapılandırmak için bkz. [Onay adımını yapılandırma](configure-approval-step-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="dc18f-212">To configure an approval step, see [Configure an approval step](configure-approval-step-workflow.md).</span></span>
