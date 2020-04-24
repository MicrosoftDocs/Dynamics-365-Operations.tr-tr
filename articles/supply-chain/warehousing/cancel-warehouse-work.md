---
title: Özel durum işleme için ambar işini iptal etme
description: Bu konu, ambar gözetmenlerinin durdurulan işi işlemesine izin veren İşi iptal et özelliğini açıklar.
author: omulvad
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSTroubIeshootingSeIfService
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2019-10-1
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: cb725885fb48293a08915f13a4fb14085e930444
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205817"
---
# <a name="cancel-warehouse-work-for-exception-handling"></a><span data-ttu-id="87aca-103">Özel durum işleme için ambar işini iptal etme</span><span class="sxs-lookup"><span data-stu-id="87aca-103">Cancel warehouse work for exception handling</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="87aca-104">Microsoft Dynamics 365 Supply Chain Management'taki İşi iptal et işlevi, yönetici kullanıcının devam etmekte olan ancak sistem tarafından durdurulan veya olağanüstü durumlar nedeniyle tamamlanamayan belirli ambar işlerini iptal etmesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="87aca-104">The Cancel work functionality in Microsoft Dynamics 365 Supply Chain Management lets the admin user cancel specific warehouse work that is currently in progress, but that is blocked by the system or can't be completed because of exceptional circumstances.</span></span> <span data-ttu-id="87aca-105">Bu işlevsel, tutarsız verileri düzelten SQL düzeltme komut dosyaları için ilgi çekici ve güvenli bir alternatiftir.</span><span class="sxs-lookup"><span data-stu-id="87aca-105">This functionality is an attractive and secure alternative to SQL corrective scripts that fix inconsistent data.</span></span> <span data-ttu-id="87aca-106">Ancak, bu komut dosyaları genellikle BT profesyonellerinden istense de, İşi iptal et işlevi şirkette yönetici haklarına sahip kullanıcılar tarafından kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="87aca-106">However, whereas these scripts are typically requested from IT professionals, the Cancel work functionality can be used by users in the company who have admin rights.</span></span>

<span data-ttu-id="87aca-107">İş iptal et işlevine **Ambar yönetimi** \> **Periyodik görevler** \> **Temizle \> İşi iptal et**'ten erişebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="87aca-107">You can access the Cancel work functionality at **Warehouse management** \> **Periodic tasks** \> **Clean up \> Cancel work**.</span></span> <span data-ttu-id="87aca-108">**İşi iptal et** iletişim kutusunda iptal edilecek için iş kodunu belirtine ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="87aca-108">In the **Cancel work** dialog box, specify the work ID of the work to cancel, and then select **OK**.</span></span>

## <a name="warehouse-work-that-can-be-canceled"></a><span data-ttu-id="87aca-109">İptal edilebilecek ambar işi</span><span class="sxs-lookup"><span data-stu-id="87aca-109">Warehouse work that can be canceled</span></span>

<span data-ttu-id="87aca-110">Ambar çekme işlemleri sırasında, bir çalışan bir depolama konumundan kendi kullanıcı konumlarına çekilen miktarları kaydettiği ancak yerine koyma işlemini kaydedemediği durumlarla karşılaşabilir.</span><span class="sxs-lookup"><span data-stu-id="87aca-110">During warehouse picking operations, a worker might encounter situations where they have registered quantities as picked from a storage location to their user location, but then they can't register the put operation.</span></span> <span data-ttu-id="87aca-111">Tutarsız ambar verileri genellikle, ancak her zaman değil, işin durdurulma nedenidir.</span><span class="sxs-lookup"><span data-stu-id="87aca-111">Inconsistent warehouse data is often, but not always, the reason why work is blocked.</span></span>

<span data-ttu-id="87aca-112">İş başlığındaki **İptal** düğmesi kullanılarak erişilebilen normal iptal işlevinden farklı olarak, İşi iptal et işlevi son tamamlanan iş satırının **koyma** türünde bir iş satırı olmasını gerektirmez.</span><span class="sxs-lookup"><span data-stu-id="87aca-112">Unlike the regular Cancel functionality that can be accessed by using the **Cancel** button on the work header, the Cancel work functionality doesn't require that the last completed work line be a work line of the **put** type.</span></span> <span data-ttu-id="87aca-113">Başka bir deyişle, İşi iptal et işlevi için, iş satırındaki madde miktarı bir kullanıcı konumunda olsa bile, iptal mantığı çalışabilir.</span><span class="sxs-lookup"><span data-stu-id="87aca-113">In other words, for the Cancel work functionality, cancellation logic can be run even if the item quantity on a work line is in a user location.</span></span>

> [!NOTE]
> <span data-ttu-id="87aca-114">Operasyonel nedenlerle iptal edilmesi gereken iş için ambar kullanıcıları iş sayfasındaki olağan İptal işlevini kullanmaya devam etmelidir.</span><span class="sxs-lookup"><span data-stu-id="87aca-114">For work that must be canceled for operational reasons, warehouse users must continue to use the regular Cancel functionality on the work page.</span></span>

<span data-ttu-id="87aca-115">İşi iptal et işlevi kullanılarak yalnızca **Satış**, **Transfer çıkışı**, **Ham madde çekme** veya **Stok yenileme** türündeki iş iptal edilebilir.</span><span class="sxs-lookup"><span data-stu-id="87aca-115">Only work of the **Sales**, **Transfer issue**, **Raw material picking**, or **Replenishment** type can be canceled by using the Cancel work functionality.</span></span> <span data-ttu-id="87aca-116">İptal mantığı dondurulan ham madde çekme işi veya normal İptal işlevi kullanılarak iptal edilebilecek iş için çalışmaz (önceki nota bakın).</span><span class="sxs-lookup"><span data-stu-id="87aca-116">Cancellation logic won't be run for frozen raw material picking work or work that can be canceled by using the regular Cancel functionality (see the preceding note).</span></span>

<span data-ttu-id="87aca-117">İşin engelini kaldırmak için sistem kalan tüm iş satırlarını iptal eder ve kullanıcının belirttiği iş koduyla ilişkilendirilmiş ambar verilerini düzeltir.</span><span class="sxs-lookup"><span data-stu-id="87aca-117">To unblock the work, the system cancels any remaining work lines and fixes the warehouse data that is associated with the work ID that the user specified.</span></span> <span data-ttu-id="87aca-118">Etkilenen madde miktarıyla ilgili normal ambar işleme operasyonları daha sonra devam edebilir.</span><span class="sxs-lookup"><span data-stu-id="87aca-118">Any regular warehouse-handling operations that involve the affected item quantity can then resume.</span></span>

<span data-ttu-id="87aca-119">İş iptal edildikten sonra etkilenen maddeyi belirli bir konuma koymak için, kullanıcının bir mobil cihazda stok hareketi veya miktar düzeltmesi işlemi kullanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="87aca-119">To put the affected item in a specific location after the work is canceled, the user must use an inventory movement or quantity adjustment operation on a mobile device.</span></span>
