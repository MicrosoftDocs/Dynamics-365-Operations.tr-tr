---
title: İş akışında otomatikleştirilmiş görevleri yapılandırma
description: Bu konu, otomatik bir görevin özelliklerini yapılandırmayı açıklar.
author: ChrisGarty
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 192061
ms.assetid: c0aceb57-b5e6-4ef3-91e7-89a21c9f048a
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4f02b128036ebc0bd8789ecafd1e72e26fe31436
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747967"
---
# <a name="configure-automated-tasks-in-a-workflow"></a><span data-ttu-id="3a703-103">İş akışında otomatikleştirilmiş görevleri yapılandırma</span><span class="sxs-lookup"><span data-stu-id="3a703-103">Configure automated tasks in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3a703-104">Bu konu, otomatik bir görevin özelliklerini yapılandırmayı açıklar.</span><span class="sxs-lookup"><span data-stu-id="3a703-104">This topic explains how to configure the properties for an automated task.</span></span>

<span data-ttu-id="3a703-105">Otomatik bir görevi iş akışı düzenleyicisinde yapılandırmak için göreve sağ tıklatın ve sonra **Özellikler**'i açmak için **Özellikler** sayfanı tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a703-105">To configure an automated task in the workflow editor, right-click the task, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="3a703-106">Ardından otomatik görevin özelliklerini yapılandırmak için aşağıdaki yordamları kullanın.</span><span class="sxs-lookup"><span data-stu-id="3a703-106">Then use the following procedures to configure the properties for the automated task.</span></span>

## <a name="name-the-task"></a><span data-ttu-id="3a703-107">Görevi adlandırma</span><span class="sxs-lookup"><span data-stu-id="3a703-107">Name the task</span></span>

<span data-ttu-id="3a703-108">Otomatik göreve bir ad vermek için aşağıdaki adımları takip edin.</span><span class="sxs-lookup"><span data-stu-id="3a703-108">Follow these steps to enter a name for the automated task.</span></span>

1. <span data-ttu-id="3a703-109">Sol bölmede **Temel Ayarlar**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3a703-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="3a703-110">**Ad** alanına görev için benzersiz bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="3a703-110">In the **Name** field, enter a unique name for the task.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="3a703-111">Bildirimlerin ne zaman gönderileceğini belirtme</span><span class="sxs-lookup"><span data-stu-id="3a703-111">Specify when notifications are sent</span></span>

<span data-ttu-id="3a703-112">Otomatik bir görev çalıştırıldığında veya iptal edildiğinde insanlara bildirimler gönderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3a703-112">You can send notifications to people when an automated task has been run or canceled.</span></span> <span data-ttu-id="3a703-113">Bildirimlerin ne zaman ve kime gönderileceğini belirlemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="3a703-113">Follow these steps to specify when notifications are sent, and who they are sent to.</span></span>

1. <span data-ttu-id="3a703-114">Sol bölmede **Bildirimler**'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3a703-114">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="3a703-115">Bildirim gönderilecek etkinliklerin yanındaki onay kutusunu seçin:</span><span class="sxs-lookup"><span data-stu-id="3a703-115">Select the check box next to the events to send notifications for:</span></span>

    - <span data-ttu-id="3a703-116">**Yürütme** – Görev çalıştırıldığında bildirim gönderilir.</span><span class="sxs-lookup"><span data-stu-id="3a703-116">**Execution** – Notifications are sent when the task has been run.</span></span>
    - <span data-ttu-id="3a703-117">**İptal Edildi** – Görev iptal edildiğinde bildirim gönderilir.</span><span class="sxs-lookup"><span data-stu-id="3a703-117">**Canceled** – Notifications are sent when the task has been canceled.</span></span>

3. <span data-ttu-id="3a703-118">2. adımda seçtiğiniz bir olay için bir satır seçin.</span><span class="sxs-lookup"><span data-stu-id="3a703-118">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="3a703-119">**Bildirim metni** sekmesinde, metin kutusuna, bildirimin metnini girin.</span><span class="sxs-lookup"><span data-stu-id="3a703-119">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5. <span data-ttu-id="3a703-120">Bildirimi kişiselleştirmek için yer tutucular ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3a703-120">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="3a703-121">Yer tutucular, bildirim kullanıcılara gösterildiğinde uygun verilerle değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="3a703-121">Placeholders are replaced with appropriate data when the notification is shown to users.</span></span> <span data-ttu-id="3a703-122">Yer tutucu eklemek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="3a703-122">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="3a703-123">Metin kutusunda, yer tutucunun görüneceği yere tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a703-123">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="3a703-124">**Yer tutucu ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3a703-124">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="3a703-125">Beliren listede, eklenecek yer tutucuyu seçin.</span><span class="sxs-lookup"><span data-stu-id="3a703-125">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="3a703-126">**Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3a703-126">Click **Insert**.</span></span>

6. <span data-ttu-id="3a703-127">Bildirimin çevirilerini eklemek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="3a703-127">To add translations of the notification, follow these steps:</span></span>

    1. <span data-ttu-id="3a703-128">**Çeviriler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a703-128">Click **Translations**.</span></span>
    2. <span data-ttu-id="3a703-129">Beliren sayfada **Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3a703-129">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="3a703-130">Beliren listede, metni girdiğiniz dili seçin.</span><span class="sxs-lookup"><span data-stu-id="3a703-130">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="3a703-131">**Çevrilen metin** alanında, metni girin.</span><span class="sxs-lookup"><span data-stu-id="3a703-131">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="3a703-132">Metni kişiselleştirmek için, 5. adımda belirtildiği gibi yer tutucular ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3a703-132">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6. <span data-ttu-id="3a703-133">**Kapat** düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a703-133">Click **Close**.</span></span>

7. <span data-ttu-id="3a703-134">**Alıcı** sekmesinde, bildirimlerin kime gönderildiğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="3a703-134">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="3a703-135">Aşağıdaki tablodaki seçeneklerden birini seçin ve 8. adıma geçmeden önce ilgili seçeneğin ek adımlarını uygulayın.</span><span class="sxs-lookup"><span data-stu-id="3a703-135">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="3a703-136">Seçenek</span><span class="sxs-lookup"><span data-stu-id="3a703-136">Option</span></span></th>
    <th><span data-ttu-id="3a703-137">Bildirim alıcıları</span><span class="sxs-lookup"><span data-stu-id="3a703-137">Notification recipients</span></span></th>
    <th><span data-ttu-id="3a703-138">Ek adımlar</span><span class="sxs-lookup"><span data-stu-id="3a703-138">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="3a703-139">Katılımcı</span><span class="sxs-lookup"><span data-stu-id="3a703-139">Participant</span></span></td>
    <td><span data-ttu-id="3a703-140">Özel bir gruba ya da role atanmış kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="3a703-140">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="3a703-141"><strong>Katılımcı türü</strong> listesindeki <strong>Rol tabanlı</strong> sekmesinde <strong>Katılımcı</strong> seçtikten sonra, bildirimlerin gönderileceği grup ya da rolün türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="3a703-141">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="3a703-142"><strong>Katılımcı</strong> listesinde, bildirimlerin gönderileceği grubu ya da rolü seçin.</span><span class="sxs-lookup"><span data-stu-id="3a703-142">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="3a703-143">İş akışı kullanıcısı</span><span class="sxs-lookup"><span data-stu-id="3a703-143">Workflow user</span></span></td>
    <td><span data-ttu-id="3a703-144">Mevcut iş akışına katılım gösteren kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="3a703-144">Users who participate in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="3a703-145"><strong>İş akışı kullanıcısı</strong> listesinde, <strong>İş akışı kullanıcısı</strong> sekmesinde, <strong>İş akışı kullanıcısı</strong>'nı seçtikten sonra, iş akışına katılım gösterecek bir kullanıcı seçin.</span><span class="sxs-lookup"><span data-stu-id="3a703-145">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="3a703-146">Kullanıcı</span><span class="sxs-lookup"><span data-stu-id="3a703-146">User</span></span></td>
    <td><span data-ttu-id="3a703-147">Belirli kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="3a703-147">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="3a703-148"><strong>Kullanıcı</strong> seçtikten sonra, <strong>Kullanıcı</strong> sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a703-148">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="3a703-149"><strong>Kullanılabilir kullanıcılar</strong> listesi, tüm  kullanıcılarını içerir.</span><span class="sxs-lookup"><span data-stu-id="3a703-149">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="3a703-150">Bildirimlerin gönderileceği kullanıcıları seçin ve sonra bu kullanıcıları <strong>Seçili kullanıcılar</strong> listesine taşıyın.</span><span class="sxs-lookup"><span data-stu-id="3a703-150">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="3a703-151">Adım 3'ten 7'ye kadar olan adımları adım 2'de seçtiğiniz tüm olaylar için yineleyin.</span><span class="sxs-lookup"><span data-stu-id="3a703-151">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]